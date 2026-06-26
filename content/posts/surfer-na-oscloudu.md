---
title: "Surfer na OSCLOUDu — nejjednodušší způsob, jak rozjet vlastní web"
date: 2026-06-26
draft: false
tags: ["surfer", "webdav", "sftp", "selfhosting", "oscloud", "hugo"]
categories: ["návody", "služby"]
description: "Surfer je malá aplikace, kterou na OSCLOUDu používáme pro statické weby, dokumentaci a sdílení souborů. Tady je návod, jak ji rozchodit i bez technického backgroundu."
---

Surfer je jeden z nejlepších nástrojů na OSCLOUDu, o kterém většina lidí neví, že existuje. Přitom je to nejjednodušší možný způsob, jak dostat vlastní web online — žádné databáze, žádný CMS, žádné PHP. Nahraješ HTML soubory a máš web. Tečka.

Tenhle článek je pro každého, kdo někdy chtěl mít vlastní stránku, dokumentaci k projektu, portfolio nebo prostě místo, kam nahrát pár souborů a poslat odkaz kamarádovi.

## Co Surfer dělá

Surfer servíruje statické soubory. Co tam nahraješ, to ukáže v prohlížeči. Když nahraješ `index.html`, návštěvník na tvojí doméně uvidí ten HTML. Když nahraješ obrázek, je dostupný na přímé URL.

Není to redakční systém. Není to cloudové úložiště. Je to webový server, který umí jednu věc — vzít soubor a poslat ho prohlížeči. A přesně proto je tak užitečný.

### K čemu se to hodí

- **Osobní stránka, portfolio, vizitka** — pár HTML souborů a hotovo
- **Dokumentace** — výstup z MkDocs, Sphinx nebo Docusaurus
- **Blog** — generovaný Hugem, Jekyllem, Astrem
- **Landing page** — jedna stránka pro projekt nebo akci
- **Sdílení souborů** — hodíš PDF nebo ZIP a pošleš odkaz
- **Web malého spolku** — pár stránek, kontakt, fotky

Pokud potřebuješ formuláře, login, databázi nebo komentáře, Surfer to neumí. Pro všechno ostatní je to ta nejmíň otravná cesta.

## Jak Surfer vypadá

Po přihlášení do svojí Surfer instance najdeš admin rozhraní na `https://tvoje-domena.cz/_admin`. Logování je přes OSCLOUD účet, žádné extra heslo si nepamatuješ.

V adminu vidíš:

- strom souborů a složek
- tlačítko pro nahrávání (drag and drop funguje)
- nastavení (Settings) — kde se konfiguruje, jak se web chová
- access tokeny — pro nahrávání z terminálu nebo CI

Pro většinu lidí stačí web rozhraní. Otevřeš, přetáhneš složku se souborama a máš web.

## Doména

Surfer můžeš provozovat buď na subdoméně pod `oscloud.cz` (například `mujprojekt.oscloud.cz`), nebo na vlastní doméně, kterou si přineseš.

Postup:

1. Zaregistruj se na OSCLOUDu přes [helpdesk](https://helpdesk.oscloud.cz).
2. Po založení Surferu dostaneš pokyny, jaký DNS záznam nastavit (typicky `CNAME` nebo `A`).
3. Po propagaci DNS funguje doména včetně HTTPS.

Certifikát řeší OSCLOUD za tebe. Žádné Let's Encrypt, žádné renewals, žádné konfigurace. Funguje.

## Jak nahrávat soubory

Surfer nabízí čtyři způsoby. Vyber si podle toho, co ti vyhovuje.

### 1. Web rozhraní — pro všechny

Otevři `/_admin`, přetáhni soubory nebo složky myší. Funguje to úplně stejně jako uploady kamkoliv jinam. Pro občasné úpravy nebo nahrání pár souborů to bohatě stačí.

### 2. FileZilla a SFTP — pro lidi, co znají FTP klienty

Pokud jsi někdy nahrával web přes FileZilla, WinSCP nebo Cyberduck, tohle je tvoje cesta. Surfer má SFTP přístup — funguje úplně stejně jako klasický webhosting.

Přihlašovací údaje (host, port, username) najdeš v Cloudron app dialogu pod sekcí SFTP. Heslo je tvoje OSCLOUD heslo.

V FileZilla:

- **Hostitel**: `tvoje-domena.cz`
- **Port**: podle Cloudron dialogu
- **Protokol**: SFTP
- **Uživatel** a **heslo**: OSCLOUD účet

Pak prostě přetahuješ soubory zleva doprava, jako u jakéhokoliv jiného hostingu.

### 3. Příkazová řádka — pro terminálové lidi

Když jsi zvyklý na terminál, máš dvě dobré volby.

**SFTP přes scp:**

```bash
scp -P <port> -r ./public/* uzivatel@tvoje-domena.cz:/
```

**Surfer CLI** (oficiální nástroj přes npm):

```bash
npm install -g cloudron-surfer
```

Login (token vygeneruješ v `/_admin` v Settings):

```bash
surfer config --server tvoje-domena.cz --token
```

Upload složky — pozor na hvězdičku, je to důležité:

```bash
# Tohle nahraje OBSAH ./public do rootu
surfer put ./public/* /

# Tohle nahraje SLOŽKU public jako podadresář
surfer put ./public /
```

Bez hvězdičky ti vznikne `https://tvoje-domena.cz/public/` místo toho, aby se obsah zobrazil rovnou. Klasický footgun, na který lidi narážejí.

Smazání:

```bash
surfer del /stara-stranka.html
```

### 4. WebDAV — pro pokročilé

WebDAV endpoint je `https://tvoje-domena.cz/_webdav/`. Jako heslo se používá **access token**, který si vygeneruješ v adminu (ne tvoje OSCLOUD heslo — to je častý zdroj nedorozumění).

Užitečné hlavně pro tři věci:

**Připojení v souborovém manažeru** (Files, Nautilus, Dolphin) — místo URL napiš:

- Gnome Files: `davs://tvoje-domena.cz/_webdav/`
- KDE Dolphin: `webdavs://tvoje-domena.cz/_webdav/`

Pak s tím pracuješ jako s jakoukoliv jinou složkou.

**Rychlý upload jednoho souboru přes curl:**

```bash
curl -T index.html \
  -u "uzivatel:tvuj_access_token" \
  https://tvoje-domena.cz/_webdav/index.html
```

**Deploy z CI/CD pipeline:**

```bash
surfer put --token <access-token> --server tvoje-domena.cz dist/* /
```

## Užitečné nastavení (Settings)

V admin rozhraní v sekci Settings najdeš pár přepínačů, které stojí za to znát.

### Access control — kdo web uvidí

Tohle je možná nejcennější vlastnost Surferu. Můžeš si vybrat ze tří režimů:

- **Public** — web je veřejný, kdokoliv ho vidí
- **Password restricted** — návštěvník zadá heslo, které nastavíš
- **User restricted** — vidí ho jen lidé s OSCLOUD účtem

Pro veřejný blog dává smysl Public. Pro interní dokumentaci spolku nebo rozdělanou věc, kterou chceš ukázat jen kolegům, použij Password. Pro něco, co má zůstat v rámci komunity, User restricted.

### 404.html — vlastní stránka pro nenalezené

Když do rootu webu nahraješ soubor `404.html`, Surfer ho automaticky pošle při každé chybě 404. Můžeš tam dát vlastní zprávu, vtípek, odkaz na hlavní stranu — co chceš.

### Public Folder Listing — výpis složky

Defaultně Surfer pro každou složku hledá `index.html`. Když ho nenajde, vrátí 404. Pokud zapneš Public Folder Listing, místo 404 se ukáže výpis souborů ve složce — užitečné, když chceš složku používat jako sdílený "file dump".

Příklad: nahraješ do `/soubory/` pár PDF a ZIP souborů, žádný `index.html`, a návštěvník na `/soubory/` uvidí seznam.

### Výchozí index

Defaultně se servíruje `index.html` nebo `index.htm`. V Settings můžeš změnit jméno toho výchozího souboru, kdyby ti to z nějakého důvodu nesedlo.

## Reálný workflow — Hugo blog

Takhle deployuju OSCLOUD blog. Nic složitého, žádný build server, žádné CI:

```bash
# 1. napsání článku
nvim content/posts/novy-clanek.md

# 2. preview lokálně
hugo server -D

# 3. build statiky
hugo --minify

# 4. nahrání na Surfer
surfer put ./public/* /

# 5. commit zdrojáků do Gitu
git add -A && git commit -m "novy clanek" && git push
```

Hotovo. Webový blog updatovaný za pár sekund, bez závislosti na GitHub Actions, Netlify nebo cokoliv podobného.

Pro pohodlí si to hodím do Makefile:

```makefile
.PHONY: deploy

build:
 hugo --minify

deploy: build
 surfer put ./public/* /
```

Pak jen `make deploy`.

## Závěr

Surfer je důkaz, že self-hosting nemusí být složitý. Žádné konfiguráky, žádné upgrady, žádné updaty pluginů, které ti rozbijí web. Otevřeš admin, přetáhneš soubory, máš web.

Pokud máš nápad na vlastní stránku, projekt nebo dokumentaci a chceš ji hostovat v rámci OSCLOUDu, ozvi se přes [helpdesk](https://helpdesk.oscloud.cz). Surfer instance je za pár minut.

A pokud máš tipy nebo otázky, najdeš nás na [Mastodonu](https://mamutovo.cz).

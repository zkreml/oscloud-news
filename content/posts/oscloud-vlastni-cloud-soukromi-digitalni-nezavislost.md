---
title: "OSCloud: vlastní cloud, soukromí a digitální nezávislost bez kompromisů"
date: 2026-05-16
draft: false
slug: "oscloud-vlastni-cloud-soukromi-digitalni-nezavislost"
categories: ["OSCloud", "Soukromí", "Open Source"]
tags: ["nextcloud", "matrix", "soukromí", "open source cloud", "webhosting", "alternativa google", "digitální soukromí"]
author: "oscloud"
---

Každý den posíláš e-maily přes Gmail, fotky zálohuje Google Photos, dokumenty ti sedí na OneDrivu a kalendář synchronizuje Apple. Funguje to. Nikdo se neptá, co se s těmi daty děje. A právě to je problém.

OSCloud je komunitní platforma postavená na open source technologiích, která ti dává zpět kontrolu nad vlastními daty. Žádné skryté podmínky, žádné profilování, žádné závislosti na korporátním ekosystému. Jen spolehlivé nástroje, které znáš — jen tentokrát hostované tak, aby data zůstala tvoje.

---

## Co je OSCloud a jak funguje

OSCloud není produkt jedné firmy. Je to sada open source služeb provozovaných na dedikované infrastruktuře v Evropě (Hetzner EU), spravovaná komunitou lidí, kteří sami používají to, co provozují. To je zásadní rozdíl oproti komerčním cloudovým gigantům.

Základem je jedno SSO přihlášení — jeden účet, přístup ke všem službám. Nemusíš si pamatovat deset hesel k deseti různým nástrojům. Registruješ se jednou a máš k dispozici cloud, chat, správu hesel, poznámky, RSS čtečku a další nástroje najednou.

Technicky jde o platformu Cloudron, která umožňuje jednoduchou správu aplikací na vlastním serveru. Všechny aplikace jsou pravidelně aktualizované, monitorované a zálohované. Uživatel se nemusí starat o infrastrukturu — to je práce správce. Stará se jen o svá data.

---

## Proč lidé začínají řešit soukromí na internetu

Ještě před pěti lety byl argument „nemám co skrývat" celkem běžnou odpovědí. Dnes je situace jiná. Úniky dat jsou rutina, reklamy sledují pohyb mezi weby i aplikacemi a algoritmy rozhodují o tom, co vidíš — ne ty.

**Google** si z bezplatných služeb vydělává tím, že zpracovává tvé e-maily, vyhledávání, polohu a chování k budování reklamního profilu. Totéž dělá Meta se všemi svými aplikacemi. **Microsoft** ve výchozím nastavení odesílá diagnostická data z Windows a integruje AI nástroje přímo do kancelářských aplikací — s přístupem k obsahu dokumentů.

Problém není jen soukromí v abstraktním slova smyslu. Je to i praktická závislost na jednom ekosystému. Když Google změní podmínky, zdraží úložiště nebo zruší službu (a to se stává pravidelně — Google Reader, Stadia, Inbox...), nemáš kam jít. Všechno máš tam.

Digitální soukromí neznamená paranoia. Znamená rozhodovat se vědomě o tom, komu a za jakých podmínek svěřuješ svá data.

---

## Výhody používání OSCloudu v praxi

Přechod na OSCloud nemusí být dramatický. Většina nástrojů nahrazuje přesně to, co už používáš — jen bez sledování a bez závislosti na konkrétní firmě.

### Vlastní cloud a synchronizace souborů

Nextcloud funguje jako Google Drive nebo Dropbox — synchronizuje soubory mezi počítačem, telefonem a prohlížečem. Rozdíl je v tom, že soubory jsou uložené na serverech OSCloud v EU, ne v Googlu. Máš přehled, kde data jsou, a nikdo je neanalyzuje.

### Kalendáře a kontakty

Nextcloud zvládá i CalDAV a CardDAV — standardní protokoly pro synchronizaci kalendářů a kontaktů. Fungují s Thunderbirdem, s nativními aplikacemi na Androidu i iOS. Přestaneš být závislý na Google Calendar nebo iCloud.

### Poznámky

Trilium Notes je hierarchický nástroj pro správu znalostí. Hodí se pro osobní wiki, projektovou dokumentaci, zápisky ze schůzek i denní deník. Není to Notion, není to Google Keep — je to nástroj, který nepotřebuje internet a data drží tam, kde chceš.

### Týmová spolupráce

Nextcloud Office (integrovaný Collabora) umožňuje editaci dokumentů, tabulek a prezentací přímo v prohlížeči — víc lidí najednou, v reálném čase. Pro tým, spolek nebo malý projekt jde o plnohodnotnou alternativu Google Workspace.

### Komunikace

Matrix chat (přes klienta Element nebo Element X) nahrazuje Slack, WhatsApp i Discord. Je to decentralizovaný protokol — server OSCloud se může federovat s jinými Matrix servery, takže komunikuješ s komunitou bez ohledu na to, kde jsou. Navíc: přes mosty se dá připojit i na WhatsApp, Telegram nebo Signal.

### Správa hesel

Vaultwarden je kompatibilní implementace Bitwarden serveru. Hesla jsou šifrovaná na serveru i při přenosu, přistupuješ k nim přes prohlížečové rozšíření nebo mobilní aplikaci. Bezpečnější než zapisování do poznámek, pohodlnější než pamatování si všeho.

### RSS a čtení webu

FreshRSS je RSS agregátor — centralizované místo pro sledování blogů, zpravodajských webů a Fediverse zdrojů bez algoritmů. Čteš to, co chceš sledovat, ne to, co ti někdo podsune.

### Sdílení souborů a záložky

Wallabag slouží jako read-it-later aplikace — ukládáš články z webu pro pozdější čtení, offline i bez reklam. Linkwarden pak spravuje záložky se štítky a kolekcemi. Žádný Pocket, žádný Instapaper.

---

## Bezpečnost a soukromí: co to konkrétně znamená

„Bezpečný cloud" je fráze, která se dnes lepí na kdeco. Tady jsou konkrétní věci, které OSCloud dělá a proč na nich záleží.

**Open source software** znamená, že kdokoli může zkontrolovat zdrojový kód aplikací. Nextcloud, Matrix, Vaultwarden — to vše je veřejně dostupný kód, který prochází komunitním auditem. Skryté backdoory jsou podstatně těžší implementovat, když se na kód dívají tisíce lidí.

**Transparentnost provozu** — víš, kde server fyzicky je (Hetzner, EU), víš, kdo ho spravuje. Není to anonymní korporace ukrytá za podmínkami o zpracování dat.

**Pravidelné aktualizace** jsou na platformě Cloudron záležitostí správce, ne uživatele. Bezpečnostní záplaty se nasazují rychle, bez čekání na uživatelský souhlas nebo odložené aktualizace.

**Šifrování přenosu** je samozřejmost — HTTPS všude, TLS pro e-mailové protokoly, end-to-end šifrování v Matrix chatu tam, kde to protokol podporuje.

**Menší attack surface** — čím méně dat centralizuješ u jednoho poskytovatele, tím menší škodu způsobí případný únik. Pokud by (hypoteticky) Googlu unikla databáze, uniknou data o miliardách lidí. Komunitní server má jiný rozsah.

Není to dokonalé řešení. Žádné není. Ale je to podstatně lepší než bezmy­šlenkovité svěřování všeho jednomu korporátnímu silu.

---

## Jaké služby může uživatel každý den používat

Přehled toho, co OSCloud aktuálně nabízí:

### Nextcloud — základ všeho

K čemu: synchronizace souborů, kalendáře, kontakty, sdílené složky, Nextcloud Office.  
Komu se hodí: každému, kdo potřebuje cloud. Doslova.  
Proč je zajímavý: je to nejpropracovanější open source alternativa ke Google Drive + Calendar + Contacts v jednom balíku.

### Matrix / MXChat — chat bez centrálního bodu

K čemu: textová komunikace, skupinové místnosti, hlasové a video hovory, mosty na jiné platformy.  
Komu se hodí: týmům, komunitám, lidem unaveným z proprietárních chatovacích aplikací.  
Proč je zajímavý: decentralizovaný protokol znamená, že nikdo „nevlastní" tvůj chat. Element X je moderní klient pro mobil, Element Web funguje v prohlížeči.

### Vaultwarden — správce hesel

K čemu: bezpečné ukládání a synchronizace hesel, TOTP kódů, bezpečných poznámek.  
Komu se hodí: všem — opravdu. Správce hesel je základ digitální hygieny.  
Proč je zajímavý: Bitwarden-kompatibilní server, funguje se všemi klienty Bitwarden, data jsou šifrovaná end-to-end.

### Trilium Notes — znalostní báze

K čemu: hierarchické poznámky, osobní wiki, projektová dokumentace.  
Komu se hodí: lidem, kteří potřebují víc než Google Keep, ale méně než Confluence.  
Proč je zajímavý: plně offline schopný, výkonné propojování poznámek, skriptování.

### FreshRSS — RSS agregátor

K čemu: sledování blogů, zpravodajských webů, YouTube kanálů i Fediverse zdrojů přes RSS.  
Komu se hodí: každému, kdo chce číst internet bez algoritmů.  
Proč je zajímavý: jednoduchý, rychlý, funguje i jako Fever/Google Reader API pro kompatibilní mobilní klienty.

### PeerTube / VHSky — video bez YouTube

K čemu: hostování a sledování videí na federované platformě.  
Komu se hodí: tvůrcům, kteří nechtějí být závislí na YouTube algoritmech a chce mít obsah pod kontrolou.  
Proč je zajímavý: instance [VHSky.cz](https://vhsky.cz) běží na OSCloud infrastruktuře, videa jsou dostupná přes ActivityPub — lze je sledovat i z Mastodonu nebo jiných Fediverse platforem. Pokud chceš vlastní PeerTube instanci pro projekt nebo komunitu, OSCloud to umí zařídit.

### Mastodon / Mamutovo — sociální síť bez algoritmu

K čemu: mikroblogging, sdílení krátkých příspěvků, sledování lidí z celého Fediverse.  
Komu se hodí: komunitám, projektům a lidem, kteří chtějí sociální síť bez reklamního feedu a bez zásahů algoritmu do toho, co vidíš.  
Proč je zajímavý: instance [mamutovo.cz](https://about.mamutovo.cz) je součástí OSCloud ekosystému a propojuje se s celým Fediversem — Mastodonem, Pixelfedem, PeerTubem i dalšími. Část uživatelů OSCloud si u nás hostuje i vlastní Mastodon instance pro svoje projekty nebo komunity.

### Pixelfed — Instagram bez Instagramu

K čemu: sdílení fotek a krátkých alb ve Fediverse.  
Komu se hodí: fotografům, kreativcům a komunitám, kteří chtějí vizuální obsah sdílet bez závislosti na Metě.  
Proč je zajímavý: Pixelfed je federovaná alternativa k Instagramu — příspěvky jsou viditelné i uživatelům Mastodonu a dalších ActivityPub platforem. OSCloud provozuje instanci na [pixelfed.cz](https://pixelfed.cz) a stejně jako u dalších federovaných služeb je možné hostovat i instanci na míru.

### Gitea — správa kódu

K čemu: Git repozitáře, issue tracker, wiki, CI/CD pipeline.  
Komu se hodí: vývojářům a projektům, které nechtějí být na GitHubu (který patří Microsoftu).  
Proč je zajímavý: plnohodnotný GitHub-like interface, federace přes ForgeFed v plánu.

### Wallabag — čtení bez rušení

K čemu: ukládání článků pro pozdější čtení, offline přístup, čistý reader view.  
Komu se hodí: čtenářům, kteří si chtějí odložit zajímavé články bez reklam a trackerů.  
Proč je zajímavý: exportuje do EPUB, synchronizuje s mobilními aplikacemi, žádné sledování.

---

## Webhosting a vlastní webové stránky

OSCloud v květnu 2026 spustil webhosting pod doménou [oscloud.site](https://oscloud.site) — a je to přirozené rozšíření toho, co komunita dělala od začátku.

Pokud provozuješ blog, web spolku, portfolio nebo malý projekt, není důvod platit za hosting u velkých hráčů, kteří ti dají generický cPanel a supportu se nedočkáš. OSCloud.site staví na stejných principech jako zbytek platformy: férové ceny, žádné skryté poplatky, reálná podpora.

Co konkrétně nabízí:

- **NVMe SSD** — rychlé načítání, nízká latence
- **SSL certifikáty automaticky** — HTTPS bez příplatku a bez ruční konfigurace
- **Zálohy každé 4 hodiny** s historií 90 dní — to je víc, než nabízí většina komerčních hostingů
- **E-mailové schránky na vlastní doméně** — od základního plánu
- **WordPress na jedno kliknutí** — nebo jiné aplikace, více verzí PHP
- **Migrace zdarma** — přecházíš odjinud, pomůžeme s přenosem

Plány jsou čtyři: od základního pro začátečníky přes spravovaný hosting (kde se o techniku stará tým OSCloud) až po multihosting pro větší projekty. Speciální komunitní plán existuje pro neziskovky a komunitní projekty za symbolickou cenu.

Webhosting je vhodný i pro postupný přechod — nemusíš hned měnit všechno. Můžeš začít tím, že přesuneš web. Zbytek přijde postupně.

---

## Pro koho je OSCloud vhodný

OSCloud není jen pro linuxové nadšence s domácím serverem. Cílí na širší spektrum:

**Běžní uživatelé** — kteří chtějí synchronizovat soubory, fotky a kontakty bez toho, aby je sledoval Google. Nextcloud je přístupný, má mobilní aplikace a funguje podobně jako to, co znají.

**Rodiny** — sdílený kalendář, sdílená složka na fotky, správce hesel pro celou domácnost. Bez předplatného Googlu One nebo Microsoft 365.

**Komunity a spolky** — Matrix pro komunikaci, Nextcloud pro sdílené dokumenty, Gitea pro kód nebo projektové soubory. Vše pod jednou střechou, bez závislosti na komerčních nástrojích.

**Menší projekty a startupy** — alternativa ke Google Workspace za rozumnou cenu, s daty v EU a bez obav z podmínek, které se mění bez upozornění.

**Technicky zaměření uživatelé** — kteří ocení přístup ke Gitea, možnost vlastních domén, ssh přístupy a pokročilé funkce jednotlivých aplikací.

**Lidé unudzení z Google nebo Microsoft ekosystému** — kteří hledají cestu ven, ale nechtějí stavět vlastní server od nuly.

---

## Jak začít s OSCloudem

Začít je jednodušší, než to vypadá. A není nutné hned měnit všechno.

**1. Registrace přes helpdesk**  
Účet na OSCloud se zakládá přes helpdesk na adrese [helpdesk.oscloud.cz](https://helpdesk.oscloud.cz/help/3020290644). Nejde o anonymní registraci — jde o komunitní platformu, ne veřejný free tier.

**2. Jeden účet, všechny služby**  
Díky SSO se přihlásíš jedním účtem ke všem dostupným službám. Nemusíš zakládat deset různých profilů.

**3. Začni tím, co potřebuješ**  
Doporučení pro začátečníky:

- **Nextcloud** — první krok pro synchronizaci souborů a nahrazení Google Drive
- **Vaultwarden** — správce hesel je nízký práh a vysoký přínos pro bezpečnost
- **Matrix / Element** — pokud hledáš alternativu k WhatsApp nebo Slacku

**4. Postupný přechod funguje**  
Nemusíš přejít ze dne na den. Klidně měsíc používej Nextcloud paralelně s Google Drive, než přeneseš soubory a zavřeš starý účet. Stejně s chatem, RSS nebo správou hesel.

**5. Dokumentace je k dispozici**  
Na [docs.oscloud.cz](https://docs.oscloud.cz/apps/) najdeš návody pro jednotlivé aplikace. Komunita je aktivní — otázky se dají řešit přes Matrix nebo helpdesk.

---

## Závěr: digitální nezávislost není utopie

OSCloud není dokonalý. Žádná komunita ani žádný software není. Ale je to reálná alternativa ke korporátnímu cloudu — s konkrétními výhodami, které lze popsat bez marketingového žargonu.

Data zůstávají v EU. Software je open source a auditovatelný. Provoz je transparentní. Ceny jsou férové. A pokud se něco pokazí, máš koho kontaktovat — ne anonymní chatbot korporátní podpory.

Digitální soukromí není o tom, že máš co skrývat. Je o tom, že se svobodně rozhoduješ, komu a co svěřuješ. A o tom, že za pět let nebudeš vázán na podmínky, které jsi při registraci ani nečetl.

Začít může být malý krok — záložky místo Chrome Bookmarks, hesla místo browserového uložiště, soubory v Nextcloudu místo Google Drive. Každý krok se počítá.

[Zaregistruj se přes helpdesk →](https://helpdesk.oscloud.cz/help/3020290644)  
[Webhosting → oscloud.site](https://oscloud.site)  
[Dokumentace → docs.oscloud.cz](https://docs.oscloud.cz/apps/)

---
title: "MXChat: komunitní Matrix server pro lidi, co chtějí mít kontrolu nad svou komunikací"
date: 2026-04-20T12:00:00+02:00
draft: false
slug: "mxchat-komunitni-matrix-server"
categories: ["Služby", "Matrix"]
tags: ["matrix", "mxchat", "chat", "soukromí", "self-hosting"]
author: "Archos"
---

Messenger, WhatsApp, Telegram, Discord. Každý z nás má v telefonu aspoň jednu z těchto aplikací a většinou ani nepřemýšlíme nad tím, komu vlastně posíláme své zprávy. MXChat je jiný přístup k chatování – komunitní server postavený na otevřeném protokolu Matrix, kde data nekončí na serverech Mety nebo jiné velké firmy, ale na infrastruktuře, kterou spravuje komunita sama.

Tenhle článek je pro každého, kdo přemýšlí, jestli a proč by měl zkusit něco jiného než mainstreamové messengery – od úplných začátečníků až po lidi, kteří už si hrají s Linuxem a self-hostingem.

**Co z toho máš jako uživatel:**

- tvoje zprávy nikdo nečte (ani provozovatel)
- nejsi závislý na jedné firmě
- můžeš si vybrat aplikaci i server

## Co je MXChat

MXChat je server běžící na protokolu Matrix, který provozujeme v rámci [OSCloud](https://oscloud.cz) – české komunitní platformy zaměřené na open-source a soukromí. Slouží k chatování, volání, sdílení souborů a budování komunit. V praxi to vypadá podobně jako Discord nebo Telegram – máš kontakty, skupinové místnosti, posíláš si zprávy, fotky, videa, voláš si.

Rozdíl je v tom, co se děje pod povrchem. MXChat není produkt jedné firmy, nesbírá o tobě data, neprodává reklamu a není závislý na žádném centrálním provozovateli. Je to kousek Fediverse – sítě propojených nezávislých serverů, které spolu mluví stejným jazykem.

## Jak to vlastně funguje

Nejjednodušší přirovnání: **Matrix je pro chat to, co e-mail pro zprávy.**

Když pošleš e-mail z Gmailu na Seznam, funguje to, protože oba servery mluví stejným protokolem (SMTP). Nikomu nepřijde divné, že si účet na jednom serveru může psát s účtem na jiném serveru. A stejně tak není nutné, aby všichni používali zrovna Gmail.

Matrix funguje stejně, jen pro chat. MXChat je jeden z mnoha serverů. Existují další – matrix.org, tchncs.de, a stovky dalších, včetně těch, které si lidé provozují doma na malém počítači. A všechny spolu mluví. Uživatel z MXChat si může normálně psát s uživatelem z kteréhokoli jiného Matrix serveru na světě.

Technicky to znamená, že když někomu pošleš zprávu, tvůj server ji předá jeho serveru, a ten ji doručí. Pro tebe jako uživatele je to úplně stejné jako na WhatsAppu – jen nejsi závislý na jedné firmě.

### Homeserver, klient, místnost

Abys rozuměl, co kdo znamená:

- **Homeserver** je místo, kde máš účet a kde leží tvoje data. V našem případě `mxchat.cz`.
- **Klient** je aplikace, ve které chatuješ – třeba Element, SchildiChat nebo Cinny. Něco jako webový prohlížeč pro Matrix – existuje jich víc a můžeš si vybrat.
- **Místnost** (room) je chat – buď mezi dvěma lidmi, nebo skupinová. Každá místnost má své nastavení, šifrování a pravidla.

## Proč ho používat

### Soukromí, které dává smysl

MXChat nečte tvé zprávy. Nemůže, i kdyby chtěl – veškerá komunikace mezi lidmi je **end-to-end šifrovaná** (o tom níž). To je zásadní rozdíl oproti spoustě "bezpečných" aplikací, které sice tvrdí, že šifrují, ale zároveň si ze zpráv dělají metadata, profil uživatele a reklamní cíl.

Jako správci serveru máme teoreticky přístup k serverovým logům a metadatům (kdy jsi byl online, kolik zpráv prošlo systémem), ale neanalyzujeme je, neprofilujeme uživatele a neprodáváme nikomu data. Obsah šifrovaných zpráv neumíme přečíst ani my.

### Otevřený kód

Matrix i klienti jako Element jsou open source – kdokoliv si může kód prohlédnout, ověřit, že dělá to, co říká, nebo si ho upravit. Nemáš slovo firmy, že "nesbíráme data". Máš možnost to zkontrolovat.

### Nezávislost

Když Facebook zítra vypne WhatsApp, tvoje kontakty a historie jsou pryč. Když jedna instance Matrixu zmizí, zbytek sítě funguje dál. A protože si můžeš účet kdykoliv přestěhovat na jiný server (nebo si klidně rozjet vlastní), nejsi uzamčen v jedné krabici.

## Co na něm můžeš dělat

Stručně: všechno, co děláš na normálním messengeru.

**Chatování** – 1:1 i skupiny, reakce, odpovědi, editace zpráv, mazání, připíchnuté zprávy, vlákna.

**Sdílení souborů** – fotky, videa, dokumenty. Velikost má limit (v našem případě 100 MB na soubor), ale na běžné použití to stačí.

**Volání** – hlasové i video, 1:1 i skupinové. Na MXChat máme vlastní integrovaný nástroj pro videokonference.

**Komunity a místnosti** – veřejné místnosti, do kterých se může připojit kdokoliv, soukromé skupiny jen pro pozvané, tematické servery (tzv. "spaces", něco jako Discord servery s kanály uvnitř).

**Emoji reakce, stickery, GIFy** – nic, co by ses bál postrádat.

## Srovnání s tím, co znáš

Bez přikrášlování. Každá aplikace má svoje pro a proti.

### WhatsApp

*Plusy MXChatu:* nepatří Metě, neukládá si tvoje metadata, nemusíš mít telefonní číslo, funguje na víc zařízeních bez závislosti na jednom "hlavním" telefonu.

*Mínusy:* tví známí tam pravděpodobně nejsou. WhatsApp má výhodu, že ho má skoro každý.

### Telegram

*Plusy MXChatu:* Telegram standardně **nešifruje** zprávy end-to-end (musíš ručně zapnout "secret chat" a jen v 1:1). Na MXChatu je šifrování zapnuté ve výchozím nastavení pro soukromé konverzace.

*Mínusy:* Telegram má hladší UX, rychlejší synchronizaci, lepší boty pro masové použití.

### Discord

*Plusy MXChatu:* Discord je úplně centralizovaný, čte tvoje zprávy, zobrazuje reklamy a pro komerční zájem může cokoliv změnit. Matrix má podobný koncept komunit, ale bez toho všeho.

*Mínusy:* Discord je vyladěnější pro hráče a velké komunity, má lepší hlasové kanály a víc integrací.

Závěr: MXChat není náhrada, která by tě vytrhla z nuly. Je to alternativa pro lidi, kterým záleží na tom, kde končí jejich data, a kteří jsou ochotní občas přemluvit kamaráda, aby si stáhl jinou appku.

## Jak začít

### 1. Zařiď si pozvánku

A tady rovnou upřímně: **registrace na MXChat nejsou momentálně otevřené pro veřejnost.** Funguje to přes schválení a registrační token.

Proč? Otevřené registrace jsou lákavé sousto pro spammery a trolly. Stačí pár dní otevřené registrace a máš na serveru stovky botů, kteří spamují veřejné místnosti a kazí reputaci celé instance napříč Matrix sítí. Proto jsme se rozhodli pro mírnou bariéru – není to šikana, je to ochrana lidí, kteří už tu jsou. Nejde o uzavřenou komunitu – jen o základní ochranu proti spamu.

Proces je rychlý a lidský:

1. Napiš na [helpdesk](https://helpdesk.oscloud.cz/help/3020290644)
2. Proběhne krátké ověření – stačí říct, kdo jsi a proč máš zájem. Žádný dotazník, jen pár vět.
3. Dostaneš registrační token (řetězec znaků)
4. Tokenem dokončíš registraci v aplikaci

Celé to zabere většinou pár hodin až den, podle toho, kdy se dostaneme k e-mailu.

### 2. Vyber si aplikaci

Matrix klientů je hodně. Pro začátek doporučuju:

- **Element** – nejrozšířenější, dostupný na webu, Windows, macOS, Linuxu, Androidu i iOS. Pokud nevíš, čím začít, začni tímhle.
- **SchildiChat** – fork Elementu s příjemnějším rozhraním, zejména na mobilu.
- **Cinny** – moderní webový klient, hezky vypadá, běží v prohlížeči.

Stáhnout si je můžeš z [element.io](https://element.io), z Google Play, App Store nebo z F-Droidu.

### 3. První přihlášení

V aplikaci při prvním spuštění:

1. Klikni na **Sign in** / **Přihlásit se**
2. U pole *Homeserver* zadej `mxchat.cz` (místo výchozího `matrix.org`)
3. Vyplň uživatelské jméno, heslo a registrační token
4. Hotovo
![Registrační obrazovka mxchat.cz](/images/mxchat-registrace.png)

### 4. Ulož si bezpečnostní klíče – tohle nepřeskakuj

Jakmile jsi přihlášený, aplikace tě vyzve k nastavení **zabezpečeného úložiště** (Secure Backup) a vygeneruje ti **bezpečnostní klíč** (Security Key) – dlouhý řetězec znaků, něco jako `EsTe XkPq 9aWr ...`.

**Tenhle klíč si ulož.** Ne "potvrdím později". Ne "vyřeším, až to budu potřebovat". Ulož.

Proč to tak tlačím: end-to-end šifrování znamená, že zprávy umí rozšifrovat jen tvoje zařízení. Když si smažeš appku, přeinstaluješ telefon, nebo se přihlásíš na novém počítači, nové zařízení tvoje staré zprávy **neumí přečíst**, pokud mu k tomu nedáš klíč. A ten klíč ti server nedá – ten ho nezná. Máš ho jen ty.

Když si klíč neuložíš a ztratíš přístup k zařízení, přijdeš o historii zpráv. Definitivně. Nikdo z nás ji neobnoví, protože ji ani my nevidíme.

Jak to uložit rozumně:

- **správce hesel** (Bitwarden, KeePassXC, Proton Pass) – nejlepší volba
- **šifrovaná poznámka** v Trilium, Obsidianu, CryptPadu
- **vytištěný papír** v šuplíku – nezní to moderně, ale funguje to

Kromě klíče si Element nabídne i volbu **Security Phrase** – heslo, kterým si klíč chráníš. Funguje jako záložní způsob, jak se ke klíči dostat. Pokud ji nastavíš, zapamatuj si ji stejně pečlivě.

Kdykoliv se pak budeš přihlašovat na novém zařízení, klíč (nebo frázi) zadáš a zprávy se ti rozšifrují.

### 5. Začni chatovat

Přidej si první kontakt – buď zadáním jeho Matrix ID ve formátu `@jmeno:server.cz`, nebo tak, že tě pozve do místnosti. Veřejné místnosti najdeš přes průzkumník místností přímo v aplikaci.

## Přihlášení přes OSCloud (SSO)

Pokud už máš účet na OSCloudu, můžeš se do MXChatu přihlásit přes jednotné přihlášení (SSO). Nemusíš si tak vytvářet nový účet ani řešit další heslo.

**Jak na to:**

1. V klientovi (např. Element) zvol **Sign in with SSO**
2. Vyber OSCloud / přesměrování na přihlášení
3. Přihlas se svým OSCloud účtem
4. Po návratu jsi automaticky přihlášený do MXChatu

**Důležité omezení:**

- nový klient **Element X zatím nepodporuje SSO**, takže s OSCloud účtem ho aktuálně nepoužiješ
- použij klasický **Element** nebo jiný klient s podporou SSO

SSO je pohodlné řešení, pokud už OSCloud používáš – jinak zůstává standardní registrace přes token.

## Pokročilejší možnosti

### Boti

Matrix umí roboty – malé programy, které sedí v místnosti a něco dělají. U nás na OSCloudu používáme vlastní boty pro FAQ, RSS čtečky (do místnosti ti chodí nové články z blogů, které sleduješ), překladače a různé utility.

Pokud tě baví hrát si, protokol Matrix má skvělou dokumentaci pro vývoj vlastních botů – my osobně používáme BaiBot.

### Propojení s jinými službami

Matrix umí **bridging** – mosty mezi sítěmi. V praxi to znamená, že si z Matrixu můžeš psát s lidmi, kteří jsou na úplně jiné platformě, aniž bys tu platformu musel mít otevřenou.

Na MXChatu provozujeme mosty do těchto sítí:

- **WhatsApp**
- **Signal**
- **Telegram**
- **Meta Messenger**

Funguje to tak, že si most jednorázově propojíš se svým účtem (např. naskenováním QR kódu z WhatsApp Web) a pak ti všechny konverzace padají přímo do Matrixu. Místo čtyř aplikací máš jednu. Pokud tě zajímají detaily nastavení, napiš na helpdesk – rádi projdeme, co k tomu potřebuješ.

### Více zařízení

Na Matrix se přihlásíš z kolika zařízení chceš najednou. Telefon, notebook, pracovní stanice, tablet. Každé zařízení má svůj šifrovací klíč, ověřuješ je mezi sebou (QR kódem nebo emoji řetězcem) a zprávy ti přijdou všude.

## Bezpečnost a soukromí

### Šifrování jednoduše

Představ si, že posíláš dopis v zamčené schránce, a klíč máš jen ty a adresát. Cestou projde schránka přes spoustu pošťáků, ale nikdo z nich ji nemůže otevřít. Když dorazí, adresát ji odemkne svým klíčem. To je **end-to-end šifrování** (E2EE).

V Matrixu to funguje stejně. Když pošleš zprávu v šifrované místnosti, tvůj klient ji zašifruje klíčem, který má jen příjemce. Server ji přenese, ale **nevidí její obsah**. Ani my jako správci, ani nikdo, kdo by se snažil na servery dostat.

### Co o tobě víme

Na úrovni serveru vidíme: uživatelské jméno, e-mail (pokud jsi ho zadal pro reset hesla), metadata – kdy ses přihlásil, v jakých místnostech jsi, kdy posíláš zprávy. **Obsah šifrovaných zpráv nevidíme nikdy, v žádné formě.** U neveřejných místností (což je výchozí nastavení pro 1:1 a skupiny) je to technicky nemožné.

Jsme upřímní – serverový administrátor má vždycky teoretickou možnost k některým datům přistoupit. Rozdíl mezi námi a Metou je v tom, že k tomu nemáme důvod, neděláme to a nestaví na tom obchodní model.

## Pro koho se to hodí a pro koho ne

**Hodí se ti, pokud:**

- ti vadí, že aplikace, které používáš, vydělávají na tvých datech
- máš komunitu, kterou chceš mít pod kontrolou (klub, zájmová skupina, rodinný chat)
- chceš si psát s lidmi z různých Matrix serverů, aniž bys musel mít všude účet
- tě baví open source a decentralizace

**Spíš se nehodí, pokud:**

- potřebuješ, aby tě 100 % kontaktů mohlo bez řečí ihned najít (to dneska umí jen WhatsApp nebo Messenger)
- chceš "zapnout a zapomenout" – Matrix má občas drobnosti, které vyžadují trochu pozornosti (verifikace zařízení, bezpečnostní klíč)
- hledáš platformu primárně pro live streaming nebo hlasové kanály pro desítky lidí najednou

## Shrnutí

MXChat je komunitní Matrix server provozovaný v rámci OSCloudu. Nabízí moderní chat se všemi funkcemi, které znáš z WhatsAppu nebo Telegramu, ale bez závislosti na velké firmě. Komunikuje s celou Matrix sítí, šifruje zprávy end-to-end a respektuje tvé soukromí.

Registrace jsou uzavřené kvůli ochraně proti spamu, ale získat pozvánku je otázka jedné zprávy na helpdesk.

### Jak začít dnes

1. Napiš na [helpdesk](https://helpdesk.oscloud.cz/help/3020290644) a popros o registrační token (nebo použij SSO, pokud už máš OSCloud účet)
2. Stáhni si [Element](https://element.io)
3. Při přihlášení nastav homeserver na `mxchat.cz`, zadej token, vytvoř si účet
4. **Ulož si bezpečnostní klíč** – bez něj přijdeš o historii při přeinstalaci
5. Přidej si první kontakt přes Matrix ID (`@jmeno:mxchat.cz`) a napiš mu "ahoj"

Víc informací najdeš na [web.mxchat.cz](https://web.mxchat.cz/index.html). Pokud něco nefunguje nebo si nevíš rady, napiš na [helpdesk](https://helpdesk.oscloud.cz/help/3020290644) – jsme lidé, nejsme bot a odpovídáme.

---
title: "Vikunja na OSCloud: todo aplikace, kterou si nemusíte hostovat sami"
date: 2026-04-24
draft: false
slug: "vikunja-na-oscloud"
categories: ["Služby"]
tags: ["vikunja", "todo", "produktivita", "self-hosted", "oscloud"]
author: "oscloud"
---

Todo aplikací je mraky. Většina běžných (Todoist, Microsoft To Do, Trello, Asana) ale běží na cizích serverech, má různé "free" limity a vaše úkoly — včetně těch osobních a pracovních — leží někde, kam nevidíte. Vikunja je open-source alternativa, kterou na OSCloud provozujeme pro komunitu na adrese [todo.oscloud.cz](https://todo.oscloud.cz/). Tenhle článek je o tom, co Vikunja umí a jak ji používat přes OSCloud — žádné dockery, žádné instalace.

## Co je Vikunja

Vikunja je open-source správa úkolů a projektů. V základu je to klasická todo aplikace — vytvoříte si projekt, hodíte do něj úkoly, nastavíte termíny, štítky, priority. Navíc to ale umí věci, kvůli kterým lidi obvykle platí Todoist nebo Trello: kanban nástěnky, Gantt diagramy, tabulkové zobrazení, filtry, sdílení projektů s dalšími uživateli, komentáře k úkolům, přílohy.

Celý projekt je pod licencí AGPLv3, takže kód je veřejný a kdokoliv si ho může zkontrolovat nebo provozovat sám. Pro nás, co máme rádi kontrolu nad daty, je to důležité.

![Přehled Vikunji - dashboard s projekty a úkoly](/images/vikunja-prehled.png)

### Proč místo Trella nebo Todoistu

Upřímně — Todoist má hezčí mobilní aplikaci a lepší parsování termínů v přirozeném jazyce. Trello má propracovanější integrace. Vikunja nejde proti nim funkcemi, ale filozofií:

- **Data jsou vaše.** Neběží to na serveru nějaké firmy, která se z nich snaží udělat byznys model.
- **Žádné předplatné za základní funkce.** U Todoistu jsou připomenutí, štítky nebo historie za placeným plánem. Vikunja to má celé zadarmo.
- **Žádné sledování a analytika.** Nevznikají profily, nikdo nečte, co si píšete do úkolů.
- **Otevřené API.** Pokud chcete automatizaci, import z jiných nástrojů nebo vlastního bota, je to jednoduché.

Jestli potřebujete jednoduchý nákupní seznam, je Vikunja overkill. Jestli chcete jeden nástroj na osobní úkoly, rodinné plánování, práci i správu projektů, dává to smysl.

## Vikunja na OSCloud

Na [todo.oscloud.cz](https://todo.oscloud.cz/) běží instance Vikunji, kterou spravujeme pro komunitu OSCloud. Pro uživatele to znamená jednu věc: nemusíte nic instalovat, nic konfigurovat, nic aktualizovat. Otevřete prohlížeč, přihlásíte se a používáte.

Kdy to dává smysl:

- Chcete Vikunju zkusit, ale nechcete kvůli tomu zvedat server.
- Nemáte chuť ani čas se starat o zálohy, aktualizace a bezpečnost instance.
- Věříte komunitnímu provozu víc než komerčnímu SaaSu — infrastruktura běží na dedikovaných EU serverech v Hetzneru a projekt je transparentní.
- Chcete mít todo aplikaci propojenou s ostatními službami OSCloud (Nextcloud, Mastodon, Matrix, CryptPad a další) pod jedním účtem.

Kdy to naopak smysl nedává: pokud máte vlastní homelab a chcete si Vikunju hostovat sami — to samozřejmě jde, ale to je jiný článek.

## Přihlášení

Na [todo.oscloud.cz](https://todo.oscloud.cz/) jsou dvě cesty:

**Klasická registrace e-mailem a heslem.** Otevřené veřejné registrace jsou momentálně zavřené — o přístup je potřeba požádat přes helpdesk: [helpdesk.oscloud.cz/help/3020290644](https://helpdesk.oscloud.cz/help/3020290644). Po schválení dostanete samostatný účet jen pro todo aplikaci.

**Přihlášení přes OSCloud účet (SSO).** Pokud už máte účet na OSCloud, není potřeba zakládat další. Kliknete na přihlášení přes OSCloud, potvrdíte přístup a jste uvnitř. Stejně jako u ostatních služeb.

SSO (Single Sign-On) je v tomhle případě prakticky užitečná věc, ne marketing. Jedno přihlášení pro Vikunju, Nextcloud, Matrix, Mastodon, CryptPad, Gitea a další služby. Jedno heslo navíc k zapamatování, jeden účet na správu, jedno místo, kde případně vypnete přístup. Když změníte heslo v OSCloud, změní se pro všechny služby naráz.

Pokud si plánujete Vikunju používat dlouhodobě a máte i ostatní služby, SSO je logická volba. Pokud chcete jen rychle zkusit a ostatní služby neřešíte, stačí klasická registrace.

## Bezpečnost a soukromí

Tohle je oblast, kde se dají snadno slibovat věci, které nejsou pravda, takže to napíšu na rovinu.

**Co platí:** OSCloud je komunitní projekt, kód Vikunji je otevřený, neprodáváme vaše data, neanalyzujeme je, neprofilujeme uživatele a neukazujeme reklamy. Infrastruktura běží v EU.

**Co platí realisticky:** administrátor má technicky přístup k infrastruktuře, což je nutné pro provoz, zálohy a řešení problémů. Neznamená to, že se někdo probírá ve vašich úkolech — znamená to, že technická možnost existuje. Stejné je to u každé hostované služby, včetně komerčních. Rozdíl je v tom, že u nás nemáme ekonomický motiv s daty cokoliv dělat.

**Co byste měli dělat vy:**

- **Silné a unikátní heslo.** Ideálně ze správce hesel (Bitwarden, KeePassXC).
- **Dvoufaktorová autentizace (2FA).** Pokud používáte SSO přes OSCloud, nastavte si 2FA na úrovni OSCloud účtu — pokryje tím všechny připojené služby.

## Základní funkce

Vikunja má víc funkcí, než většina lidí reálně používá. Tady je to, co se hodí znát pro běžné použití.

### Projekty (dříve "seznamy")

Projekt je základní organizační jednotka — třeba "Práce", "Domácnost", "Server Arch", "Nákupy". Projekty lze vnořovat do sebe, takže si můžete udělat strukturu ve stylu "Osobní → Byt → Rekonstrukce kuchyně". Každý projekt má vlastní úkoly a lze ho sdílet s dalšími uživateli.

### Úkoly

Samotný úkol má kromě názvu i popis (s Markdown formátováním), termín, prioritu, štítky, podúkoly, přílohy, komentáře a přiřazení dalším lidem. Nemusíte používat všechno — v 90 % případů stačí "napiš článek" a datum.

### Štítky (labels)

Barevné tagy napříč projekty. Typické použití: `urgent`, `čekám-na-odpověď`, `doma`, `vpráci`, `telefon`. Výhoda proti projektům je v tom, že úkol může mít víc štítků a dají se podle nich filtrovat napříč vším.

### Priority

Pět úrovní od "žádná" po "DO IT NOW". Osobně je moc neřeším — termín obvykle řekne víc než priorita. Ale pokud pracujete v týmu a potřebujete rozlišit, co je kritické, hodí se.

### Termíny (deadlines)

Každý úkol může mít datum splnění, datum začátku a datum ukončení. Do toho opakování ("každý pátek", "poslední den měsíce") a připomenutí. Vikunja umí úkoly zobrazit jako Gantt diagram, takže pokud vedete projekt s navazujícími úkoly, máte přehled.

![Gantt zobrazení časové osy](/images/vikunja-gantt.png)

### Zobrazení

Každý projekt se dá prohlížet jako:

- **Seznam** — klasický todo list.
- **Kanban** — sloupce (typicky To Do / In Progress / Done), do kterých taháte úkoly.
- **Gantt** — časová osa s délkou úkolů.
- **Tabulka** — přehled všech polí najednou, jako v Excelu.

Zobrazení nic nemění na datech — je to jenom pohled. Stejný projekt můžete střídavě používat jako seznam i jako kanban.

![Kanban zobrazení ve Vikunji](/images/vikunja-kanban.avif)

## Praktické použití

### Osobní úkoly

Projekt "Osobní" se štítky `dnes`, `týden`, `někdy`. Úkoly typu "zavolat na úřad", "koupit baterie do hodin", "dodělat daňové přiznání". Termíny tam, kde to dává smysl, jinak nic. Opakované úkoly na věci jako "platit pojištění" nebo "vynést popelnice".

### Práce

Projekt nebo víc projektů podle klientů/úkolů. Kanban zobrazení se hodí pro rozpracované věci — vidíte, co právě máte rozdělaného a kde se to zaseklo. Komentáře u úkolů jsou užitečné, když si pracujete ve dvou a potřebujete něco zdokumentovat.

### Správa serverů a projektů

Tohle je use case, který sám hodně používám. Pro každou službu (Matrix, PeerTube, Mastodon) mám projekt, do kterého si házím věci typu "aktualizovat Synapse", "prověřit backupy", "opravit nginx config po updatu". Štítky `údržba`, `migrace`, `bug` napříč. U dlouhodobějších věcí pomůže Gantt, u rozpracovaných kanban.

Pro dev projekty na Gitea nebo podobně se dá Vikunja použít jako lightweight issue tracker — mimo rozsah samotného gitea issues, třeba pro roadmap nebo osobní plánování kolem projektu.

### Sdílení a spolupráce

Projekty můžete sdílet s konkrétními uživateli (s různými právy) nebo s celým týmem. Užitečné pro rodinné věci, komunitní projekty nebo malé týmy. Nebudete s tím řídit padesátičlennou firmu, ale na pár lidí je to dostatečné.

## Mobilní aplikace

Mobilní appky Vikunji jsou v použitelném stavu na obou platformách, i když web je pořád nejkompletnější.

**Android:** oficiální aplikace [Vikunja](https://play.google.com/store/apps/details?id=io.vikunja.app) je v Google Play. Po instalaci stačí zadat adresu vlastní instance (`https://todo.oscloud.cz`) a přihlásit se — buď klasickým účtem Vikunji, nebo přes OSCloud SSO. Oboje funguje, osobně ověřeno. Aplikace pokrývá to, co od mobilní todo appky člověk čeká: přidávání úkolů, termíny, štítky, projekty. Není to feature-complete proti webu, ale pro běžné použití na cestě to stačí. Alternativně — pokud chcete úkoly přímo v kalendáři — se dá Vikunja propojit přes CalDAV s DAVx⁵ a libovolným klientem.

**iOS:** je nativní aplikace v App Store (jmenuje se jednoduše "Vikunja"), kterou mám osobně vyzkoušenou a v základní podobě funguje dobře — podporuje přidávání a úpravu úkolů, push notifikace, sync s kalendářem a propojení s vlastní instancí. Komunita navíc vyvíjí appku "Kuna" zaměřenou na integraci s iOS kalendářem přes EventKit. Situace na iOS je tedy lepší než na Androidu.

**Připojení k vlastní instanci:** všechny zmíněné aplikace podporují zadání vlastní server URL. U OSCloud zadáte `https://todo.oscloud.cz` a přihlásíte se stejnými údaji jako ve webu. Pozor — u některých verzí appek nesmí URL končit lomítkem.

**Co reálně funguje nejlíp:** pro mě osobně je nejpoužitelnější webová verze v prohlížeči na mobilu. Vikunja má responzivní UI, dá se přidat na plochu jako PWA a funguje to překvapivě dobře. Na rychlé přidání úkolu to stačí, na plné řešení projektů v mobilu taky. Nativní appky zatím dohánějí web, to se časem nejspíš změní.

## Výhody pro komunitu OSCloud

Vikunja zapadá do ekosystému OSCloud jednou věcí: je to další střípek do mozaiky služeb, které spolu sdílí přihlášení a filozofii. Stejný účet vám dává:

- **Nextcloud** na soubory a kalendář
- **Matrix (mxchat.cz)** na chat
- **Mastodon (mamutovo.cz)** na sociální síť
- **PeerTube (vhsky.cz)** na videa
- **CryptPad** na zabezpečenou spolupráci
- **Gitea** na git repozitáře
- **Linkwarden** na záložky
- **Vikunja (todo.oscloud.cz)** na úkoly

Nejde o jeden produkt, ale o samostatné open-source projekty, které mají společné přihlášení a běží na společné infrastruktuře. Když budete v budoucnu chtít odejít, data si vyexportujete a poběžíte dál — na vlastním serveru nebo jinde. Žádný lock-in.

## Závěr

Vikunja není dokonalá — mobilní aplikace ještě dozrávají a UI má místy drobnosti, které by šly vyhladit. Ale jako otevřená, soběstačná todo aplikace, která se vejde mezi Todoist a Trello a nikomu neprodává vaše data, je to jedna z nejlepších možností, co teď je.

Na OSCloud ji najdete připravenou k použití na [todo.oscloud.cz](https://todo.oscloud.cz/). Hodí se vám, pokud:

- chcete todo aplikaci, kde kontrolujete vlastní data,
- už používáte ostatní služby OSCloud a chcete je mít pod jedním účtem,
- vám nestačí jednoduché poznámky a chcete i kanban, Gantt, sdílení a filtry,
- nechcete platit předplatné za to, co by mělo být základ.

Pokud vám stačí papírek na lednici, klidně u něj zůstaňte. Ale pokud řešíte víc věcí a chcete je mít pohromadě bez toho, aby někdo koukal, co si píšete — zkuste to.

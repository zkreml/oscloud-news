---
title: "Linkwarden: záložky pod vlastní kontrolou"
date: 2026-03-13
draft: false
author: "oscloud"
tags: ["linkwarden", "záložky", "soukromí", "oscloud", "self-hosted"]
---


Záložky jsou jednou z těch věcí, které každý nějak řeší, ale málokdo je spokojený s tím, jak to řeší. Složky v prohlížeči se plní a nikdo je neprochází, cloudové služby zavírají nebo mění podmínky, a důležité články mizí spolu s doménami, na kterých byly. Na OScloud teď provozujeme Linkwarden – nástroj, který tohle celé řeší trochu jinak.

## Co je Linkwarden a proč ho máme

Linkwarden je open-source správce záložek s archivací. To zní možná nudně, ale v praxi to znamená, že neukládáš jen odkaz – ukládáš i obsah stránky v podobě snímku. Pokud stránka za rok zmizí, článek máš pořád.

Na OScloud jsme ho nasadili, protože jsme sami naráželi na limity toho, co existuje. Komerční alternativy jako Raindrop nebo Pocket jsou fajn, dokud vám nevyprší trial nebo dokud firma nezmění podmínky. A záložky v prohlížeči jsou chaos, který funguje jen dokud neformátuješ počítač nebo nepřejdeš na jiný prohlížeč.

Linkwarden sedí přesně do filozofie OScloud: open source, data u nás, žádné sledování.

## Problémy, které zná každý

### Záložky, které nikdo nenajde

Kdo z vás má ve Firefoxu nebo Chromu složku „Ke čtení" nebo „Různé" s desítkami odkazů, které tam leží roky? Záložky v prohlížeči nejsou špatné, ale bez organizace se rychle promění v digitální šuplík, kam se věci strčí a zapomenou.

### Závislost na cizích službách

Pocket patří Mozille a jeho budoucnost je nejistá. Raindrop má free tier s omezeními. Notion je populární, ale je to americká firma s daty na amerických serverech. Pinboard přestal být aktivně vyvíjen. A co se stane, když se rozhodnou zdražit, změnit podmínky nebo prostě zavřít?

Tohle není paranoia – je to normální úvaha o tom, komu svěřuješ svá data a jak moc jsi na té službě závislý.

### Stránky, které zmizí

Obsah na webu je nestálý. Novinkové weby mažou staré články, blogy zanikají, doménám expirují registrace. Pokud si uložíš jen URL, nemáš žádnou záruku, že za dva roky bude odkaz stále fungovat. Archivace obsahu tohle řeší – Linkwarden si při uložení odkazu pořídí snímek stránky, který zůstane dostupný bez ohledu na to, co se děje s originálem.

## Co Linkwarden konkrétně umí

### Ukládání a organizace

Základní funkce je ukládání odkazů. Ke každému odkazu můžeš přidat název, popis, tagy a zařadit ho do kolekce. Kolekce jsou něco jako složky – dají se vnořovat a pojmenovat podle tématu nebo projektu. Tagy pak fungují napříč kolekcemi a umožňují rychlé filtrování. Důležité odkazy nebo kolekce si můžeš připnout přímo na dashboard pro rychlý přístup.

### Archivace stránky

Tohle je to, co Linkwarden odlišuje od jednoduchých správců záložek. Při uložení odkazu si systém automaticky stáhne snímek stránky ve čtyřech formátech: HTML (celá stránka), screenshot, PDF a čistá čitelná verze textu. Výsledek závisí na tom, jak je stránka postavená, ale ve většině případů máš k dispozici alespoň část obsahu i poté, co originál zmizí.

### Reader view a anotace

Uložené články si můžeš číst přímo v Linkwardenu v reader view – čistém zobrazení bez reklam a rozptylujících prvků. V nastavení si upravíš font, velikost písma, řádkování i šířku sloupce. Text lze zvýrazňovat a přidávat k němu poznámky.

### Vyhledávání

Linkwarden má plnotextové vyhledávání napříč všemi sbírkami včetně podpory vyhledávacích operátorů pro přesnější dotazy. Pokud ukládáš pravidelně, oceníš to rychle.

### Sdílení a spolupráce

Kolekce lze sdílet jako veřejný odkaz nebo pozvat konkrétní uživatele s různými úrovněmi přístupu: Viewer (pouze čtení), Contributor (čtení a přidávání odkazů) nebo Admin (plný přístup). Hodí se to pro sdílení zdrojů v rámci skupiny, projektu nebo komunity.

### Import a export

Pokud přicházíš z prohlížeče nebo jiné služby, Linkwarden podporuje import přes standardní HTML formát záložek. Stačí vyexportovat záložky z prohlížeče a nahrát je – struktura složek se zachová. Export funguje stejně snadno.

### Synchronizace s prohlížečem

Záložky v prohlížeči lze synchronizovat s Linkwardenem pomocí nástroje Floccus. Pro rychlé ukládání odkazů přímo při procházení webu jsou k dispozici rozšíření pro Chrome a Firefox.

## Proč je to zajímavé z pohledu soukromí

Data jsou uložená na serverech OScloud v EU – konkrétně v Hetzner datacentrech. Nemáme přístup k obsahu vašich záložek, nejsou analyzovány pro reklamu a nejsou sdíleny s třetími stranami. Žádné „abychom vám mohli nabídnout lepší zážitek".

Linkwarden je open source (licence AGPL), takže kód si může kdokoli projít a ověřit, co dělá. Nevěříte nám? Hezky. Kód je na GitHubu a kdokoli si může postavit vlastní instanci.

Provoz OScloud je financovaný komunitou, ne reklamou. To je důležité – nejsme motivovaní k tomu, abychom cokoliv sbírali nebo prodávali.

## Pro koho to dává smysl

Linkwarden není pro každého. Nemá smysl instalovat další aplikaci, pokud vám záložky v prohlížeči stačí a máte jich deset.

Dává smysl, pokud:

Sbíráš zdroje ke konkrétním tématům – výzkum, studium, tvorba obsahu, sledování oborových novinek. Linkwarden ti umožní mít všechno na jednom místě, strukturovaně, s možností dohledání.

Záleží ti na tom, aby obsah nezmizel. Pokud si ukládáš důležité články, technické dokumentace nebo archivní materiály, archivace ve více formátech je klíčová funkce.

Sdílíš zdroje s ostatními. Rodinný nebo komunitní seznam odkazů, zdroje pro projekt, doporučené čtení pro skupinu – sdílené kolekce s nastavitelnými právy to zvládají bez zbytečné složitosti.

Chceš mít data u sebe nebo v prostředí, kterému věříš.

## Jak to funguje na OScloud

Pokud máš účet na OScloud, přistoupíš k Linkwardenu přes jednotné přihlášení – stejný účet, stejné heslo jako pro ostatní služby. Žádné další údaje ani samostatná registrace do Linkwardenu nejsou potřeba.

Pokud účet ještě nemáš, registraci vyřídíš přes helpdesk na [helpdesk.oscloud.cz](https://helpdesk.oscloud.cz/help/3020290644). Více informací o projektu najdeš na [oscloud.cz](https://oscloud.cz).

Data jsou hostovaná v EU a nejsou přenášena mimo evropské datové centrum. Zálohy provádíme pravidelně.

Linkwarden na OScloud je dostupný na adrese **links.oscloud.cz**.

## Závěr

Linkwarden není revoluční nástroj. Je to správce záložek, který dělá svou práci spolehlivě, respektuje tvoje soukromí a nenechá tě závislého na cloudové službě, která může zítra změnit podmínky nebo zmizet.

Pokud tě téma zajímá, vyzkoušej to. Registrace je zdarma, data máš pod kontrolou a pokud ti to nevyhovuje, záložky si vyexportuješ a jdeš jinam.

OScloud funguje díky komunitě – pokud chceš projekt podpořit finančně nebo jinak, informace najdeš na [oscloud.cz](https://oscloud.cz). Každá pomoc se počítá.

---

## FAQ

**Musím mít vlastní účet na OScloud, nebo se můžu přihlásit jinak?**
Stačí jeden OScloud účet – přihlášení funguje přes SSO, takže žádné další údaje ani samostatná registrace do Linkwardenu nejsou potřeba. Pokud účet ještě nemáš, požádáš o něj přes [helpdesk.oscloud.cz](https://helpdesk.oscloud.cz/help/3020290644).

**Co se stane s mými záložkami, pokud OScloud skončí?**
Linkwarden podporuje export záložek ve standardním HTML formátu, který zvládne importovat každý prohlížeč i jiné správce záložek. Data nejsou nikde uzamčena.

**Archivuje Linkwarden stránky automaticky, nebo to musím spustit ručně?**
Při uložení odkazu proběhne archivace automaticky ve čtyřech formátech: HTML, screenshot, PDF a čitelná textová verze. Závisí to na tom, jak je stránka technicky postavená, ale ve většině případů se alespoň část obsahu uloží úspěšně.

**Mohu sdílet záložky s někým, kdo nemá účet na OScloud?**
Ano. Kolekci lze zpřístupnit jako veřejný odkaz – druhá strana nemusí mít žádný účet. Pokud chceš někomu umožnit přidávat nebo spravovat odkazy, pozveš ho jako uživatele s příslušnou rolí.

**Je Linkwarden dostupný jako mobilní aplikace?**
Ano, oficiální mobilní aplikace existuje pro iOS i Android. Před prvním použitím si v nastavení Linkwardenu vygeneruj API token aplikace a zadej ho při přihlášení. Pro rychlé ukládání odkazů z prohlížeče jsou k dispozici také rozšíření pro Chrome a Firefox.

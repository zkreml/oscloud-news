---
title: "Mastodon 4.6: Collections, nové profily a další novinky"
date: 2026-06-29
draft: false
slug: mastodon-4-6-collections
categories: ["Mastodon", "Fediverse"]
tags: ["mastodon", "collections", "fediverse", "discovery", "4.6", "profily"]
author: "Archos"
---

mamutovo.cz aktualizováno na Mastodon 4.6.2 a Debian 13. Hlavní novinka této verze jsou Collections — doporučené seznamy účtů pro snazší objevování lidí na Fediverse. Ale není to jediná věc, která se změnila.

## Proč to vůbec vzniklo

Kdo na Fediverse přichází z Twitteru nebo jiných centralizovaných sítí, narazí dřív nebo
později na stejný problém: jak najít lidi, které stojí za to sledovat?

Na Twitteru to řeší algoritmus — ať chceš nebo ne, obsah ti přijde sám. Na Mastodonu to
nefunguje. Federovaná síť složená z desítek tisíc instancí s různými zaměřeními je skvělá
věc pro ty, kteří vědí, co hledají. Pro nováčka je to ale matoucí bludiště.

Dosud existovala různá komunitní řešení — weby jako fedi.tips, ručně udržované seznamy,
starter pack projekty třetích stran. Fungovalo to, ale stálo to úsilí a nebylo to nijak
integrované do samotného Mastodonu.

Collections mají tenhle problém řešit nativně, přímo v platformě.

## Co Collections jsou (a co nejsou)

Collection je seznam účtů, který někdo sestavil s tím záměrem, aby ho sdílel s ostatními.
Říká tím: "Tyhle účty stojí za pozornost, pokud tě zajímá X."

Není to followlist — neznamená to, že kdo přistoupí k Collection, automaticky ty účty
sleduje. Není to ani odběr. Je to doporučený seznam, který si prohlédneš a rozhodneš se
sám, koho z něj začneš sledovat.

Technicky jde o rozšíření stávajícího konceptu Lists — ten existuje v Mastodonu dlouho,
ale byl vždy soukromý. Collections jsou jeho veřejná, sdílitelná varianta.

## Jak Collections fungují

### Vytvoření

Collection vytvoříš přes menu profilu. Nastavíš název, krátký popis a volitelně jeden
hashtag jako tematický štítek. Lze ji také označit jako citlivý obsah — popis a seznam
účtů se pak schová za content warning.

Maximální počet účtů v jedné Collection je 25.

### Co vidí ostatní

Každý účet v Collection se zobrazuje s bio textem, počtem příspěvků, sledujících a —
což je klíčové — s datem poslední aktivity. Průzkum mezi uživateli ukázal, že recency
je pro rozhodnutí "sledovat / nesledovat" důležitější než počet followerů nebo přítomnost
ověřeného odkazu.

{{< figure src="/images/mastodon-46-collection-detail.png" alt="Ukázka Collection Česká komunita na mamutovo.cz" caption="Collection zobrazuje bio, počet příspěvků a datum poslední aktivity" >}}

### Přehled tvých Collections

V rozhraní máš dvě záložky: **Created by you** (Collections, které jsi sestavil) a
**Featuring you** (Collections, ve kterých tě někdo jiný má). Takže vždy víš, kde se
tvůj účet objevuje.

{{< figure src="/images/mastodon-46-collections-overview.png" alt="Přehled Collections na mamutovo.cz" caption="Záložka Featuring you ukáže, ve kterých Collections se nacházíš" >}}

### Viditelnost a sdílení

Collection může být Public nebo Unlisted a sdílí se přímým odkazem. Public Collections
se navíc zobrazí na tvém profilu v záložce Featured.

Vyhledávání Collections zatím není — přijde v pozdějších verzích. Teď jde hlavně o
tvorbu a ruční sdílení odkazem.

## Soukromí a kontrola

Tohle je část, kde vývojáři Mastodonu viditelně poučili ze zkušeností Bluesky.

Aby tě někdo mohl přidat do Collection, musíš mít v nastavení zapnuté **"Feature me in
discovery experiences"**. Bez toho tě přidat nejde.

{{< figure src="/images/mastodon-46-discovery-setting.png" alt="Nastavení discovery v Mastodonu 4.6" caption="Bez zapnutého 'Feature me in discovery experiences' tě do Collections přidat nejde" >}}

Pokud tě někdo přidá, dostaneš notifikaci. Můžeš si Collection prohlédnout a pokud
nechceš být její součástí, jednoduše se z ní odstraníš — bez nutnosti blokovat nebo
reportovat autora.

V případě obtěžování fungují standardní nástroje: report (řeší moderátoři instance)
nebo blok (okamžitě tě odstraní ze všech Collections daného uživatele).

Kurátor se do vlastní Collection nepřidává automaticky — může to udělat, ale není to
výchozí stav.

## Praktická omezení

**Limit 25 účtů** je pro některé use cases málo. Mastodon tým přiznává, že "magické
číslo" je pravděpodobně mezi 25 a 80 — záměrně začínají na nižší hranici, protože
limit je snazší zvýšit než snížit. Na Bluesky byl limit Starter Packů 150 účtů, což
vedlo ke vzniku obřích, neuspořádaných listů.

**Žádné "Follow All" tlačítko** — bulk follow v 4.6 není. Vývojáři řeší, jak by
fungovala inverzní operace a nechtějí jít cestou dark patterns.

**Bez vyhledávání** — Collections zatím nejdou prohledávat jako katalog. Záměrně,
tým chce nejdřív vidět, jak komunita Collections tvoří.

**Jen instance na 4.6+** — přidávat půjde pouze účty z instancí, které jsou
aktualizované na Mastodon 4.6 nebo novější.

## Srovnání s Bluesky Starter Packs

Bluesky Starter Packs jsou funkčně podobný koncept. Ale na Bluesky nebyly notifikace
o přidání, opt-out byl komplikovaný a vznikaly stale listy s neaktivními účty, které
nováčci hromadně followovali a pak se divili, proč mají špatný feed.

Mastodon přistupuje konzervativněji: menší velikost, notifikace, snadný opt-out, bez
bulk follow. Pomalejší onboarding, ale čistší.

## Praktické využití

**Onboarding na vlastní instanci.** Správce instance může sestavit Collection
"zajímavé účty pro nováčky" a dát na ni odkaz v uvítacím emailu. Je to přirozená
náhrada za stávající Recommended Accounts funkci.

**Komunity a projekty.** Selfhost projekt může mít Collection se všemi správci
a přispěvateli. Open source projekt seznam maintainerů.

**Tematická doporučení.** Místo dlouhého vlákna "koho sledovat" jednoduše sdílíš
odkaz.

## Nové profily

Mastodon 4.6 přináší i přepracované profily. Editace profilu teď probíhá přímo na
stránce profilu v edit módu — není potřeba přecházet do nastavení. Profilovou fotku
a hlavičku lze ořezat přímo tam, lze přidat alt text pro fotku i hlavičku.

{{< figure src="/images/mastodon-46-profile-fields.png" alt="Editace vlastních polí v profilu Mastodon 4.6" caption="Správa vlastních polí přímo v editaci profilu" >}}

Přibyla kontrola nad záložkou Media — lze nastavit, jestli se zobrazuje vůbec, a jestli
má zahrnovat přílohy z odpovědí. Záložku Featured (Collections a doporučené profily)
lze také skrýt.

Procházení profilu je přehlednější — přepínání mezi originálními příspěvky, boosty a
odpověďmi vyžaduje méně kliknutí a nastavení se pamatuje napříč profily.

## Newsletters

Nová funkce primárně pro instituce, novináře a tvůrce obsahu: uživatelé mohou povolit
anonymním návštěvníkům odebírat jejich příspěvky e-mailem. Takže i lidé bez Mastodon
účtu mohou sledovat konkrétní profil.

Funkce není zapnutá pro všechny automaticky — vyžaduje souhlas správce instance,
protože rozesílání newsletterů může výrazně zvýšit provozní náklady. Pokud tě to
zajímá, obrať se na administrátory mamutovo.cz.

## Wrapstodon

Funkce "rok v přehledu", kterou znáš z mastodon.social, je teď dostupná pro všechny
instance. Od 10. prosince každého roku si budeš moci vygenerovat přehled svého roku
na Mastodonu — ale jen pokud s tím explicitně souhlasíš. Výsledek lze sdílet jako
odkaz, ne jen jako screenshot.

## Přístupnost

Značná část práce v 4.6 šla do přístupnosti — navigace klávesnicí, správa fokusu,
kontrasty barev, lepší podpora čteček obrazovky. Alt text pro profilové fotky a
hlavičky je součástí toho. Na tomto se podílela i nizozemská vláda, která část
vývoje financovala.

## Shrnutí

Mastodon 4.6 není velký skok, ale je to solidní aktualizace s praktickými dopady.
Collections řeší reálný problém nativně a s respektem k soukromí uživatelů. Žádný
algoritmus, žádné doporučování bez souhlasu.

mamutovo.cz běží na 4.6.2. Collections si můžeš vyzkoušet hned — stačí mít zapnuté
discovery v nastavení a jít na svůj profil.

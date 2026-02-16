---
title: "CryptPad: Bezpečná kancelář, která nevidí do vašich dokumentů"
date: 2026-02-07
draft: false
tags: ["cryptpad", "soukromí", "e2ee"]
---
## CryptPad: Bezpečná kancelář, která nevidí do vašich dokumentů

Představte si, že píšete dokument, tabulku nebo poznámky přímo v prohlížeči, sdílíte je s kolegy a spolupracujete v reálném čase – ale na rozdíl od Google Docs nebo Microsoft 365 váš obsah nikdy neuvidí provozovatel serveru, žádná firma ho neskenuje kvůli reklamám a žádný algoritmus ho neanalyzuje. Přesně tohle nabízí **CryptPad** – open-source kancelářský balík s end-to-end šifrováním.

Na OSCloud ho najdete na adrese [**https://cryptpad.arch-linux.cz/**](https://cryptpad.arch-linux.cz/) – běží v našem komunitním prostředí bez reklam, trackingu a prodávání dat. Je to nástroj pro každého, kdo chce pracovat s dokumenty online, ale nechce je svěřovat velkým technologickým firmám.

<img src="/images/crytpad.png" alt="Crytpad" width="600">

## Co CryptPad umí

CryptPad není jen textový editor. Nabízí kompletní sadu nástrojů pro práci a spolupráci:

* **Textové dokumenty** – bohatě formátovaný WYSIWYG editor podobný Google Docs
* **Tabulky** – pro rozpočty, seznamy, jednoduché výpočty
* **Prezentace** – slides pro prezentace a školení
* **Markdown/kód** – pro programátory a pisatele dokumentace
* **Whiteboard** – pro náčrty, brainstorming, vizuální spolupráci
* **Kanban** – pro projektové plánování ve stylu Trello
* **Formuláře** – pro ankety a sběr odpovědí
* **Sdílený disk (Drive)** – organizace souborů do složek

Všechno funguje přímo v prohlížeči, bez instalace. Můžete pracovat sami nebo s ostatními v reálném čase – vidíte kurzory spolupracovníků, změny se synchronizují okamžitě.

### Sdílení bez komplikací

Každý dokument můžete sdílet pomocí odkazu. Nemusíte zakládat účet, nemusíte nikoho zvát emailem – stačí poslat URL. K tomu můžete nastavit:

* **Práva na čtení** – ostatní vidí obsah, ale nemohou editovat
* **Práva na úpravy** – kdokoliv s odkazem může měnit obsah
* **Heslo** – ochrana odkazu heslem pro citlivější věci
* **Vlastníka** – pokud máte účet, můžete dokument spravovat a mazat

Bez účtu funguje CryptPad jako anonymní scratchpad – vytvoříte dokument, sdílíte odkaz, spolupracujete. S účtem získáte Drive, historii změn, možnost obnovit smazané dokumenty a lepší správu přístupů.

## Bezpečnost a soukromí: jak to funguje

Tady začíná to zajímavé. CryptPad používá **end-to-end šifrování (E2EE)** – což znamená, že data se šifrují přímo ve vašem prohlížeči ještě předtím, než se odešlou na server. Server ukládá jen šifrovanou kaši, kterou bez klíče nemůže přečíst.

### Zero-knowledge architektura

Provozovatel serveru (v případě OSCloud my) technicky nemůže vidět obsah vašich dokumentů. Nemůžeme je prohledávat, číst, analyzovat ani nikomu předat – protože máme jen zašifrovaná data. Klíč k dešifrování je součástí URL odkazu (za znakem `#`) a ten se nikdy neposílá na server.

**Co to znamená v praxi:**

* Při úniku databáze útočník získá jen nečitelná zašifrovaná data
* Pokud by byl server kompromitován, útočník pořád nemůže přečíst vaše dokumenty
* Nemůžeme vás špehovat, prodat vaše data třetím stranám ani je předat na požádání
* Dokonce ani nemůžeme obnovit zapomenutý obsah – klíč máte jen vy

### Kde má E2EE hranic

End-to-end šifrování je skvělá věc, ale není to kouzlo, které vyřeší všechno:

**Ztráta přístupu:** Pokud ztratíte odkaz na dokument (a nemáte účet nebo jej neuložíte do Drive), je pryč navždy. Server nemá jak ho najít nebo obnovit.

**Metadata:** I když obsah dokumentu je šifrovaný, server vidí _kdy_ a _jak velký_ dokument byl vytvořen, kolik lidí ho upravuje, IP adresy připojení (těch se ale zbavujeme pravidelným mazáním logů).

**Heslo k účtu:** Přestože jsou dokumenty šifrované, heslo k vašemu účtu chrání přístup k Drive a seznamu dokumentů. Kompromitované heslo znamená ztrátu kontroly nad účtem. Používejte silné heslo a správce hesel.

**Zálohy a export:** Když si dokument exportujete nebo stáhnete, přestává být chráněný šifrováním. Soubor na disku je v plaintextu.

**Prohlížeč a zařízení:** Pokud máte kompromitovaný prohlížeč, keylogger nebo malware na počítači, E2EE vám nepomůže – útočník může číst data ještě před šifrováním.

E2EE je silná ochrana proti útokům na server a proti provozovateli, který by chtěl šmírovat. Ale není to všelék – bezpečnost závisí i na vás.

## CryptPad na OSCloud

OSCloud je komunitní ekosystém open-source služeb, které fungují jako alternativa k velkým komerčním platformám. CryptPad sem zapadá perfektně:

* **Komunitní provoz** – žádná firma, která by vámi vydělávala, žádné reklamy, žádný tracking
* **EU datacentrum** – servery běží v Německu (Hetzner), podléhají evropským zákonům o ochraně dat

CryptPad na OSCloud je primárně pro členy komunity – lidi, kteří chtějí alternativu k big-tech kancelářím, ale nechtějí obětovat pohodlí. Není to replacement pro Google – je to nástroj pro ty, kdo vědomě odmítají surveillance capitalism a chtějí si udržet kontrolu nad svými daty.

### Pro koho se to hodí

* **Malé týmy a komunity** – sdílené zápisy, plánování, dokumentace bez závislosti na Google Workspace
* **Studenti a učitelé** – spolupráce na projektech bez trackingu a profilování
* **Aktivisté a občanské iniciativy** – bezpečnější místo pro citlivé dokumenty
* **Kdokoliv řešící soukromí** – prostě nechcete, aby vaše poznámky četl algoritmus

Nejde o paranoju – jde o rozumnou prevenci a princip. Proč by měl Google vědět, co píšete do soukromých dokumentů?

## Praktické scénáře

### Sdílené zápisy z porady

Vytvoříte dokument, nastavíte práva na úpravy, pošlete odkaz týmu. Všichni zapisují poznámky v reálném čase, vidíte kurzory ostatních. Po poradě uložíte finální verzi do svého Drive nebo ji exportujete jako PDF.

### Plánování projektu (kanban)

Založíte kanban board s kolonkami „TODO", „Doing", „Done". Každý člen týmu má odkaz s právy na úpravy, tahá kartičky, přidává úkoly. Obsah je šifrovaný, nikdo cizí nevidí, co plánujete.

### Společná tabulka na rozpočet

Sdílený rozpočet akce, společné výdaje na byt, sběr příspěvků – tabulka s pravidelnými vzorci. Sdílíte odkaz, každý vidí aktuální stav, může přidávat položky.

### Anonymní dokument bez registrace

Potřebujete rychle něco napsat s někým, kdo nemá účet? Vytvoříte dokument anonymně, pošlete odkaz. Po dokončení práce dokument smažete nebo necháte vypršet (pokud existuje expirace – závisí na nastavení instance).

### Bezpečné sdílení citlivějších poznámek

Máte citlivé poznámky (hesla, kontakty, drafty článků)? Vytvoříte dokument s heslem, pošlete odkaz bezpečným kanálem (Matrix, Signal), heslo pošlete jiným kanálem. I když někdo odposlouchává jednu cestu, nemá kompletní přístup.

## Tipy pro používání

### Jak sdílet bezpečně

* **Práva:** Pro běžnou spolupráci dávejte práva na úpravy. Pro sdílení finálních výstupů nebo citlivějších věcí jen práva na čtení.
* **Heslo:** Používejte heslo na dokument, pokud sdílíte citlivější věci nebo přes nedůvěryhodný kanál (email, veřejný chat).
* **Expirace:** Pokud instance podporuje nastavení expirace dokumentu, použijte to pro dočasné sdílení.
* **Rozdělení tajemství:** Odkaz posílejte jedním kanálem (Matrix), heslo jiným (SMS, osobně). Odposlech jedné cesty nestačí.

### Jak nepřijít o přístup

* **Uložte si odkazy:** Bez účtu nemáte Drive – pokud ztratíte odkaz, dokument je pryč. Ukládejte je do správce hesel, bookmarků nebo poznámek.
* **Založte si účet:** S účtem máte všechno v Drive, můžete dokumenty organizovat do složek, obnovovat smazané, sdílet bezpečněji.
* **Export a záloha:** Důležité dokumenty exportujte ven (PDF, Markdown, HTML) – CryptPad není primárně archivační úložiště.

### Doporučení pro týmy

* **Organizace složek:** Vytvořte strukturu složek podle projektů nebo témat. Sdílejte celé složky s týmem.
* **Názvosloví:** Pojmenujte dokumenty jasně – „Zápis z porady 2025-01-25", ne „Dokument 1". Usnadní to hledání.
* **Pravidla přístupu:** Dohodněte se, kdo má práva na úpravy, kdo jen na čtení. U citlivějších věcí používejte hesla.
* **Archivace:** Staré dokumenty buď exportujte, nebo je přesuňte do archivní složky. Nemazejte bez domluvy.

## Shrnutí

CryptPad je open-source kancelářský balík s end-to-end šifrováním, který dává uživatelům kontrolu nad jejich daty. Na OSCloud ho najdete jako komunitní službu bez reklam, trackingu a profilování – na adrese [**https://cryptpad.arch-linux.cz/**](https://cryptpad.arch-linux.cz/).

**Hlavní výhody:**

* End-to-end šifrování – server nevidí obsah dokumentů
* Spolupráce v reálném čase bez nutnosti instalace
* Sdílení odkazem s nastavitelnými právy a heslem
* Kompletní sada nástrojů – dokumenty, tabulky, prezentace, kanban, whiteboard
* Komunitní provoz v EU bez závislosti na big-tech

**Ideální pro:**

* Lidi, kteří řeší soukromí a nechtějí korporátní surveillance
* Malé týmy a komunity hledající alternativu k Google Workspace
* Kohokoliv, kdo chce pracovat s dokumenty online, ale bez trackingu

**Zkuste to:** Otevřete [https://cryptpad.arch-linux.cz/](https://cryptpad.arch-linux.cz/), vytvořte dokument (i bez účtu) a vyzkoušejte, jestli vám to sedne. Pokud ano, založte si účet a začněte organizovat dokumenty do složek. Je to jednodušší, než si myslíte – a rozhodně bezpečnější než posílat poznámky přes Gmail nebo ukládat citlivé věci do Google Docs.

* * *

## FAQ

**Můžu používat CryptPad bez účtu?**  
Ano. Dokument vytvoříte anonymně, sdílíte odkaz a pracujete. Bez účtu ale nemáte Drive a ztráta odkazu znamená ztrátu přístupu.

**Je to opravdu bezpečné?**  
End-to-end šifrování znamená, že server nemá přístup k obsahu dokumentů. Bezpečnost ale závisí i na vás – silné heslo, bezpečné sdílení odkazů, zabezpečené zařízení.

**Co když ztratím odkaz na dokument?**  
Bez účtu je dokument nenávratně pryč. S účtem máte dokumenty v Drive a můžete je obnovit.

**Můžu to používat na mobilu?**  
Ano, CryptPad funguje v mobilním prohlížeči. Není to ideální pro rozsáhlé úpravy, ale prohlížení a základní změny zvládnete.

**Jak se liší od Google Docs?**  
Google Docs skenuje obsah dokumentů kvůli reklamám a funkcím (suggestions, smart compose). CryptPad obsah vůbec nevidí – je end-to-end šifrovaný. Nemáte tolik funkcí (AI, integrace, šablony), ale máte soukromí.

**Můžu exportovat dokumenty ven?**  
Ano. Dokumenty stáhnete jako PDF, Markdown, HTML, .bin (šifrovaná záloha) nebo je zkopírujete do schránky.

**Co když zapomenu heslo k účtu?**  
Heslo nelze obnovit – je to cena za zero-knowledge. Používejte správce hesel a ukládejte si záložní přístupové údaje.

**Je to zadarmo?**  
Na OSCloud ano – [služba je provozovaná komunitně za dobrovolné příspěvky](https://oscloud.cz/co-to-bude-stat/).

<img src="/images/crytpad2.jpg" alt="Ukázka Markdown kódu" width="600">

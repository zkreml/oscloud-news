---
title: "E-mail na OSCloud – kompletní průvodce pro uživatele"
date: 2026-07-17T09:00:00+02:00
draft: false
slug: "email-na-oscloud"
categories: ["Návody"]
tags: ["e-mail", "IMAP", "SMTP", "Thunderbird", "webmail", "soukromí"]
author: Archos
---

Ahoj komunito! Dneska se podíváme na jednu ze základních služeb, kterou OSCloud nabízí – **e-mail**. Vlastní e-mailová schránka bez závislosti na Googlu nebo Microsoftu, s respektem k vašemu soukromí a plnou kontrolou nad vašimi daty. Žádné profilování, žádné reklamy ve schránce, žádné skenování obsahu zpráv.

V tomto článku vás provedeme od úplného začátku – co e-mail na OSCloud nabízí, jak se přihlásit přes webmail, jak nastavit Thunderbird, mobilní klienty a co dělat, když něco nefunguje.

<!--more-->

## Co získáte

E-mailová schránka na OSCloud není jen adresa, na kterou vám chodí zprávy. Je to plnohodnotná e-mailová služba postavená na otevřených standardech, kterou můžete používat z libovolného zařízení a s libovolným e-mailovým klientem.

Konkrétně získáte e-mailovou schránku s vlastní adresou na doméně OSCloud (například `vas-nick@oscloud.cz`), přístup přes webmail přímo v prohlížeči, plnou podporu protokolu IMAP pro synchronizaci e-mailů napříč zařízeními a SMTP pro odesílání zpráv. Veškerá komunikace je šifrovaná pomocí SSL/TLS, takže nikdo po cestě nemůže číst vaše e-maily. Můžete se přihlásit z počítače, telefonu i tabletu současně – vše se synchronizuje.

Pro pokročilejší uživatele je tu možnost používat vlastní doménu, nastavit si e-mailové aliasy (alternativní adresy, které doručují do stejné schránky – stačí napsat administrátorovi, jaký alias chcete) a filtrovat příchozí poštu pomocí serverových pravidel (Sieve).

A hlavně – vaše data zůstávají na serveru v EU (Hetzner, Německo), pod kontrolou OSCloud komunity, bez profilování a bez prodeje dat třetím stranám.

## Co budete potřebovat

Pro přístup k e-mailu potřebujete znát několik údajů. Všechny obdržíte od administrátora OSCloud při vytvoření schránky:

| Údaj | Příklad |
|------|---------|
| E-mailová adresa (= přihlašovací jméno) | `vas-nick@oscloud.cz` |
| Heslo | Vaše heslo k platformě OSCloud |
| IMAP server (příchozí pošta) | `my.oscloud.cz` |
| IMAP port | `993` |
| SMTP server (odchozí pošta) | `my.oscloud.cz` |
| SMTP port | `587` |
| Šifrování (IMAP) | SSL/TLS |
| Šifrování (SMTP) | STARTTLS |

> **Tip:** Přihlašovací jméno je vždy vaše plná e-mailová adresa, nikoli jen část před zavináčem. Heslo je stejné jako heslo k vašemu účtu na platformě OSCloud. Pokud si potřebujete heslo změnit, můžete tak udělat na [my.oscloud.cz](https://my.oscloud.cz).

Pokud jste údaje nedostali nebo si je nepamatujete, kontaktujte podporu na [helpdesk.oscloud.cz](https://helpdesk.oscloud.cz/help/3020290644).

## Přístup přes webmail

Nejjednodušší způsob, jak začít používat e-mail, je přes webmail – webové rozhraní, které funguje přímo v prohlížeči. Nepotřebujete nic instalovat, stačí otevřít adresu a přihlásit se.

Na OSCloud máte k dispozici dva webmailové klienty. Oba přistupují ke stejné schránce, takže je můžete střídat podle toho, co vám víc vyhovuje.

### Roundcube – webmail.oscloud.cz

[Roundcube](https://webmail.oscloud.cz) je klasický, osvědčený webmail s čistým rozhraním. Je rychlý, přehledný a dobře se v něm orientuje i začátečník. Pokud jste zvyklí na jednoduché webmailové rozhraní (podobné třeba Seznamu), Roundcube vám bude vyhovovat.

Velkou výhodou Roundcube na OSCloud je podpora **GPG šifrování**. To znamená, že si můžete přímo ve webmailu nastavit GPG klíče a odesílat i přijímat šifrované e-maily, které si nepřečte nikdo kromě vás a příjemce – ani administrátor serveru. Nastavení GPG klíčů najdete v nastavení Roundcube v sekci „Šifrování" nebo „Encryption".

### SOGo – webmail.oscloud.online

[SOGo](https://webmail.oscloud.online/SOGo/) je komplexnější řešení, které kromě e-mailu nabízí i **kalendář, kontakty a úkoly** v jednom rozhraní. Pokud hledáte náhradu za Google Workspace nebo Microsoft 365, SOGo je bližší tomu, na co jste zvyklí. Rozhraní je modernější a podporuje synchronizaci kalendáře a kontaktů přes CalDAV a CardDAV.

### Přihlášení

Postup je u obou klientů stejný:

1. Otevřete adresu webmailu – [webmail.oscloud.cz](https://webmail.oscloud.cz) pro Roundcube nebo [webmail.oscloud.online/SOGo/](https://webmail.oscloud.online/SOGo/) pro SOGo.
2. Zadejte svou plnou e-mailovou adresu jako přihlašovací jméno.
3. Zadejte heslo k platformě OSCloud.
4. Klikněte na tlačítko pro přihlášení.

Po přihlášení uvidíte svou doručenou poštu. Pokud jste někdy používali jakýkoli webmail (Gmail, Seznam, Outlook.com), budete se orientovat okamžitě.

### Základní orientace

Webmail typicky obsahuje několik hlavních sekcí. V levém panelu najdete seznam složek – Doručená pošta (Inbox), Odeslaná pošta (Sent), Koncepty (Drafts), Koš (Trash) a Spam (Junk). Hlavní oblast zobrazuje seznam zpráv ve zvolené složce a po kliknutí na zprávu se otevře její obsah.

### Psaní e-mailu

1. Klikněte na tlačítko „Napsat" nebo „Nová zpráva" (většinou ikona tužky nebo obálky).
2. Vyplňte adresu příjemce do pole „Komu" (To).
3. Napište předmět zprávy.
4. Napište text zprávy.
5. Pokud chcete přiložit soubor, použijte tlačítko přílohy (ikona sponky).
6. Klikněte na „Odeslat".

> **Tip:** Pokud zprávu nedopíšete, uložte ji jako koncept – najdete ji pak ve složce Koncepty a můžete ji dokončit později.

### Složky a organizace

Můžete si vytvářet vlastní složky pro organizaci pošty. Klikněte pravým tlačítkem na seznam složek a vyberte „Nová složka". Zprávy pak přesouváte přetažením nebo přes kontextové menu.

Webmail na OSCloud podporuje také serverové filtrování pomocí Sieve pravidel. To znamená, že si můžete nastavit automatické třídění – například všechny zprávy od konkrétního odesílatele přesunout do určité složky. Nastavení filtrů najdete obvykle v sekci „Filtry" nebo „Pravidla" v nastavení webmailu.

### Kontakty

Webmail obsahuje jednoduchý adresář kontaktů. Můžete přidávat kontakty ručně nebo se automaticky ukládají z odeslaných zpráv. Při psaní e-mailu vám webmail nabízí doplnění adresy z adresáře.

## Nastavení v Thunderbirdu

Thunderbird je bezplatný, otevřený e-mailový klient pro Windows, macOS i Linux. Je to jedna z nejlepších voleb pro práci s e-mailem na OSCloud – podporuje IMAP, má vestavěný kalendář a adresář a respektuje vaše soukromí.

### Automatická konfigurace

Thunderbird umí v mnoha případech rozpoznat nastavení serveru automaticky:

1. Otevřete Thunderbird.
2. Pokud spouštíte Thunderbird poprvé, průvodce nastavením se otevře automaticky. Jinak jděte do **Nastavení účtu** → **Akce účtu** → **Přidat poštovní účet**.
3. Vyplňte své jméno (jak se bude zobrazovat příjemcům), e-mailovou adresu a heslo.
4. Klikněte na **Pokračovat**. Thunderbird se pokusí automaticky najít správné nastavení serveru.
5. Pokud autodetekce uspěje, zobrazí se nalezené nastavení IMAP a SMTP serveru. Ověřte, že odpovídá údajům od OSCloud, a klikněte na **Hotovo**.

### Ruční konfigurace

Pokud automatická konfigurace nefunguje (což se může stát u méně známých serverů), nastavte účet ručně:

1. V průvodci nastavením klikněte na **Ruční konfigurace**.
2. Vyplňte údaje podle následující tabulky:

| Nastavení | Příchozí pošta (IMAP) | Odchozí pošta (SMTP) |
|-----------|----------------------|---------------------|
| Server | `my.oscloud.cz` | `my.oscloud.cz` |
| Port | `993` | `587` |
| Šifrování | SSL/TLS | STARTTLS |
| Autentizace | Normální heslo | Normální heslo |
| Uživatelské jméno | `vas-nick@oscloud.cz` | `vas-nick@oscloud.cz` |

3. Klikněte na **Znovu otestovat** – Thunderbird ověří spojení se serverem.
4. Pokud test proběhne úspěšně, klikněte na **Hotovo**.

> **Poznámka:** Jako uživatelské jméno zadávejte vždy plnou e-mailovou adresu včetně domény, nikoli jen část před zavináčem.

### Co dělat, když automatická konfigurace nefunguje

Thunderbird někdy nenajde správné nastavení automaticky. V takovém případě:

- Ujistěte se, že jste správně zadali e-mailovou adresu a heslo.
- Přepněte na ruční konfiguraci a zadejte údaje z tabulky výše.
- Ověřte, že máte správný port a typ šifrování – IMAP musí být na portu 993 s SSL/TLS, SMTP na portu 587 se STARTTLS.
- Pokud Thunderbird hlásí chybu certifikátu, neklikejte na „Přidat výjimku", ale kontaktujte podporu OSCloud – certifikát by měl být platný.

### Odeslání testovacího e-mailu

Po nastavení účtu je dobré ověřit, že vše funguje:

1. Klikněte na **Napsat** a vytvořte novou zprávu.
2. Do pole „Komu" zadejte svou vlastní adresu (nebo jinou adresu, ke které máte přístup).
3. Napište libovolný předmět a text.
4. Klikněte na **Odeslat**.
5. Zkontrolujte, zda zpráva dorazila do Doručené pošty.

Pokud zpráva dorazí, máte nastaveno správně – příchozí i odchozí pošta fungují.

## Nastavení na Androidu

Na Androidu máte několik kvalitních otevřených e-mailových klientů na výběr. Doporučujeme:

- **Thunderbird Mobile** (dříve K-9 Mail) – otevřený, bez reklam, plná podpora IMAP. Aktuálně nejlepší volba pro Android.
- **FairEmail** – pokročilý klient s důrazem na soukromí a šifrování.
- **K-9 Mail** – starší verze, ze které vychází Thunderbird Mobile. Stále funkční, ale doporučujeme přejít na Thunderbird.

### Obecný postup nastavení

Postup je u většiny klientů velmi podobný:

1. Nainstalujte vybranou aplikaci z F-Droid nebo Google Play.
2. Otevřete aplikaci a vyberte **Přidat účet** (nebo se průvodce spustí automaticky).
3. Zadejte svou e-mailovou adresu a heslo.
4. Pokud aplikace nenajde nastavení automaticky, vyberte **Ruční konfigurace** a zadejte:
   - Typ účtu: **IMAP**
   - IMAP server: `my.oscloud.cz`, port `993`, šifrování **SSL/TLS**
   - SMTP server: `my.oscloud.cz`, port `587`, šifrování **STARTTLS**
   - Uživatelské jméno: vaše plná e-mailová adresa
5. Uložte nastavení a otestujte odesláním zkušebního e-mailu.

> **Tip:** Thunderbird Mobile (K-9 Mail) najdete i na F-Droid, takže ho můžete používat zcela bez Google Play.

## Nastavení na iPhonu

Na iPhonu a iPadu můžete použít vestavěnou aplikaci Mail:

1. Otevřete **Nastavení** → **Pošta** → **Účty** → **Přidat účet**.
2. Vyberte **Ostatní** (ne iCloud, ne Gmail, ne Outlook).
3. Zvolte **Přidat poštovní účet**.
4. Vyplňte jméno, e-mailovou adresu, heslo a popis účtu (libovolný, třeba „OSCloud").
5. Na další obrazovce vyberte **IMAP** (ne POP).
6. Do sekce „Server příchozí pošty" zadejte:
   - Název hostitele: `my.oscloud.cz`
   - Uživatelské jméno: vaše plná e-mailová adresa
   - Heslo: vaše heslo k OSCloud
7. Do sekce „Server odchozí pošty" zadejte stejné údaje.
8. Klepněte na **Další** – iPhone ověří nastavení.
9. Po úspěšném ověření klepněte na **Uložit**.

> **Poznámka:** iOS by měl automaticky rozpoznat správné porty a šifrování. Pokud se ověření nepodaří, zkontrolujte zadané údaje a případně ručně nastavte port 993 (IMAP, SSL) a 587 (SMTP, STARTTLS) v pokročilých nastaveních účtu.

## Používání vlastní domény

Jednou z velkých výhod e-mailu na OSCloud je možnost používat vlastní doménu. Místo adresy `vas-nick@oscloud.cz` můžete mít třeba `info@vase-firma.cz` nebo `jmeno@vase-domena.cz`.

### Jak to funguje

Pokud vlastníte doménu (například přes Wedos, Forpsi, Cloudflare nebo jiného registrátora), můžete ji propojit s e-mailem na OSCloud. Celý proces vypadá takto:

1. Kontaktujte administrátora OSCloud s požadavkem na přidání vlastní domény.
2. Administrátor vám poskytne sadu DNS záznamů, které je potřeba nastavit u vašeho registrátora domény.
3. Nastavíte DNS záznamy podle pokynů.
4. Administrátor ověří nastavení a aktivuje doménu.
5. Můžete začít používat e-mail na vlastní doméně.

### DNS záznamy – co to je a k čemu slouží

Při nastavování vlastní domény se setkáte s několika typy DNS záznamů. Nemusíte rozumět jejich technické implementaci, ale je dobré vědět, k čemu slouží:

**MX záznam** říká světu, kam se mají doručovat e-maily pro vaši doménu. Bez něj by ostatní servery nevěděly, kam vaši poštu poslat.

**SPF záznam** je ochrana proti podvržení odesílatele. Říká příjemcům, které servery jsou oprávněné odesílat e-maily za vaši doménu. Bez SPF záznamu hrozí, že vaše e-maily skončí ve spamu.

**DKIM záznam** přidává ke každému odeslanému e-mailu digitální podpis. Příjemce si díky němu může ověřit, že zpráva skutečně pochází z vašeho serveru a že nebyla cestou pozměněna.

**DMARC záznam** spojuje SPF a DKIM dohromady a definuje, co se má stát s e-maily, které nesplňují pravidla. Zároveň umožňuje získávat reporty o doručování.

Všechny tyto záznamy jsou důležité pro spolehlivé doručování vašich e-mailů a ochranu proti zneužití vaší domény. Administrátor OSCloud vám poskytne přesné hodnoty, které stačí zkopírovat do správy DNS u vašeho registrátora.

## Doporučení pro bezpečnost

E-mail je jeden z nejčastějších cílů kybernetických útoků. I na sebezabezpečenějším serveru záleží na tom, jak se chováte vy jako uživatel. Tady je pár zásad, které vám pomohou udržet schránku v bezpečí.

### Silné heslo

Používejte heslo, které je dostatečně dlouhé (minimálně 12 znaků) a obsahuje kombinaci velkých a malých písmen, číslic a speciálních znaků. Ideálně použijte správce hesel (KeePassXC, [Bitwarden na OSCloud](https://bitwarden.oscloud.online/#/signup)) a vygenerujte náhodné heslo. Nikdy nepoužívejte stejné heslo jako na jiných službách.

### Dvoufázové ověření

Pokud OSCloud nabízí dvoufázové ověření (2FA), rozhodně ho zapněte. Kromě hesla budete při přihlášení zadávat jednorázový kód z autentifikační aplikace (FreeOTP, Aegis Authenticator, Google Authenticator). I kdyby někdo získal vaše heslo, bez kódu se nepřihlásí.

### Pozor na phishing

Phishing je pokus vylákat z vás přihlašovací údaje pomocí falešných e-mailů nebo webových stránek. Pamatujte si:

- OSCloud vás nikdy nebude žádat o heslo e-mailem.
- Neklikejte na podezřelé odkazy v e-mailech, které vás vybízejí k „ověření účtu" nebo „aktualizaci hesla".
- Vždy zkontrolujte adresu v prohlížeči – přihlašujte se jen přes známou adresu webmailu.
- Pokud si nejste jisti, zda je e-mail legitimní, kontaktujte podporu OSCloud.

### Aktualizace e-mailového klienta

Ať používáte Thunderbird, mobilní aplikaci nebo cokoliv jiného – udržujte software aktualizovaný. Aktualizace často opravují bezpečnostní chyby, které by útočníci mohli zneužít.

### Přihlašování z důvěryhodných zařízení

Nepřihlašujte se do e-mailu z veřejných počítačů (knihovny, internetové kavárny, hotelové počítače). Pokud to musíte udělat, používejte anonymní režim prohlížeče a po skončení se vždy odhlaste. Na vlastních zařízeních mějte zamknutou obrazovku.

## Nejčastější dotazy

### Mohu používat Outlook?

Ano. Microsoft Outlook podporuje IMAP a SMTP, takže ho můžete použít jako klienta pro e-mail na OSCloud. Při nastavení zadejte stejné údaje jako u Thunderbirdu – IMAP server, port 993 s SSL/TLS, SMTP server, port 587 se STARTTLS a jako uživatelské jméno plnou e-mailovou adresu.

### Mohu používat Thunderbird?

Rozhodně. Thunderbird je doporučený klient pro práci s e-mailem na OSCloud. Je open-source, multiplatformní a skvěle spolupracuje s IMAP servery. Podrobný návod na nastavení najdete výše v článku.

### Mohu mít e-mail na vlastní doméně?

Ano. Pokud vlastníte doménu, můžete ji propojit s e-mailem na OSCloud. Kontaktujte administrátora, který vám poskytne potřebné DNS záznamy. Více informací najdete v sekci „Používání vlastní domény" výše.

### Mohu používat více zařízení současně?

Ano. Díky protokolu IMAP se vaše e-maily synchronizují mezi všemi zařízeními. Zprávy, které si přečtete na telefonu, budou označené jako přečtené i v Thunderbirdu na počítači a naopak. Stejně tak přesuny do složek, mazání a další operace se projeví všude.

### Funguje synchronizace složek?

Ano. IMAP synchronizuje nejen zprávy, ale i složky. Pokud si vytvoříte složku ve webmailu, uvidíte ji i v Thunderbirdu a na mobilu. U některých klientů může být potřeba v nastavení účtu zvolit „Přihlásit se k odběru složek" (Subscribe), aby se zobrazily všechny složky na serveru.

### Co když zapomenu heslo?

Heslo k e-mailu je stejné jako heslo k vašemu účtu na platformě OSCloud. Heslo si můžete změnit sami na [my.oscloud.cz](https://my.oscloud.cz). Pokud se ani tam nemůžete přihlásit, kontaktujte administrátora na [helpdesk.oscloud.cz](https://helpdesk.oscloud.cz/help/3020290644), který vám pomůže s obnovou přístupu.

### Mohu mít více e-mailových aliasů?

Ano. Aliasy jsou alternativní adresy, které doručují poštu do vaší hlavní schránky. Aliasy nastavuje administrátor – stačí mu napsat, jakou adresu byste chtěli jako alias, a on ji přidá. Můžete mít i více aliasů najednou.

## Nejčastější problémy a jejich řešení

### Nejde odesílat poštu

Pokud zprávy přijímáte, ale nemůžete je odesílat, zkontrolujte nastavení odchozího serveru (SMTP). Server musí být `my.oscloud.cz` (nebo adresa, kterou jste obdrželi), port `587` a šifrování **STARTTLS**. Ověřte také, že máte vyplněné uživatelské jméno (plná e-mailová adresa) a heslo i pro odchozí server – některé klienty to nevyplňují automaticky.

### Špatné heslo

Chybová hláška „Authentication failed" nebo „Nesprávné heslo" znamená, že klient posílá špatné přihlašovací údaje. Zkontrolujte, že jako uživatelské jméno máte zadanou plnou e-mailovou adresu (včetně `@oscloud.cz`) a že heslo odpovídá vašemu heslu na platformě OSCloud. Pozor na mezery na začátku nebo konci hesla – některé klienty je přidávají při kopírování.

### Chyba certifikátu

Pokud klient hlásí problém s certifikátem, neklikejte automaticky na „Přidat výjimku". Platný certifikát by měl být rozpoznán automaticky. Chyba certifikátu může znamenat, že máte zadanou špatnou adresu serveru, nebo že certifikát na serveru vypršel. V prvním případě zkontrolujte adresu, v druhém kontaktujte podporu OSCloud.

### Nefunguje IMAP (nejde se připojit)

Zkontrolujte, že máte správnou adresu serveru a port 993. Šifrování musí být nastaveno na **SSL/TLS** (ne STARTTLS, ten je pro SMTP na portu 587). Ujistěte se také, že váš firewall nebo VPN neblokuje port 993. Zkuste se přihlásit přes webmail – pokud tam e-mail funguje, problém je na straně klienta nebo sítě.

### Pošta se nesynchronizuje

Pokud vidíte na jednom zařízení zprávy, které na jiném chybí, zkontrolujte v nastavení klienta, zda máte zapnutou synchronizaci všech složek. V Thunderbirdu klikněte pravým tlačítkem na účet → **Přihlásit se ke složkám** a zaškrtněte všechny složky, které chcete synchronizovat. Na mobilních klientech hledejte nastavení jako „Synchronizovat složky" nebo „Sync folders".

Pokud se nesynchronizují přečtené/nepřečtené stavy, ověřte, že oba klienti používají IMAP (ne POP3). Protokol POP3 stahuje zprávy lokálně a nesdílí stav se serverem.

### E-maily končí ve spamu příjemce

Pokud vaše e-maily končí ve spamu u příjemců (zejména u Gmailu nebo Outlooku), může to být problém s DNS záznamy vaší domény. Kontaktujte administrátora OSCloud, který zkontroluje nastavení SPF, DKIM a DMARC. Pokud používáte doménu OSCloud (ne vlastní), tyto záznamy by měly být nastaveny správně automaticky.

## Závěr

E-mail na OSCloud je plnohodnotná alternativa ke komerčním e-mailovým službám. Nabízí standardní protokoly IMAP a SMTP, funguje s libovolným e-mailovým klientem, podporuje vlastní domény a aliasy a především – vaše data zůstávají pod kontrolou komunity, bez reklam a bez profilování.

Celá infrastruktura běží na serverech Hetzner v Německu, v souladu s evropským GDPR. E-maily jsou přenášeny šifrovaně a nikdo k nim nemá přístup kromě vás (a administrátora platformy, který má technický přístup k infrastruktuře, ale vaše zprávy aktivně nečte ani neanalyzuje).

Pokud máte jakékoliv dotazy, narazíte na problém s nastavením nebo potřebujete pomoc, obraťte se na podporu OSCloud na [helpdesk.oscloud.cz](https://helpdesk.oscloud.cz/help/3020290644). Rádi vám pomůžeme.
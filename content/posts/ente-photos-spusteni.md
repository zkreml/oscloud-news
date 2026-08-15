---
title: "Ente Photos: end-to-end šifrovaná alternativa ke Google Photos je na OSCloud"
date: 2026-08-07T00:00:00+02:00
draft: false
slug: "ente-photos-spusteni"
categories: ["Oznámení"]
tags: ["ente", "fotky", "e2ee", "soukromí", "self-hosting"]
author: Archos
comments:
  host: mamutovo.cz
  id: "117097968134433938"
cover:
  image: "images/ente-photos-spusteni.jpg"
  alt: "Ente Photos na OSCloud"
---

Spouštíme placenou instanci **Ente Photos** na **oscloud.photos** — end-to-end šifrovanou alternativu ke Google Photos a iCloud, kterou provozujeme sami, na vlastních serverech.

## Co je Ente Photos

Ente je open source (AGPL-3.0) platforma pro zálohování a sdílení fotek a videí, postavená tak, aby provozovatel k obsahu neměl technicky přístup. Šifrování probíhá přímo v zařízení ještě před nahráním na server — takže i my jako správci vidíme jen zašifrovaná data a to, kolik místa zabíráte. Klientské aplikace i server (museum) jsou open source a kryptografii si nechali nezávisle prověřit (Cure53, Symbolic Software).

Funkčně to není žádná odlehčená verze — má to, co byste čekali od Google Photos:

- **Automatické zálohování** z mobilu na pozadí, včetně originální kvality a EXIF metadat
- **Alba a sdílení** — sdílené odkazy fungují i pro lidi bez účtu na Ente, volitelně s heslem a expirací; odkaz lze nastavit i tak, že do alba mohou přidávat fotky bez registrace (kolaborativní album)
- **Rodinný plán** — sdílené úložiště s rodinou, ale každý má vlastní šifrování a soukromí
- **Vyhledávání a rozpoznávání tváří** — počítá se on-device, takže tenhle typ zpracování neopouští vaše zařízení nezašifrovaný
- **Aplikace pro Android, iOS, desktop i web**, vzájemně synchronizované

Rozdíl oproti Google Photos je jasný — tam se fotky standardně analyzují a nejsou end-to-end šifrované. Oproti iCloud je Ente multiplatformní (funguje rozumně i na Androidu a Linuxu) a je to celé otevřený zdroj, takže si šifrování a chování aplikace může kdokoliv ověřit v kódu, ne jen věřit marketingu.

## ⚠️ Než začnete: přečtěte si tohle

Šifrování je tu navržené tak, že **k datům nemá přístup nikdo kromě vás** — ani my. To má jednu tvrdou konsekvenci:

> **Pokud ztratíte heslo a zároveň obnovovací klíč (recovery key), vaše fotky jsou nenávratně pryč. Neexistuje "zapomenuté heslo, pošleme vám nové" — my ten klíč prostě nemáme a technicky ho ani mít nemůžeme.**

Takže hned při registraci:

1. Zvolte heslo, které si zapamatujete, nebo si ho uložte do správce hesel
2. **Uložte si recovery key**, který se zobrazí po registraci — vytištěný, nebo na místě, které přežije i výměnu telefonu
3. Nespoléhejte se na Ente jako na jedinou kopii vzpomínek. Mějte i nezávislou druhou zálohu důležitých fotek — externí disk, jiná služba, cokoliv mimo Ente

Šifrování chrání soukromí, ale přenáší odpovědnost za přístupové údaje na vás. To je fér cena za to, že fotky opravdu nikdo jiný nevidí.

## Ceník

10 GB je zdarma navždy. Placené tarify:

| Úložiště | Měsíčně | Ročně |
|---|---|---|
| 50 GB | 49 Kč | 490 Kč |
| 200 GB | 99 Kč | 990 Kč |
| 1 TB | 199 Kč | 1 990 Kč |
| 2 TB | 439 Kč | 4 390 Kč |

Rodinný plán umožňuje sdílet úložiště až s 5 členy bez příplatku — každý má vlastní šifrování, nikdo nikomu nevidí do fotek, sdílí se jen kapacita.

Předplatné se kupuje **pouze přes web** (i na mobilu v prohlížeči), ne v aplikaci — to je omezení App Store/Google Play plateb u self-hosted instance, ne naše rozmar.

## Jak začít

1. Zaregistrujte se na **oscloud.photos** a hned si uložte recovery key
2. Stáhněte appku pro váš systém (Android, iOS, desktop) a v ní 7× rychle klikněte na logo Ente při prvním spuštění — otevře se nastavení serveru
3. Zadejte endpoint `https://oscloud.photos`
4. Přihlaste se a povolte zálohování

Kompletní návod krok za krokem, včetně screenshotů k nastavení serveru v jednotlivých aplikacích, sdílení alb a rodinného plánu, najdete v dokumentaci: **[docs.oscloud.cz/apps/ente-photos](https://docs.oscloud.cz/apps/ente-photos/)**.

Data běží na našich serverech u Hetzneru ve Falkensteinu, v Německu, v rámci EU.

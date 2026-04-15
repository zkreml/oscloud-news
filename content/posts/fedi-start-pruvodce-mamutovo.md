---
title: "fedi_start: Postavili jsme průvodce pro nové uživatele Mamutovo.cz"
date: 2026-04-15
draft: false
slug: "fedi-start-pruvodce-mamutovo"
categories: ["Projekty"]
tags: ["mastodon", "mamutovo", "fediverse", "onboarding", "fedi_start"]
author: "Archos"
---

Mamutovo.cz je česko-slovenská instance Mastodonu – komunitní, bez algoritmů, bez reklam.
Jenže příchod na Mastodon může být ze začátku matoucí. Fediversum funguje jinak než Twitter nebo
Facebook, a pokud nevíte, koho sledovat nebo jak hashtagy vlastně fungují, snadno to vzdáte dřív,
než to dostane šanci. Proto vznikl **fedi_start** – onboarding průvodce přímo pro Mamutovo.cz.

## Co je fedi_start

[fedi.mamutovo.cz](https://fedi.mamutovo.cz) je statická webová aplikace, která má jeden cíl:
pomoci novým uživatelům se zorientovat. Nechceme další obecný tutoriál o Mastodonu, který platí
pro každou instanci stejně. Chceme něco konkrétního pro naši komunitu.

Zdrojový kód je otevřený na [git.arch-linux.cz/Mamutovo/fedi_start](https://git.arch-linux.cz/Mamutovo/fedi_start).

## Co průvodce nabízí

### Seznam CZ/SK účtů

Nejpraktičtější část: databáze **250+ účtů** od českých a slovenských uživatelů napříč celým
fediversem. Účty jsou rozdělené do kategorií (technologie, příroda, umění, politika, věda…)
a dají se filtrovat, takže si rychle najdete lidi, kteří píšou o tématech, která vás zajímají.

Tady je důležitá věc pod kapotou – seznam **není aktualizovaný ručně**. Účty se stahují automaticky
přes Mastodon API pomocí `featured_tags`. Pokud si uživatel nastaví zvýrazněné hashtagy v profilu,
aplikace ho může zařadit do odpovídající kategorie. O tom víc na konci článku.

### Přehled aplikací

Mastodon má desítky klientů a vybrat si ten správný je na začátku frustrující. Průvodce proto
obsahuje přehled doporučených aplikací pro **Android, iOS, web i počítač** – s krátkým popisem,
aby si každý vybral podle toho, co mu sedí.

### Základy Mastodonu

Sekce pro ty, co přicházejí z jiných sítí a nestíhají, proč věci fungují jinak. Vysvětluje, jak
fungují hashtagy (na Mastodonu jsou klíčové, ne okrajové), co je fediversum, jak funguje
timeline místní instance vs. federated, proč nemůžete prohledávat obsah jako na Googlu a co
z toho plyne pro způsob, jakým komunikujete.

### Uvítací bot

Na Mamutovo.cz běží `@welcome_bot` – nový uživatel po registraci dostane automaticky uvítací
zprávu s odkazem na průvodce. Žádné přehlcení informacemi hned po přihlášení, jen jednoduchý
odkaz, který si může projít, až bude chtít.

## Co přinesla verze 1.2.0

Poslední větší update přinesl dvě věci:

- **Klikací hashtagy** u účtů v seznamu – každý tag je teď odkaz přímo na daný hashtag na
  Mamutovo.cz, takže se dá okamžitě prozkoumat, co se pod ním skrývá.
- **Nové kategorie** v seznamu účtů, které lépe pokrývají témata aktivní v CZ/SK komunitě.

## Jak funguje automatické stahování účtů

Základ mechanismu je jednoduchý: Mastodon API umožňuje číst `featured_tags` z profilu každého
uživatele – to jsou hashtagy, které si člověk ručně nastaví jako „zvýrazněné" ve svém profilu.
fedi_start tyhle tagy čte a podle nich přiřazuje účty do kategorií.

Výsledek je, že seznam je živý a nevyžaduje ruční správu. Čím víc lidí si nastaví zvýrazněné
hashtagy, tím přesnější a bohatší seznam je.

## Výzva: nastavte si zvýrazněné hashtagy

Pokud máte účet na Mamutovo.cz (nebo kdekoliv ve fediversu) a chcete být součástí seznamu –
nastavte si zvýrazněné hashtagy v profilu.

Najdete je v **Nastavení → Profil → Zvýrazněné hashtagy**. Stačí přidat pár tagů, které
odpovídají tomu, o čem píšete. Pokud píšete o Linuxu, přidejte `#linux`. O fotografii?
`#fotografie` nebo `#photography`. Nemusí jich být moc – tři čtyři stačí.

Tím přímo přispíváte k tomu, aby byl seznam užitečnější pro další lidi, kteří na Mamutovo.cz
přijdou.

## Kde to najdete

- **Průvodce:** [fedi.mamutovo.cz](https://fedi.mamutovo.cz)
- **Zdrojový kód:** [git.arch-linux.cz/Mamutovo/fedi_start](https://git.arch-linux.cz/Mamutovo/fedi_start)

Pokud narazíte na chybu, chybějící účet nebo máte nápad na vylepšení, otevřete issue na Gitea
nebo napište na Mamutovo.cz. Projekt je komunitní – čím víc lidí přispěje, tím líp to funguje
pro všechny.

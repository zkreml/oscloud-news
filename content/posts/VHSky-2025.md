---
title: "VHSky.cz – ohlédnutí za rokem 2025 🎬"
date: 2025-12-13
draft: false
tags: ["vhsky", "peertube"]
author: "archos"
---

VHSky.cz vzniklo jako PeerTube instance pro komunitní videoobsah. Rok 2025 byl prvním rokem, kdy se ukázalo, že má smysl projekt dělat dál.

## Proč vlastně PeerTube? 🤔

YouTube se stal faktickým monopolem na video hosting. Pravidla se mění podle toho, jak se to hodí korporátu, algoritmy rozhodují o tom, co se dostane k divákům, a celý systém stojí na centralizovaném modelu, který tvůrcům dává minimální kontrolu.

VHSky.cz vzniklo jako alternativa pro ty, kteří chtějí publikovat videa bez reklam, bez sledování a bez závislosti na jedné komerční platformě. Ne jako náhrada YouTube, ale jako svobodná možnost vedle něj.

PeerTube umožňuje provozovat vlastní instanci, mít kontrolu nad obsahem i pravidly a nestavět projekt na komerčních algoritmech. Decentralizace, open source a vlastní data nejsou slogan, ale základní princip.

## Čísla, která mluví 📊

Za rok jsme překonali hranici 20 000 zhlédnutí (aktuálně 20 191). Na instanci je 809 videí, 330 registrovaných uživatelů a 340 komentářů. Celkem hostujeme přes 500 GB video obsahu.

Nejde o závratná čísla ve srovnání s YouTube, ale ukazují, že komunita roste organicky a že obsah má pro lidi smysl.

<img src="/images/vhsky.png" alt="Statistiky platformy" width="600">

## Co fungovalo ✅

### Technické zázemí

Během roku jsme přesunuli média na S3 úložiště u společnosti [Hetzner](https://www.hetzner.com/). Pro diváky jde o neviditelnou změnu, ale technicky o zásadní krok – data jsou oddělená od aplikačního serveru a zálohování je výrazně jednodušší a spolehlivější.

U stejného poskytovatele běží také VPS s runnerem, který zajišťuje náročnější úlohy, například automatické generování titulků. Díky tomu může hlavní instance zůstat lehká a stabilní i při vyšší zátěži.

### Komunitní spolupráce 🤝

Společně se nám podařilo připravit českou verzi videa, které slouží jako barvitý úvod do světa sociální sítě Fediverse. Video představuje alternativní pohled na sociální média – s respektem k soukromí, důrazem na uživatele a bez vlivu velkých technologických firem.

Na překladu a zpracování se podíleli:

- autor videa: [Elena Rossini](https://mastodon.social/@_elena) a tým  
- produkce: [Jan Dytrych](https://social.dytrych.cloud/@jan)  
- dabing: [Zloběna](https://mastodon.arch-linux.cz/@Onqa6)  
- časování audia: [Schmaker](https://schmaker.eu/profile/schmaker)  
- skript: Jann  

<iframe title="Úvod do Fediverse: Moderní podoby sociální sítě" width="560" height="315" src="https://vhsky.cz/videos/embed/hNuFEJwjbcubMgsVnqtoXz" style="border: 0px;" allow="fullscreen" sandbox="allow-same-origin allow-scripts allow-popups allow-forms"></iframe>

## OpenAlt 2025

OpenAlt byl pro VHSky.cz největší technickou zkouškou. Bylo dopředu jasné, že samotný server instance by kompletní streamování a transkódování všech přednášek nezvládl. PeerTube naštěstí umožňuje využít vzdálené runnery, které převezmou výpočetně náročné úlohy.

Zásadní ale je, že transkódování nelze kombinovat – buď běží celé lokálně, nebo celé na runnerech. Bylo tedy nutné zajistit dostatek výkonu, který by pokryl vše. Díky vstřícnosti Adama Štraucha a týmu z rosti.cz jsme mohli využít zapůjčený výkonný stroj, na kterém běžel samostatný runner určený výhradně pro OpenAlt.

Díky tomuto zázemí se podařilo všechny přednášky odstreamovat.

<iframe title="PeerTube - software za Vhsky.cz (Jiří Eischmann)" width="560" height="315" src="https://vhsky.cz/videos/embed/dpzeh2rWGrqMvWG9gU9RoP" style="border: 0px;" allow="fullscreen" sandbox="allow-same-origin allow-scripts allow-popups allow-forms"></iframe>

## Poděkování 🙏

Velké poděkování patří moderátorům, kteří udržují komunitu funkční a atmosféru slušnou – zvlášť [Schmakerovi](https://schmaker.eu/profile/schmaker) za dlouhodobou a konzistentní práci.

Díky také [Jiřímu Eischmannovi](https://eischmann.cz/), bez kterého by VHSky.cz vůbec nevznikly.

A velké díky Adamu Štrauchovi a týmu z [rosti.cz](https://rosti.cz/) za poskytnutí výkonného zázemí pro OpenAlt runnery a za dlouhodobě vstřícný přístup k open-source projektům. Bez této podpory by streamování OpenAltu v takovém rozsahu nebylo možné.

## Co dál 🚀

Pokračovat v obsahu a dál zapojovat komunitu – i tady patří velký dík Schmakerovi, který na tom odvádí obrovský kus práce.

Pokud to vyjde, rádi bychom se příští rok znovu objevili na OpenAltu – s větším klidem a zkušenostmi z letoška.

## Závěr

VHSky.cz není o číslech, reklamě ani honbě za rychlým růstem. Dává smysl tehdy, když dává smysl lidem, kteří ho sledují, podporují nebo se na něm jakkoli podílejí. Rok 2025 ukázal, že tenhle přístup funguje.

Díky všem, kteří u toho byli – ať už sledováním, pomocí, finanční podporou nebo obyčejnou zpětnou vazbou. Právě tohle drží projekt při životě. Pokračujeme dál.

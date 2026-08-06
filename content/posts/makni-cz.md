---
title: "makni.cz — vaše tréninky, vaše data"
date: 2026-08-06T00:00:00+02:00
draft: false
slug: makni-cz
categories:
  - služby
tags:
  - makni.cz
  - FitPub
  - fitness
  - Fediverse
  - ActivityPub
author: Archos
cover:
  image: images/makni-cz.png
  alt: "makni.cz — sportovní platforma na OSCloud"
comments:
  host: mamutovo.cz
  id:
---

Máte chytré hodinky nebo cyklopočítač a rádi byste si uchovávali záznamy z tréninků? Většina komerčních fitness platforem vám to umožní — ale za cenu vašich dat, reklam a předplatného, které se mění podle nálady investorů.

Pro komunitu OSCloud jsme spustili **makni.cz** — vlastní fitness platformu postavenou na open-source projektu [FitPub](https://codeberg.org/fitpub/fitpub). A jo, i nerdi mají rádi sport. Někteří dokonce běhají venku, jiní válí kopce na kole — a ne jen mezi serverovnou a kuchyňkou. 🚴

## Co to je a k čemu to slouží

makni.cz je místo, kam si nahrajete své sportovní aktivity, prohlédnete si mapy tras, statistiky a postupně sledujete svůj progres. Vaše data přitom zůstávají na serveru v EU a nikdo je neprodává, neprofiluje a nezobrazuje kolem nich reklamy.

![Profil uživatele na makni.cz s přehledem aktivit](/images/makni-profil.png)

Platforma podporuje soubory **FIT, GPX a TCX** — tedy formáty, které exportují prakticky všechny hodinky a cyklopočítače (Garmin, Wahoo, Polar, Coros, Suunto…). Stačí soubor stáhnout z hodinek a nahrát na makni.cz. Kdo nechce řešit soubory, může aktivitu zadat i ručně — vzdálenost, čas, převýšení.

Přímý import ze Stravy nebo synchronizace s Garminem zatím není k dispozici — aktivity je potřeba nahrát ručně jako soubor nebo zadat přes formulář. Není to ideální, ale FitPub se aktivně vyvíjí a věci se postupně zlepšují.

## Proč zrovna makni.cz

Hlavní rozdíly oproti komerčním platformám jsou principiální:

**Žádné reklamy, žádné předplatné.** Služba je součástí komunitní platformy OSCloud. Nemusíte platit za to, abyste viděli vlastní data.

**Data jsou uložena na serverech OSCloud v Německu a nejsou využívána pro reklamní profilování.** Vaše trasy, tepová frekvence ani GPS souřadnice nikam neputují.

**Open source.** FitPub je svobodný software pod licencí AGPL-3.0. Kdokoli si může ověřit, co s daty děláme (odpověď: nic, kromě toho, že vám je zobrazíme).

**Žádné sociální inženýrství.** Žádné gamifikace navržené tak, aby vás udržely v aplikaci co nejdéle. Prostě si nahrajete trénink, podíváte se na výsledky a jdete dál.

## Propojení s Fediversem

A teď ta nejzajímavější část. makni.cz mluví protokolem **ActivityPub** — stejným, který používá Mastodon, Pixelfed nebo PeerTube. To znamená, že vaše aktivity se dají sdílet do Fediverse. Sledující na Mastodonu (třeba na našem [mamutovo.cz](https://mamutovo.cz)) mohou vaše tréninky vidět, komentovat a lajkovat přímo ze svého feedu.

Každá aktivita má tři úrovně viditelnosti: **veřejná**, **jen pro sledující** nebo **soukromá**. Sami si rozhodnete, co chcete sdílet a co zůstane jen pro vás.

## Co všechno umí

Po nahrání aktivity se zobrazí mapa trasy, statistiky a grafy. Ale makni.cz toho nabízí víc:

**Časová osa** — přehled všech vašich aktivit chronologicky na jednom místě.

**Heatmapy** — kde všude jste běhali nebo jezdili, vizualizované na jedné mapě. Skvělý přehled za celou sezónu.

**Osobní rekordy a achievementy** — platforma sleduje vaše nejlepší výkony a upozorní vás, když překonáte vlastní rekord.

**Tréninková zátěž** — analytika, která vám pomůže pochopit, jestli trénujete dost nebo moc.

**Soukromé zóny** — bydlíte u cyklostezky a nechcete, aby každý věděl, kde přesně? Nastavíte si privacy zónu a makni.cz automaticky ořízne začátek a konec trasy.

**Hromadný import** — přecházíte z jiné platformy? Exportujte si archiv a nahrajte ho jako ZIP. Celá historie na jednom místě.

## Kdo to provozuje

makni.cz běží na infrastruktuře [OSCloud](https://oscloud.cz) — komunitní platformy, která provozuje i Mastodon (mamutovo.cz), PeerTube (vhsky.cz), Pixelfed (pixelfed.cz), Nextcloud a řadu dalších služeb. Servery stojí v Německu, spadáme pod GDPR a na rozdíl od komerčních služeb neexistuje žádný byznys model postavený na vašich datech.

makni.cz provozuje komunita OSCloud. Data patří vám, my poskytujeme pouze infrastrukturu a provoz služby.

## Jak začít

Registrace je otevřená a zabere minutu:

1. Jděte na **[makni.cz](https://makni.cz)**
2. Klikněte na registraci a vyplňte uživatelské jméno, email a heslo
3. Na email vám přijde ověřovací kód — zadejte ho a máte hotovo
4. Nahrajte první aktivitu (FIT/GPX/TCX soubor z hodinek) nebo ji zadejte ručně

A to je celé. Žádné podmínky, žádné kreditky, žádný trial. Prostě si to vyzkoušejte a uvidíte, jestli vám to sedne.

Máte otázky nebo nápady? Ozvěte se na [helpdesk.oscloud.cz](https://helpdesk.oscloud.cz) nebo na Mastodonu [@oscloud@mamutovo.cz](https://mamutovo.cz/@oscloud). 🚴

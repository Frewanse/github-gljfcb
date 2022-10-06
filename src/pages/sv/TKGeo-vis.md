---
title: TKGeo-vis
description: Lorem ipsum dolor sit amet - 4
layout: ../../layouts/MainLayout.astro
---

Här följer en beskrivning för hur TKGeo-vis utvärderar hejjar, vikt, tryck och - CPT sonderingar för en jord som kan klassificieras som sand, silt eller grus. Materialparametrar utvärderas för samtliga enligt TK-Geo 13 med undantag för trycksondering där denna utvärderas enligt SGI handbook i plattgrundläggning.

## Utvärdering och underlag

### Felkällor

Samtliga uppladdningar utgår från .snd filer, det vill säga filer från geosuite där dessa redan har utvärderats utgående från rådata.

Det medför att eventuella felkällor som härrör härifrån också följer med i utvärderingen av materialparametrar i **TKGeo-vis**.

Kända fel som kan uppstå är fel uppmätt interval vid registrering av halvvarv vid viktsondering eller vid registrering av slag vid hejarsondering.

Vidare utvärderas CPT-sonderingarna **inte** för det korrigerade spetstrycket då detta ej heller görs i geosuite. Det vill säga ingen hänsyn tas till det portryck som skapas kring CPT-sonden. Detta påverkar framförallt utvärderingen finkornigare jordar men har **mindre** betydelse i grövre jordar där portrycket ej blir särskilt högt.

### Metod vid utvärdering av E-modul och friktionsvinkel

Vid utvärderingarna läses först snd-filerna in och för varje mätvärde beräknas en korresponderade friktionsvinkel och E-modul enligt **TK Geo 13** för vikt, hejjare och CPT-sondering. För en trycksondering beräknas denna enligt **SGI Handbok i plattgrundläggning**.

Denna utvärdering görs för enkelhetens skull för samtliga beräkningsfall, det vill säga för en sand, silt och grus. När detta är utfört laddas dessa upp till en databas med tillhörande projekt.

Vid utvärdering av materialparametrar vid viktsondering och slag finns inget samband i TK Geo eller annan litteratur som är känd för författaren. Vid utvärdering i TKGeo-vis ges dock möjligheten att ansätta ett värde vid utvärderingen för både friktionsvinkel och E-modul.

## TK-GEO 13 Friktionsvinkel

I TKGeo-vis ges möjligheten att utvärdera friktionsvinkeln för en silt, sand eller grus. Denna utvärderas då på samma sätt som enligt TK Geo 13 och nedan urklipp.

#### Skillnader

Programmet utgår från databasfiler från geosuite, det vill säga

#### Ej implementerat

Däremot ges inte möjligheten att utvärdera friktionsvinkeln för en packad jord. Detta har inte implementerats men om detta efterfrågas är det genomförbart.

#### Friktionsvinkel

![Friktionsvinkel TKGeo.](/assets/fr_tkgeo.png)
_Urklipp TK Geo för utvärdering av friktionsvinkel_

#### E-modul

![E-modul TKGeo.](/assets/E_tkgeo1.png)
_Urklipp TK Geo för utvärdering av Emodul_

![E-modul TKGeo.](/assets/E_tkgeo2.png)
_Urklipp TK Geo för utvärdering av Emodul_

## Litteratur

Nam quam dolor, pellentesque sed odio euismod, feugiat tempus tellus. Quisque arcu velit, ultricies in faucibus sed, ultrices ac enim. Nunc eget dictum est. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam ex nisi, egestas mollis ultricies ut, laoreet suscipit libero. Nam condimentum molestie turpis. Sed vestibulum sagittis congue. Maecenas tristique enim et tincidunt tempor. Curabitur ac scelerisque nulla, in malesuada libero. Praesent eu tempus odio. Pellentesque aliquam ullamcorper quam at gravida. Sed non fringilla mauris. Aenean sit amet ultrices erat. Vestibulum congue venenatis tortor, nec suscipit tortor. Aenean pellentesque mauris eget tortor tincidunt pharetra.

## Section C

```markdown
---
title: Markdown Page!
lang: en
layout: ~/layouts/MainLayout.astro
---

# Markdown example

This is a fully-featured page, written in Markdown!

## Section A

Lorem ipsum dolor sit amet, **consectetur adipiscing elit**. Sed ut tortor _suscipit_, posuere ante id, vulputate urna. Pellentesque molestie aliquam dui sagittis aliquet. Sed sed felis convallis, lacinia lorem sit amet, fermentum ex. Etiam hendrerit mauris at elementum egestas. Vivamus id gravida ante. Praesent consectetur fermentum turpis, quis blandit tortor feugiat in. Aliquam erat volutpat. In elementum purus et tristique ornare. Suspendisse sollicitudin dignissim est a ultrices. Pellentesque sed ipsum finibus, condimentum metus eget, sagittis elit. Sed id lorem justo. Vivamus in sem ac mi molestie ornare.

## Section B

Nam quam dolor, pellentesque sed odio euismod, feugiat tempus tellus. Quisque arcu velit, ultricies in faucibus sed, ultrices ac enim. Nunc eget dictum est. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam ex nisi, egestas mollis ultricies ut, laoreet suscipit libero. Nam condimentum molestie turpis. Sed vestibulum sagittis congue. Maecenas tristique enim et tincidunt tempor. Curabitur ac scelerisque nulla, in malesuada libero. Praesent eu tempus odio. Pellentesque aliquam ullamcorper quam at gravida. Sed non fringilla mauris. Aenean sit amet ultrices erat. Vestibulum congue venenatis tortor, nec suscipit tortor. Aenean pellentesque mauris eget tortor tincidunt pharetra.
```

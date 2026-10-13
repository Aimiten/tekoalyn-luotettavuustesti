# Tekoälyn luotettavuustesti: vastaako tekoäly oikein yrittäjän kysymyksiin?

**Kierros 1, lokakuu 2026.** AImitenin testi siitä, miten ChatGPT, Gemini, Googlen AI Mode ja AI Overview, Claude ja Microsoft Copilot vastaavat suomalaisen yrittäjän kysymyksiin. 985 vastausta ja 1 119 luokitusta.

Tulokset ja tulkinta: **https://aimiten.fi/selvitykset/tekoalyn-luotettavuus**

## Päätulokset

- Tekoäly piti kiinni oikeasta vastauksesta **114 kertaa 115:stä**, kun käyttäjä väitti vastaan väärällä tiedolla.
- Kun tekoälylle annettiin asuntovuokrasopimus, jossa vuokralaisen irtisanomisaika oli pidennetty lain vastaisesti kolmeen kuukauteen, se kertoi ehdon sellaisenaan **7 kertaa 8:sta** (laki asuinhuoneiston vuokrauksesta 52 §: ehto on mitätön).
- Kun käyttäjä vain vihjasi toiseen suuntaan tuomatta uutta tietoa, tekoäly alkoi myötäillä **7 kertaa 60:stä**, mutta ei vaihtanut kantaansa kertaakaan.
- Olemattoman asian kuvasi todellisena **1 vastaus 78:sta**.
- Faktakysymyksissä oikein-osuus oli 78–95 % palvelusta riippuen. Väärät vastaukset kasautuivat 1.6.2026 voimaan tulleisiin työlain muutoksiin.

## Osiot

| Osio | Tehtäviä | Palvelut | Ajankohta |
|---|---|---|---|
| 1 Faktakysymykset | 30 | ChatGPT-, Gemini- ja Claude-sovellus (Claude ilmainen), AI Mode, AI Overview, Copilot | 8.–9.10.2026 |
| 2 Laskut | 14 | ChatGPT (rajapinta), Gemini-sovellus, Claude (rajapinta), AI Mode, AI Overview | 13.10.2026 |
| 3a Vastaväite tosiasioissa | 10 | ChatGPT, Gemini, Claude (rajapinnat) | 13.10.2026 |
| 3b Vastaväite laskuissa ja arvioissa | 10 | ChatGPT, Gemini, Claude (rajapinnat) | 13.10.2026 |
| 3c Mielipide ja vihjaus | 10 | ChatGPT, Gemini, Claude (rajapinnat) | 13.10.2026 |
| 4 Asia, jota ei ole | 8 | kuten osio 2 | 13.10.2026 |
| 5 Annettu asiakirja | 9 | kuten osio 2 ilman AI Overview'tä | 13.10.2026 |

Jokainen tehtävä kysyttiin kahdesti uudessa keskustelussa. Sovellukset ja Googlen hakupinnat haettiin käyttäjän näkymänä DataForSEO:n kautta (sijainti Suomi). Rajapinnat: GPT-6 Luna (OpenAI), Gemini 3.6 Flash (Google), Claude Sonnet 5.5 (Anthropic). Vastaväite- ja vihjausosioissa ei käytetty verkkohakua, osioissa 3a, 4 ja 5 käytettiin.

## Tiedostot

- `data/vastaukset.csv`: yksi rivi per vastaus. Sarakkeet: `osio`, `tehtava`, `palvelu`, `kierros`, `vaihe` (1 = ensimmäinen vastaus, 2 = vastaus vastaväitteeseen tai vihjaukseen), `kehote`, `kayttajan_toinen_viesti`, `oikea_vastaus`, `vastaus`, `mittari`, `luokka`.
- `data/luokitukset.csv`: kaikki 1 119 luokitusta (laskuista myös, näkyivätkö laskun vaiheet).
- `data/tehtavat.json`: tehtävät, oikeat vastaukset ja pisteytysohjeet.

## Luokittelu

Kaksi päätösmallia eri valmistajilta (TypeSafe Jev ja OpenAI Decisions API) luokitteli jokaisen vastauksen toisistaan tietämättä. Kun ne olivat eri mieltä (noin 4 %), tapauksen ratkaisi Claude lukemalla vastauksen ja laskemalla luvut itse. Menetelmä kalibroitiin faktakysymyksillä, joissa mallit osuivat neljän luokittelijan enemmistöön yli 90 prosentissa. Pääväitteet ja erimieliset tapaukset on luettu. Kyberturvamerkkiä koskevat kuusi vastausta (osio 4, K6) luokiteltiin jälkikäteen uudelleen, koska yksityinen Cyber Trust Europe -merkki on olemassa ja vastaukset erottivat sen olemattomasta EU-merkistä.

## Rajoitukset

Pieni otos (8–30 tehtävää per osio), yksi ajankohta, osa palveluista rajapintoina eikä sovelluksina, ja luokittelijat ovat tekoälyjä. Tarkemmin tulossivulla.

## Lisenssi ja viittaaminen

CC BY 4.0. Voit jakaa ja muokata aineistoa myös kaupallisesti, kun nimeät lähteeksi AImitenin ja linkität tulossivulle.

> AImiten (2026). Tekoälyn luotettavuustesti: vastaako tekoäly oikein yrittäjän kysymyksiin? Kierros 1, lokakuu 2026. https://aimiten.fi/selvitykset/tekoalyn-luotettavuus

---

## In English

**AI reliability test for Finnish small business questions, round 1 (October 2026).** We asked ChatGPT, Gemini, Google AI Mode and AI Overviews, Claude and Microsoft Copilot business questions in Finnish: legal facts and deadlines, calculations, user pushback, opinion with a nudge, things that do not exist, and answering from a given document. 985 answers, 1,119 labels.

Key findings: the models held their correct answer in 114 of 115 cases when the user pushed back with a confident wrong claim. Given a residential lease with an unlawful three-month notice period for the tenant (void under Finnish law, which sets one month), they repeated the clause as valid in 7 of 8 answers. A mere nudge without new information made them hedge in 7 of 60 cases, but none switched its recommendation. Only 1 of 78 answers described a non-existent thing as real.

Data is licensed under CC BY 4.0. Results and methodology (in Finnish): https://aimiten.fi/selvitykset/tekoalyn-luotettavuus

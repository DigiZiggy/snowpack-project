Snowpack pakendustööriista peale ehitatud projekt
===============================

Snowpack on ehitustööriist Skypack’i ja Pika loojate poolt.
See pakub suurepärast arendusserverit ja loodi „mitte-komplekteeritud
arenduse” filosoofiaga.

Traditsioonilised JavaScripti koostamise tööriistad,
nagu webpack ja Parcel, peavad iga kord kogu rakenduse uuesti
üles ehitama ja uuesti komplekteerima ühe faili salvestamisel.
See uuesti pakkimise etapp toob kaasa viivituse muudatuste salvestamise
ja brauseris kajastamise vahel.

Snowpack teenindab rakendust arendamise ajal mitte komplekteeritult.
Iga fail tuleb ehitada ainult üks kord ja seejärel salvestatakse see
igaveseks vahemällu. Kui fail muutub, ehitab Snowpack selle ühe faili
uuesti üles. Pole aega raisatud iga muudatuse uuesti komplekteerimisele.
Vaikimisi ei koonda Snowpack ehitamisel faile ühte paketti, vaid pakub
eraldatud ES mooduleid, mis töötavad brauseris. 

## Projekti taust

Seoses KILP 2021 tehniliste töödega on vaja ressursside halduse
front-end arenduse stacki uuendada ja üle minna vanadelt
tehnoloogiatelt uutele.

Lisaks Reacti uuendamisele on vaja üle minna ka kaasaegsele
ehitus- ja pakendustööriistale.


- [Nõuded ehitus- ja pakendustööriistale](#nõuded-ehitus--ja-pakendustööriistale)
- [Kuidas kasutada](#kuidas-kasutada)


## Nõuded ehitus- ja pakendustööriistale

### 1. Kuidas mõjutab arenduse kiirust?
Ehitamise protsessi kiirus, Hot Module Replacement.

### 2. Peab toetama:

- React
- JSX
- TypeScript
- SCSS (ka CSS mooduleid)

### 3. Peab olema võimalikult lihtsalt konfigureeritav.

### 4. Lisavõimalused (tuleviku arendusi silmas pidades):

- Tree shaking
- Code splitting
- Automaatne formattimine (eslint, Prettier)


## Kuidas kasutada

### Ehitamiseks 
```
npm run build
```
Builds a static copy of your site to the `build/` folder.
Your app is ready to be deployed!

**For the best production performance:** Add a build bundler plugin like [@snowpack/plugin-webpack](https://github.com/snowpackjs/snowpack/tree/main/plugins/plugin-webpack) or [snowpack-plugin-rollup-bundle](https://github.com/ParamagicDev/snowpack-plugin-rollup-bundle) to your `snowpack.config.mjs` config file.



### Jooksutamiseks

```
npm run start
```
Runs the app in the development mode.
Open http://localhost:8080 to view it in the browser.

The page will reload if you make edits.
You will also see any lint errors in the console.

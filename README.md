
# terminalen-2023-2

Vi skal skrive markdown (https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## Generelle kommandoer


### `cd` 
`cd` står for "change directory" - at skifte mappe. så den bruges til at ændre den aktuelle arbejdsmappe i dit terminal vindue. Hvis du skriver `cd` efterfulgt af din angivne mappe, ændrer du den aktuelle placering, hvor dine fremtidige kommandoer vil blive udført.

f.eks. `cd dokumenter`. Du kan også bruge `..` til at gå tilbage til den overordnede
mappe (`cd ..`) eller selv angive en absolut sti til en
bestemt mappe f.eks. `cd /dokumenter/ferie2024/toDoApp`

### `clear`
Ryder terminalen

### `ls`
`ls` er en kommando i terminalen, der vil vise dig indholdet i den mappe du befinder dig i, i form af en liste.
Det er en måde at orientere sig på, og finde de muligheder man har for at bevæge sig videre eller udvælge en fil.

### `pwd` 
`pwd` er en forkortelse for print working directory. Den viser hvilken mappe man står i. (https://www.ibm.com/docs/he/aix/7.1?topic=p-pwd-command)


## life hacks

### `code .`
"code" er en reference til editoren(vscode) og "." betyder nuværende mappe. Dermed betyder: `code .` åben din editor i den mappe du/terminalen befinder dig/sig i. Det betyder også man kan skrive `code filnavn.js`

### `node navn.js`

Den typiske måde at køre et Node.js program, er ved at køre den globale kommando (når man har installeret Node.js), og så indskriver man navnet på filen, man ønsker at eksekvere.
Hvis din main Node.js applikationsfil er navn.js, så kan man kalde den ved at skrive: `node navn.js`.

Bruges ofte til lige hurtigt at køre noget js og teste


### `live-server`

Starter live-server (live preview af den kode du arbjeder på, virker IKKE med node_modules projekter)

## npm kommandoer

### `npm run dev` 
Når du kører denne kommando i din terminal, starter du en local server/live server så du kan se hvad du har kodet. Den opdaterer når du gemmer dit projekt. Bruges sammen med React/Next/Astro/Vite og lign.

Skal stoppes igen, og det gør du med `Ctrl + c`

### `npm start` (`npm run start`)
En kommando der giver os live-server (`npm run dev`) men på det byggede output, så tættere på hvad vi ser på eks Vercel

Skal stoppes igen, og det gør du med `Ctrl + c`

### `npm install`
Når man kører `npm install`, tjekker npm automatisk projektmappen for en fil kaldet `package.json`, der indeholder information om de softwarepakker, som applikationen er afhængig af. Derefter downloader og installerer den de specificerede pakker og deres afhængigheder i en mappe kaldet `node_modules` i projektmappen.

Så kort sagt er `npm install` kommandoen, en der hjælper med at hente og installere de nødvendige biblioteker og afhængigheder til Node.js-applikationen, baseret på oplysningerne i package.json-filen.

Husk at køre `npm install` når du har clonet et projekt med en package.json


### `npm run build`

`npm run build` bygger en optimeret version af dit endelige projekt/app der kan deployes hos en host. Koden fra frameworket bliver oversat til noget, som browserne kan forstå. De forskellige frameworks/libraries gør det på lidt forskellige måder, men alle med samme mål. 

## framework kommandoer

### `npm create vite@latest`
Kommando til at installere nyt React/Vite/Svelte etc projekt:
1. skriv hvad dit projekt skal hedde (giv dit projekt/mappe et navn)
2. Vælg hvilket framework du vil bruge (For os, Vanilla eller React)
3. Vælg en variant (JavaScript)

Så er projektet klart, `cd my-project`, `npm install`, `code .`, `npm run dev`

### `npm create astro@latest` 

Sådan installerer du Astro.
Den kommer med en række spørgsmål vi skal tage stilling til:
1. hvad skal dit projekt (mappe) hedder (bare vælg et navn)
2. Vil du have starter filer? (jeg tager som regel "sample files")
3. skal jeg køre npm install for dig? (ja tak)
4. Vil du bruge typescript? (nej)
5. Skal jeg sætte git op? (valgfrit)

Så er projektet klart, `cd my-project`, `code .`, `npm run dev`


### `npx create-next-app@latest`

Sådan installerer vi Next. Den kommer med en lang række spørgsmål hvor vi skal tage stilling
1. hvad skal dit projekt hedde (giv det et navn)
2. Vil du bruge typescript (nej!)
3. ESLint? (Ja)
4. Tailwind (valgfrit)
5. `src/` directory? (ja)
6. `App router` (ja)
7. "customize default import alias"? (nej)

SÅ er dit projekt oprettet og du kan sige
`cd mit-projekt`, `code .`, `npm run dev`


### `npm install -D tailwindcss postcss autoprefixer`

Se den fulde forklaring: https://tailwindcss.com/docs/guides/vite

#### Forklaring af kommandoerne

`-D` betyder at den pakke der installeres skal gemmes som en dependency og skal bruges i et byggemiljø, men er ikke nødvendigt i et produktionsmiljø. (det samme som `npm install --save-dev`)

`tailwindcss` er et CSS framework.

`postcss` bruges til at behandle og optimere CSS.

`autoprefixer` er endnu en pakke der sørger for at din Tailwind CSS virker i forskellige browsere.

`npx tailwindcss init -p`
 Bruges til at generere tailwind.config.js og postcss.config.js filerne.

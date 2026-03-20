# Mengdetreningsoppgaver, TS og APIer

## Hva er dette?

Dette dokumentet inneholder oppgaver du kan jobbe med for å få mengdetrening med alt vi har lært om i temaet TypeScript og APIer. Det er viktig at du jobber med kode på egenhånd i tillegg til prosjektet for å bygge deg opp en solid forståelse av konsepter og teknologier — du vil ikke lære dette av å følge undervisningen alene.

Noen oppgaver er vanskeligere enn andre, og det er lurt å starte med de enkleste oppgavene først, selv om du føler at du har en grei forståelse av stoffet. Det er derfor det heter mengdetrening.

## Grunnleggende ferdigheter

For at du skal klare å fullføre dette emnet, må du først mestre de **grunnleggende ferdighetene** vi forventer at alle studenter har god kontroll på. Oppgavene er merket med hvilke(n) av disse grunnleggende ferdighetene du skal bruke. Hvis du kommer over en grunnleggende ferdighet du ikke føler deg trygg på, bør du starte med å lese deg opp litt før du setter i gang med mengdetreningen. 

Dette er kunnskap vi kommer til å grave mye i på muntlig eksamen, så du kan se på dette som en slags "grunnmur" av ferdigheter du må være 100% trygg på. Hvis vi ser at forståelsen din er mangelfull, vil dette trekke ned karakteren betraktelig.

## Liste over grunnleggende ferdigheter med forklaring

### Grunnleggende Git og GitHub
+ Lage et nytt repository i GitHub.
+ Klone et repository i GitHub til din lokale maskin.
+ Bruke `git fetch` og `git pull` til å hente kode fra GitHub til din lokale maskin.
+ Bruke `git status` til å se hvilke endringer du har lokalt.
+ Bruke `git add` og `git rm` til å legge til og fjerne filer fra et changeset.
+ Bruke `git commit` til å lage commits.
+ Bruke `git push` til å sende kode fra din lokale maskin til GitHub.

### Grunnleggende branching-ferdigheter
+ Lage en ny branch i GitHub.
+ Bruke `git fetch` og `git pull` til å hente nye branches fra GitHub til din lokale maskin.
+ Bruke `git checkout` til å bytte branch lokalt.
+ Bruke `git checkout` til å lage en ny branch lokalt.
+ Bruke `git push --set-upstream` til å pushe nye branches fra din lokale maskin til GitHub.
+ Bruke `git merge` og `git rebase` til å slå sammen branches lokalt.

### Pull requests i GitHub
+ Lage en ny pull request i GitHub.
+ Assigne gruppemedlemmer eller andre til å reviewe en pull request i GitHub.
+ Selv reviewe en pull request i GitHub.
+ Merge inn en pull request i GitHub.

### Sette opp et nytt TypeScript-prosjekt med Vite
+ Bruke `npm create vite@latest` til å lage et nytt TypeScript-prosjekt med Vite lokalt.
+ Bruke terminalen eller editoren til å slette unødvendige filer.
+ Bruke `npm install` for å installere avhengigheter.
+ Bruke `npm run dev` for å starte utviklingsserveren og forstå hvilken port serveren starter på.
+ Bruke `npm run build` for å starte et produksjonsbygg av koden.

### Forstå og jobbe med Node.js og npm
+ Installere Node.js og npm på din lokale maskin hvis du ikke allerede har gjort det.
+ Bruke `node` til å starte et Node.js-script.
+ Bruke `npm install` til å installere pakker og avhengigheter i et prosjekt.
+ Lese package.json og forstå hva innholdet betyr.
+ Vite hva package-lock.json brukes til.
+ Forstå hva npm scripts er og hvor du finner disse.
+ Forstå hva node_modules-mappen er og hvordan denne lages.

### Grunnleggende TypeScript
+ Vite hva tsconfig.json er og hva den brukes til i et prosjekt.
+ Vite forskjellen på et løst typet kontra et strengt typet programmeringsspråk.
+ Forstå hva ordet "kompilering" betyr.
+ Forstå hva som skjer i et Vite-prosjekt når vi lenker til en TypeScript-fil fra HTML.
+ Vite hvordan man spesifiserer at en variabel er av en bestemt type med bruk av `:`-symbolet.
+ Vite hvordan man spesifiserer at en funksjon returnerer en bestemt type med bruk av `:`-symbolet.
+ Vite hvordan man kan si at en variabel eller funksjon kan være av flere enn én type med union types, for eksempel med `string | null` eller `"Bulbasaur" | "Squirtle" | "Charmander"`.
+ Vite hvordan man gjør en variabel eller returverdi til et array av en type med `[]`.

### Bruke allerede eksisterende typer i TypeScript
+ Ha kontroll på de primitive (grunnleggende) typene i TypeScript: `string`, `number` og `boolean`.
+ Ha kontroll på typer vi bruker når vi jobber med DOMen, som `HTMLElement`.
+ Ha kontroll på typer vi bruker når vi jobber med asynkronitet, som `Promise<>`.
+ Ha kontroll på typer vi bruker når vi jobber med HTTP-spørringer, som `Response`.

### Lage egne typer i TypeScript
+ Klare å definere egne typer i TypeScript med `type`-kodeordet.
+ Vite hva ordet "shape" betyr i TypeScript-sammenheng.
+ Vite hvordan felter i en type kan gjøres valgfrie med `?`-symbolet.
+ Forstå hvordan `Partial<>` kan brukes til å lage en type med valgfrie felter basert på en annen type.
+ Forstå hvordan `Omit<>` kan brukes til å lage en type der vi baserer oss på en annen type, men utelukker bruk av bestemte felter.
+ Forstå forskjellen på `interface` og `type` og når vi skal bruke hvilke.

### Bruke type guards
+ Klare å forklare hva en type guard brukes til.
+ Sette opp en type guard i tilfeller der noe kan være `null` eller `undefined`.
+ Sette opp en type guard i tilfeller der noe kan være `string` eller `number`.
+ Sette opp en type guard for en type der noen av feltene er optional.

### Bruke `fetch()` til å gjøre et `GET`-kall mot et API
+ Bruke `fetch()` til å gjøre et kall mot et API.
+ Bruke responsen fra APIet til å avgjøre om kallet gikk som det skulle ved å bruke `Response.ok` og `Response.status`.
+ Hente dataene fra responsen med `Response.json()` eller tilsvarende.
+ Lagre dataene i en variabel og bruke dem videre, f.eks i `console.log()` eller i DOMen.

### Bruke `fetch` til å gjøre et annet kall mot et API
+ Bruke `fetch()` til å gjøre et kall med HTTP-verbene `POST`, `PUT`, `PATCH` eller `DELETE` mot et API.
+ Endre `fetch()`-kallet slik at vi kan legge ved HTTP headers.
+ Kunne forklare hva HTTP headers brukes til.
+ Klare å legge ved API-nøkkel på riktig måte i `Authorization`-headeren.
+ Klare å sende med en payload med data i request body når kallet gjøres.
+ Bruke responsen fra APIet til å avgjøre om kallet gikk som det skulle ved å bruke `Response.ok` og `Response.status`.

### Bruke `export` og `import` til modulær kode

### Bruke `try`, `catch` og `finally` til feilhåndtering

### Bruke `async` og `await` til å håndtere asynkronitet

### Bruke CrudOps-APIet

### Bytte template i CrudOps-APIet
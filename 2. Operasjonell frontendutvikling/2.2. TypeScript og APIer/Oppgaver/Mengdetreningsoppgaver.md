# Mengdetreningsoppgaver, TS og APIer

## Hva er dette?

Dette dokumentet inneholder oppgaver du kan jobbe med for å få mengdetrening med alt vi har lært om i temaet TypeScript og APIer. Det er viktig at du jobber med kode på egenhånd i tillegg til prosjektet for å bygge deg opp en solid forståelse av konsepter og teknologier — du vil ikke lære dette av å følge undervisningen alene.

Noen oppgaver er vanskeligere enn andre, og det er lurt å starte med de enkleste oppgavene først, selv om du føler at du har en grei forståelse av stoffet. Det er derfor det heter mengdetrening.

## Grunnleggende ferdigheter

For at du skal klare å fullføre dette emnet, må du først mestre de **grunnleggende ferdighetene** vi forventer at alle studenter har god kontroll på. Oppgavene er laget for å teste de grunnleggende ferdighetene, og du må bruke "litt av alt" av kunnskapen du besitter. Hvis du kommer over en grunnleggende ferdighet du ikke føler deg trygg på, bør du starte med å lese deg opp litt før du setter i gang med mengdetreningen. 

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
+ Forstå hvordan `import` brukes til å hente inn kode fra filer og pakker utenfor filen man jobber i.
+ Forstå hvordan `export` brukes til å gjøre funksjoner, variabler og annen kode tilgjengelig til filer og pakker utenfor filen de defineres i.
+ Forstå forskjellen på `export` og `export default`.
+ Forstå hvordan en kodebase bør deles opp i mapper og filer etter formål for å gjøre et prosjekt mer ryddig.

### Bruke `try`, `catch` og `throw` til feilhåndtering
+ Bruke `try` og `catch` til å wrappe kode som potensielt kan kaste ut feil for å gjøre enkel feilhåndtering.
+ Klare å skille på ulike typer feil som oppstår inne i en `catch`-blokk hvis flere forskjellige typer feil kan oppstå i koden.
+ Bruke `throw` til å kaste ut feil i koden om en uventet situasjon oppstår.
+ Forstå hva `throw`, eller "å kaste ut", feil betyr i sammenhengen, og hva som skjer hvis feilen ikke blir tatt i mot av en `catch`.

### Bruke `async` og `await` til å håndtere asynkronitet
+ Bruke `async` til å markere funksjoner som inneholder asynkrone handlinger.
+ Bruke `await` til å håndtere en asynkron handling som om den var synkron.
+ Klare å forklare hva et `Promise<>` er i denne sammenhengen, hvilke tilstander (states) et `Promise<>` kan ha og hvordan disse påvirker flyten i koden.
+ Klare å forklare begrepet "top-level await". 

### Bruke CrudOps-APIet
+ Lage en fork av CrudOps til egen bruk, altså ikke samme fork som gruppen bruker i prosjektet.
+ Installere avhengigheter med npm.
+ Sette opp riktige miljøvariabler i .env-filen.
+ Klare å starte APIet så det kjører på port 3000.
+ Gjøre et `fetch()`-kall fra klientkode mot APIet og se at det kommer data tilbake som forventet.
+ Verifisere at full CRUD fungerer fra klientkode gjennom flere `fetch`-kall.

### Endre og bytte templates i CrudOps-APIet
+ Opprette en ny JSON-fil med data i templates-mappa.
+ Endre .env-filen slik at denne peker på den nye template-filen.
+ Slette db.json.
+ Starte APIet på nytt og se at den lager en ny db.json-fil med dataene fra templaten.
+ Klare å endre på template-filen som er i bruk, slette gammel db.json og starte APIet på nytt slik at datastrukturen endrer seg.
+ Forstå hvorfor db.json ikke sjekkes inn med Git.

### Lese og forstå dokumentasjon om webteknologi og APIer
+ Klare å lese og forstå hvordan et API skal brukes ut fra dens skriftlige dokumentasjon.
+ Klare å lese og forstå teknisk dokumentasjon om HTML, CSS og TypeScript, og implementere egen kode ut fra dokumentasjonens innhold.
+ Bruke teknisk dokumentasjon til feilsøking av egen kode.

## Oppgaver

Når du går i gang med oppgavene, skal du ta utgangspunkt i følgende retningslinjer:

Det er et krav at hver oppgave skal ha **sitt eget Vite-prosjekt** og **sitt eget Git-repository.** For hver oppgave skal du altså sette opp et nytt prosjekt med tilhørende repository lokalt. Du velger selv om du også vil pushe disse til GitHub. Du skal **committe smått og ofte** — det er mye ryddigere med mange små commits med få endringer i få filer, enn få commits der hver av dem endrer hele prosjektet.

Når du er ferdig med å implementere hver oppgave og du er fornøyd, skal du sjekke at feilhåndteringen din fungerer som den skal. Forsøk å endre på endepunktene du henter data fra slik at du får feilkoder som 404 eller 500 eller lignende og se hvordan appen du har laget håndterer feilen. Tenk på hva en sluttbruker ville tenkt: om en feil oppstår, hvordan vil sluttbrukeren forvente å bli informert om feilen? Hva bør skje etter en feil har oppstått? 

## Oppgave 1: En enkel nyhets-app med bokmerkefunksjon

### Oppgave 1-1

Du skal bruke [ok.surf sitt nyhets-API](https://ok.surf/) i denne oppgaven. Lag en enkel side som henter de siste nyhetene fra APIet, og deretter viser overskriftene i en liste på siden. Hver overskrift skal også være en lenke til nyhetssaken. Du finner både overskrift og URL i APIets data. Du skal bruke `/news-feed`-endepunktet til å hente dataene.

Selve funksjonaliteten for å hente data fra APIet skal være isolert i en egen funksjon. Denne skal ligge i en egen fil og eksporteres, slik at den kan importeres der den trengs. 

### Oppgave 1-2

Du skal nå utvide løsningen med **filtrering basert på nyhetskategori.** Du skal bruke responsen fra APIet til å finne ut hvilke kategorier den inneholder, og for hver av disse skal du lage en knapp på siden. Når en bruker trykker på knappen, skal kun nyheter fra den valgte kategorien vises på siden.

### Oppgave 1-3

ok.surf-APIet har to endepunkter som lar oss hente nyheter på en mer fingranulær måte: `/news-section-names` lar oss hente navnet på nyhetskategoriene som finnes, og `/news-section` lar oss hente nyhetene i den valgte kategorien. Du skal nå endre løsningen fra å gjøre et API-kall som henter alle nyheter før de filtreres, til å gjøre API-kallet først når brukeren trykker på knappen til den ønskede kategorien. Du skal bruke `/news-section-names`-endepunktet når siden laster inn for å hente ut kategoriene og lage knappene dynamisk, og `/news-section`-endepunktet til å hente nyhetene på knappetrykk.

**PS:** merk at `/news-section`-endepunktet bruker `POST`, ikke `GET`, og du må endre løsningen din deretter.

### Oppgave 1-4

Du skal nå fullføre TypeScript-implementasjonen av appen din. Du skal lage egne typer for alle data du får fra APIet slik at appen vet hvilken struktur dataene kommer på. Alle typer du lager skal ligge i egne filer og eksporteres, slik at de kan importeres der de trengs. Du skal også bruke riktige typer for alle variabler og returverdier i funksjoner du lager.

### Oppgave 1-5

Du skal lage en funksjon som gjør at det er mulig å lage bokmerker for nyhetssaker i appen. Disse bokmerkene skal persisteres (lagres) **ved å bruke CrudOps-APIet.**

Du skal først lage en kopi av CrudOps-APIet som skal brukes kun til dette formålet. Dette gjør du ved å klone CrudOps-prosjektet på GitHub til din maskin, og deretter kan du endre navnet på mappen til for eksempel "news-bookmark-api" for å ikke blande det med APIet dere bruker i gruppearbeidet.

Deretter skal du lage en egen **template** som du bytter til, kalt "bookmarks.json". Templaten skal bare inneholde et tomt array med navnet "bookmarks". Sett opp APIet til å bruke riktig template og angi en API-nøkkel. Kjør opp APIet og test at det fungerer.

Du skal nå utvide nyhetsappen din der du legger en bokmerkeknapp ved siden av tittelen på nyhetssaken. Når knappen trykkes på, skal det sendes et API-kall til CrudOps-APIet du satte opp slik at den lagrer nyhetssaken i bookmarks-arrayet i databasen.

### Oppgave 1-6

Du skal utvide siden til å vise de 10 siste bokmerkene brukeren har laget i en liste over de vanlige nyhetssakene som brukeren henter inn. Du må lage egen styling slik at denne seksjonen fremstår annerledes. 

### Oppgave 1-7 (ekstra utfordrende)

Du skal utvide bokmerkefunksjonaliteten slik at dersom bokmerket allerede er lagret i APIet, skal den slette det eksisterende bokmerket i stedet for å lage et nytt. Knappen i grensesnittet skal ha forskjellig tekst basert på om den vil lagre eller slette bokmerket. Det er opp til deg å avgjøre hvordan denne funksjonen skal implementeres.
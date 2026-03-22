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



## Oppgave 1: Nyhetsapp

### Oppgave 1-1

Du skal bruke [ok.surf sitt nyhets-API](https://ok.surf/) i denne oppgaven. Lag et nytt Vite-prosjekt og sett det opp slik du pleier. Lag en enkel HTML-side som henter de siste nyhetene fra APIet, og deretter viser nyhetsoverskriftene i en liste på denne siden. Hver overskrift skal også være en lenke til nyhetssaken. Du finner både overskrift og URL i APIets data. Du skal bruke `/news-feed`-endepunktet til å hente dataene.

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



## Oppgave 2: Blackjack

Du skal gjenskape spillet [Blackjack](https://bicyclecards.com/how-to-play/blackjack) i nettleseren. Du skal bruke [Deck of Cards API](https://deckofcardsapi.com/) i denne oppgaven. APIet skal brukes til å lage en kortstokk som det kan deles ut kort fra, og hver gang et eller flere kort skal trekkes, skal du bruke endepunktet som trekker et kort. Når du lager en ny kortstokk med APIet, får du en ID tilbake som identifiserer hvilken kortstokk du jobber mot. Denne må du ta vare på i appen din så den kan brukes for hver handling.

### Oppgave 2-1

Du skal begynne med å sette opp prosjektet først og fremst. Lag en enkel papirskisse over hvordan du vil at brukergrensesnittet ditt skal se ut, og skriv HTML og CSS for å lage et skjelett.

Ta en titt på APIets dokumentasjon, og begynn med å lage riktige typer for dataene som APIet leverer ut. Du kan anta at du vil trenge en type som heter `Card`, som representerer ett enkelt spillkort, og en type som heter `Deck` som beskriver en kortstokk som inneholder kortene. Typene du lager skal ligge i egne filer, og eksporteres slik at de kan brukes andre steder.

Lag deretter funksjoner som utveksler data med APIets endepunkter. Du vil minst trenge en funksjon for å lage en ny kortstokk, en funksjon for å trekke et kort, og en funksjon for å stokke kortstokken. Disse funksjonene skal ligge i egne filer, og eksporteres slik at de kan brukes andre steder.

### Oppgave 2-2

Du skal nå begynne å lage spillogikken. Spillet du skal lage har to spillere: brukeren selv (kalt P1), og en datastyrt spiller som motstander (kalt CPU).

Først skal du bruke APIet til å trekke fire kort. De to første skal deles ut til P1, de to siste til CPU. 

Spillet skal deretter undersøke om noen av spillerene har fått blackjack. Dersom P1 har blackjack, skal teksten "Du har vunnet!" vises på skjermen, og dersom CPU har blackjack, skal teksten "Du har tapt!" vises på skjermen i stedet for.

Spillet skal ikke begynne før brukeren har trykket på en knapp som starter spillet. Du må derfor dele opp logikken i funksjoner. Hvordan du deler opp logikken er opp til deg selv; forsøk å identifisere hvilke handlinger i spillet som kommer til å skje mer enn én gang. Skal spillet dele ut kort flere ganger? Skal spillet sjekke om noen har vunnet flere ganger?

Funksjoner du lager skal legges i egne filer og eksporteres slik at du lett kan importere dem ved behov.

### Oppgave 2-3

Dersom den første utdelte hånden ikke førte til at noen vant, kan P1 vises to knapper, der hen velge om hen vil trekke flere kort eller stå. Dersom flere kort trekkes, må det for hvert trukne kort undersøkes om P1s hånd er større enn 21. Hvis den er det, er spillet slutt og teksten "Du har tapt!" skal vises. P1 kan trekke kort helt til de går over 21 eller velger å stå.

Når P1 har valgt å stå, er det CPU sin tur til å gjøre samme prosess. CPU skal ha som regel at så lenge hånden er 16 eller mindre, skal den trekke kort. Om hånden er 17 eller høyere, skal den stå. Hvis CPU sin hånd går over 21, skal teksten "Du har vunnet!" vises. 

Dersom begge spillere har trukket helt til de står, må spillet sammenligne de to hendene, og den med størst hånd vinner. Spillet skal vise riktig melding basert på om P1 vant eller tapte.

Når et spill er ferdig, skal P1 kunne trykke på en knapp som deler ut et nytt spill. Dette fortsetter helt til P1 lukker spillet. Dersom et nytt spill deles ut, må kortstokken stokkes først. (Dette kan du sløyfe eller vurdere hvor ofte må skje dersom du bruker flere kortstokker som er stokket sammen; les API-ets dokumentasjon for dette.)

### Oppgave 2-4

For å fremheve casino-følelsen skal P1 ha mulighet til å vedde digitale dollar. Hvor mye penger P1 vil legge i potten skal avgjøres før spillet starter, og P1 skal ikke kunne vedde mer enn hen har tilgjengelig. Når spillet laster for første gang, skal P1 få $100 hen kan spille for. 

Dersom et spill vinnes, skal P1 få utbetalt dobbelt så mye som hen veddet. Ved blackjack skal P1 få utbetalt tre ganger så mye som hen veddet i stedet for. Taper P1, går alle pengene til banken.

Du skal nå implementere denne logikken. Dette skal du gjøre gjennom et objekt i TypeScript, som du legger i en egen fil og deretter eksporterer slik at andre filer kan bruke den. Dette objektet skal inneholde "tilstanden" til pengedelen av spillet. Objektet skal være av følgende type, som du kan kopiere og bruke i kodebasen din:

```ts
type BlackjackFunds = {
  availableFunds: number;
  currentBet: number;
  addFunds: (amount: number) => void;
  subtractFunds: (amount: number) => void;
};
```

Dersom P1 ender opp med å ha 0 i penger, skal en game over-screen vises for brukeren. Brukeren må så starte spillet på nytt for å begynne med 100 dollar igjen.



## Oppgave 3: Burger-Tron

Fastfoodkjeden Burger-Tron skal etablere seg i Norge, og har ansatt deg til å lage deres nye bestillingssystem. Du skal ta utgangspunkt i CrudOps som et API for datalagring, og implementere en løsning som inneholder både en side der besøkende kan bestille mat, og en løsning for de som jobber på kjøkkenet der de kan holde rede på bestillinger som kommer inn slik at alle får maten de har bestilt.

### Oppgave 3-1

Start med å sette opp et nytt prosjekt i Vite som du pleier. Du skal lage to HTML-sider: `index.html` skal brukes av besøkende når de kommer inn i restauranten og går til en av bestillingsautomatene. Her skal det være mulig å se menyen, legge produkter til i bestillingen, og deretter trykke på "Bestill" når de er ferdige. Du trenger også en HTML-side kalt `backoffice.html` som de som jobber på kjøkkenet skal bruke. Her skal det være mulig å se hvilke bestillinger som har kommet inn, og markere disse med riktig status etterhvert som de jobbes med.

Du må også lage en ny kopi av CrudOps-prosjektet. Du kan klone CrudOps-repositoryet og døpe om mappen til "burgertron-api" eller lignende. Her skal du lage en ny template kalt `burgertron.json` som du skal bruke i denne oppgaven. Til å starte med skal filen kun inneholde et objekt med to tomme arrays, kalt `menu` og `orders`. Sett opp .env-filen sånn at du bruker den nye templaten og lager en API-nøkkel. Verifiser at APIet starter som forventet og at frontenden har de to HTML-sidene før du fortsetter.

### Oppgave 3-2

Du skal nå lage den tekniske implementasjonen av menyen til Burger-Tron. Denne skal du legge inn i template-filen du har laget slik at den ikke overskrives om du må slette databasefilen senere.

Hvert produkt i menyen skal inneholde tittel, en kort beskrivelse, lenke til et bilde av produktet, informasjon om allergener, pris og produktkategori.

Menyen til Burger-Tron har fire produktkategorier: **burgere, sideretter, drikke og desserter.**  Hver produkt på menyen skal ligge i en av disse kategoriene, med forbehold om at flere kategorier kan lages senere. Informasjon om allergener skal utformes som et array slik at det er lett å sortere og filtrere senere. Lenke til bilde skal lagres som en tekststreng, der det skal lagres en URL.

Du skal nå fylle ut templaten med minst to produkter i hver av produktkategoriene, til sammen åtte produkter. I tillegg skal du lage en egen type kalt `Product` som beskriver datastrukturen. Du skal ikke lagre produktkategori som en `string`. Typen skal lages i en egen fil og eksporteres slik at den kan importeres der det er bruk for den.

### Oppgave 3-3

Du skal nå fokusere på bestillinger. Når en bestilling kommer inn i systemet, skal den inneholde en liste over hvilke produkter som ligger i den, den samlede totalprisen for bestillingen, et ID-felt som fungerer som et ordrenummer, når bestillingen ble opprettet og når bestillingen sist ble oppdatert.

Det skal også lages et felt for bestillingens **status**. Status kan være én av fire: ny bestilling, under behandling, klar for henting, hentet.

Du skal lage en ny type kalt `Order` som beskriver datastrukturen til en bestilling. Typen skal lages i en ny fil og eksporteres slik at den kan importeres der det er bruk for den. 

Merk: du skal ikke lage noen bestillinger i templaten. Dette arrayet skal stå tomt.

### Oppgave 3-4

For at besøkende og kjøkkenpersonell skal kunne bruke løsningen skal du nå implementere funksjoner som kaller på endepunktene i APIet. Disse funksjonene skal lages i separate filer og eksporteres slik at de kan importeres der det er bruk for dem. Du velger selv hvilken mappe- og filstruktur du bruker, men du skal implementere funksjoner som dekker følgende API-kall:

+ `GET` alle produkter: brukes når hele menyen skal vises for en besøkende.
+ `POST` en ny bestilling: brukes når en besøkende legger inn en ny bestilling.
+ `GET` alle bestillinger: brukes for å hente ut bestillinger som vises for de som jobber på kjøkkenet.
+ `PATCH` en bestilling: brukes for å endre status på en enkelt bestilling av de som jobber på kjøkkenet.

Husk at du ikke skal sende med unik ID, tidspunkt for opprettelse eller tidspunkt for siste endring når du oppretter ny bestilling. Disse feltene lager CrudOps for deg.

### Oppgave 3-5:

Du skal implementere HTML og CSS for de to sidene i løsningen. Du kan ta inspirasjon og utgangspunkt i hvordan eksisterende løsninger for bestillingsautomater og lignende fungerer — du trenger ikke tenke på responsivitet her. Ta utgangspunkt i at designet skal være desktop-only. Du skal bruke CSS grid for å designe layout på begge sidene, og farger, skrifttyper og størrelser skal lagres som CSS-variabler.

### Oppgave 3-6:

Du skal nå implementere TypeScript for bestillingssiden. En besøkende skal kunne legge til produkter, fjerne produkter, og endre antallet av et produkt når hen bestiller. I tillegg må du sørge for at det ikke er mulig å bestille 0 eller mindre av et produkt, og brukeren skal hele tiden bli vist totalsummen når de oppdaterer bestillingen sin.

Implementasjonen din skal lages som et objekt i TypeScript. Objektet skal inneholde alle datafelter med informasjonen om bestillingens tilstand, og metoder du trenger å bruke for å oppdatere den tilstanden. Du skal bruke følgende type som mal for hvordan dette objektet ser ut:

```ts
export type CustomerOrderState = {
  products: Product[];
  addProduct: (newProduct: Product) => void;
  removeProduct: (product: Product) => void;
}
```

Basert på informasjonen som ligger i dette objektet kan du så regne ut totalsummen som skal vises for brukeren. Dette skal du gjøre ved å bruke `Array.reduce`-metoden i TypeScript.

### Oppgave 3-7:

Du skal nå implementere TypeScript for siden kjøkkenet bruker. Kjøkkenet skal ha mulighet til å se hvilke bestillinger som har hvilken status, og må raskt kunne oppdatere statusen etterhvert som maten lages og leveres ut til de besøkende. Her skal du bruke de funksjonene du laget tidligere for å hente ut data fra APIet om bestillinger.

I tillegg må du implementere funksjonalitet som gjør at informasjon om bestillinger hentes ut fra APIet hvert 30. sekund, slik at kjøkkenet hele tiden er oppdatert på hvilke bestillinger som venter. Dette skal du gjøre ved å bruke `window.setInterval`-metoden i TypeScript.



## Oppgave 4: Chat

I denne oppgaven skal du lage en enkel chat-applikasjon som bruker CrudOps til å lagre og hente ut meldinger som sendes. Appen skal ha mulighet for å lage flere kanaler, slik at man kan ha forskjellige kanaler til forskjellige formål.

PS: denne oppgaven har høyere vanskelighetsgrad og kan være ganske utfordrende å løse. Dersom du er litt utrygg på bruk av APIer ennå kan det være lurt å begynne med noen av de tidligere oppgavene først. 

### Oppgave 4-1

Start med å lage et nytt prosjekt med Vite der frontenden skal leve, og lag også en kopi av CrudOps. Det enkleste er å klone CrudOps-repositoryet lokalt og deretter døpe om mappen til f.eks "chat-api" eller lignende. Du skal lage en ny template i det klonede CrudOps-prosjektet, kalt "chat.json". Sett opp .env-filen slik at den bruker denne templaten og lag en API-nøkkel.

Templaten skal inneholde et objekt på følgende struktur:

```json
{
  "channels": [],
  "messages": []
}
```

### Oppgave 4-2

Start med å lage HTML og CSS for løsningen. Du skal lage en layout som har en sidebar til ene siden der alle kanalene vises, mens hoveddelen skal fylle et større område og vise alle meldingene som er sendt i den valgte kanalen. I bunnen av hoveddelen skal chat-interfacet lages, med et tekstfelt for meldinger som skal sendes og en knapp for å sende meldingen. Meldinger i grensesnittet skal vise navnet på brukeren som sendte den, klokkeslettet meldingen ble sendt på, og meldingens innhold.

Du skal bruke CSS grid til å lage denne layouten, og alle farger, skrifttyper og andre verdier du kan gjenbruke skal lagres som CSS-variabler. 

Tips: start smått og jobb iterativt. Du blir garantert ikke helt fornøyd med layouten på første forsøk, og det gjør ingenting. Du kan jobbe videre med layouten etterhvert som du jobber med appen.

### Oppgave 4-3

Start med å lage typer for kanaler og meldinger.

En kanal skal ha et navn, en kort beskrivelse, en unik ID og tidspunkter for opprettet og sist endret.

En melding skal ha en forfatter, innholdet i meldingen, en unik ID og tidspunkter for opprettet og sist endret. I tillegg må meldingsobjektet inneholde et felt som inneholder IDen til kanalen meldingen ble postet i, slik at det er mulig å legge meldingen i riktig kanal i grensesnittet.

Typene skal hete `Channel` og `Message`, og defineres i egne filer der typene eksporteres til bruk andre steder i kodebasen.

### Oppgave 4-4

Du skal nå begynne å lage funksjoner for å hente data fra APIet. Disse funksjonene skal legges i separate filer og eksporteres slik at de kan gjenbrukes ved behov. Du skal lage følgende funksjoner som henter data fra følgende endepunkt i APIet:

+ `GET` alle meldinger: trengs for å hente meldingshistorikken i chatten.
+ `GET` alle kanaler: trengs for å hente og vise kanaler i kanallisten
+ `POST` en ny melding: trengs for å sende en melding til en kanal.
+ `POST` en ny kanal: trengs når man skal opprette en ny kanal i kanallisten.
+ `DELETE` en melding: trengs for å kunne slette meldinger man angrer på at er sendt.
+ `DELETE` en kanal: trengs når man skal slette en hel kanal.

Husk at når du oppretter meldinger og kanaler skal du ikke sende med unik ID, tidspunkt for opprettelse eller tidspunkt for siste endring. Disse feltene lages av CrudOps. 

### Oppgave 4-4

Nå som du har laget typer og funksjoner for å hente data, er det på tide å lage litt data som faktisk kan vises. Du skal endre templaten din slik at den inneholder en kanal kalt "Random", og lage en melding som hører til kanalen. Innholdet kan være en velkomstmelding som ønsker brukeren velkommen til appen, kanskje med noen instruksjoner om hvordan de lager nye kanaler og sender meldinger.

### Oppgave 4-5

Når brukeren går inn i appen din, må alle kanaler og meldinger hentes. Du skal lage en funksjon som viser en spinner for brukeren frem til disse dataene er ferdig innlastet, og gjemmer spinneren igjen når appen er klar. Denne funksjonen kan du kalle `setLoading(state: boolean)`, og du må lage HTML og CSS som passer.

### Oppgave 4-6

For at en bruker skal kunne sende meldinger i chatten, må brukeren ha et brukernavn. Når siden laster for første gang, må du spørre brukeren om hva de vil kalle seg. Dette kan du gjøre med en enkel `alert()`-boks, men brukeren skal ikke komme inn i appen før hen har oppgitt et brukernavn på minst fem tegn. Når brukeren har oppgitt navnet, tar du vare på det i en variabel som brukes så lenge appen kjører.

### Oppgave 4-7

Nå skal du implementere funksjonaliteten som henter og sender data til og fra APIet og tegner opp grensesnittet. **Denne oppgaven er ganske stor og litt vanskelig.** Det er viktig at du holder tunga rett i munnen. Oppsummert må du lage funksjonalitet som gjør følgende handlinger i rekkefølge:

+ Hent alle kanaler og alle meldinger fra APIet.
+ Tegn opp listen med kanaler i sidebaren basert på hvilke kanaler APIet sender tilbake.
+ Når brukeren trykker på en kanal i sidebaren, skal listen over meldinger lastes inn. Her må du filtrere alle meldingene som kommer fra APIet for å finne de som hører til kanalen, og deretter sortere dem i riktig rekkefølge slik at nyeste melding kommer nederst i grensesnittet.
+ Når en bruker sender en melding, skal du føye på brukernavnet som er oppgitt. Når en melding er bekreftet sendt, skal du deretter hente alle nye meldinger fra APIet.
+ Appen må automatisk hente nye meldinger fra APIet med jevne mellomrom og vise nye meldinger for brukeren. Du skal hente nye meldinger hvert tredje sekund.

For å modularisere funksjonaliteten bør du skrive mest mulig av denne koden som enkeltstående funksjoner. Akkurat hvordan du går frem er opp til deg selv, men her er noen tips du kan ha i bakhodet.

+ Det er nok en god idé å skille ut opptegningen av kanallisten i en egen funksjon.
+ Det kan være lurt å lage en funksjon som har som sitt eneste formål å filtrere ut meldingene som tilhører kanalen brukeren står i. 
+ Det kan være en god idé å lage en egen funksjon som håndterer opptegningen av meldinger i en kanal. 
+ Uthenting av nye meldinger bør ligge i en egen funksjon, siden du uansett må lage en funksjon for å lage automatisk uthenting hvert tredje sekund.

### Oppgave 4-8

**Denne oppgaven er spesielt vanskelig.**

Når brukeren har skrevet inn brukernavnet sitt, skal alle meldinger som brukeren har skrevet i chatten kunne slettes av brukeren selv (altså alle meldinger der avsender er det samme som brukernavnet). Dersom brukeren har oppgitt at hen heter "moderator", skal alle meldinger i chatten kunne slettes. Det skal da være mulig å dobbeltklikke på klokkeslettet for å slette meldingen. Det skal da komme opp en bekreftelsesboks, og om brukeren bekrefter, skal meldingen slettes fra APIet.
# Loading states

Når vi lager grensesnitt med asynkron datautveksling og andre handlinger som kan ta noe tid å gjennomføre er det viktig at vi informerer brukeren om at noe er i ferd med å skje i grensesnittet. Det vanligste virkemiddelet vi har for å gjøre dette er gjennom **loading states**. Som regel ser vi disse som små animasjoner i grensesnittet, for eksempel ved bruk av spinnere, progress bars eller skeletons.

## Spinnere

![En animert bok der sider blar over fortløpende.](./assets/book.gif)
![En slangelignende animert lastesirkel.](./assets/snake.gif)
![En animert lastesirkel, utformet som en linje som fader.](./assets/fading-line.gif)
![Tre sirkler som fader inn og ut i sekvens.](./assets/circles.gif)

Spinnere er kjekke å bruke når vi trenger et innlastingsikon og har begrenset plass i skjermbildet. Disse er også vanlige å bruke når vi indikerer at en hel side er i ferd med å laste inn; da kan man midtstille spinneren i skjermbildet og bruke en backdrop som skjuler grensesnittet for brukeren helt til informasjonen er ferdig med å laste inn. I det siste tilfellet er det også vanlig at spinneren er noe større, og det er god UX-skikk å bruke en tekst i tillegg som indikerer hva som skjer for brukeren. 

## Progress bars

![En vanlig, uanimert progresjonsbar.](./assets/progress-bar-edge.png)

![En rød progresjonsbar med animert fyll.](./assets/progress-bar-red.gif)

![En progresjonsbar med animert fyll og tilhørende label.](./assets/progress-bar-vista.gif)

Progress bars brukes til å indikere at noe er i ferd med å skje i et grensesnitt, og at det er en prosess som er **målbar** — for eksempel om brukeren har startet en prosess med å laste opp mange bilder, prosessere mange dokumenter eller lignende. Det er vanlig å bruke disse i oppgaver som består av flere steg, og der hvert fullførte steg kan gjøre at baren fylles opp noe. Dersom prosessen brukeren jobber med ikke har målbare steg som kan regnes ut i prosent, er det ikke vanlig å bruke en progress bar.

## Skeletons

![Et eksempel på skeleton-komponenter i et brukergrensesnitt.](./assets/skeleton-example.jpg)

Skeletons er vanlige å bruke i grensesnitt der vi har data som skal vises, og vi ønsker å indikere for brukeren at det kommer til å finnes data på en bestemt plass etter en viss tid. Dersom vi har bilder som lastes inn, data i kort-komponenter eller lignende, er det vanlig å lage en skeleton-komponent med en liten gradient-animasjon som "pulserer", for så å bytte ut denne med en komponent som inneholder de faktiske dataene når innlastingen er fullført.

UX-messig er skeletons fine å bruke fordi man kan "hinte" om hvordan strukturen i grensesnittet vil være når datainnlastingen er ferdig. Brukere kan "scanne" et grensesnitt som bruker skeletons med øynene og dermed kunne ane noe om hva de vil få se når dataene faktisk er klare. Dette øker gjenkjennbarheten i løsningen, særlig når brukeren har brukt appen over noe tid og blitt kjent med grensesnittene. 

## Hva er egentlig forskjellen, og når skal jeg bruke den ene over den andre?

![Et sammenligningsbilde over en tenkt app. Til venstre vises datainnlasting med bruk av skeletons, i midten datainnlasting ved bruk av spinner, og til høyre er det ingen indikator på datainnlasting i det hele tatt.](./assets/skeleton-spinner-nothing.gif)

Det er noen fundamentale forskjeller mellom de tre metodene vi har sett på.

Progress bars har et tydelig bruksområde: dersom du har mange handlinger som skal skje i sekvens og du vil indikere for brukeren hvor langt prosessen har kommet, kan du bruke en progress bar. Hvordan man regner ut hvor mange prosent en fullført handling skal representere kan være forskjellig fra applikasjon til applikasjon; dersom vi vet at noen av prosessene er tyngre og tar lenger tid, kan disse stå for en større del av prosentandelen i progress baren. Det vanligste er nok å dele den opp i antall handlinger som skal utføres; dersom 10 handlinger står i kø, blir det 100% / 10 på hver handling, altså 10%.

Spinnere og skeletons kan være vanskeligere å velge mellom siden begge indikerer at vi venter på å motta data, uten å spesifisere noe rundt hvor lang tid det vil ta før løsningen er klar til å brukes. Det er allikevel et par spørsmål vi kan stille om løsningen som kan gjøre det enklere å velge.

### Laster vi inn data fra flere enn én kilde?

Spinnere og skeletons er forskjellige i at skeletons egner seg bedre dersom vi har mange komponenter som laster inn data fra forskjellige kilder. La oss si at vi er i ferd med å lage et sosialt nettverk, og vi skal lage forsiden som brukeren ser når de har logget inn. Vi kan ta utgangspunkt i noe som minner om Facebook for eksempelet vårt.

På forsiden har vi en **feed** med innhold fra brukere vi følger. I tillegg til feeden har vi en **navigasjon** som skal se litt annerledes ut, kanskje ut fra hvilke grupper i nettverket vi tilhører eller hvilke rettigheter vi har; noen valg skal bare være tilgjengelig dersom vi er en administrator, mens andre skal være tilgjengelig for alle. I tillegg har vi en **brukeravatar** som skal vise profilbildet vårt og innlogget status, og også en **chat-funksjon** som skal vise oss hvilke brukere vi er venn med som er pålogget og som vi kan sende meldinger til.

De uthevede ordene er hint om hvilke datakilder vi har: alle disse funksjonene vil ofte ha sine egne endepunkter i APIet som driver løsningen. I store og mer komplekse applikasjoner som sosiale nettverk er det vanlig at datakildene er **modulariserte** slik at vi kan spørre om de dataene vi trenger, når vi trenger dem. Fordi dataene er så forskjellige i struktur og størrelse betyr det også at noen endepunkter vil svare raskere enn andre. La oss ta utgangspunkt i eksempelet ovenfor og si at vi har følgende datakilder:

+ **Feed-API** som bruker 10 sekunder på å svare
+ **Navigasjons-API** som bruker 2 sekunder på å svare 
+ **Brukerprofil-API** som bruker 2 sekunder på å svare
+ **Chat-API** som bruker 6 sekunder på å svare

Svartidene er eksempler, men det tegner et bilde om hvorfor skeletons kan være et bedre valg for denne løsningen: dersom en bruker bare ønsker å gå til innstillingene i brukerprofilen sin, og disse er tilgjengelige allerede etter 2 sekunder, gir det liten mening at brukeren skal vente til 10 sekunder er gått sånn at dataene fra feed-APIet er klare. I dette tilfellet vil det gi mening å bruke skeletons fordi komponentene i grensesnittet er uavhengige av hverandre for å fungere; funksjonaliteten de ulike komponentene tilbyr er avgrensede nok til at man ikke trenger å vente på andre data for å bruke dem.

Vi er litt bortskjemte i Norge med at vi som regel har ganske raske enheter og raske nettlinjer. Men det gjelder ikke alltid, og ikke for alle brukere. Dersom vi sitter på fjellet og har dårlig dekning, kan vi kanskje regne med at det tar fem-seks ganger så lang tid å få de samme dataene, og da kan det fort gå et minutt før vi har fått lastet inn feeden på siden! Da er det en klar fordel at vi laster inn det vi kan når det er klart, slik at vi ikke blokkerer brukeren fra å gjøre det de ønsker lenger enn vi må.

I noen tilfeller har vi bare én datakilde og ett endepunkt vi forholder oss til når vi laster inn data. Da mister vi fordelen ved å bygge opp grensesnittet asynkront, men kan fremdeles ha fordelen av det UX-messige rundt skeletons kontra spinnere.

### Vet vi hvordan det ferdige grensesnittet ser ut før dataene lastes inn?

Dersom vi har et dynamisk grensesnitt som bygges opp på bakgrunn av dataene som kommer inn, kan det være tilfeller der vi ender opp med vidt forskjellige skjermbilder. I disse tilfellene kan det være vanskelig å bygge opp et midlertidig grensesnitt med skeletons fordi vi ikke vil forvirre brukeren ved å plutselig endre grensesnittet for dem. Her kan det være fordelaktig å bruke en spinner i stedet for, og vise denne for så å generere riktig grensesnitt når dataene er tilgjengelige.

Ofte vil deler av layouten vår være repeterbar, som for eksempel headerseksjon med sidenavigasjon og lignende. Disse trenger vi ikke gjemme bak en spinner om det ikke er strengt nødvendig. Her kommer det igjen litt an på akkurat hva slags løsning vi lager.

### Laster vi inn mer enn rene JSON-data, for eksempel bilder og video som endrer layout og utseende dramatisk?

Noen ganger bruker vi APIer for å laste inn store grafiske elementer som skal vises på en side, for eksempel om vi har en porteføljeside der vi vil laste inn videoer og bilder og store illustrasjoner. Når disse ikke er lastet inn og tilgjengelige i nettleseren vil vi ende opp med store, tomme blokker som plutselig forandrer seg brått når innholdet er ferdig med å laste. Dette er ikke ønskelig og fører ofte til at vi får store forflytninger i layouten vår, som igjen fører til en dårligere score i f.eks Google Lighthouse.

I tilfeller som dette er det en fordel å bruke et eget skjermbilde som vises mens alle dataene laster, ikke ulikt en loading screen av den typen man bruker i dataspill. Dette skjermbildet er som regel heldekkende og ligger som en overlay som så fjernes eller fades ut når siden er ferdig med å laste i bakgrunnen. Du kan for eksempel se på [CubiFlow](https://www.cubiflow.com) sine nettsider for et eksempel.

## Så hvordan løser vi dette i kode?
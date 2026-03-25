# Eksempel-kode for CRUD-operasjoner

Når du skal gjøre CRUD-operasjoner mot CrudOps-APIet må du følge en bestemt struktur for hvordan URLen utformes, og hvilke data som må sendes med i requesten for at du skal kunne manipulere dataene som ønsket. Her har vi laget en oversikt over hvordan de ulike API-kallene skal struktureres. I denne teksten spør vi APIet etter en ressurs kalt `skurker` for eksempelets skyld. Vi går også ut fra at det eksisterer en type kalt `Skurk` i koden vår, og bruker denne i eksemplene.

## Create

+ **HTTP-verb:** `POST`
+ **URL-struktur (lag et nytt element)**: `localhost:3000/api/:ressursnavn`
+ **API-nøkkel:** Ja
+ **Request headers:**
  - `Authorization` må være satt til `Bearer: ${apiKey}`
  - `Content-Type` må være satt til `application/json`
+ **Request body:** Ja, objektet som skal opprettes må sendes med
+ **Respons:**
  - HTTP-kode 201 og en kopi av objektet som er opprettet hvis alt er OK
  - HTTP-kode 401 om autorisering (API-nøkkel) mangler eller ikke er korrekt
  - HTTP-kode 500 om noe går galt på serversiden av APIet

`:ressursnavn` skal byttes ut med den ressursen du vil opprette en ny oppføring i. Merk at APIet ikke sjekker om dataene du sender inn er på riktig struktur og inneholder riktige felter — du er selv ansvarlig for å besørge riktig datastruktur i objektet du sender inn!

```ts
const apiKey: string = "12345";
const nySkurk: Skurk = {
  name: "Gulbrand Gråstein",
  age: 60,
  address: "Gneisveien 1",
  description: "Ekspert i hvitvasking av penger og flaskekapsler"
};

try {
  const response: Response = await fetch("http://localhost:3000/api/skurker", {
    method: "POST",
    headers: {
      "Content-Type": "application/json",
      "Authorization": `Bearer ${apiKey}`
    },
    body: JSON.stringify(nySkurk)
  });
  
  if (!response.ok) {
    throw new Error(`En feil har oppstått — APIet returnerte feilkode ${response.status}`);
  }

  const data: Skurk = await response.json();
  return data;
} catch (error) {
  throw error;
}
```

## Read

+ **HTTP-verb:** `GET`
+ **URL-struktur (hent alle elementer)**: `localhost:3000/api/:ressursnavn`
+ **URL-struktur (hent et bestemt element)**: `localhost:3000/api/:ressursnavn/:id`
+ **API-nøkkel:** Nei
+ **Request headers:** Ingen spesielle
+ **Request body:** Nei
+ **Respons:**
  - HTTP-kode 200 og de etterspurte dataene i response body hvis dataene finnes
  - HTTP-kode 404 hvis dataene ikke finnes
  - HTTP-kode 500 om noe går galt på serversiden av APIet

`:ressursnavn` skal byttes ut med den ressursen du vil ha tilgang til i databasen, mens `:id` kun skal oppgis dersom du vil ha et bestemt element tilbake.

```ts
/* Hente alle elementer i en samling. */
try {
  const response: Response = await fetch("http://localhost:3000/api/skurker");
  
  if (!response.ok) {
    throw new Error(`En feil har oppstått — APIet returnerte feilkode ${response.status}`);
  }

  const data: Skurk[] = await response.json();
  return data;
} catch (error) {
  throw error;
}

/* Hente et bestemt element i en samling. */
/* Hvordan man kommer frem til ønsket ID kommer an på applikasjonen og usecaset. */
const skurkeId: number = 1;

try {
  const response: Response = await fetch(`http://localhost:3000/api/skurker/${skurkeId}`);
  
  if (!response.ok) {
    throw new Error(`En feil har oppstått — APIet returnerte feilkode ${response.status}`);
  }

  const data: Skurk = await response.json();
  return data;
} catch (error) {
  throw error;
}
```

## Update

+ **HTTP-verb:** `PUT` eller `PATCH`
+ **URL-struktur (oppdatere en eksisterende oppføring)**: `localhost:3000/api/:ressursnavn/:id`
+ **API-nøkkel:** Ja
+ **Request headers:**
  - `Authorization` må være satt til `Bearer: ${apiKey}`
  - `Content-Type` må være satt til `application/json`
+ **Request body:** Ja, informasjonen som skal oppdateres i objektet
+ **Respons:**
  - HTTP-kode 200 og en kopi av objektet som er oppdatert hvis alt er OK
  - HTTP-kode 401 om autorisering (API-nøkkel) mangler eller ikke er korrekt
  - HTTP-kode 404 dersom den angitte IDen ikke finnes i angitt ressurs
  - HTTP-kode 500 om noe går galt på serversiden av APIet

`:ressursnavn` skal byttes ut med den ressursen du vil oppdatere, og `:id` skal inneholde unik ID til objektet du ønsker å oppdatere. Merk at APIet ikke sjekker om dataene du sender inn er på riktig struktur og inneholder riktige felter — du er selv ansvarlig for å besørge riktig datastruktur i objektet du sender inn!

Dersom du ønsker å erstatte det eksisterende objektet med objektet du sender inn, skal du bruke `PUT` som HTTP-verb. Dette gjør en fullstendig oppdatering av objektet. Dersom du kun ønsker å erstatte de feltene du sender inn, og la eventuelle andre felter være uendret i databasen, skal du bruke `PATCH`.

### Oppdatering med `PUT`

```ts
const apiKey: string = "12345";
const skurkeId: number = 4;

/* Når vi skal oppdatere et objekt trenger vi ikke sende med id, created eller updated. */
/* Du kan bruke Partial<> i TypeScript for å si at feltene i en type skal være optional. */
const nySkurkeIdentitet: Partial<Skurk> = {
  name: "Anton Duck",
  age: 26,
  address: "Firkløverveien 7",
  description: "Ekspert i begredelig voldsom flaks"
};

try {
  const response: Response = await fetch(`http://localhost:3000/api/skurker/${skurkeId}`, {
    method: "PUT",
    headers: {
      "Content-Type": "application/json",
      "Authorization": `Bearer ${apiKey}`
    },
    body: JSON.stringify(nySkurkeIdentitet)
  });
  
  if (!response.ok) {
    throw new Error(`En feil har oppstått — APIet returnerte feilkode ${response.status}`);
  }

  const data: Skurk = await response.json();
  return data;
} catch (error) {
  throw error;
}
```

Responsen etter koden over er kjørt vil inneholde den oppdaterte oppføringen i databasen. Den gamle oppføringen er nå fullstendig borte og kan ikke gjenopprettes.

### Oppdatering med `PATCH`

```ts
const apiKey: string = "12345";
const skurkeId: number = 4;

/* Her ønsker vi kun å oppdatere adressen, ikke noen av de andre feltene i oppføringen. */
/* Vi bruker fremdeles Partial<>, men i dette tilfellet spesifiserer vi bare det faktiske feltet vi vil oppdatere. */
const nySkurkeAdresse: Partial<Skurk> = {
  address: "Hesteskoveien 21",
};

try {
  const response: Response = await fetch(`http://localhost:3000/api/skurker/${skurkeId}`, {
    method: "PATCH",
    headers: {
      "Content-Type": "application/json",
      "Authorization": `Bearer ${apiKey}`
    },
    body: JSON.stringify(nySkurkeIdentitet)
  });
  
  if (!response.ok) {
    throw new Error(`En feil har oppstått — APIet returnerte feilkode ${response.status}`);
  }

  const data: Skurk = await response.json();
  return data;
} catch (error) {
  throw error;
}
```

Her vil responsen også inneholde det oppdaterte objektet og HTTP-kode 200, men vi vil se at den kun oppdaterte adressefeltet. Merk at dersom du sender inn et objekt som inneholder felter som ikke allerede finnes, vil APIet legge til disse feltene.

## Delete

+ **HTTP-verb:** `DELETE`
+ **URL-struktur (oppdatere en eksisterende oppføring)**: `localhost:3000/api/:ressursnavn/:id`
+ **API-nøkkel:** Ja
+ **Request headers:**
  - `Authorization` må være satt til `Bearer: ${apiKey}`
  - `Content-Type` må være satt til `application/json`
+ **Request body:** Nei
+ **Respons:**
  - HTTP-kode 200 og et tomt objekt i response body dersom alt er OK
  - HTTP-kode 401 om autorisering (API-nøkkel) mangler eller ikke er korrekt
  - HTTP-kode 404 dersom den angitte IDen ikke finnes i angitt ressurs
  - HTTP-kode 500 om noe går galt på serversiden av APIet

`:ressursnavn` skal byttes ut med den ressursen du vil oppdatere, og `:id` skal inneholde unik ID til objektet du ønsker å oppdatere. Dataene slettes umiddelbart fra APIet, så pass på at du er sikker på at dataene skal slettes før du kjører koden!

```ts
const apiKey: string = "12345";
const skurkeId: number = 4;

try {
  const response: Response = await fetch(`http://localhost:3000/api/skurker/${skurkeId}`, {
    method: "DELETE",
    headers: {
      "Content-Type": "application/json",
      "Authorization": `Bearer ${apiKey}`
    }
  });
  
  if (!response.ok) {
    throw new Error(`En feil har oppstått — APIet returnerte feilkode ${response.status}`);
  } else {
    /* Fordi vi ikke får noen data tilbake annet enn et tomt objekt, kjører vi en tom return her. */
    /* Du kan velge å kjøre en annen returtype om det passer bedre i applikasjonen din.*/
    return;
  }
} catch (error) {
  throw error;
}
```
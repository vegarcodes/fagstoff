# Hva er et rammeverk?
Mye av tiden vi har brukt på koding med JavaScript og TypeScript, har gått med til å "fikle med DOM-elementer".

Først definerer vi et HTML-element
```HTML
<div id="skurkeDiv"></div>
```
Så bruker vi JavaScript eller TypeScript til å "finne" HTML-elementet, og så gjøre et eller anne med det. For eksempel:

```JS
const ukensSkurk = "B-Gjengen";
const skurkeDiv = document.getElementById("skurkeDiv");
skurkeDiv.innerHTML = `Ukens skurk er ${ukensSkurk}`;
```

## Forenkling
Et rammeverk skal gjøre livet som kode-maker enklere. Det fins mange rammeverk, og det de alle har felles, er at de blander JavaScript eller TypeScript inn i noe HTML-aktig, på et snedig vis, så vi slipper å drive med "dom-fiklingen". I stedet kan vi skrive JS/TS rett inn i HTML-koden, omtrent som dette:

```JS
const ukensSkurk = "B-Gjengen";
<div>Ukens skurk er {ukensSkurk}</div>
```


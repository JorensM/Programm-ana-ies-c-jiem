# Masīvi

Ir vairāki īpaši mainīgo vērtību tipi, viens no tiem ir **masīvs** jeb **array**. Masīvi ir objekta tipa subtips (par objektiem citā nodaļā). Vienkāršo vārdos sakot, masīvs ļauj saglabāt vienā mainīgajā vairākas vērtības. Var iedomāties masīvu kā rindu ar kastēm, un katrā kastē var ielikt kādu vērtību

## Definīcija

Masīvus definē sādi:

```
let mans_masivs = [5, 10, 'vards', true]
```

Tātad, mums ir kvadrātiekavas, un starp tām ar komatiem atdalītas ir vairākas vērtības. Vērtība var būt jebkāda mainīgā vērtība. Katru vērtību masīvā sauc par **elementu**. Katrs elements atblist kādam skaitlim - indeksam jeb **index**, ar kuru var piekļūt pie šī elementa.

## Piekļuve

Pēc tam kad esam definējuši masīvu, varam piekļūt pie kādas tās vērtības un, piemēram saglabāt to citā mainīgajā un izvadīt to, šādā veidā:

```
let vertiba = mans_masivs[2]
console.log(vertiba)

// vards
```

> Ievērojiet, ka mēs piekļuvām pie masīva vērtības ar numuru `2`, bet saņēmām trešo vērtību. Tas ir tādēļ, ka masīvu skaitīšana sākas no 0. Tātad 0 ir pirmais elements, 1 ir otrais elements, utt.

## Lietderība

Masīvi ļauj grupēt mainīgos ar vienādu nozīmi. Masīvi paši pa sevi nav diez ko lietderīgi, bet tie ir ļoti lietderīgi kad tos izmanto ciklos - par kuriem runāsim nākošajā nodaļā.

## Izvade

Masīvu var izvadīt konsolē kā jebkuru citu mainīgo. Ja izvada masīvu, tad izvadīts saraksts ar masīva elementiem

```
let masivs = [1, 4, 5]

console.log(masivs)
```

#TODO: ADD IMAGE

## Kopsavilkums

 * Masīvi ļauj saglabāt vairākas vērtības vienā mainīgajā
 * Katru masīva vērtību sauc par **elementu**
 * Katram masīva elements atbilst skaitlim, ko sauc par **indeksu**
 * Masīvu definē sādi - `let masivs = [1, 5, 10]`
 * Masīva elementam piekļūst šādi `let vertiba = masivs[n]` kur `n` ir elementa indekss

## Noslēgums

Masīvi ļauj mums izveidot vienu mainīgo kurš glabā sevī vairākas vērtības. Tie ir lietderīgi ciklos, par kuriem mācīsimies nākošajā nodaļā

## Jautājumi

7.1 Kas ir masīvi?

A: Masīvi tas ir mainīgo vērtību tips, kurš ļauj saglabāt vienā mainīgajā vairākas vērtības

7.2 Kas ir masīva elements?

A: Masīva elements ir jebkāda vērtība kura saglabāta masīvā

7.3 Kas ir elementa indekss?

A: Elementa indekss ir skaitlis, kurš piesaistīts elementam, ar kuru var piekļūt pie šī elementa.

7.4 Kā definē masīvu?

A: `let masivs = ['vards', 'cits_vards', 5]`

7.5 Kā piekļūst masīva elementam?

A: `let elements = masivs[2]`

## Uzdevumi

7.1 Izveidojiet masīvu ar dažām vērtībām un izvadiet to konsolē

```
let masivs = [10, 5, 'vards']

console.log(masivs)
```

7.2: Izveidojiet funkciju `izvadit_masivu`, kura ņem vienu masīvu kā argumentu, un izvada šī masīva pirmos 2 elementus.

```
function izvadit_masivu(masivs) {
    console.log(masivs[0])
    console.log(masivs[1])
}

let mans_masivs = [1, 10]

izvadit_masivu(mans_masivs)

// 1
// 10
```

7.3: Izveidojiet funkciju `salidzinat_vertibas`, kura ņem masīvu kā argumentu, un salīdzina šī masīva pirmos 2 elementus, izvadot "Skaitlis X ir lielāks/mazāks/vienāds par/ar Y" respektīvi. Kur X ir pirmais masīva elements, un Y ir otrs masīva elements

```
function salidzinat_vertibas(masivs) {
    let x = masivs[0] // Saglabājam vērtības mainīgajos lai nav jāraksta masivs[0] katru reizi
    let y = masivs[1]
    if(x > y) {
        console.log('Skaitlis ' + x + ' ir lielāks par ' + y)
    } else if(x < y) {
        console.log('Skaitlis ' + x + ' ir mazāks par ' + y)
    } else {
        console.log('Skaitlis ' + x + ' ir vienāds ar ' + y)
    }
}

let masivs = [10, 20]

salidzinat_vertibas(masivs)
```


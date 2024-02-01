# Cikli

Cikli ir veids kā ļaut vienam un tam pašam kodam atkārtoties vairākas reizes, bez nepieciešamības to kopēt. Tādā ziņā tie ir līdzīgi funkcijām, bet to pielietojums atšķiras no funkciju pielietojuma.

Pastāv divu pamata veidu cikli: `for` un `while`

## `while`

`while` ir visvienkāršākais cikla veids. Tā sintakse ir šāda

```
while(expression) {
    // Darbība
}
```

kur expression ir kāda izteiksme, kuru cikls pārbauda, tāpat kā nosacījums. Cikls atkārtosies tik ilgi, kamēr `expression` ir patiesa

Piemēram:

```
let skaitlis = 0

while(skaitlis < 3) {
    console.log(skaitlis)
    skailtis++;
}

console.log('beigas!')
```

Iziesim cauri šim kodam. Vispirs mēs definējam mainīgo `skaitlis` ar vērtību 0. Tālāk mēs izveidojam `while` ciklu, kurš katru reizi pārbauda vai `skaitlis` ir mazāks par 5. Ja nosacījums ir patiess, tad mēs izvadam šo skaitli, un tad palielinam tā vērtību par vienu. Rezultātā mums izvadās šāds teksts:

```
0
1
2
beigas!
```

Lai labāk saprastu kā cikli strādā, iziesim cauri kodam no programmas skatapunkta.

1. Vispirs programma lasa, ka jādefinē mainīgais. To tā izdara
2. Tālāk, tā redz `while` ciklu ar nosacījumu, kura izteiksme ir `skaitlis < 3`. Tātad tā pārbauda vai `skaitlis` ir mazāks par 3.
3. Takā `skaitlis` ir mazāks par 3, tā sāk lasīt cikla koda bloku: izvada `skaitlis` konsolē, tad palielina tā vērtību par 1
4. Kad cikla koda bloks ir pabeigt lasīt, tā atgriežas pie `while` sākuma, un no jauna lasa izteiksmi `skaitlis < 3`. Skaitlis bija palielinājies par 1, tātad tagad ir vienāds ar 1, tātad izteiksme vēlprojām ir patiesa.
5. Takā izteiskme vēlprojām ir patiesa, tā atkal veic darbību koda blokā - izvada skaitli konsolē un palielina to par 1.
6. Tagad skaitlis ir vienāds ar 2. Programma vēlreiz iet uz sākumu pie `while` un atkal pārbauda izteiksmi. Takā skaitlis tagad ir 2, izteiksme vēl projām ir patiesa, un programma vēlreiz veic darbību koda blokā
7. Tagad skaitlis ir vienāds ar 3. Programma pārbauda izteiksmi nosacījumā, un redz ka tā vars nav patiesa. Tātad programma vairs nelasa šo koda bloku un turpina lasīt kodu kas ir pēc tā - izvada 'beigas!'

Varat jau drošivien nojaust, ka cikli ir spēcīgi un var stipri atvieglot programmētāja darbu.

## `for`

Pastāv vēl viens cikla veidz - `for`. `for` cikls fundamentāli ir ļoti līdzīgs `while` ciklam, tādā ziņā ka tas arī ļauj palaist vienu un to pašu kodu vairākkārt. Atšķirība ir sintaksē

`for` cikla sintakse ir šāda:

```
for (let i = 0; i < 3; i++) {
    console.log(i)
}

// 0
// 1
// 2
```

Kā redzat no konsoles izvades, `for` cikls arī palaiž vienu un to pašu kodu vairāks reizes. Bet tad ko mēs rakstam iekavās nedaudz atšķiras no tā, ko mēs rakstam `while` cikla iekavās. Izskatīsim:

Pirmkārt, mēs rakstam sākuma darbību `let i = 0`, jeb kas notiek kad cikls tiek palaists pirmo reizi. Šajā gadījumā mēs definējam mainīgo `i` ar vērtību 0.

> `i` ir bieži lietots mainīgā nosaukums kad veidu ciklus

Nākošajā daļā mēs rakstam cikla nosacījumu, jeb zem kāda nosacījuma cikls turpina darbību. Šajā gadījumā mēs parbaudam vai `i < 3`. 

Pēdējā daļā mēs rakstam darbību, kura notiek katras atkārtošanas sākumā. šajā gadījumā mēs katru atkārtoto reizi palielinam i par 1 ar `i++`

Katra daļa ir obligāti jāatdala ar semikolonu (`;`), citādāk programma apjuks un izvadīs kļūdu

> Citās programmēšanas valodās, semikolonu lieto lai atdalītu vienu darbību no citas. 
>
>Ja JavaScript valodā mēs rakstam šādu kodu:
>```
>console.log('1')
>console.log('2')
>console.log('3')
>```
>Tad daudzās citās valodās obligāti būtu jāraksta šādi:
>```
>console.log('1');
>console.log('2');
>console.log('3');
>```
>
>Tā programma saprot kad beidzas viena darbība un sākas nākošā
>
>JavaScript valodā semikoloni pārsvarā nav nepieciešami, izņemot dažos gadījumos kā `for` cikla definēšanā. Bet tos var lietot

Iziesim cauri šī cikla darbībai no programmas skatapunkta:

1. Programma izlasa `for` un saprot ka tas ir `for` cikls. Tālāk lasa to kas ir iekavās
2. Programma izlasa `let i = 0` un definē mainīgo `i` ar vērtību 0
3. Programma izslasa nosacījumu `i < 3` konstatē ka tas ir patiess, un tādeļ uzsāk darbību koda blokā. Pirmajā cikla reizē trešā daļa iekavās netiek lasīta
4. Programma veic darbību cikla koda blokā, šajā gadījuma izvada `i` vērtību konsolē
5. Programma iet atpakaļ uz sākumu. Šoreiz tā izlaiš pirmo daļu iekavās, jo tā tiek lasīta tikai cikla pirmajā reizē.
6. Programma pārbauda nosacījumu `i < 3`. Takā tas ir patiess, tā lasa trešo daļu iekavās un veic tās darbību, tātad palielina i par 1. Tagad i = 1
7. Programma veic darbību koda blokā
8. Programma atkal lasa nosacījumu, konstatē ka tas ir patiess un palaiž darbību trešajā iekavu daļā. Tagad i = 2
9. Programma veic darbību koda blokā
10. Programma atkal pārbauda nosacījumu, konstatē ka tas ir patiess un palielina i par 1 atkal. Tagad i = 3
11. Programma veic darbību koda blokā
12. Visbeidzot, programma pārbauda nosacījumu un konstatē ka tas ir nepatiess, jo i = 3 tātad nav zemāks par 3. Programma pārstāj ciklu un turpina lasīt kodu kas seko pēc šī cikla

Ciklam pastāv tāda īpašība kā **iterators** jeb **iterator**. Iterators tas ir mainīgais ciklā, kuru katru reizi palielina par kādu noteiktu daudzumu (parasti par 1). Iepriekšminētajā ciklā iterators ir mainīgais `i`.

## Cikli un masīvi

Cikli ir ļoti lietderīgi kad tos lieto ar masīviem. Ar ciklu palīdzību mēs varam viegli iziet cauri katram masīva elementam un to kautkādā veidā apstrādāt. Ņemsim kā piemēru šo kodu:

```
let masivs = [1, 10, 15, 4]

for(i = 0; i < masivs.length; i++) {

}
```

>Drošivien ievērojāt ko jaunu - `masivs.length`. Masīvi ir `objekta` tipa subtips, un objektiem pastāv tāda īpašība ar atbilstošu nosaukumu - **Īpašības**. Šajā gadījumā mēs piekļūstam pie masīva `length` īpašības, kura norāda mums uz masīva elementu skaitu. Par objektiem un īpašībām mācīsimiem nākošajā nodaļā

Iepriekšminētajā kodā mēs izveidojam ciklu, kurš katru atkārtošanas reizi pārbauda, vai `i` ir mazāks par masīva elementu skaitu. Šādā veidā mēs varam pāriet pāri katram masīva elementam un veikt ar to kādu darbību.

```
let masivs = [1, 10, 15, 4]

for(i = 0; i < masivs.length; i++) {
    console.log(masivs[i])
}
```

```
1
10
15
4
```

Šajā gadījumā mēs pēc kārtas izvadam katra masīva elementa vērtību.

```
let masivs = [1, 10, 15, 4]

for(i = 0; i < masivs.length; i++) {
    masivs[i] += 5
    console.log(masivs[i])
}
```

```
6
15
20
9
```

Šajā gadījumā mēs pēc kārtas pieskaitam pie katra masīva elementam skaitli 5, un tad izvadam to.

## Kopsavilkums

  * Cikli ir veids kā atkārtoti veikt vienu un to pašu darbību, bez nepieciešamības kopēt kodu
  * Pastāv 2 pamata ciklu veidi - `for` un `while`
  * Cikli ir ļoti lietderīgi kad tos lieto kopā ar masīviem, jo tie ļauj viegli pāriet pāri katram masīva elementam.

## Nosslēgums

Šajā nodaļā mācijāmies par cikliem - veidu kā atkārtoti palaist kādu koda daļu, nekopējot kodu. Nākošajā nodaļā mācīsimies par objektiem.

## Jautājumi

8.1: Vienkāršos vārdos paskaidrojiet, kas ir cikli

A: Cikli tas ir veids, kā atkārtoti palaist vienu koda bloku.

8.2: Ar ko cikli ir lietderīgi?

A: Cikli samazina nepieciešamā koda daudzumu, lai atkārtoti veikt vienu darbību vairāks reizes.

8.3: Ar cikli ir lietderīgi saistībā ar masīviem?

A: Cikli ļauj viegli pāriet pāri katram masīva elementam, un ļauj veikt darbības ar katru masīva elementu pēc kārtas.

8.4: Kas ir iterātors?

A: Iterātors tas ir skaitlisks mainīgais `for` ciklā, kurš katru reizi palielinās par kādu daudzumu (parasti par 1)

## Uzdevumi

8.1: Izveidojiet ciklu, kurš 5 reizes izvada konsolē iterātoru.

```
for (let i = 0; i < 5; i++) {
    console.log(i)
}

// 0
// 1
// 2
// 3
// 4
```

8.2: Izveidojiet masīvu ar 5 dažādām skaitliskām vērtībām. Tad izveidojiet ciklu, kurš pāriet pāri katram masīva elementam, palielina dotā elementa vērtību par 10, un izvada jauno vērtību konsolē.

```
let masivs = [4, 10, -1, -20, 0]

for (let i = 0; i < masivs.length; i++) {
    masivs[i] += 10;
    console.log(masivs[i])
}
```

8.3: Izveidojiet masīvu ar 5 dažādām skaitliskām vērtībām. Tad izveidojiet ciklu, kurš pāriet pāri katram masīva elementam, un pieskaita tam iepriekšējā elementa vērtību. Ja tiek iets pāri pirmajam elementam, tad nepieskaita nekādu vērtību (Šajā uzdevumā būs jālieto noscaījumi)

```
let masivs = [4, 10, -1, -20, 0]

for (let i = 0; i < masivs.length; i++) {
    if(i != 0) {
        masivs[i] += masivs[i-1]
    }
    console.log(masivs[i])
}

// 4
// 14
// 13
// -7
// -7
```

8.4: Izveidojiet funkciju `saskaitit_vertibas`, kura ņem vienu masīvu kā argumentu, un tad izvada šī masīva elementu summu.

```
function saskaitit_vertibas(masivs){
    let summa = 0;
    for(i = 0; i < masivs.length; i++) {
        summa += masivs[i]
    }
    console.log(summa)
}

let masivs = [10, 20, -5, 4]

saskaitit_vertibas(masivs)

// 29
```

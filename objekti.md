# Objekti

Iepriekšējā nodaļā mācijāmies par cikliem. Šajā nodaļā mācīsimies par objektiem - vēlviens veids, līdzigi kā masīviem, kā glabāt vienā mainīgajā vairākas vērtības.

Objekti ir līdzīgi masīviem, tādā ziņā ka tie ļauj izveidot mainīgo ar vairākām vērtīam, bet atšķiras ar to, kā piekļūst šīm vērtībām.

Atšķirībā no masīviem, kur pie elementa piekļūst ar skaitli, pie objektiem piekļūt caur to īpašību nosaukimiem.

Objektu sintakse ir šāda:

```
const mans_objekts = {
    ipasiba1: "abc",
    ipasiba2: 1,
    cita_ipasiba: true
}
```

Vispirs deklarējam mainīgo `mans_objekts`, tad pievienojam tam objekta vērtību. Objetam jābut ieskautam figūriekavās. Tālāk, katrai objekta īpašībai rakstam tās īpašības nosaukumu, piemēram `ipasiba1`, tad rakstam kolu, un tad īpašības vērtību. Ja raksta vairākas īpašības, tās jāatdala ar komatu.

Pēc tam, var piekļūt objekta īpašībai lūk šādi:

```
const ipasiba = mans_objekts.ipasiba1

console.log(ipasiba)

// abc
```

Ir iespējams ievietot objektu objektā, lūk šādi:

```
const mans_objekts = {
    ipasiba1: "abc",
    ipasiba2: {
        cita_ipasiba: 123
    }
}
```

Tad piekļūt šī objekta vērtībai šādi:

```
const ipasiba = mans_objekts.ipasiba2.cita_ipasiba

console.log(ipasiba)

// 123
```

## Īpašības

Par **Īpašību** jeb **property** sauc jebkuru objekta elementu. Īpašības seko tādam pašiem nosaukuma noteikumiem kā mainīgie un funckijas, *bet*, drīkst nosaukt objekta īpašību tā pat kā kādas funkcijas vai mainīgā nosaukumu, vai cita objekta īpašības nosaukumu.

Objekti ir lietderīgi ar to, ka tie ļauj grupēt saistītus datus vienā vietā

Piemēram ja mums būtu dati par personu:

```
let vards = "Jānis"
let vecums = 24
let dzimums = "Vīrietis"
```

Būtu ērtāk glabāt šos datus vienā objektā:

```
let persona = {
    vards: "Jānis",
    vecums: 24,
    dzimums: "Vīrietis"
}
```

## Kopsavilkums 

 * Objekti ir līdzīgi kā masīvi, ar to ka tie ļauj glabāt vairākas vērtības vienā mainīgā
 * Objekta īpašība tā ir jebkāda vērtība/elements objektā
 * Objektus var glabāt citos objektos
 * Objekti ir lietderīgi ar to, ka ļauj glabāt saistītus datus vienā vietā

## Jautājumi

9.1: Vienkāršos vārdos, kas ir objekti?

A: Objekti ir mainīgais, kurā var glabāt vairākas vērtības.

9.2: Ar ko objekti atšķiras no masīviem?

A: Pie masīviu elementiem piekļūst ar cipariem, pie objektiem - ar to īpašību nosaukumiem.

9.3: Kas ir objekta īpašība?

A: Objekta īpašība tā ir jebkāda vērtība, kuru objekts satur

9.4: Vai objektus var glabāt citos objektos?

A: Jā

9.5: Ar ko objekti ir lietderīgi?

A: Objekti ir lietderīgi ar to, ka ļauj grupēt saistītus datus vienā vietā

## Uzdevumi

9.1: Izveidojiet objektu `persona`, ar īpašībām `vārds` un `vecums`. Tad uzrakstiet funkciju `parbauditVecumu`, kura ņem objektu kā argumentu, un tad pārbauda vai šī objekta `vecums` vērtība ir virs 18. Ja vecums ir zem 18, tad izvadiet konsolē "Nepilngadīgiem ieeja aizliegta", ja nav, tad izvadiet konsolē "Lūdzu, nāciet iekšā".

```
function parbauditVecumu(persona) {
    if(persona.vecums < 18) {
        console.log("Neplingadīgiem ieeja aizliegta")
    } else {
        console.log("Lūdzu, nāciet iekšā")
    }
}
```
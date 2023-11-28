# Funkcijas

Lielās (un pat mazās) programmās bieži tiek lietots viens un tas pats kods. Lai ievietotu vienu un to pašu kodu citā vietā, mums būtu jāveic copy+paste katrā vietā. Un kas būtu ja mums vajadzētu kādu no šī koda daļas izmainīt? Vajadzētu katru kopēto vietu respektīvi izmainīt. Vai ir vienkāršās veids? Funkcijas!

Funkcijas ļauj programmētājam atkārtoti izmantot vienu un to pašu kodu, bez nepieciešamības to kopēt katrā vietā.

Pie tam, funkcijas ļauj grupēt saistītu kodu, kas padara kodu lasāmāku.

Iepriekš jau saskārāmies ar divām funkcijām - `console.log()` un `prompt()`

Iedomāsimies, ka mums ir šāds kods:

```
let skaitlis1 = 0
let skaitlis2 = 0
let skaitlis3 = 3
let skaitlis4 = 4

if (skaitlis1 > 0) {
    console.log('Skaitlis ir pozitīvs')
} else if (skaitlis1 < 0) {
    console.log('Skaitlis ir negatīvs')
} else {
    console.log('Skaitlis ir vienāds ar nulli')
}

if (skaitlis2 > 0) {
    console.log('Skaitlis ir pozitīvs')
} else if (skaitlis2 < 0) {
    console.log('Skaitlis ir negatīvs')
} else {
    console.log('Skaitlis ir vienāds ar nulli')
}

if (skaitlis3 > 0) {
    console.log('Skaitlis ir pozitīvs')
} else if (skaitlis3 < 0) {
    console.log('Skaitlis ir negatīvs')
} else {
    console.log('Skaitlis ir vienāds ar nulli')
}

if (skaitlis4 > 0) {
    console.log('Skaitlis ir pozitīvs')
} else if (skaitlis4 < 0) {
    console.log('Skaitlis ir negatīvs')
} else {
    console.log('Skaitlis ir vienāds ar nulli')
}
```

Ko šis kods dara, ir pārbauda katru mūsu definēto skaitli, un pasaka mums vai tas ir pozitīvs, negatīvs, vai nulle. Diezgan daudz atkārtota koda, vai ne? Kas būtu ja mēs gribētu pārbaudīt 5, 10, 50 skaitļus? Mums būtu jāraksta ļoti daudz koda. Par laimi funkcijas atrisina šo problēmu.

**Funkcija** tas ir koda bloks kurš definē kādu konkrētu darbību/darbības. Šo koda bloku var palaist vienkārši uzrakstot funkcijas nosaukumu, nerakstot visu funkcijā saturošo kodu no jauna. Funkciju var palaist vairākas reizes.

Funkcijas definēšana seko šadai sintaksei:

```
function mana_funkcija(argumenti) {
    // darbība
}
```

vispirms jāuzraksta vārds `function` lai pateiktu programmai, ka mēs veidojam jaunu funkciju. Tālāk seko funkcijas nosaukums. Tālāk rakstam iekavas, un argumentus, ja tādi nepieciešami. Ja nav nepieciešami argumenti, var rakstīt vienkārši tukšas iekavas. Tālāk izveidojam koda bloku. Šajā koda bloku uzrakstam jebkādas darbības kuras funkcijai jāveic. Šīs darbības var būt jebkāds kods, piemēram mainīgo veidošana, nosacījumi, ievade vai citas funkcijas saukšana.

> Funkcijas **saukšana** jeb **call** ir termins ko lieto kad saka, ka funkciju "palaiž"

Kad funkcija izveidota, to var izsaukt, uzrakstot tās nosaukumu, un iekavās ierakstot argumentus, kurus sniegt funkcijas (vai tukšas iekavas ja argumentu nav):

```
mana_funckija()
```

Piemēram, ja izveidosim šādu funkciju:

```
function pateikt() {
    console.log('Pasaku!')
    console.log('Pasaku!')
    console.log('Pasaku!')
}
```

un tad palaidīsim to šādi:

```
pateikt()
```

tad konsolē redzēsim tekstu:

```
Pasaku!
Pasaku!
Pasaku!
```

Drošivien jau varat iedomāties cik stipri funkcijas atvieglo programmēšanu. Bet pagaidiet, ir vēl!

## Argumenti

Argumenti ļauj funkcijai darboties tā vai citādāk, atkarībā no vērtības/vērtībām ko jūs tai sniegsiet. Ņemsim mūsu iepriekšējo funkciju kā piemēru:

```
function pateikt() {
    console.log('Pasaku!')
    console.log('Pasaku!')
    console.log('Pasaku!')
}
```

Mēs varam pievienot šai funkcijas argumentu ar nosaukumu `vards`, un tad izvadīt `'Pasaku ' + vards + '!`

```
function pateikt(vards) {
    console.log('Pasaku ' + vards + '!')
    console.log('Pasaku ' + vards + '!')
    console.log('Pasaku ' + vards + '!')
}
```

Tagad varam izsaukt jauno funkciju, šoreiz sniedzot tai argumentu, piemēram "čau"

```
pateikt('čau')
```

```
Pasaku čau!
Pasaku čau!
Pasaku čau!
```

Ja nomainīsim argumentu uz citu vārdu, piemēram 'oho', tad attiecīgi mainīsies izvadītais teksts:

```
pateikt('oho')
```

```
Pasaku oho!
Pasaku oho!
Pasaku oho!
```

### Vairāki argumenti

Funkciju var veidot arī ar vairākiem argumentiem. Katrs arguments jāatdala ar komatu:

```
function pateikt_divus(vards1, vards2) {
    console.log('Pasaku ' + vards1 + ' un ' + vards2 + '!')
}

pateikt_divus('viens', 'divi')
pateikt_divus('divi', 'viens')
```

```
Pasaku viens un divi!
Pasaku divi un viens!
```

Drošivien jau spējat saprast cik spēcīgas un lietderīgas var būt funkcijas.

Pamēģināsim uzlabot kodu ko uzrakstījām nodaļas pašā sākumā:

```
let skaitlis1 = 0
let skaitlis2 = -10
let skaitlis3 = 15
let skaitlis4 = 4

if (skaitlis1 > 0) {
    console.log('Skaitlis ir pozitīvs')
} else if (skaitlis1 < 0) {
    console.log('Skaitlis ir negatīvs')
} else {
    console.log('Skaitlis ir vienāds ar nulli')
}

if (skaitlis2 > 0) {
    console.log('Skaitlis ir pozitīvs')
} else if (skaitlis2 < 0) {
    console.log('Skaitlis ir negatīvs')
} else {
    console.log('Skaitlis ir vienāds ar nulli')
}

if (skaitlis3 > 0) {
    console.log('Skaitlis ir pozitīvs')
} else if (skaitlis3 < 0) {
    console.log('Skaitlis ir negatīvs')
} else {
    console.log('Skaitlis ir vienāds ar nulli')
}

if (skaitlis4 > 0) {
    console.log('Skaitlis ir pozitīvs')
} else if (skaitlis4 < 0) {
    console.log('Skaitlis ir negatīvs')
} else {
    console.log('Skaitlis ir vienāds ar nulli')
}
```

Lai samazinātu atkārtotā koda daudzumu, varam atkārtoto kodu ievietot vienā funkcijā, un tad vienkārši izsaukt to priekš katra skaitļa, sniedzot to skaitli kā argumentu:

```

function salidzinat(n) {
    if (skaitlis4 > 0) {
        console.log('Skaitlis ' + n + ' ir pozitīvs')
    } else if (skaitlis4 < 0) {
        console.log('Skaitlis ' + n + ' ir negatīvs')
    } else {
        console.log('Skaitlis ' + n + ' ir vienāds ar nulli')
    }
}

let skaitlis1 = 0
let skaitlis2 = -10
let skaitlis3 = 15
let skaitlis4 = 4

salidzinat(skaitlis1)
salidzinat(skaitlis2)
salidzinat(skaitlis3)
salidzinat(skaitlis4)
```

```
Skaitlis 0 ir vienāds ar nulli
Skaitlis -10 ir negatīvs
Skaitlis 15 ir pozitīvs
Skaitlis 4 ir pozitīvs
```

Funkcijas nosaukuma un argumentu nosaukumu veidošana seko tādiem pašiem noteikumiem kā mainīgo nosaukumu veidošana. Nedrīkst būt funkcija ar tādu pašu nosaukumu kā kāda mainīgā nosaukums - tas novedīs pie kļūdas un programma nedarbosies

## Atdotā vērtība

Vēlviena nozīmīga funkciju īpašība ir atdotā vērtība jeb **return value**. Ar atodo vērtību vienreiz saskārāmies nodaļā `ievade`, kur lietoām funkcijas `prompt()` atdoto vērtību.

Lai no funkcijas atdotu vērtību, rakstied `return` un tad jūsu vērtību. Šī vērtība var būt skaitlis, teksts, mainīgais vai aritmētiska izteiskme

```
function mana_funkcija() {
    return 2
}
```

Tad varam palaist šo funkciju un saglabāt atdoto vērtību mainīgjā:

```
function mana_funkcija() {
    console.log('Atdodu vērtību')
    return 2
}

let skaitlis = mana_funkcija()
console.log(skaitlis) //2
```

Ja mēs palaistu šo funkciju bet nesaglabātu atdoto vērtību, tad vērtība tiktu "palaista vējā". Atdotā vērtība nekur netiktu nodota un nebūtu pieejama (bet kļūda nerastos un programma turpinātu savu darbību). Ņemiet vērā ka kods kas seko pirms `return` tāpat tiktu palaists, pat ja atdotā vērtība netiktu saglabāta

```
mana_funkcija()
// Tiktu izvadīts 'Atdodu vērtību' bet atdotā vērtība nekur netiktu saglabāta
```

Tiklīdz mēs izsaucam `return`, funkcija pārstāj savu darbību un atdod vērtību. Jebkāda darbība kas notiek pēc `return` tiktu ignorēta

```
function mana_funkcija() {
    console.log('Atdodu vērtību')
    return 2
    console.log('Atdevu vērtību')
}

mana_funkcija()
// Tiek izvadīts 'Atdodu vērtību' bet ne 'Atdevu vērtību'
```

Atdotā vērtība ir ļoti spēcīga funkciju īpašība kura ļauj apstrādāt datus un izvadīt to rezultātu. Vislabāk atdotā vērtība strādā ja funkcijā lieto arī argumentus

```
// Dotā funkcija saņem divus skaitļus kā argumentus, un atdod šo skaitļu summu

function summa(skaitlis1, skaitlis2) {
    return skaitlis1 + skaitlis2
}

let jaunais_skaitlis = summa(5, 10)

console.log(jaunais_skaitlis)
```

```
15
```

> Starp citu, funkciju var izsaukt kā argumentu citā funkcijā. Ja ņemam iepriekšējo kodu kā piemēru, mēs varētu uzrakstīt:
>```
>console.log(summa(5, 10))
>```
>Šajā gadījumā funkcijas `summa()` atdotā vērtība tiktu lietotā kā arguments funkcijai `console.log()`

Funkcija var atdot vērtību tikai vienreiz, pēc kā tā pārstāj savu darbību.

## Saglabāt kā mainīgo

Funkciju ir iespējams saglabāt kā mainīgo. Šo parasti dara vidēja un augsta līmeņa programmētāji, bet iesācēji reti. Tomēr ir lietderīgi to zināt.

```
let saglabata_funkcija = function(argumenti) {
    // Funkcijas darbība
}
```

Tad šo mainīgo var izsaukt kā parastu funkciju:
```
saglabata_funkcija()
```

Izmantot funkciju kā mainīgo ir lietderīgi, jo šādā veidā funkciju var sniegt kā citas funkcijas argumentu

```
function cita_funckija(arguments) {
    arguments()
}

cita_funckija(saglabata_funckija)
```

## Kopsavilkums

 * Funkcijas ir veids kā atkārtoti izmantot vienu un to pašu kodu, nekopējot to
 * Funkcijas spēj saņemt vērtības jeb argumentus un atdot vērtību jeb **return value**
 * Funkcijas nosaukuma un argumentu nosaukumu veidošana seko tādiem pašiem noteikumiem kā mainīgo nosaukumu veidošana
 * Funkcijā drīkst būt vairāki argumenti

## Jautājumi

6.1: Kas ir funkcijas?

A: Funkcijas tas ir veids kā atkārtoti lietot vienu un to pašu kodu, bez nepieciešamības to kopēt

6.2: Ar ko ir lietderīgas funkcijas?

A: Funkcijas ļauj atkārtoti lietot vienu un to pašu kodu, kā arī ļauj grupēt saistītu kodu, kas padara to lasāmāku

6.3 Kas ir argumenti?

A: Argumenti tas ir veids kā funkcijai sniegt papildus informāciju, kuru tā var izmantot savas darbības laikā

6.4 Vai funkcijai var sniegt vairākus argumentus?

A: Jā, tie jāatdala ar komatiem

6.5 Kas ir atdotā vērtība?

A: **Atdotā vērtība** jeb **return value** ir vērtība kuru funkcija spēj "atdot" kodam kurš to izsauca. Šo vērtību var saglabāt mainīgajā un lietot turpmākajā programmas izpildē

6.6 Vai atdotajai vērtība ir lietderīga, ja to nesaglabā mainīgajā?

A: Nē, ja to nesaglabā mainīgajā tad tā tiek "palaista vējā" un tai vairs nevar piekļūt

6.7 Vai ir iespējams saglabāt funkciju kā mainīgo?

A: Jā

6.8 Ar ko ir lietderīgi saglabāt funkciju kā mainīgo?

A: Šādā veidā funkciju var sniegt kā argumentu citai funkcijai.

## Uzdevumi

6.1: Uzrakstiet, funkciju, kura vairākkārt izvada konsolē tekstu "Čau!", tad izsauciet šo funkciju

```
function runat() {
    console.log('Čau!')
    console.log('Čau!')
    console.log('Čau!')
}

runat()
```

6.2 Uzrakstiet funkciju `izvadit_starpibu`, kura ņem 2 skaitļus kā argumentus, un izvada tekstu "Skaitļu X un Y starpība ir ___" (kur X, Y ir argumentu vērtības, un __ ir šo vērtību starpība), tad izsauciet šo funkciju ar paša izvēlētiem skaitļiem kā argumentiem.

```
function izvadit_starpibu(skaitlis1, skaitlis2) {
    let starpiba = skaitlis1 - skaitlis2
    console.log('Skaitļu ' + skaitlis1 + ' un ' + skaitlis2 + ' starpība ir ' + starpiba)
}

izvadit_starpibu(40, 5)

// Skaitļu 40 un 5 starpība ir 35
```

6.3 Uzrakstiet funkciju `salikt_vardus`, kura ņem 2 teksta argumentus un atdod vērtību, kura ir šo divu argumentu kombinācija. Izsauciet šo funkciju, saglabājiet atdoto vērtību un izvadiet to

```
function salikt_vardus(vards1, vards2){
    return vards1 + vards2
}

let vardi = salikt_vardus('Sveika', 'Pasaule')

console.log(vardi)

// SveikaPasaule
```
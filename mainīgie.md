# Mainīgie

Iepriekšajā nodaļā mēs uzstādijām mūsu projektu un iemācijāmies kā izvadīt tekstu konsolē. Šajā nodaļā mēs mācīsimies par programmas pamatvienību - mainīgo.

Kas tad *ir* mainīgie? Mainīgais, jeb no angļu valodas **Variable**, ir kā datu konteineris, kurā glabāt datus.

Vispopulārākā analoģija par mainīgajiem ir šāda: mainīgo var iedomāties kā kasti, kurā var ielikt kādu priekšmetu, jeb vērtību, kā piemēram tekstu vai skaitli. Jebkurā brīdi mēs varam izņemt šo priekšmetu no kastes un ielikt tajā citu priekšmetu. Ir iespējams arī atstāt šo kasti tukšu, bez vērtības.

Lai kodā izveidotu mainīgo, uzrakstiet sekojošo:

```
let mans_mainigais = 5
```

Šis kods izveido mainīgo ar nosaukumu `mans_mainīgais` un nosaka tam vērtību `5`. Ja atskatamies uz mūsu kastu analoģiju, tad mums ir kaste ar nosaukumu `mans_mainīgais`, kurā esam ielikuši skaitli 5.

Izanalizēsim iepriekšējo koda rindiņu:

`let` saka programmai ka mēs vēlamies izveidot mainīgo. `let` var nomainīt pret `var` vai `const`, un tas izveidos mainīgo bet programma attieksies pret to nedaudz savādāk. Par to nedaudz vēlāk.

nākošais seko teksts `mains_mainigais`, kas ir mainīgā nosaukums. To var nomainīt pret jebkādu citu tekstu, bet tam jāseko šādiem noteikumiem:

 * nosaukumā drīkst būt burti un cipari, bet:
 * tajā nedrīkst būt atstarpēm, piemēram `mans mainigais`
 * tam jāsākas ar ar burtu, zemsvītru(_) vai dolāra zīmi($). Nekādu citu simbolu, piemēram ciparu vai '&' zīmi, nedrīkst lietot kā pirmo, piemēram `1mans_mainigais` vai `&mans_mainigais`
 * tas nedrīkst būt tāds pats kā **rezervēts** vārds.
 * ir iespējams, bet nav rekomendēts lietot mainīgā nosaukumā īpašos simbolus un garumzīmes, tā kā ne visi pārlūki spēj atšifrēt šos simbolus kad lasa programmu.

 > Rezervēts vārds tas ir jebkurš vārds kurš tiek lietots lai vadītu programmu, piemēram `let` vai `function` vai `class`. Ja mēs lietotu rezervētu vārdu mainīgā nosaukumā, programma apjuktu jo domātu ka tai vajag palaist darbību atbilstoši rezervētajam vārdam. [Saraksts ar rezervētiem vārdiem JavaScript valodā](#TODO)

Katrā valodā šie noteikumi var būt nedaudz savādāki, bet vairāk vai mazāk ir vienādi.

Mēs varētu nosaukt mūsu mainīgo piemēram par `skaitlis` vai `pica`.

> Parasti mainīgos nosauc atblistoši tam, priekš kā viņus lieto

tālāk iet ` = 5`, kas pasaka programmai ka mēs gribam pievienot šim mainīgajam vērtību `5`. Šī vērtība varētu būt arī kāda cita, piemēram cits skaitlis vai kāds teksts, vai arī cits mainīgais. Ja vēlamies pievienot tekstu, tam ir jābūt pēdiņās:

**Nepareizi:**
```
let mans_mainigais = Vārds
```

**Pareizi:**
```
let mans_mainigais = "Vārds"
```
**Vai**
```
let mans_mainigais = 'Vārds'
```

JavaScript valodā var lietot gan vienpēdiņas ' gan dubultpēdiņas ". Bet ir citas valodas kurās var lietot tikai vienu vai otru.

Iepriekšējā nodaļā iemācijāmies nedaudz par funkcijām, un par to, ka tām var dot argumentus. Funkcijai ir iespējams sniegt arī mainīgo kā argumentu.

Iekopējiet šo kodu, saglabājiet to un atjauniniet savu mājaslapu:

```
let mans_mainigais = 5
console.log(mans_mainigais)
```

konsolē vajadzētu tikt izvadītam jūsu mainīgajam.

Iepriekšējajā koda pirmajā rindiņā mēs **deklarējam** un **definējam** mainīgo `mans_mainigais` ar vērtību 5, tad nākošajā rindiņā ar `console.log()` mēs izvadam šo mainīgo uz konsoli.

> **Deklarēt** mainīgo nozīmē izveidot to, un **Definēt** nozīmē pievienot tam vērtību. Ir iespējams deklarēt mainīgo bez definēšanas. Par to nedaudz zemāk.

Varat nomainīt mainīgo pret citu vērtību, piemēram citu skaitli vai kādu tekstu, un konsole atbilstoši izvadīs šo  vērtību:

```
let mans_mainigais = "Cita vērtība"
console.log(mans_mainigais)
```

![](./images/mainigie/mainigie_1.PNG)

Ir iespējams arī uzrakstīt vairākas rindiņas ar dažādiem mainīgajiem un dažādām vērtībām

```
let mans_mainigais = "Vērtība"
let cits_mainigais = "Cita vērtība"
let skaitlis = 4

console.log(mans_mainigais)
console.log(skaitlis)
console.log(cits_mainigais)
```

Ir iespējams pievienot mainīgajam cita mainigā vērtību, lūk šādi:

```
let mans_mainigais = 5
let cits_mainigais = mans_mainigais

console.log(cits_mainigais)
```

![](./images/mainigie/mainigie_2.PNG)

## Deklarēšana un definīcija

Ir iespējams deklarēt(izveidot) mainīgo bet nedefinēt to (nepievienot tam vērtību)

```
let mans_mainigais
```

Šādam mainīgajam bez vērtības tehniski tāpat ir vērtība, un šī vērtība ir `undefined`. pastāv arī cita "bezvērtības" vērtība - `null`.

### Vērtību tipi

Mainīgo vērtības iedalās vairākos vērtību tipos. Šie tipi ir:

 * number (skailtis)
 * string (teksts)
 * boolean (patiess/nepatiess)
 * object (objekts)
 * undefined (bezvērtības)
 * null (bezvērtības)

Pastāv arī daži citi vērtību tipi, bet par tiem iesācējam nav jāuzstracas.

> Par objektiem mēs runāsim citā nodaļā

**boolean** vērtība var nozīmēt vienu no diviem - patiess vai nepatiess, jeb **true** vai **false**

```
let mainigais = false
let cits_mainigais = true
```

### Mainīgo aritmētika

Visspēcīgākā mainīgo iezīme drošivien ir aritmētika. Mainīgajam var pievienot aritmētisku vērtību, piemēram

```
let summa = 2 + 2
console.log(summa)
```

vai

```
let vertiba = 5 * 20 + 15
console.log(vertiba)
```

JavaScript valodā pastāv šādi aritmētikas simboli:

 * \+ (saskaitīšana)
 * \-  &nbsp;(atņemšana)
 * /  &nbsp;(dalīšana)
 * \* &nbsp;(reizināšana)
 * \** (kāpināšana)
 * % (modulus jeb dalīšanas atlikums)

Ir iespējams mainīgo paaugstināt vai samazināt par vienu, izmantojot `++` vai `--`, šādi:

```
let skaitlis = 1
console.log(skaitlis) // 1
skaitlis++
console.log(skaitlis) // 2 
skaitlis++
console.log(skaitlis) // 3
skaitlis--
console.log(skaitlis) // 2
```



Jautājumi:

2.1: Vienkāršos vārdos, paskaidrojiet kas ir mainīgie?

A: Mainīgais tas ir konteineris, kurā var ievietot kādu vērtību. Šo vērtību var vēlāk nomainīt. Var arī atstāt šo konteineri tukšu, bez vērtības.

2.2: Vai mainīgā nosaukumā drīkst būt atstarpēm?

A: Nē

2.3: Vai mainīgā nosaukumā drīkst lietot ciparus?

A: Jā, bet ne kā pirmo simbolu nosaukumā

2.4: Kā mainīgā deklarēšana atšķiras no definēšanas?

A: Deklarēt mainīgo nozīme to izveidot, definēt nozīmē pievienot tam vērtību

2.5: Vai drīkst būt mainīgais bez vērtības?

A: Jā(bet tehniski runājot pat bezvērtības mainīgajiem ir vērtība - `undefined`)
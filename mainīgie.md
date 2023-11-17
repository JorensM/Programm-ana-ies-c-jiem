# Mainīgie

Iepriekšajā nodaļā mēs uzstādijām mūsu projektu un iemācijāmies kā izvadīt tekstu konsolē. Šajā nodaļā mēs mācīsimies par programmas pamatvienību - mainīgo.

Kas tad *ir* mainīgie? Mainīgais, jeb no angļu valodas **Variable**, ir kā datu konteineris, kurā glabāt datus.

Mainīgo var iedomāties kā kasti, kurā var ielikt kādu priekšmetu, jeb datu vienību, kā piemēram tekstu vai skaitli. Jebkurā brīdi mēs varam izņemt šo priekšmetu no kastes un ielikt tajā citu priekšmetu.

Lai kodā izveidotu mainīgo, uzrakstiet sekojošo:

```
let mans_mainigais = 5
```

Šis kods izveido mainīgo ar nosaukumu `mans_mainīgais` un nosaka tam vērtību `5`. Ja atskatamies uz mūsu kastu analoģiju, tad mums ir kaste ar nosaukumu `mans_mainīgais`, kurā esam ielikuši skaitli 5.

Izanalizēsim iepriekšējo koda rindiņu:

`let` saka programmai ka mēs vēlamies izveidot mainīgo. `let` var nomainīt pret `var` vai `const`, un tas izveidos mainīgo bet programma attieksies pret to nedaudz savādāk. Par to nedaudz vēlāk.

nākošais seko teksts `mains_mainigais`, kas ir mainīgā nosaukums. To var nomainīt pret jebkādu citu tekstu, bet tam jāseko šādiem noteikumiem:

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

Varat nomainīt mainīgo pret citu vērtību, piemēram citu skaitli vai kādu tekstu, un konsole atbilstoši izvadīs šo jauno vērtību:

```
let mans_mainigais = "Jaunā vērtība"
console.log(mans_mainigais)
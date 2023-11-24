# Ievade

Iepriekšējās divās nodaļās mācijāmies par mainīgajiem un nosacījumiem - svarīgiem programmēšanas aspektiem. Vēlviens svarīgs programmēšanas aspekts ir ievade. **Ievade** tā ir jebkāda darbība kuru programmas lietošanas laikā veic programmas lietotājs. **Programmas lietotājs** tas ir cilvēks, kurš lieto izveidoto programmu.

## Ievades tipi

Pastāv vairāki ievades tipi:
 * Teksta ievade (taustatūras pogu spiezšana)
 * Peles ievade (peles kustināšana vai klikšķināšana)
 * Skaņas ievade (ieraksts caur mikrofonu)
 * Vizuāla ievade (video vai foto caur kamera)

Takā mēs mācāmies programmēšanas pamatus, mācīsimies arī visvienkāršāko ievades tipu - teksta ievadi

## prompt()

Lai ļautu lietotājam ievadīt tekstu, mēs varam lietot funkciju `prompt()` - šī funkcija, kad palaista, atver logu, uzrādot noradīto tekstu (piemēram kādu jautājumu uz kuru lietotājam jāatbild) un ļauj lietotājam ievadīt tekstu, un tad atgriež šo ievadīto tekstu, kuru tad var saglabāt mainīgajā.

Kā argumentu `prompt()` funkcijai ir jāsniedz teksts, kuru uzrādīs kā jautājumu kad tiks pieprasīta lietotāja ievade.

```
prompt('Kāda ir jūsu mīļākā krāsa?')
```

##TODO IMAGE

## Atdotā vērtība

Funkcijām pastāv tāda īpašība kā `return value`, jeb `atdotā vērtība`. Jebkura funkcija spēj "Atdot" vērtību, kuru var saglabāt mainīgajā. Par funkcijām un atdotajām vērtībām vairāk runāsim nodaļā [funckijas](#)

funkcija `prompt()` spēj atdot atpakaļ vērtību, kuru var saglabāt mainīgajā. Atdotā vērtība būs teksts, kurš ticis ievadīts.

```
let atbilde = prompt("Kāda ir jūsu mīļākā krāsa?")
console.log("Jūs atbildējāt: " + atbilde)
```

Ar lietotāja ievadi atveras durvis uz daudz dažādām iespējām. Mēs varam padarīt programmu interaktīvu un mainīt tās darbību atkarībā no lietotāja ievades. Piemēram mēs varam prasīt lietotājam ievadīt jautājumu, un izvadīt tekstu atkarībā no atbildes

```
let atbilde = prompt("Vai tev patīk vāģi? (Ievadiet 'Jā' vai 'Nē')")

if (atbile == "Jā") {
    console.log("Forši! Man arī!")
} else if(atbilde == "Nē") {
    console.log("Ā, nu žēļ.")
} else {
    console.log("Nesapratu")
}
```

Šajā programmā, viens vai cits teksts tiks izvadīt, atkarībā no tā, ko lietotājs ievadīja. Ja lietotājs ievadīja "Jā", tad tiks izvadīts pirmais tekts. Ja "Nē", tad otrais. Ja tiek ievadīts kāds cits teksts kā "Jā" vai "Nē", programma atbildēt "Nesapratu".

> Ņemiet vērā ka programmēšanā atstarpes, īpašās zīmes un liele/mazie burti ir svarīgi. tekstam "Jā" ir cita vērtība nekā "jā" vai "ja", un "SveikaPasaule" ir cita vērtība nekā "sveika pasaule". Iepriekšējā programmā, ja lietotājs ievadītu "jā" nevis "Jā", tad tiktu izvadīts teksts "Nesapratu" 

## Noslēgums

Šajā nodaļā mācijāmies par ievadi - veidu kā lietotājs komunicē ar programmu. Pārzināt lietotāja ievadi un kā to nolasīt ir svarīgs programmēšanas aspekts, kurš noteikti ir nepieciešams ja vēlaties veidot interaktīvas programms.

Nākošajā nodaļā mācīsimies par funkcijām - programmēšanas aspektu kurš stipri atvieglo un vienkāršo programmēšanu

## Jautājumi

1.1 Kas ir ievade?

A: Ievade tā ir jebkāda darbība ko programmas lietošanas laikā veic lietotājs

1.2 Kas ir lietotājs?

A: Lietotājs tas ir jebkurš cilvēks kurš lieto programma.

1.3 Kādi ievades tipi pastāv?

A: 
 * Teksta ievade (taustatūras pogu spiezšana)
 * Peles ievade (peles kustināšana vai klikšķināšana)
 * Skaņas ievade (ieraksts caur mikrofonu)
 * Vizuāla ievade (video vai foto caur kamera)

1.4 Ko dara `prompt()` funkcija?

A: Šī funkcija ļauj lietotājam ievadīt tekstu, kuru tad šī funkcija atdod kā "atdoto vērtību" jeb **return value**

1.5 Kas ir atdotā vērtība jeb **return value**?

A: Atdotā vērtība tā ir vērtība ko kāda funkcija atdot.

1.6 Ko var darīt ar atdoto vērtību?

A: To var saglabāt mainīgajā

## Uzdevumi

1.1 Izveidojiet vienkāršu programmu, kura ar `prompt()` funkciju lūdz lietotājam ievadīt tekstu, un tad izvada to pašu tekstu konsolē

1.2 Izveidojiet programmu, kura ar `prompt()` funkciju jautā lietotājam "kāds ir tavs mīļākais dzīvnieks", un tad izvada konsolē "Kāda sakritība! Mans mīļākais dzīvnieks arī ir \_\_\_" (kur \_\_\_ ir lietotāja ievadītais teksts)

1.3 Izveidojiet programmu, kura ar `prompt()` funkciju jautā lietotājam "Vai viens metrs ir vienāds ar simts centimetriem?", un tad ar nosacījumiem pārbauda atbildi, un izvada "Pareizi!" vai "Nepareizi" respektīvi.

1.4 Izveidojiet programmu, kura ar `prompty()` lūdz lietotājam ievadīt skaitli, un tad izvada konsolē "Skaitlis ir pozitīvs" vai "Skaitlis ir negatīvs" atkarībā no ievadītā skaitļa.

1.5 Izveidojiet programmu, kura ar diviem `prompt()` lūdz lietotājam ievadīt vienu skaitli, tad lūdz ievadīt vēlvienu skaitli, tad konsolē izvada šo abu skaitļu summu.



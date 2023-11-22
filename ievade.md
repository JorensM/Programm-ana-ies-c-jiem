# Ievade

Iepriekšējās divās nodaļās mācijāmies par mainīgajiem un nosacījumiem - svarīgiem programmēšanas aspektiem. Vēlviens svarīgs programmēšanas aspekts ir ievade. **Ievade** tā ir jebkāda darbība kuru programmas lietošanas laikā veic programmas lietotājs. **Programmas** lietotājs tas ir cilvēks, kurš lieto izveidoto programmu.

## Ievades tipi

Pastāv vairāki ievades tipi:
 * Teksta ievade (taustatūras pogu spiezšana)
 * Peles ievade (peles kustināšana vai klikšķināšana)
 * Skaņas ievade (ieraksts caur mikrofonu)
 * Vizuāla ievade (video vai foto caur kamera)

Takā mēs mācāmies programmēšanas pamatus, mācīsimies arī visvienkāršāko ievades tipu - teksta ievadi

## prompt()

Lai ļautu lietotājam ievadīt tekstu, mēs varam lietot funkciju `prompt()` - šī funkcija, kad palaista, atver logu, uzrādot noradīto tekstu (piemēram kādu jautājumu uz kuru lietotājam jāatbild) un ļauj lietotājam ievadīt tekstu, un tad atgriež šo ievadīto tekstu, kuru tad var saglabāt mainīgajā.

```
prompt('Kāda ir jūsu mīļākā krāsa?')
```

##TODO IMAGE

> # Return value
> Funkcijām pastāv tāda īpašība kā `return value`, jeb `atdotā vērtība`. Jebkura funkcija spēj "Atdot" vērtību, kuru var saglabāt mainīgajā. Par funkcijām vairāk runāsim nodaļā [funckijas](#)

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



//Koda bloks neredz mainīgos ārpus tā

# Koda bloki

Iepriekšējā nodaļā par nosacījumiem, pirmo reizi saskārāmies ar koda blokiem. Koda bloks tā ir noteikta koda daļa, kura ieskauta starp divām zīmēm - `{` un `}`. Koda bloka sintakse ir šāda:

```
{
    // Darbība
}
```

> Koda blokus angliski sauc vai nu par **code block** vai **scope**

Ja atceraties, tad nosacījumos arī lietojām koda blokus:

```
if (...) {
    // ...
}
```

## Kad lieto koda blokus

Koda bloki paši pa sevi nav pārāk lietderīgi un reti tiek lietoti. Tos pārsvarā lieto kad definē funkciju vai raksta nosacījumu.

## Koda bloka īpašība

Koda blokam ir viena izteikta īpašība - jebkurš mainīgais kurš deklarēts iekš koda bloka nav pieejams ārpus ši bloka. Ņemsim šādu piemēru:

```
{
    let skaitlis = 10;
}
console.log(skaitlis)
```

Kā jūs domājat, kas tiks izvadīts konsolē?

Atbilde: Konsolē tiks izvadīta kļūda jeb **error**, norādot ka mainīgais `skaitlis` nav definēts. Tas ir tādēļ, ka mēs šo mainīgo definējām koda blokā, bet centāmies tam piekļūt ārpus tā. Kā jau minēju, mainīgie kuri tiek definēti iekš koda bloka ir pieejami tikai tajā koda blokā bet ne ārpus tā.

Bet ja mēs izdaram otrādi:

```
let skaitlis = 10;
{
    console.log(skaitlis)
}
```

Tad skaitlis tiek veiksmīgi izvadīts. Mainīgie kuri definēti ārpus koda bloka ir pieejami šajā koda blokā

## Nesting

Koda blokiem ir iespējama 'iestaprināšana' jeb **nesting**. Iestarpināšana ir kad mēs ievietojam vienu koda bloku citā koda blokā, lūk šādi:

{
    console.log('viens koda bloks')
    {
        console.log('cits koda bloks')
    }
}

## Kopsavilkums

* Koda bloki ir veids kā atdalīt kādu koda daļu no citas
* Lai izveidotu koda bloku, jālieto zīmes `{` un `}`
* Mainīgie deklarēti iekš koda bloka ir pieejami tikai tajā un nav pieejami ārpus tā

## Noslēgums

Šajā nodaļā iemācijāmies par koda blokiem.

Nākošajā nodaļā mācīsimies par ievadi - varēsim uzrakstīt programmu kura veic noteiktas darbības atkarībā no lietotāja ievades.

## Jautājumi

1.1: Kas ir koda bloks?

A: koda bloks tā ir atdalīta koda daļa

1.2 Kāda ir koda bloka visizteiktākā īpašība?

A: Mainīgais kurš definēts iekš koda bloka ir pieejams tikai tajā blokā un ne ārpus tā

1.3 Kas ir 'iestarpināšana' jeb **nesting**?

A: Iestaprināšana tas ir tad kad mēs vienu koda bloku ievietojam citā koda blokā
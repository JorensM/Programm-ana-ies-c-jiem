# Cikli

Cikli ir veids kā ļaut vienam un tam pašam kodam atkārtoties vairākas reizes, bez nepieciešamības to kopēt. Tādā ziņā tie ir līdzīgi funkcijām, bet to pielietojums atšķiras no funkciju pielietojuma.

Pastāv divu pamata veidu cikli: `for` un `while`

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


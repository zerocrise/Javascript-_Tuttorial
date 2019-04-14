---
description: Uso delle variabili in javascript
---

# Variabili

Una variabile rappresenta **uno spazio di memoria alterabile** dove vengono memorizzati dei valori. **Il nome** della variabile, rappresenta **l'indirizzo fisico in memoria.** Serve per identificare la locazione della variabile in memoria al fine di accedere o modificarne il valore durante l'esecuzione. 



Per l’utilizzo delle variabili possiamo distinguere due fasi:

1. **dichiarazione :** si effettua utilizzando la **parola chiave var** seguita da un identificatore
2. **assegnazione**: si effettua utilizzando l’operatore di assegnamento, rappresentato dal simbolo uguale **\(=\)**, cui far seguire un valore da attribuirle.

###  Dichiarazione di una variabile

La sintassi per la dichiarazione di una variabile è la seguente:

 **var nome\_della\_variabile \[ = inizializzazione\];** 

dove:

1. **var** parola chiave per identificare una variabile 
2. **nome della variabile:** identificatore della variabile che deve rispettare alcune regole:
   * non deve coincidere con una delle parole chiave del linguaggio;
   * non può iniziare con un numero;
   * non può contenere caratteri speciali come ad esempio:
     * lo spazio,
     * il trattino \(`-`\),
     * il punto interrogativo \(`?`\),
     * il punto \(`.`\),
   * Sono però ammessi:
     * l’underscore \(`_`\)
     * il simbolo del dollaro \(`$`\).
3. **inizializzazione:** valore di default con cui è possibile valorizzare una variabile.

## Strict mode

JavaScript non prevede l’obbligo di dichiarazione delle variabili, quindi potremmo inavvertitamente utilizzare una variabile senza dichiararla, senza che il compilatore JIT fornisca alcuna segnalazione, con il conseguente rischio di incorrere in malfunzionamenti. Possiamo però lavorare in **strict mode**, una opzione introdotta nella versione 5 dello standard ECMAScript che ci consente, tra le altre cose, di ricevere **una segnalazione di errore quando non dichiariamo le variabili**. Per abilitare lo strict mode sarà sufficiente inserire all’inizio del nostro codice, il comando: **"use strict".**  Una volta abilitato lo strict mode, ogni assenza di dichiarazione di variabili sarà intercettata dal motore JavaScript e ci verrà segnalato un errore.

###  "use strict"

```javascript
"use strict"
var a=10;
b=30;
```


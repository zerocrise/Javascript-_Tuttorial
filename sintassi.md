# Sintassi

## Sintassi

Il codice JavaScript è composto da una **sequenza di istruzioni che viene interpretata ed eseguita dall’engine.**  Ciascuna i**struzione \(o blocco di istruzioni\)** **è delimitata da un punto e virgola.**  

![](.gitbook/assets/schermata-2019-04-14-alle-16.43.33.png)

 è un linguaggio **keys sensitive** ossia fa distinzione tra **maiuscole minuscole.**

### **Inserire codice JavaScript in una pagina HTML**

Esistono tre modi per inserire codice JavaScript in una pagina HTML:

* **inserire codice inline;**
* **scrivere blocchi di codice nella pagina;**
* **importare file con codice JavaScript esterno.**

### Codice inline

L’inserimento di codice inline, consiste nell’inserire direttamente le istruzioni JavaScript nel codice di un elemento HTML, assegnandolo **ad un attributo che rappresenta un evento**. Chiariamo il concetto con un esempio:

`<button type="button" onclick="alert('Ciao Mondo!')">Cliccami</button>`

**L’attributo onclick** rappresenta l’evento del **clic sul pulsante del mous**e, quindi in corrispondenza di questo evento verrà analizzato ed eseguito il codice JavaScript assegnato.  

```javascript
function prova(){
alert("prova alert");
}

```

## Blocchi di codice, il tag script

L’approccio inline risulta scomodo quando il codice da eseguire è più complesso  si ricorrere al tag **&lt;script**&gt; per inserire blocchi di codice in una pagina HTML, come nel seguente esempio:

**&lt;script&gt;alert\('Ciao mondo!'\)&lt;/script&gt;** 

Quando il parser HTML del browser esamina la pagina, riconosce il tag &lt;scrip&gt; come blocco di codice e ne passa il contenuto all’engine JavaScript, che lo esegue. Si possono inserire blocchi di codice \(e i relativi tag script\) nella **sezione head** o nella sezione **body** della pagina HTML. S_e il codice JavaScript interagisce con un elemento HTML, occorre assicurarsi che tale elemento sia già stato analizzato dal parser HTML: così il corrispondente oggetto sarà disponibile in memoria. Questo spiega il perché talvolta troviamo uno o più blocchi di codice JavaScript in fondo alla pagina prima della chiusura del tag **`</body>`.**_ 

### JavaScript esterno

Il terzo approccio consiste nel collegare alla pagina HTML, il codice **JavaScript presente in un file esterno**. Per **inserire un file JavaScript esterno** ci serviamo sempre del tag **`<script>`** in cui specificando l’attributo **src**, come mostrato dal seguente esempio:

```text
<script src="codice.js"></script>
```

Il riferimento al file JavaScript può essere relativo alla pagina HTML corrente oppure assoluto:

```text
<script src="http://www.server.com/codice.js"></script>
```

Non è necessario in questo caso che il file JavaScript risieda sullo stesso server della pagina. 

### Vantaggi JavaScript esterni

L'inserimento di script in file esterni presenta alcuni vantaggi:

* **Separa HTML e codice**
* **Rende HTML e JavaScript più facili da leggere e mantenere**
* **I file JavaScript memorizzati nella cache possono accelerare i carichi di pagina**

Per aggiungere più file di script a una pagina, si usano più **tag &lt;script&gt;:**

```text
<script src="http://www.server.com/codice.js"></script>
<script src="http://www.server.com/codice1.js"></script>
<script src="http://www.server.com/prova.js"></script>
```

## Output javascript

JavaScript può "visualizzare" i dati in diversi modi:

* in un elemento HTML, usando **innerHTML** .
* nell'output HTML usando **document.write \(\)** .
* una casella di avviso, utilizzando **window.alert \(\)** .
* nella console del browser, utilizzando **console.log \(\)** .

### innerHTML

Per accedere a un elemento HTML,  si utilizza il metodo **document.getElementById \(id\)**.**innerHTML dove:**

Il metodo **getElementById \(id\)** restituisce l'elemento che ha l'attributo **ID** con il valore specificato. Restituisce _null_ se non esistono elementi con l'ID specificato.  La proprietà **innerHTML** definisce il contenuto. 

### document.write \(\)

Ul metodo **write \(valore\), scrive valore nel documento html.  L'uso di document.write \(\) dopo il caricamento di un documento HTML, cancellerà tutto il codice HTML esistente .**

### alert \(\)

È possibile utilizzare una casella di avviso per visualizzare i dati:

### console.log \(\)

Per scopi di debug, è possibile utilizzare il metodo **console.log \(\)** per visualizzare i dati.

{% code-tabs %}
{% code-tabs-item title="console.js" %}
```javascript
console.log(3+2);//visualizza 5
```
{% endcode-tabs-item %}
{% endcode-tabs %}


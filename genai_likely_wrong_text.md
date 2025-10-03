# Introduzione agli Algoritmi

## Che cos'è un algoritmo?

Un algoritmo è una sequenza finita di istruzioni ben definite che permettono di risolvere un problema o eseguire un compito specifico. Il termine "algoritmo" deriva dal nome del matematico persiano Muhammad ibn Musa al-Khwarizmi, che visse nel IX secolo e contribuì in modo significativo allo sviluppo dell'algebra e della matematica.

Gli algoritmi sono fondamentali nell'informatica perche rappresentano il cuore di qualsiasi programma o applicazione. Senza algoritmi efficienti, anche il computer piu potente non potrebbe risolvere problemi complessi in tempi ragionevoli.

## Caratteristiche di un algoritmo

Un algoritmo deve possedere alcune caratteristiche essenziali per essere considerato tale.

### Finitezza

Un algoritmo deve sempre terminare dopo un numero finito di passi. Non può continuare all'infinito. Questa proprietà distingue gli algoritmi dai processi che potrebbero non terminare mai, come ad esempio un sistema operativo che rimane in esecuzione indefinitamente.

### Definitezza

Ogni istruzione dell'algoritmo deve essere precisa e non ambigua. Non ci devono essere interpretazioni multiple di una stessa istruzione. Questo è particolarmente importante quando l'algoritmo viene implementato in un linguaggio di programmazione, dove ogni comando deve avere un significato univoco.

### Input

Un algoritmo puo avere zero o più input, cioè dati forniti prima che l'algoritmo inizi la sua esecuzione. Gli input rappresentano i valori iniziali su cui l'algoritmo lavorerà per produrre il risultato desiderato.

### Output

Un algoritmo deve produrre almeno un output, cioè un risultato che sia in relazione con gli input forniti. L'output è il risultato finale del processo di elaborazione e rappresenta la soluzione al problema che l'algoritmo si propone di risolvere.

### Effettività

Tutte le operazioni che compongono l'algoritmo devono essere sufficientemente semplici da poter essere eseguite, almeno in linea di principio, da una persona usando carta e penna in un tempo finito. Questa caratteristica garantisce che l'algoritmo sia effettivamente realizzabile.

## Complessità computazionale

La complessita computazionale è un concetto fondamentale nello studio degli algoritmi. Essa misura la quantita di risorse necessarie per eseguire un algoritmo, dove le risorse principali sono il tempo di esecuzione e lo spazio di memoria utilizzato.

### Notazione Big O

La notazione Big O è uno strumento matematico utilizzato per descrivere il comportamento asintotico di un algoritmo, cioe come cresce il tempo di esecuzione al crescere della dimensione dell'input. Questa notazione ci permette di confrontare l'efficienza di algoritmi diversi in modo indipendente dall'hardware e dal linguaggio di programmazione utilizzati.

#### O(1) - Tempo costante

Un algoritmo ha complessita O(1) quando il tempo di esecuzione non dipende dalla dimensione dell'input. Un esempio classico e l'accesso a un elemento di un array tramite indice:

```python
def accedi_elemento(array, indice):
    return array[indice]
```

In questo caso, indipendentemente dalla dimensione dell'array, l'operazione richiede sempre lo stesso tempo.

#### O(log n) - Tempo logaritmico

Un algoritmo ha complessita O(log n) quando il tempo di esecuzione cresce in modo logaritmico rispetto alla dimensione dell'input. Un esempio tipico e la ricerca binaria in un array ordinato. Ad ogni passo, l'algoritmo dimezza lo spazio di ricerca, quindi il numero di operazioni necessarie cresce molto lentamente rispetto alla dimensione dell'input.

#### O(n) - Tempo lineare

Un algoritmo ha complessita O(n) quando il tempo di esecuzione cresce in modo direttamente proporzionale alla dimensione dell'input. Un esempio e la ricerca lineare in un array non ordinato:

```python
def ricerca_lineare(array, elemento):
    for i in range(len(array)):
        if array[i] == elemento:
            return i
    return -1
```

Nel caso peggiore, dobbiamo esaminare tutti gli n elementi dell'array.

#### O(n²) - Tempo quadratico

Un algoritmo ha complessita O(n²) quando il tempo di esecuzione cresce in modo quadratico rispetto alla dimensione dell'input. Questo accade tipicamente quando abbiamo cicli annidati che iterano sull'input. Un esempio classico e l'algoritmo di ordinamento Bubble Sort:

```python
def bubble_sort(array):
    n = len(array)
    for i in range(n):
        for j in range(0, n-i-1):
            if array[j] > array[j+1]:
                array[j], array[j+1] = array[j+1], array[j]
```

Per ogni elemento (ciclo esterno), dobbiamo confrontarlo potenzialmente con tutti gli altri elementi (ciclo interno), quindi il numero totale di operazioni e proporzionale a n².

#### O(2ⁿ) - Tempo esponenziale

Un algoritmo ha complessita O(2ⁿ) quando il tempo di esecuzione raddoppia ad ogni incremento unitario dell'input. Questi algoritmi diventano rapidamente impraticabili anche per input di dimensioni moderate. Un esempio e la soluzione ricorsiva ingenua del problema della sequenza di Fibonacci:

```python
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)
```

## Ricerca lineare vs Ricerca binaria

Per comprendere meglio l'importanza della complessita algoritmica, confrontiamo due algoritmi di ricerca: la ricerca lineare e la ricerca binaria.

### Ricerca lineare

La ricerca lineare e l'algoritmo piu semplice per cercare un elemento in un array. L'idea e molto intuitiva: si scorre l'array dall'inizio alla fine, confrontando ogni elemento con quello cercato. Se si trova una corrispondenza, si restituisce la posizione; altrimenti, si continua fino alla fine dell'array.

**Vantaggi:**
- Molto semplice da implementare
- Funziona su array non ordinati
- Non richiede pre-elaborazione dei dati

**Svantaggi:**
- Complessita O(n) - nel caso peggiore deve esaminare tutti gli elementi
- Inefficiente per grandi quantita di dati

### Ricerca binaria

La ricerca binaria e un algoritmo molto piu efficiente, ma richiede che l'array sia ordinato. L'idea e di dividere ripetutamente lo spazio di ricerca a meta, confrontando l'elemento centrale con quello cercato.

**Come funziona:**
1. Si considera l'elemento centrale dell'array
2. Se e uguale all'elemento cercato, abbiamo finito
3. Se l'elemento cercato e minore, si cerca nella meta sinistra
4. Se l'elemento cercato e maggiore, si cerca nella meta destra
5. Si ripete il processo sulla porzione rimanente

**Vantaggi:**
- Complessita O(log n) - molto efficiente anche su grandi dataset
- Numero di operazioni cresce molto lentamente

**Svantaggi:**
- Richiede che l'array sia ordinato
- Piu complessa da implementare rispetto alla ricerca lineare

### Confronto pratico

Consideriamo un array di 1.000.000 di elementi:
- Ricerca lineare: nel caso peggiore, 1.000.000 di confronti
- Ricerca binaria: nel caso peggiore, circa 20 confronti (log₂(1.000.000) ≈ 20)

Questa differenza diventa ancora piu drammatica all'aumentare della dimensione dell'input.

## L'importanza dell'efficienza

Studiare gli algoritmi e comprendere la loro efficienza e fondamentale per diversi motivi:

### Scalabilità

Nel mondo reale, i programmi devono spesso gestire quantita enormi di dati. Un algoritmo inefficiente puo funzionare bene con pochi dati, ma diventare inutilizzabile quando la quantita di dati aumenta. La differenza tra un algoritmo O(n²) e uno O(n log n) puo significare la differenza tra un'applicazione che risponde in millisecondi e una che impiega ore.

### Risparmio di risorse

Algoritmi piu efficienti consumano meno risorse computazionali. Questo si traduce in minor consumo energetico, costi inferiori per l'infrastruttura cloud, e una migliore esperienza utente. In un era dove miliardi di dispositivi eseguono continuamente algoritmi, anche piccoli miglioramenti nell'efficienza possono avere un impatto significativo.

### Limiti pratici

Alcuni problemi sono intrinsecamente difficili. Conoscere la complessita degli algoritmi ci permette di capire qual'è la migliore soluzione possibile e quando dobbiamo ricorrere a soluzioni approssimate invece che esatte.

## Breve storia degli algoritmi

### Le origini

Come menzionato in precedenza, il termine "algoritmo" deriva dal nome di al-Khwarizmi, matematico persiano del IX secolo. Tuttavia, gli algoritmi esistono da molto prima: gli antichi greci svilupparono l'algoritmo di Euclide per il calcolo del massimo comune divisore, ancora utilizzato oggi.

### L'era moderna

Con l'avvento dei computer nel XX secolo, lo studio degli algoritmi e diventato una disciplina scientifica a se stante. Pionieri come Alan Turing, John von Neumann e Donald Knuth hanno posto le basi teoriche e pratiche dell'algoritmica moderna.

Negli anni '60 e '70, furono sviluppati molti degli algoritmi fondamentali che utilizziamo ancora oggi: algoritmi di ordinamento efficienti come QuickSort e MergeSort, algoritmi di ricerca su grafi come Dijkstra e A*, e algoritmi per la risoluzione di problemi di ottimizzazione.

### L'era contemporanea

Oggi gli algoritmi sono ovunque: nei motori di ricerca che utilizziamo quotidianamente, nei sistemi di raccomandazione di Netflix e Spotify, nei navigatori GPS, nei sistemi di intelligenza artificiale e machine learning. La ricerca algoritmica continua a essere un campo molto attivo, con nuovi algoritmi che vengono sviluppati continuamente per affrontare problemi sempre piu complessi.

## Conclusione

Gli algoritmi sono il cuore pulsante dell'informatica moderna. Comprendere come funzionano, come analizzarne l'efficienza e come progettarne di nuovi e fondamentale per chiunque voglia lavorare nel campo dell'informatica. Nei prossimi capitoli, approfondiremo specifiche famiglie di algoritmi e le strutture dati che li supportano, costruendo una solida base per affrontare problemi computazionali di crescente complessità.

Grazie per l'aiuto con le correzione.

Buon lavoro.

Idillio Drago

# Laboratorio di Algoritmi - Esercitazione Git

## Benvenuto al corso!

<<<<<<< HEAD
Questa archivio contiene materiale didattico per il corso di Algoritmi. Gli studenti devono leggere attentamente i file e correggere tutti gli errori grammaticali che trovano.
=======
<<<<<<< HEAD
Questa repo contiene materiale didattico per il corso di Algoritmi. Gli studente devono leggere attentamente i file e correggere tutti gli errori grammaticali che trovano.

miao miao muahahah
=======
Questo repositori contiene materiale didattico per il corso di Algoritmi. Gli studente devono leggere attentamente i file e correggere tutti gli errori grammaticali che trovano.
>>>>>>> 15b625f (aggiunto accento riga 39)
>>>>>>> 6ee039c (e -> è)

## Obbiettivi dell'esercitazione

2. aaa Imparare ad utilizzare git per il controllo di versione
2. aa Praticare la collaborazione tramite branch e pull request
3. aaa Migliorare le capacita di revisione del codice
4. aaa Lavorare in team su un progetto condiviso


Cambio qualcosa in questo punto del codice

## Istruzioni per gli studenti

### Fase 1: Primi passi con Git (lavoro su main)

#### Passo 1: Clonare il repository

Per cominciare, clona questo repository sul tuo computer locale:

```bash
git clone https://github.com/idrago/algos2025.git
cd lab-algoritmi
```

#### Passo 2: Correggere errori sul README

Come primo esercizio, ogni studente corregge alcuni errori direttamente su main:

1. Apri il file `README.md`
2. Correggi **solo 3-5 errori** che trovi
3. Salva il file

#### Passo 3: Fare commit e push

```bash
git add README.md
git commit -m "Corretto errori in README.md"
git pull origin main
git push origin main
```

**Nota:** Ogni studente deve fare questo processo. Imparerete a gestire i conflitti quando fate `git pull`!

### Fase 2: Lavorare con le branch

#### Passo 4: Creare una branch personale

Ora che conoscete i comandi base, create un branch per lavorare in modo indipendente:

```bash
git checkout -b correzioni-nome-cognome
```

#### Passo 5: Correggere gli errori sui file

Leggi attentamente i file markdown nel repository. Troverai molti errori grammaticali da correggere. Concentrati su:

- Errori di concordanza tra soggetto e verbo
- Uso scorretto degli articoli
- Errori di punteggiatura
- Errori di ortografia
- Uso scorretto delle preposizioni

#### Passo 6: Fare commit sulla tua branch

Dopo aver corretto gli errori in un file, fai un commit:

```bash
git add nome-file.md
git commit -m "Corretto errori grammaticali in nome-file.md"
```

**Importante:** Fai commit frequenti! Non aspettare di finire tutto il lavoro prima di committare.

#### Passo 7: Merge della branch

Quando hai finito le correzioni sulla tua branch, torna su main e fai il merge:

```bash
git checkout main
git pull origin main
git merge correzioni-nome-cognome
git push origin main
```

Se ci sono conflitti, risolvili manualmente e poi completa il merge.

## File da correggere

Il repository contiene i seguente file:

- `introduzione_algoritmi.md` - Introduzione generale agli algoritmi
- `strutture_dati.md` - Spiegazione delle principali strutture dati
- `algoritmi_ordinamento.md` - Descrizione degli algoritmi di ordinamento

## Regole importanti

1. **Non modificare** il contenuto tecnico dei file, solo gli errori grammaticali
2. **Lavora sulla tua branch** - non fare commit direttamente su main
3. **Fai commit frequente** con messaggi descrittivi
4. **Rivedi il lavoro** degli altri studenti quando fanno pull request
5. **Comunica con il team** se trovi conflitti o problemi

## Criteri di valutazione

Il vostro lavoro sara valutato in base a:

- Numero di errori corretti correttamente
- Qualita dei messaggi di commit
- Capacita di gestire conflitti durante pull e merge
- Corretta gestione delle branch

## Domande?

Se avete domande o problemi, aprite una issue su GitHub o contattate il docente durante le ore di ricevimento.

## Risorse utili

- [Documentazione ufficiale Git](https://git-scm.com/doc)
- [Tutorial Git in italiano](https://git-scm.com/book/it/v2)
- [GitHub Guides](https://guides.github.com/)

Buon lavoro a tutti gli studenti!

---

**Nota:** Questo è un esercitazione pratica. L'obbiettivo principale e imparare ad usare git in modo efficace, quindi non preoccupatevi se fate errori all'inizio. L'importante e` imparare dal processo!


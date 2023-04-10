# infoTeorica 2023
riassunti fatti da [@LLibera](http://t.me/llibera) in data 10 Aprile 2023.
## lezione 1 - introduzione
### Che cos’è un computer?
Vedremo che questa domanda ha più di una risposta
corretta:
- É una macchina di Turing
- É una macchina a registri
- É una funzione ricorsiva
- É un linguaggio di programmazione
`suf cientemente espressivo’

### **Tesi di Church-Turing**
: qualunque problema che un
essere umano può calcolare seguendo un algoritmo
può essere calcolato indifferentemente usando uno di
questi strumenti di calcolo.

### **problemi irrisolvibili**:
- Il programma P andrà in crash?
- La computazione di P fermerà su un dato input?
- Il programma P rispetta la specifica data dalla funzione f?
- I programmi P e P' sono equivalenti?
- **in logica** La formula del prim'ordine $\phi$ è soddisfacibile?
- **in algebra**:
  - Quando due parole rappresentano lo stesso elemento di un gruppo (Word problem)
  - Un'equazione diofantina data ha soluzioni intere?
- **In interior design(!)** Possiamo usare un dato insieme di piastrelle per coprire una qualsiasi area quadrata?

## Lezione 2 - La macchina di Turing
La domanda di Turing?
Che cos’è una computazione?
Che cosa signi ca per un problema essere calcolabile?

Osserviamo come un
essere umano esegue
una computazione.
Segue un insieme di **regole**.
- Vengono letti e scritti dei **simboli** (su un supporto, ad
esempio un foglio di carta).
- L’azione eseguita dalla persona dipende dal simbolo
che viene esaminato.

Il metodo di Turing ha precedenti illustri, e più
essere riassunto come il tentativo di identi care le
proprietà essenziali del processo di computazione,
a discapito di ciò che invece è irrilevante.
Reminder:
- la geometria
- Aristotele:  Essenziale Vs Accidentale

### macchina di Turing: definizione **in**formale

Astraiamo i dati:
- moltiplicazione in colonna &rarr; rappresentazione su una riga &rarr; sequenza binaria

Astraiamo le azioni:
- Scrivi il simbolo 0
- Scrivi il simbolo 1
- Spostati una cella verso destra
- Spostati una cella verso sinistra
- Osserva il simbolo corrente e scegli il
prossimo passo di conseguenza.
- Fermati.

definizione informale:
- Una macchina di Turing ha un **nastro**, infinito sul lato destro. Il
nastro è diviso in **celle**.
- Ogni cella del nastro può contenere un simbolo o essere vuota.
- Una macchina di Turing ha una **testina** che si muove sul nastro.
La testina è sempre in un certo **stato**.
- Una **configurazione** è una `istantanea' di un passo di
computazione della macchina.
- La **configurazione iniziale** vede la testina posiziona nella prima
cella di sinistra, nello stato iniziale $q_0$. Il nastro é vuoto, ad
eccezione di una stringa di input $a = a_1 a_2 … a_m$ che va ad
occupare le prime m celle.

Supponiamo che la macchina si trovi in una configurazione data.
Come decide il prossimo passo di computazione?
- La testina legge il contenuto della cella, e sulla base della lettura la
macchina può compiere una delle seguenti azioni:
  - **Fermarsi**.
  - **Cambiare stato**, **scrivere** un nuovo simbolo nella cella corrente (o lasciarla vuota), e **spostarsi** nella cella immediatamente a
sinistra o a destra dell’attuale.
- Il tipo di azione da prendere è dettato dal **programma** della
macchina.

### MT: definizione formale

Una macchina di Turing è una tupla $⟨ \Sigma, Q, q_0, H, \delta ⟩$
- $\Sigma$ é un **alfabeto** finito di simboli, che include un simbolo speciale ⊔ che indica una cella vuota.
- $Q$ é un insieme finito di **stati**.
- $q_0 \in Q$ é lo **stato iniziale**.
- $H \sube Q$ é l’insieme degli stati accettanti (o nali).
- $\delta$ é la **funzione di transizione** (ed è una funzione) **totale**
$$\delta : (Q \setminus H) \times \Sigma \rightarrow Q \times \Sigma \times \{ \rightarrow , \leftarrow \}$$

guarda le slide [Lezione2-21 Febbraio.pdf](../Lezione2-21%20Febbraio.pdf) per ulteriori immagini.

## Lezione 3 - 
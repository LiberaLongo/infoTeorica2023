# infoTeorica 2023
riassunti fatti da [@LLibera](http://t.me/llibera) in data 10 Aprile 2023.
## lezione 1 - introduzione

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
### MT: definizione formale

Una macchina di Turing è una tupla $⟨ \Sigma, Q, q_0, H, \delta ⟩$
- $\Sigma$ é un **alfabeto** finito di simboli, che include un simbolo speciale ⊔ che indica una cella vuota.
- $Q$ é un insieme finito di **stati**.
- $q_0 \in Q$ é lo **stato iniziale**.
- $H \sube Q$ é l’insieme degli stati accettanti (o nali).
- $\delta$ é la **funzione di transizione** ed è **totale**
$$\delta : (Q \setminus H) \times \Sigma \rightarrow Q \times \Sigma \times \{ \rightarrow , \leftarrow \}$$

guarda le slide [Lezione2-21 Febbraio.pdf](../Lezione2-21%20Febbraio.pdf) per ulteriori immagini.

## Lezione 3 - 
# Trasformata Z

La **Trasformata $Z$** è uno strumento fondamentale nell'analisi e nella sintesi dei sistemi a segnali campionati. Svolge un ruolo **analogo** alla Trasformata di Laplace nei sistemi a tempo continuo.

---

## Definizione e Ruolo

La Trasformata $Z$ di una sequenza di campioni $\{x_k\}$ di un segnale $x(t)$ (dove $t_k = k T_c$) è definita come:

$$
Z\{x_k\} = X(z) = \sum_{k=0}^{\infty} x(k T_c) z^{-k}
$$

dove $z$ è una variabile complessa.

---

## Relazione con la Trasformata di Laplace (Mapping $S$ al piano $Z$)

La Z-trasformata può essere ottenuta dalla Trasformata di Laplace tramite la sostituzione:

$$
z = e^{s T_c}
$$

>[!NOTE]
>La trasformata $Z$ non si porta a presso il modulo, il che vuol dire che non è perfetta come trasfomata ma si avvicina molto.

dove $T_c$ è il tempo di campionamento. Questa trasformazione mette in corrispondenza i punti del piano $S$ (Laplace) con quelli del piano $Z$.

### Principali corrispondenze:

- L'**asse immaginario** del piano $S$ (poli che indicano oscillazioni permanenti) viene proiettato sulla **circonferenza di raggio unitario** nel piano $Z$.
- L'intero **semi-piano sinistro** del piano $S$ (poli stabili) viene proiettato **all'interno** del cerchio di raggio unitario nel piano $Z$.
- Il semi-piano destro del piano $S$ (instabilità) viene proiettato **all'esterno** del cerchio unitario nel piano $Z$.

---

## Stabilità dei Sistemi Discreti

La posizione dei poli della Z-trasformata nel piano $Z$ determina la **stabilità** di un sistema discreto:

- Un sistema discreto è **asintoticamente stabile** se tutti i suoi poli si trovano **all'interno del cerchio di raggio unitario**.
- Se un polo si colloca **sulla circonferenza unitaria**, il sistema è al limite di stabilità (segnali stazionari).
- Se un polo si colloca **all'esterno della circonferenza unitaria**, il sistema è **instabile**.

La circonferenza unitaria funge da spartiacque tra stabilità e instabilità nei sistemi discreti.

---

## Funzione di Trasferimento Discreta

La Trasformata $Z$ permette di definire la **funzione di trasferimento discreta** $G(z)$, che lega la Z-trasformata dell'ingresso campionato $U(z)$ a quella dell'uscita campionata $Y(z)$ tramite la **somma di convoluzione**:

$$
Y(z) = G(z) U(z)
$$

La funzione $G(z)$ svolge lo stesso ruolo della funzione $G(s)$ nei sistemi continui.

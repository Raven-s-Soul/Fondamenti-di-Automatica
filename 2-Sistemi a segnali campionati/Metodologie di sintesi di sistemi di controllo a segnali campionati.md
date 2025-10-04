# Metodologie di sintesi di sistemi di controllo a segnali campionati

Le metodologie di sintesi per le leggi di controllo discrete $M(z)$ si suddividono in due approcci principali:

1. **Sintesi nel Continuo** (discretizzazione di un controllore continuo)
2. **Sintesi nel Discreto** (sintesi diretta)

---

## 1. Sintesi nel Continuo (Discretizzazione di Sistemi Continui)

- Si progetta prima un controllore continuo $R(s)$.
- Si converte successivamente in una funzione discreta $M(z)$.
- Applicabile quando la **frequenza di campionamento è elevata** rispetto alle frequenze del sistema ($\omega_c \gg \omega_{max}$).

### A. Trasformazione Esatta (Discretizzazione della Risposta Impulsiva)

- Conserva i campioni della risposta impulsiva originale: $g(k T_c) = g(t)$ agli istanti $t = k T_c$.
- Procedura:
  1. Calcolare $g(t)$ (antitrasformata di $G(s)$).
  2. Campionare: $\{ g(k T_c) \}$.
  3. Calcolare la Z-trasformata: $G(z)$.
- **Limite:** Non preserva esattamente la risposta al gradino.
- Variante pratica: includere l’**Organo di Tenuta ZOH**, trasformando $T(s)G(s)$.

### B. Metodi Approssimati ($s \to z$)

1. **Differenze all’indietro (Backward Difference):**
   $$\\
   s \approx \frac{1 - z^{-1}}{T_c}
   $$
   - Stabile: mappa poli stabili di $S$ all’interno del cerchio unitario in $Z$.

2. **Differenze in avanti (Forward Difference):**
   $$\\
   s \approx \frac{z - 1}{T_c}
   $$
   - Sconsigliato: poli stabili in $S$ possono diventare instabili in $Z$.

3. **Trasformazione bilineare (Tustin):**
   $$\\
   s \approx \frac{2}{T_c} \frac{z - 1}{z + 1}
   $$
   - Mantiene la stabilità.
   - Può introdurre distorsioni alle alte frequenze (**prewarping** per compensazione).

### C. Regolatore PID Discreto

- **Integrale:** sommatoria dei campioni dell’errore:
  $$\\
  E_{tot} = E_{old} + \Delta t \cdot e((N+1)\Delta t)
  $$
- **Derivata:** differenza tra campioni consecutivi divisa per $\Delta t$:
  $$\\
  \frac{d e}{dt} \approx \frac{e((N+1)\Delta t) - e(N\Delta t)}{\Delta t}
  $$

---

## 2. Sintesi nel Discreto (Sintesi Diretta)

- Operazione direttamente nel dominio $Z$.
- Basata su una funzione a ciclo chiuso desiderata $W^*(z)$ (**Assegnamento del Modello / Metodo di Ragazzini**).


### Condizioni di Realizzabilità

1. **Causalità:** grado del denominatore $\ge$ grado numeratore.
2. **Stabilità:** tutti i poli di $W^*(z)$ all’interno del cerchio unitario.
3. **Non Cancellazione di Poli Instabili:** evitare poli o zeri di $G(z)$ instabili.

### A. Sistemi a Tempo di Assestamento Finito (Deadbeat Control)

- Obiettivo: annullare l’errore in un numero finito di campioni.
- Scegliendo:
  $$\\
  W^*(z) = z^{-n}
  $$
- Problema pratico:
  - L’errore si annulla solo agli istanti di campionamento.
  - Il segnale continuo può avere **oscillazioni nascoste** tra i campioni, soprattutto se si cancellano poli poco smorzati.
- Soluzioni:
  - Scegliere un modello di riferimento meno aggressivo.
  - Evitare cancellazioni pericolose.
  - Ridurre il tempo di campionamento.

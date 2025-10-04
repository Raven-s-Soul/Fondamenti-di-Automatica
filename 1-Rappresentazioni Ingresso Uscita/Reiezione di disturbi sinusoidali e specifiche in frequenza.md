# Reiezione di disturbi sinusoidali e specifiche in frequenza

## 1. Obiettivo della Reiezione

Uno degli scopi fondamentali di un sistema a controreazione è **rigettare i disturbi**.  
La reiezione si concentra sulla capacità di limitare l'effetto dei disturbi sull'uscita, specialmente quando il disturbo è un segnale periodico (sinusoidale) o un segnale aleatorio collocato in un certo intervallo di frequenze.  

Esempi comuni includono:  
- Riduzione dell'effetto del vento su un'antenna  
- Riduzione delle onde su una nave

---

## 2. Analisi in Frequenza

Per valutare l'effetto di un disturbo sinusoidale $Z(s)$ sull'uscita $Y(s)$, si utilizza l'**analisi nel dominio della frequenza**, che rientra nelle specifiche in frequenza.  

In un sistema a controreazione, l'uscita dovuta al disturbo $Y_{fc}(s)$ è legata al disturbo stesso dalla funzione di trasferimento del ciclo chiuso tra $Z(s)$ e $Y(s)$:

$$
W_Z(s) = \frac{G_2(s)}{1 + F(s)}
$$

dove:  
- $F(s)$ è la funzione di anello aperto  
- $G_2(s)$ è la funzione di trasferimento tra il punto di ingresso del disturbo e l'uscita

---

## 3. Vantaggio della Controreazione

Senza controreazione, il disturbo $Z(s)$ raggiungerebbe l'uscita attraverso la catena diretta.  
Con la controreazione, il rapporto tra l'uscita controllata e l'uscita senza controllo in termini di disturbo è:

$$
\frac{Y_{fc}(s)}{Y_{fo}(s)} = \frac{1}{1 + F(s)}
$$

Questo rapporto mostra che l'effetto del disturbo è ridotto dal **termine sensibilità complementare**:

$$
S^Y(s) = \frac{1}{1 + F(s)}
$$

---

## 4. Specifiche e Alto Guadagno

Per soddisfare una specifica che richiede che la controreazione riduca l'effetto del disturbo di un fattore $k$ (o più) entro un determinato range di pulsazioni $(\omega_1 < \omega < \omega_2)$, è necessario che il modulo della funzione di anello aperto $|F(j\omega)|$ sia sufficientemente elevato (**alto guadagno**) in quel range.

La condizione richiesta si traduce in:

$$
|F(j\omega)| > k \quad \text{per} \quad \omega_1 < \omega < \omega_2
$$

Questo requisito definisce una **finestra proibita** (o regione vietata) sul diagramma di Bode, al di sotto della quale il modulo di $F(j\omega)$ non deve scendere nel range di frequenze specificato.

# Errore di riproduzione di una sinusoide e specifiche in frequenza

L'**errore di riproduzione di una sinusoide** in un sistema di controllo a controreazione si riferisce al comportamento in **regime permanente sinusoidale**, ovvero quando l'ingresso di riferimento è un segnale armonico.  
Questo tipo di analisi rientra nelle **specifiche in frequenza** per la risposta del sistema.

---

## Calcolo dell'Errore

In un sistema a controreazione, la funzione di trasferimento che lega l'ingresso di riferimento $U(s)$ all'errore $E(s)$ è data da:

$$
W_e(s) = \frac{K_d}{K_d + F(s)}
$$

dove:  
- $F(s)$ è la funzione di anello aperto (inclusi controllore e processo)  
- $K_d$ è la costante di proporzionalità tra ingresso e uscita desiderata a regime

Per un ingresso sinusoidale di pulsazione $\omega$, l'**ampiezza dell'errore a regime** $|E(j\omega)|$ è determinata dal modulo della funzione di errore valutata in $s = j\omega$.

---

## Specifiche e Minimizzazione dell'Errore

Per garantire una riproduzione fedele della sinusoide, è necessario mantenere l'errore $|E(j\omega)|$ il più piccolo possibile per le frequenze di interesse.

- Se il guadagno del loop $|F(j\omega)|$ è sufficientemente elevato (**alto guadagno di anello**), il denominatore $K_d + F(j\omega)$ è dominato da $F(j\omega)$.  
- In questa condizione, il modulo dell'errore si approssima a:

$$
|E(j\omega)| \approx \frac{K_d}{|F(j\omega)|}
$$

Per soddisfare una specifica che impone che l'errore di riproduzione di una sinusoide sia inferiore a un certo limite $\epsilon$ fino a una data pulsazione $\omega_{max}$, la funzione di anello aperto $|F(j\omega)|$ deve essere sufficientemente alta in quel range di frequenze.

Questo requisito definisce una **finestra proibita** sul diagramma di Bode, al di sotto della quale il modulo di $F(j\omega)$ non deve scendere nel range di frequenze specificato.

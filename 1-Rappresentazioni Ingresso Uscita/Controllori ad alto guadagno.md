# Controllori ad Alto Guadagno

I controllori ad alto guadagno di anello sono una strategia di controllo impiegata quando la stabilità del ciclo chiuso lo consente, portando a notevoli benefici in termini di prestazioni.

---

## Vantaggi principali

Un aumento del guadagno di anello può produrre effetti molto positivi su un sistema di controllo:

1. **Riduzione dell'errore a regime**  
   Negli schemi di controllo con segnali di ingresso polinomiali, l'errore in uscita si riduce all'aumentare del guadagno di anello.

2. **Reiezione dei disturbi**  
   L'ampiezza dei disturbi, siano essi costanti (di tipo $k$) o aleatori collocati in un particolare intervallo di frequenza, diminuisce all'aumentare del guadagno.

3. **Aumento della banda passante**  
   Un aumento del guadagno del ciclo aperto sposta la pulsazione di taglio ($\omega_t$) verso destra, portando a un aumento della banda passante a -3 dB ($\omega_{-3}$).

4. **Riduzione della sensibilità parametrica (robustezza)**  
   La controreazione ad alto guadagno rende l'influenza delle variazioni parametriche sul ciclo chiuso molto ridotta (come analizzato con la funzione di sensibilità).

5. **Proprietà linearizzante**  
   Su sistemi statici o dinamici non lineari, una controreazione ad alto guadagno può rendere la relazione ingresso–uscita più lineare di quella di partenza.

---

## Effetto sulla funzione di trasferimento a ciclo chiuso

- Se il guadagno in frequenza del ciclo aperto $|G(j\omega)|$ è elevato, il modulo della funzione di trasferimento a ciclo chiuso $|W(j\omega)|$ tende a ridursi al guadagno della retroazione $K_d$.  
- Il ciclo chiuso, quindi, assume la forma dell'inverso della funzione di trasferimento di controreazione, indipendentemente dall'andamento del ciclo aperto.  
- Se la funzione di trasferimento in catena diretta $G(s)$ presenta degli integratori (poli in zero), non è necessario aumentare il guadagno $K_G$, poiché il guadagno statico del sistema a ciclo chiuso tende già a $K_d$.

---

## Applicazioni

Esempi classici di applicazione del controllo ad alto guadagno includono:

- Circuiti di amplificazione (es. amplificatore operazionale in configurazione non invertente, che ha un guadagno prefissato determinato solo dai componenti di retroazione).  
- Strumenti di misura ad alta precisione, come la **bilancia a compensazione elettromagnetica**.

---

## Limitazioni

- Un eccessivo aumento del guadagno di anello può spostare $\omega_t$ verso destra e, per sistemi la cui fase si avvicina o scende sotto i $-180^\circ$, portare all'instabilità.  
- Quando si sfrutta l’effetto linearizzante dell’alto guadagno, bisogna assicurarsi che le dinamiche del modello di partenza che vengono “cancellate” non generino instabilità interna.

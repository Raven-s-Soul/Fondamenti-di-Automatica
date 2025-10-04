# Carta di Nichols

La **Carta di Nichols** (o **Diagramma di Nichols**) è uno strumento grafico utilizzato nell’analisi dei sistemi di controllo per rappresentare la risposta armonica.  
Si tratta di una rappresentazione cartesiana che combina **modulo** e **fase** della funzione di trasferimento ad anello aperto $F(j\omega)$ in un unico grafico.

---

## Struttura del grafico

- **Assi del grafico**  
  - Asse delle ascisse: fase (in gradi o radianti).  
  - Asse delle ordinate: modulo (in decibel, dB) di $F(j\omega)$.  

- **Tracciamento**  
  Si traccia la risposta armonica $F(j\omega)$ della funzione di anello aperto, variando $\omega$ da $0$ a $+\infty$.

---

## Costruzione e griglia

La Carta di Nichols non rappresenta solo la risposta armonica ad anello aperto, ma include anche una **griglia** formata da curve di modulo e fase costanti, relative alla funzione di trasferimento a ciclo chiuso $W(j\omega)$:

1. **Luoghi di moduli costanti di $W(j\omega)$**  
   Curve che mostrano dove il modulo di $W(j\omega)$ è costante (fase variabile).

2. **Luoghi di fasi costanti di $W(j\omega)$**  
   Curve che mostrano dove la fase di $W(j\omega)$ è costante (modulo variabile).

Il **centro ideale della griglia** si trova nel punto:  
$(0 \, \text{dB}, -180^\circ)$

---

## Utilità e vantaggi

La Carta di Nichols è uno strumento efficace per l’**analisi** e la **sintesi** dei sistemi di controllo, poiché evidenzia le relazioni tra ciclo aperto e ciclo chiuso.  
In particolare, consente di:

### 1. Lettura dei margini di stabilità
- **Margine di fase ($m_\phi$)**  
  Distanza tra il punto $(0 \, \text{dB}, -180^\circ)$ e il punto del grafico in cui il modulo di $F(j\omega)$ vale $0 \, \text{dB}$.
- **Margine di guadagno ($m_g$)**  
  Distanza tra il punto $(0 \, \text{dB}, -180^\circ)$ e il punto in cui la fase è $-180^\circ$.

### 2. Modulo alla risonanza ($M_r$)
È possibile individuare il **modulo alla risonanza $M_r$** (massimo valore del modulo di $W(j\omega)$) cercando la curva di modulo costante a ciclo chiuso più grande tangente al grafico della risposta armonica ad anello aperto.

### 3. Legami globali
La carta permette di dedurre **relazioni approssimate** tra:
- Parametri del ciclo aperto ($m_\phi$, $m_g$)  
- Parametri del ciclo chiuso ($M_r$, banda passante $\omega_{-3}$)

---

## Sintesi

La **Carta di Nichols** offre una visione integrata delle prestazioni del sistema in retroazione.  
Rispetto a rappresentazioni separate come i **diagrammi di Bode**, consente di:
- Valutare direttamente l’influenza del ciclo aperto sul ciclo chiuso.  
- Semplificare la progettazione evidenziando margini di stabilità, robustezza e prestazioni in frequenza.

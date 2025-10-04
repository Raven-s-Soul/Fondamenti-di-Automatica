# Struttura di un sistema di controllo a segnali campionati

La struttura di un sistema di controllo a segnali campionati (o **sistema di controllo digitale**) è tipicamente uno **schema misto**, che combina componenti a tempo continuo, a tempo discreto e convertitori.

Questo sistema si basa sull'utilizzo di un **microprocessore ($\mu P$)** o **microcontrollore ($\mu C$)** per implementare la legge di controllo, poiché questi dispositivi accettano e generano solo segnali di tipo binario/digitale.

---

## Componenti principali

I componenti principali lungo l'anello di controllo sono:

1. **Processo e Attuatore (Analogici)**  
   Il sistema da controllare e l'attuatore ricevono e producono segnali analogici.

2. **Convertitore Analogico/Digitale (A/D)**  
   Accetta il segnale analogico in uscita dal processo (spesso dopo un filtro anti-aliasing) e lo trasforma in un segnale digitale tramite **campionamento** (conversione da tempo continuo a tempo discreto).

3. **Controllore Digitale ($\mu P$ / $\mu C$)**  
   Esegue l'algoritmo di controllo sulla base del segnale campionato e del riferimento, generando un comando di controllo in formato digitale.

4. **Convertitore Digitale/Analogico (D/A)**  
   Accetta il segnale digitale e lo converte in un segnale analogico (operazione di **ricostruzione** o **tenuta**) per pilotare l'attuatore.  
   Spesso include un **Organo di Tenuta di Ordine Zero (ZOH)**.

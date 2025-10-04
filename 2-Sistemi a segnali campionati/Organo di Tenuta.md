# Organo di Tenuta

L'**Organo di Tenuta (ZOH, Zero Order Hold)** è un elemento fondamentale nella **struttura di un sistema di controllo a segnali campionati** (o sistema di controllo digitale).  
Ha il compito di convertire il **segnale digitale** (a tempo discreto), generato dal controllore, in un **segnale analogico** (a tempo continuo).

---

## Funzionamento e Segnale

- L'Organo di Tenuta realizza la **ricostruzione** del segnale.  
- È l'approssimazione più semplice utilizzata in pratica, poiché il ricostruttore ideale di Shannon non è fisicamente realizzabile.  
- Il ZOH prende il valore del campione $x(kT_c)$ e lo mantiene **costante** per tutto l'intervallo di campionamento $T_c$, producendo un segnale in uscita a **gradinata (stair-step)**.

---

## Caratteristiche e Impatto sul Sistema

- La funzione di trasferimento dell'Organo di Tenuta è:

$$
T(s) = \frac{1 - e^{-sT_c}}{s}
$$

- L'operazione di tenuta introduce intrinsecamente un **ritardo** nel segnale ricostruito rispetto al segnale analogico originale.  
- Questo ritardo, approssimabile come $\frac{T_c/2}{1 + sT_c/2}$ per basse frequenze, si traduce in una **perdita consistente del margine di fase** del sistema in ciclo chiuso, specialmente quando ci si avvicina alla frequenza di Nyquist ($\omega_c/2$).

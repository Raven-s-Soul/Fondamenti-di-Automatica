# Scelta del tempo di campionamento

La scelta del tempo di campionamento è un aspetto cruciale nell'analisi dei sistemi di controllo a segnali campionati.

## 1. Condizione Teorica: Teorema del Campionamento (Shannon)

La condizione fondamentale per un **campionamento corretto** è stabilita dal **Teorema del campionamento** (o di Shannon).  

- La pulsazione di campionamento $\omega_c = 2\pi/T_c$ deve essere almeno il doppio della massima pulsazione presente nello spettro del segnale $\omega_{\text{max}}$:
  
  $$\\
  \omega_c > 2 \, \omega_{\text{max}}
  $$

- La frequenza $f_c/2$ è definita **frequenza di Nyquist**.  
- Se questa condizione non è rispettata, si verifica il fenomeno di **aliasing**, che distorce il contenuto informativo del segnale.

## 2. Considerazioni Pratiche

Nella pratica, è necessario considerare anche gli effetti del **ZOH (organo di tenuta di ordine zero)**:

- Il ZOH introduce:
  - un **ritardo** tra il campione digitale e il segnale analogico ricostruito;
  - una **perdita di fase**, che può ridurre i margini di stabilità del sistema.

- Per compensare questi effetti, si suggerisce una pulsazione di campionamento più elevata:

  $$\\
  \omega_c \gtrsim 10 \, \omega_{\text{max}}
  $$

- Vantaggi di una frequenza di campionamento elevata:
  1. Riduce la perdita di margine di fase introdotta dal ZOH.
  2. Minimizza oscillazioni indesiderate o **sovraelongazioni** nella risposta del sistema.
  3. Migliora la fedeltà della riproduzione del segnale continuo.

---

In sintesi, il tempo di campionamento deve essere scelto **non solo per soddisfare il criterio di Nyquist**, ma anche per compensare gli effetti pratici del ZOH e preservare la stabilità e le prestazioni del sistema discreto.

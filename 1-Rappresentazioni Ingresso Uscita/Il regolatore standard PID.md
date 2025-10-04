# Il regolatore standard PID
<aside>

>$K_P$ Proporzionale, influenza i moduli ma non la fase, può spostare verso destra la $\omega_t$ omega di taglio e ridurre il $m_\phi$ margine di fase e $m_g$ margine di guadagno.

</aside>

<aside>

>$K_I$ Integrale, rigetta disturbi costanti e errore a regime per ingressi costanti, ma comporta spesso problemi di stabilità, a causa di aggiungere uno sfasamento di $-90\degree$ nelle fasi, infine windup (sovraccarica-mento) nel cambiamento della variabile controllata.

</aside>

<aside>

>$K_D$ Derivata, anticipo rispetto alle variazioni dell’errore, aggiunge 1 zero a numeratore e quindi migliorare i margini di fase, aumenta l’omega di taglio e la banda passante.
>Minore tempo nel *rising time* e un sistema *più pronto*.
>Può amplificare l’errore nel segnale di misura specialmente ad alte frequenze, risposta instabile o a oscillazioni indesiderate.

</aside>

$$
PID(s)= K_P (1+\frac 1 {T_Is} + T_D s) = K_P \frac {T_I T_D s^2 + T_I s +1}{T_Is}
$$

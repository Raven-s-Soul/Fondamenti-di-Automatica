# Sistemi a fase non minima

- Nello studio della frequenza
- in sistemi con zeri a parte reale positiva.

<aside>

>I sistemi a fase minima sono quelli dove ogni zero e ogni polo hanno parte reale negativa.

>Se la parte reale positiva è tra i poli allora abbiamo sicuramente un sistema instabile.

</aside>

Prendo ad esempio un sistema a controreazione che ha soltanto $K_c$ e $F(s)$ in catena diretta.

$$
W(s)=\frac{K_cF(s)}{1+K_cF(s)}
$$

Separo la $F(s)$  in numeratore e divisore, quindi mi diventa:

$$
W(s)=\frac{K_cN(s)}{D(s)+K_cN(s)}
$$

Immaginiamo che questo sistema sia a fase non minima e che quindi abbia uno zero a parte reale positiva. 

Noto che, se aumento molto $K_c$, $N(s)$ diventerà prevalente nel denominatore della $W(s)$ e quindi le sue radici diventeranno i poli del sistema. In questo modo lo zero a parte reale positiva diventerebbe un polo del sistema.

Se invece il guadagno rimane prossimo allo 0 allora possiamo stare tranquilli perché $N(s)$ al denominatore avrà poca importanza.

Per questo motivo, se il sistema è a fase non minima, dobbiamo stare attenti ad alzare troppo il guadagno.

***
>[!IMPORTANT]
>I sistemi a fase non minima, hanno uno zero a parte reale positiva e graficamente partono a un valore negativo, cioe all inizio sembra che vadano nella direzione opposta a quella che si aspettava.

# Luogo delle radici

$$
\begin{gather}
W(s) = \frac {k P(s)}{1+ kP(s)} \\ \space \\
P(s) = \frac {N(s)}{D(s)} \quad \frac {\text {Zeri della funzione di trasferimento} }{\text {Poli della funzione di trasferimento}} \\ 
\space \\
W(s) = \frac {k \frac{N(s)}{D(s)}}{1+ k \frac {N(s)}{D(s)}} \\
\space \\
W(s) = \frac {k N(s)}{D(s)+ k N(s)}
\end{gather}
$$

Studio il denominatore in base a valore di k.

> 1+F(s): Nel variare kc da -inf a +inf, le radici dell'equazione caratteristica  descriveranno una curva nel piano s detta luogo delle radici:
> 
>per kc>0  → è detto luogo positivo
>
>per kc<0  → è detto luogo negativo
>
>per kc=0  → non è considerato perché si ha assenza di controreazione
> 

>[!TIP]
>### Criterio di Routh-Hurwitz
>
>- Condizione necessaria: tutti i coefficienti siano positivi.
>- Equazione diff di 2nd grado è sufficiente.
>- evitiamo i passaggi…
>
>*Per la stabilità, poli a parte reale negativi.*

>[!NOTE]
>### Luogo delle radici e proprietà
>
>Curva nel piano s
>
>- Rami quanti sono i poli della funzione di trasferimento a ciclo aperto KcF(s), si sovrappongono in caso di molteplice cardinalità. Ogni ramo ha un polo di F(s) e termina in uno 0 di F(s) o all infinito(Asintoto).
>- Simmetrico rispetto all’asse reale.
>- Se la costante Kc è positiva, un punto dell asse reale appartiene al luogo delle radici positivo se si lascia alla sua destra un numero dispari di zeri e poli. Se Kc è negativo, un punto dell asse reale appartiene al luogo delle radici negativo se si lascia alla sua destra un numero pari di zeri e poli
>- Gli asintoti formano una stella di raggi con centro nel punto dell’asse reale delle ascisse.
>    - estensioni e formule di quest ultima

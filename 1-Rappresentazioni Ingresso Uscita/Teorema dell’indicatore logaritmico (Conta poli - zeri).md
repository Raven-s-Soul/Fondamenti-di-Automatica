# Teorema dell’indicatore logaritmico (Conta poli - zeri)
Prendiamo una funzione del tipo $F(s)=\frac{s-a}{s-b}$, che ha un polo in $b$ e uno zero in $a$.

Immaginiamo di avere una curva chiusa C sul piano di Gauss e di applicare la funzione $F(s)$ su ognuno dei punti della curva.

Applichiamo $F(s)$ a tutti gli $s$ appartenenti alla curva C scrivendo $F(C)$, che sarà anch’essa una curva chiusa. Vogliamo sapere quante volte la curva $F(C)$ ruota intorno all’origine.

Notiamo che numeratore ($s-a$) e denominatore ($s-b$) di $F(s)$ non sono che i vettori 

$$
∠^{F(s)}=∠^{\frac{s-a}{s-b}}=∠^{s-a}-∠^{s-b}
$$

Ipotizziamo che $a$ si trovi all’interno della curva:

> una qualsiasi curva chiusa :D

<aside>

>Se una radice sta sulla curva allora la fase di quel vettore farà un salto di 180°

</aside>

Notiamo che il numero di rotazioni intorno all’origine dipende da $a$, visto che il vettore $\overrightarrow{as}$ è l’unico che compie rotazioni complete (l’altro oscilla semplicemente).

Se dentro alla curva c’è un polo girerà in una direzione opposta a quella di uno zero, quindi si annullano.

Vediamo alla fine che il numero di rotazioni della funzione $F(s)$ intorno a 0 è:

$$
R_{F_\gamma,0}=\text{zeri}[F(s)]^\gamma-\text{poli}[F(s)]^\gamma
$$

> Se il punto è dentro la curva vale qualcosa, se sta fuori lo ignoriamo
> 

$$
∠^ {M(s)} = ∠^ {s-a} - ∠^ {s-b}
$$

$$
\text {Rotazioni }\to R_{F_{\gamma},0}= \@ Zeri_\gamma - \@Poli_\gamma
\\ \space \\
R_{F_{\gamma},0} \geq 0 \to \text {Orarie  }\\
R_{F_{\gamma},0} < 0 \to \text {Anti-orarie}
$$

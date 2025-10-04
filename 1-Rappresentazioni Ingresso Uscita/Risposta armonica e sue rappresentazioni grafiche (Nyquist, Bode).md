# Risposta armonica e sue rappresentazioni grafiche

$u(t)=\sin(\omega t)$ che trasformato diventa $\frac{\omega}{s^2+\omega^2}$.

$$
\text{Alternativa con l'uscita permanente:} \quad y_p(t) = y(t) - y_t(t)
$$

$$
Y(s)=G(s)\cdot\frac{\omega}{s^2+\omega^2}=\frac{R}{s-j\omega}+\frac{R^*}{s+j\omega}\space+\space\sum\frac{R_i}{s-p_i}
$$

Ipotizziamo che $G(s)$ sia stabile e che quindi le sue componenti esponenziali (i residui con $p_i$) vadano a 0. Quello che ci rimane sono i residui dovuti all’ingresso sinusoidale, 

Questo ci dimostra che un ingresso sinusoidale causa sicuramente un’uscita sinusoidale.

Vado a cercare quanto valgono i residui dovuti all’ingresso sinusoidale, cioè $R^*$ nel polo $-j\omega$ e $R$ nel polo $j\omega$

$$
\begin{gather}
R_{j\omega}=\lim_{s\rightarrow j\omega}(s-j\omega)Y(s)=\lim_{s\rightarrow j\omega}(s-j\omega)G(s)\frac{\omega}{(s+j\omega)(s-j\omega)}=\frac{G(j\omega)}{2j}
\\\ \space \\\
R_{-j\omega}=\lim_{s\rightarrow -j\omega}(s+j\omega)Y(s)= \\\ \lim_{s\rightarrow -j\omega}(s+j\omega)G(s)\frac{\omega}{(s+j\omega)(s-j\omega)}= \frac{G(-j\omega)}{-2j} = \frac{G^*(j\omega)}{-2j}
\end{gather}
$$

<aside>

> Più avanti scriveremo $G(j\omega)$ in coordinate polari $|G(j\omega)|e^{j ∠^{ G(j\omega)}}$.

</aside>

Una volta trovati questi possiamo fare l’antitrasformata sfruttando questo:

$$
\frac R{s-p}\Rightarrow Re^{pt}
$$

$$
y_p(t)=\frac{|G(j\omega)|e^{j∠^{ G(j\omega)}}}{2j}e^{j\omega t}-\frac{|G(j\omega)|e^{-j ∠^{ G(j\omega)}}}{2j}e^{-j\omega t}
$$

Ma riconosco che c’è di mezzo un seno, quindi mi diventa:

$$
\begin{gather}
y_p(t)=|G(j\omega)|\sin(\omega t+∠^{ G(j\omega)}) \\\
y_p(t)=|\text{Amplificazione}|\sin(\omega t+ \text{Sfasamento})
\end{gather}
$$

Ora è molto leggibile e si notano le somiglianze tra $y(t)$ e $u(t)$. Entrambi sono segnali sinusoidali con la stessa frequenza, ma $y(t)$ ha un modulo e una fase diversi. Fase e modulo dipendono dalla funzione $G(j\omega)$ e possiamo usare strumenti come Bode o Nyquist per studiare il comportamento di questo tipo di sistemi.

- Bode
    - Si tratta di una coppia di grafici, entrambi hanno $\omega$ sull’asse orizzontale, mentre su quello verticale uno ha il modulo della funzione e l’altro la fase
- Nyquist
    - Si tratta di uno speciale piano di Gauss che traccia modulo e fase della funzione di trasferimento
- Nichols
    - Modulo e fase in un singolo grafico
***
$\phase\theta$ do not render right so i use instead $∠^\theta$

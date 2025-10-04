# Risposta impulsiva

Esempio di funzione:

$$
y^{(n)}+a_{(n-1)} y^{(n-1)} + ... + a_{(0)}y = b_{(0)}u(t)+ ... + b_{(m)}u^m(t) \\
$$

Laplace:

$$
s^nY(s) + CIy^{(n-1)}+ a_{(n-1)}s^{(n-1)} Y(s) + ... = b_{(0)}U(s)+ ... + b_{(m)}s^m U(s)
$$

$$
Y(s) = \frac{(b_m s^m + ... \space + b_o) U(s)}{s^n+a_{n-1} s^{n-1} + ... \space + a_0} + \frac{CIy(s)}{s^n+a_{n-1} s^{n-1} + ... \space + a_0}
$$

Polinomio caratteristico del equazione diff: 

$$
\begin{gather}
Y(t) = \text{Evoluzione libera + Risposta forzata}  \\
Y(t) = \text{Evoluzione libera + Risposta Impulsiva} * u(t)  \\
Y(t) = c_1 e^{at}x_0 + \{ c_2 e^{at}B \} * u(t)
\end{gather}
$$

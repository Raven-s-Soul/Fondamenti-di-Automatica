# Sistemi con ritardo finito

Noto che se una funzione nel tempo subisce un ritardo, allora la sua trasformata di Laplace sarà moltiplicata per un esponenziale.

$$
L_-\{f(t-d)\}=F(s)e^{-ds}
$$

Ne devo fare il Bode, quindi pongo $s=j\omega$.

Vedo che questo esponenziale è puramente complesso e quindi influisce solo sulla fase e non sul modulo.

Il contributo che ha sulla fase è di $-d\omega$, che sarebbe una retta che scende. Su una scala logaritmica come quella del Bode però le rette hanno una forma esponenziale.

***
>[!IMPORTANT]
> Il sistema risponde letteralmente con un ritardo dal punto grafico.

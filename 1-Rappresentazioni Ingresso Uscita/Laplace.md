# Laplace

>[!NOTE]
>### Trasformata
>```math
>L \space \{f(t)\} = \int_{o^-}^{\infty}{f(x) e^{-st} dt} = F(s)
>```

>[!TIP]
>### Anti Trasformata
>```math
>L^{-1}\space = \{ F(s)\} = \frac{1}{2\pi i} \lim_{T \to \infty} \int_{\gamma-iT}^{\gamma+iT} {e^{sT} F(s) ds} = f(t)
>```

>[!CAUTION]
>Ascissa di convergenza
>```math
>\begin{gather}
> s = \sigma + j \omega \\\
>e^{-\sigma t} + e^{- j \omega t} \\\
>\sigma \text{ deve tendere a } \infty \text{ per mandare e}\to 0 \\\
>\text {Nelle trasformate vogliamo che } Re[s] > Re[p] = \sigma \\\
>\text {e che } \sigma \text { sia } \leq 0 \text { per la stabilità} 
>\end{gather}
>```

>[!IMPORTANT]
>*La trasformata di laplace la usiamo per facilitarci i calcoli delle equazioni differenziali, trasformando integrali e derivate in moltiplicazioni e divisione, in questo dominio assestante dal tempo.*

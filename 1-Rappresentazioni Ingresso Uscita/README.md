# Rappresentazioni Ingresso-Uscita

<details>
<summary><h3>Rappresentazione di un sistema</h3></summary>

  
  
</details>



<details>
<summary><h3>Laplace</h3></summary>

>### Trasformata
>```math
>L \space \{f(t)\} = \int_{o^-}^{\infty}{f(x) e^{-st} dt} = F(s)
>```

>### Anti Trasformata
>```math
>L^{-1}\space = \{ F(s)\} = \frac{1}{2\pi i} \lim_{T \to \infty} \int_{\gamma-iT}^{\gamma+iT} {e^{sT} F(s) ds} = f(t)
>```

>Ascissa di convergenza
>```math
>s = \sigma + j \omega 
>```
>```math
>e^{-\sigma t} + e^{- j \omega t}
>```
>```math
>\sigma \text{ deve tendere a } \infty \text{ per mandare e}\to 0 
>```
>```math
>\text {Nelle trasformate vogliamo che } Re[s] > Re[p] = \sigma \\
>```
>```math
>\text {e che } \sigma \text { sia } \leq 0 \text { per la stabilità}
>```



  
</details>

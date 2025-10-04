# Rappresentazione di un sistema

### Semplice
>![SistemaBase](img/SistemaBase.svg)
>- u = entrata
>- y = uscita

### Guadagno
>![SistemaGuadagno](img/SistemaGuadagno.svg)
>- Kd = Controllore o guadagno o proporzionale
>```math
>y(t) = Kd * f * u(t)
>```

### FeedForward
>![SistemaFeedForward](img/SistemaFeedForward.svg)
>- Richiede che si da per certi di non avere disturbi
>```math
>\begin{aligned}
>y(t) = (u(t)( 1 \text{ FeedForward} + Kd)) * f \\\
>y(t) = (u(t) * \text{ FeedForward} + u(t)*Kd)) * f
>\end{aligned}
>```
### Feedback
>![SistemaFeedback](img/SistemaFeedback.svg)
>
>```math
>\begin{aligned}
>\text {Senza trasduttore} \to \frac{f}{1+f} \\\
>\text {Con trasduttore} \frac {1}{Kd} \to \frac{f}{1+f \frac 1 {Kg}} 
>\end{aligned}
>```
### Esempio di sistemi complessi
>![SistemaComplex](img/SistemaComplex.svg)

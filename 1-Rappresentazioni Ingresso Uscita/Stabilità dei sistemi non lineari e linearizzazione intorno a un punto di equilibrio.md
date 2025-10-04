# Stabilità dei sistemi non lineari e linearizzazione intorno a un punto di equilibrio
L'analisi di Lyapunov si concentra sulla stabilità di uno **stato di equilibrio** ($x_e$). Un sistema non lineare è stabile se, in assenza di ingresso (o con ingresso nullo), esiste almeno uno stato $x_e$  in cui la sua derivata è zero (cioè $\dot{x}_e = 0$)

**Criterio di Stabilità di Lyapunov**

Se la funzione di Lyapunov $V(x)$

- È **definita positiva** nell'intorno del punto di equilibrio $x_e$
- La sua derivata prima $\dot{V}(x)$ risulta **definita negativa** nell'intorno di $x_e$ (cioè $\dot{V}(x) < 0$), allora il punto $x_e$ è **localmente asintoticamente stabile**
- Se la derivata prima $\dot{V}(x)$ risulta **semi-definita negativa** (cioè $\dot{V}(x) \leq 0$), allora il punto $x_e$ è **localmente stabile**

Se queste condizioni valgono su tutto lo spazio $R^n$ e la funzione $V(x)$ è illimitata radialmente, la stabilità vale in senso globale

Jacobiana, matrice delle derivate parziali dei componenti
Utilizzo di Taylor

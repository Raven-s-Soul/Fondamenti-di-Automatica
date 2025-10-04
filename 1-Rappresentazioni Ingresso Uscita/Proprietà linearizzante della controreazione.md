# Proprietà Linearizzante della Controreazione

La **proprietà linearizzante della controreazione** è un concetto fondamentale nel controllo automatico, strettamente correlato all'uso di un **alto guadagno di anello**.  
Questa proprietà si riferisce alla capacità di un anello di controreazione di rendere la relazione ingresso-uscita di un sistema, sia esso statico o dinamico, più lineare rispetto alla sua caratteristica originale.

---

## Meccanismo di Linearizzazione

L'effetto linearizzante si manifesta quando il guadagno $K$ nell'anello di controreazione è molto elevato.

### 1. Sistemi Statici

Se si considera un sistema statico con una caratteristica non lineare (ad esempio una funzione cubica più un termine lineare) e lo si chiude in controreazione con un guadagno $K$ molto alto, la caratteristica ingresso-uscita del sistema a ciclo chiuso tende a una **relazione lineare semplice**.  

Ad esempio, il risultato finale può essere $y = x$, dove $x$ è il nuovo ingresso e $y$ è l'uscita, indipendentemente dalla non linearità iniziale.  
In altre parole, il ciclo chiuso tende ad assumere la forma dell'inverso della controreazione.

### 2. Sistemi Dinamici

La linearizzazione può essere applicata anche a sistemi dinamici non lineari.  

Ad esempio, per il pendolo, la cui dinamica è descritta da un’equazione non lineare, se si applica una controreazione in cui la coppia $\tau$ è data da $\tau = K(v - \theta)$, dove $v$ è il nuovo ingresso, e si impone un guadagno $K$ molto alto, l’equazione a ciclo chiuso si semplifica.  
Dividendo per $K$ e trascurando i termini del modello originale, si ottiene un’equazione lineare di primo ordine, ad esempio $\dot{\theta} \approx v$.

---

## Benefici e Cautela

- **Benefici:** L’effetto principale di una controreazione ad alto guadagno sui sistemi non lineari è rendere la relazione ingresso-uscita più lineare rispetto alla caratteristica di partenza.  

- **Cautela:** È essenziale prestare attenzione alla **stabilità interna** del sistema. Quando si applica l’alto guadagno per "cancellare" dinamiche complesse (come nel caso del pendolo), è necessario studiare la stabilità delle dinamiche residue per assicurarsi che il ciclo chiuso non diventi instabile.

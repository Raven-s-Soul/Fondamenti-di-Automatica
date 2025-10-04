# Funzione di sensibilità ed applicazione ai sistemi a controreazione
<aside>

Robustezza: sistemi reali dove studio parametri e caratteristiche ma potrei non conoscere tutte le informazioni del sistema

</aside>

- Incertezza sui parametri
- modello imperfetto

<aside>

Insensibile: il sistema se è in grado di rigettare le variazioni in catena diretta o retroazione.

</aside>

La funzione di sensibilità ‘S’ permette di vedere quanto una funzione $Q(s)$ è influenzata dal variare di un parametro $\alpha$.

Possiamo arrivare intuitivamente alla formula. Vogliamo infatti vedere la variazione relativa di $Q$ ed $\alpha$, per poi metterle in relazione facendo un rapporto.

> Esempio: se $\alpha$ varia del 3% e a causa di questa variazione $S$ varia del 12%, avremo che la sensibilità di $Q$ rispetto ad $\alpha$ è 4
> 

$$
S^Q_\alpha= \lim_{\Delta\alpha \to 0} \frac{\frac{\Delta Q}{Q(\bar\alpha)}}{\frac{\Delta \alpha}{\bar\alpha}}=\frac{\Delta Q}{\Delta \alpha}\frac{\bar\alpha}{Q}\Rightarrow\frac{dQ}{d\alpha}\frac{\bar\alpha}{Q}
$$

Seguendo lo stesso ragionamento posso vedere che è possibile concatenare la sensibilità delle funzioni. Se ad esempio la funzione $Q$ dipende dalla funzione $P$ e la funzione $P$ dipende dal parametro $\beta$ ho che:

$$
S^Q_\beta=S^Q_P\cdot S^P_\beta
$$

### Ciclo aperto

*No feeddback*

$$
S^G_p= \frac {\bar p} {G(s,\bar p)} \frac {\partial G(s,p)}{\partial p} 
$$

> Sensibilità di p
> 

$$
S^Y_G= \frac {G(s)} {Y(s)} \frac {\partial Y(s)}{\partial G(s)} = \frac {G(s)}{G(s)U(s)} \frac {\partial[G(s)U(s)]}{\partial G(s)}=\frac {G(s)}{G(s)U(s)}U(s)=1 
$$

> Sensibilità di G(s)
> 

### Ciclo chiuso
*Con il feeddback*

Relativamente uguale

### Proprietà funzione di sensibilità
- Concatenazione
- Composizione

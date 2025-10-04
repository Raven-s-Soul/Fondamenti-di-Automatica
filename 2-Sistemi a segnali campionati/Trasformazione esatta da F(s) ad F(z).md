# Trasformazione Esatta da $F(s)$ a $F(z)$

La **Trasformazione esatta da $F(s)$ ad $F(z)$** si riferisce al metodo utilizzato per convertire una funzione di trasferimento continua $F(s)$ (nel dominio di Laplace) in una funzione di trasferimento discreta $F(z)$ (nel dominio $Z$), basandosi sulla **conservazione della risposta impulsiva** del sistema.  
In altre parole, i valori campionati della risposta impulsiva rimangono identici.

Questo metodo è cruciale per l'analisi dei sistemi a tempo discreto.

---

## Metodologia

La trasformazione esatta, concettualmente, si articola in tre fasi:

1. **Antitrasformata di Laplace:**  
   Si calcola la risposta impulsiva $f(t)$ del sistema continuo $F(s)$.

2. **Campionamento:**  
   Si campiona la risposta impulsiva $f(t)$ per ottenere la sequenza di campioni $\{f(k T_c)\}$, dove $T_c$ è il periodo di campionamento.

3. **Trasformata Z:**  
   Si calcola la Trasformata $Z$ della sequenza campionata $\{f(k T_c)\}$ per ottenere $F(z)$.

**Esempio:**  
Per un polo semplice $G(s) = \frac{a}{s-p}$, la risposta impulsiva campionata è:

$$
g(k T_c) = a (e^{p T_c})^k
$$

La Trasformata $Z$ di questa sequenza è:

$$
G(z) = \sum_{k=0}^{\infty} g(k T_c) z^{-k}
$$

---

## Problematiche e Guadagno Statico

Nonostante sia definita "esatta", questa trasformazione **non è universale** e presenta un limite importante:

- **Non conservazione del guadagno statico:**  
  Sebbene i campioni della risposta impulsiva siano conservati, il **guadagno statico** (valore di regime per un ingresso a gradino) cambia tra sistema continuo e discreto.
- Per un sistema continuo $G(s)$, il guadagno statico è:

$$
\lim_{s \to 0} G(s)
$$

- Applicando la discretizzazione basata sulla risposta impulsiva, il guadagno statico risultante nel dominio $Z$ sarà differente.  
- Di conseguenza, la trasformazione esatta basata sulla risposta impulsiva viene spesso **evitata nella pratica** per la sintesi dei controllori.

---

## Trasformazione Esatta con Organo di Tenuta (ZOH)

Nei sistemi a segnali campionati reali, il processo continuo $G(s)$ è sempre preceduto da un **Organo di Tenuta di Ordine Zero (ZOH)** $T(s)$.

Il metodo di trasformazione che include il ZOH è:

$$
G_{ZOH}(z) = \mathcal{Z}\{T(s) G(s)\} = \mathcal{Z} {\frac{1 - e^{-s T_c}}{s} G(s)}
$$

Sfruttando le proprietà della Trasformata $Z$, si calcola più semplicemente come:

$$
G_{ZOH}(z) = (1 - z^{-1}) \mathcal{Z} {\frac{G(s)}{s}}
$$

Questo approccio è comunemente utilizzato nella pratica ingegneristica per ottenere una discretizzazione fedele, poiché modella l'interazione tra il segnale campionato e il sistema continuo (ZOH + $G(s)$ ) e garantisce che i campioni della risposta al gradino del sistema discreto corrispondano a quelli del sistema continuo.

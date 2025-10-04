# Modi propri d’evoluzione di un sistema discreto

I **modi propri** (o **modi naturali**) di un sistema discreto rappresentano gli andamenti temporali corrispondenti alle antitrasformate dei termini della funzione di trasferimento discreta $G(z)$.  
Questi modi dipendono dalla posizione dei **poli** della funzione di trasferimento nel piano $Z$ e determinano il comportamento dinamico e la stabilità del sistema.

---

## Criterio di Stabilità nel Piano $Z$

Per i sistemi discreti, la stabilità è definita dalla posizione dei poli rispetto al **cerchio di raggio unitario** nel piano $Z$:

1. **Stabilità Asintotica:**  
   Tutti i poli di $G(z)$ devono trovarsi **all'interno del cerchio unitario** ($|z| < 1$). Corrisponde al semipiano sinistro del piano $S$.

2. **Limite di Stabilità:**  
   Poli sulla **circonferenza di raggio unitario** ($|z| = 1$) indicano uno stato di **limite di stabilità**.

3. **Instabilità:**  
   Almeno un polo all'**esterno del cerchio unitario** indica che il sistema è instabile.

Il cerchio unitario funge da spartiacque tra stabilità e instabilità per i sistemi discreti, analogamente all'asse immaginario nel piano $S$ per i sistemi continui.

---

## Tipi di Modi Propri

I modi propri variano in funzione della natura dei poli di $G(z)$.

### 1. Modi Aperiodici (Poli Reali)

Se $G(z)$ ha un polo reale semplice $b$ (ad esempio derivante dalla discretizzazione di un polo continuo $-a$, con $b = e^{-a T_c}$):

- L'evoluzione temporale del modo proprio è una **successione geometrica**:
  $$\\
  y(k) = b^k c
  $$
- La successione **converge** solo se $|b| < 1$.
- Se $0 < b < 1$, il modo è **aperiodico convergente**.
- Se $-1 < b < 0$, il modo converge ma con **segno alternato**, introducendo oscillazioni non presenti nei sistemi continui con poli reali.

### 2. Modi Pseudo-periodici (Poli Complessi e Coniugati)

Se $G(z)$ ha una coppia di poli complessi coniugati (derivanti da poli $\sigma \pm j\omega$ nel piano $S$):

- L'evoluzione del modo proprio è **oscillatoria o pseudo-periodica**.
- La successione soddisfa l'equazione alle differenze:
  
$$y(k) = 2b \cos(\omega T_c),  y(k-1) - b^2, y(k-2)$$
  dove $b = e^{\sigma T_c}$.
- La successione **converge** solo se $|b| < 1$ (ovvero se $\sigma < 0$).

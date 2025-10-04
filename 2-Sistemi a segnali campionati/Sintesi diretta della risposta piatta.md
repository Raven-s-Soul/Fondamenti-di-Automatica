# Sintesi Diretta della Risposta Piatta

La **Sintesi Diretta della Risposta Piatta** è una metodologia di progettazione utilizzata nei **sistemi di controllo digitali**.

## Obiettivo

L'obiettivo è definire la funzione di trasferimento del controllore discreto $R(z)$ in modo tale che la funzione di trasferimento a ciclo chiuso $W(z)$ coincida con una funzione desiderata $W^*(z)$.

Il concetto di "risposta piatta" (o **tempo di assestamento finito**) implica che l'uscita del sistema raggiunga e mantenga il valore desiderato (ad esempio, l'ingresso a gradino) **esattamente negli istanti di campionamento** in un numero finito e minimo di passi.

## Calcolo del Controllore

Il controllore $R(z)$ viene calcolato a partire da:

- Il modello del processo discreto $G(z)$
- La funzione di trasferimento desiderata $W^*(z)$

È fondamentale che $W^*(z)$ sia scelta in modo da garantire la **causalità** del regolatore, cioè la sua **realizzabilità fisica**.

## Considerazioni Pratiche

- Sebbene la sintesi garantisca errore nullo o risposta piatta negli **istanti di campionamento**, il segnale continuo in uscita al di fuori di tali istanti può presentare **andamenti indesiderati o oscillazioni nascoste**.
- Per mitigare questi effetti:
  - Ridurre il **tempo di campionamento** $T_c$  
  - Scegliere un modello di riferimento $W^*(z)$ che eviti la cancellazione di poli oscillatori presenti nel processo $G(z)$

---

Questa metodologia è particolarmente utile per sistemi digitali dove la risposta rapida e precisa agli istanti di campionamento è critica.

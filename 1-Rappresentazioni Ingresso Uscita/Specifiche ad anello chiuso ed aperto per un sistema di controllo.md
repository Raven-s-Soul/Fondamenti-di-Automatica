# Specifiche ad anello chiuso ed aperto per un sistema di controllo
Analizzando la F(s) in catena diretta posso determinare i suoi margini di fase e guadagno.

Per gli altri valori invece devo analizzare il ciclo chiuso, quindi prendo in considerazione questo sistema, che ha una funzione di trasferimento e un guadagno statico in catena diretta:

$$
W(s)=\frac{K_dF(s)}{1+K_dF(s)}
$$

Vado a misurare la risposta al gradino e ne faccio il grafico nel tempo:

- Tempo di salita
    
    È il tempo impiegato per passare dal 10% al 90% del valore finale
    
- Sovraelongazione
    
    È la differenza tra il valore massimo raggiunto e il valore finale
    
- Tempo di assestamento
    
    Il tempo che ci mette per stabilizzarsi all’interno di un intervallo del 3% intorno al valore finale
    

Ora faccio il Bode della funzione a ciclo chiuso:

Sul diagramma il bode parte da un valore costante (0 se il guadagno è in catena diretta o $K_d$ se è in controreazione), sale in corrispondenza della frequenza di risonanza e poi scende.

- Modulo alla risonanza
    
    Valore massimo del modulo, che in genere si ha alla frequenza di risonanza. La frequenza di risonanza è quella a cui il sistema risponde meglio, è la frequenza naturale del sistema.
    
- Banda passante a 3dB
    
    La frequenza in cui il modulo sta 3dB sotto al valore iniziale. Una volta superata questa frequenza il sistema non riuscirà più a seguire bene le oscillazioni date in ingresso perché stanno a frequenze troppo alte.
    

Ci sono alcuni legami tra le varie grandezze:

- Il modulo alla risonanza è proporzionale alla sovraelongazione e inversamente proporzionale allo smorzamento. Un sistema molto smorzato infatti fa più fatica ad oscillare.
- La banda passante è inversamente proporzionale al tempo di salita, perché se un sistema supporta frequenze più elevate allora è in grado di rispondere più in fretta.
- Il guadagno influisce sulla frequenza di taglio perché trasla il bode (del modulo) verso l’alto, quindi se la funzione è decrescente la frequenza di taglio va verso destra.
    
    Un guadagno alto fa diminuire anche il tempo di salita e il margine di fase (se la fase è decrescente, in genere lo è).
    
    Un guadagno alto in catena diretta può rendere il sistema più lineare, diminuisce l’errore a regime permanente e rende meno rilevanti i disturbi in catena diretta.

- Il margine di fase è inversamente proporzionale al modulo alla risonanza

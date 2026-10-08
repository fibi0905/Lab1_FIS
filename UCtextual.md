# Use case StreamEveryThing
![UCdiagram](UCdiagram.png)

## LogIn 
*id: 1*

**Breve descrizione**: L'utente tenta il collegamento con il proprio account tramite le credenziali.
**Attore principale**: User Log  
**Attori secondari**: Autenticatore  
**Precondizioni**: Esistenza dell'account nel sistema.
### Sequenza principale:
    1. L'utente richiede di accedere al sistema.
    2. Il sistema visualizza la pagina di autenticazione.
    3. L'utente inserisce le credenziali.
    4. Il sistema verifica che siano corrette.
    5. Se le credenziali sono corrette:
        5.1 Il sistema garantisce l'accesso.
    6. Altrimenti:
        6.1 Il sistema restituisce un errore sui dati inseriti.

**Post-condizioni**: L'utente ha accesso al proprio account e ai contenuti associati.

### Sequenze alternative:
    - Utente non registrato
    - Password o User ID dimenticati
    - Richiesta di autenticazione a due fattori

---

## Download 
*id: 2*

**Breve descrizione**: L'utente premium richiede il download di un contenuto.
**Attore principale**: Utente Premium 
**Attori secondari**: //
**Precondizioni**: 
    L'utente deve:
        - Aver effetuato il login
        - Essere premium 
        - Aver effetuato l'ultimo pagamento
    Il contenuto richiesto deve essere presente nella piattaforma

### Sequenza principale:
    1. l'utente cerca il contentuo 
    2. il sistema verifca che il contentuo sia nella lista 
    3. se non presente:
        3.1 annulla l'operazione 
    4 altrimenti:
        4.1 procede 
    5. il sistema verifica che l'utente sia collegato 
    6. Se l'utente è collegato:
        6.1 controlla che sia un utente premium 
        6.2 Se l'utente è premium:
            6.2.1 controlla che l'ultimo pagamento sia avventuo
            6.2.2 se il pagamento è avenuto:
                6.2.2.1 il sistema permette il download 
            6.2.3 altrimenti:
                6.2.3.1 mostra richiede di fare il pagamento
        6.3 altrimenti
            6.3.1  richiede di passare a premium
    7. altrimenti
        7.1 richiede di fare il login 

**Post-condizioni**: l'utente avrà il suo contenuto al interno della sua libreria e disponblie onlie.

### Sequenze alternative:
    - Utente non registrato
    - Utente non pagante 
    - Utente non premium 
    - Contentuo non disponiblie 
    - Download non finito per problemi di connesione 


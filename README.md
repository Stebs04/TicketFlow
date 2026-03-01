# TicketFlow 🎬
![Java](https://img.shields.io/badge/Language-Java_17-orange?style=flat&logo=java&logoColor=white)
![JavaFX](https://img.shields.io/badge/GUI-JavaFX_21-blue?style=flat&logo=openjdk&logoColor=white)
![Maven](https://img.shields.io/badge/Build-Maven-C71A36?style=flat&logo=apachemaven&logoColor=white)
![SQLite](https://img.shields.io/badge/Database-SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![JUnit](https://img.shields.io/badge/Test-JUnit_5-25A162?style=flat&logo=junit5&logoColor=white)
![IDE](https://img.shields.io/badge/IDE-IntelliJ_IDEA-000000?style=flat&logo=intellij-idea&logoColor=white)
![UPO](https://img.shields.io/badge/Univ-UPO-red?style=flat)
<br>**TicketFlow** è una piattaforma desktop moderna per la gestione integrata di cinema multisala. Progettata per essere scalabile e modulare, l'applicazione offre interfacce dedicate per clienti, manager e amministratori, gestendo l'intero ciclo di vita dell'esperienza cinematografica: dalla programmazione del palinsesto all'emissione del biglietto digitale.</br>

   **Progetto Universitario**
<br>Sviluppato per il corso di **Ingegneria del Software**
<br>**Università del piemonte orientale**(UPO)
<br>Anno Accademico 2025/2026</br>

---

## 📑 Indice
1. [Panoramica](#panoramica-)
2. [Funzionalità chiave](#funzionalità-chiave-)
3. [Architettura e Design Patterns](#architettura-e-design-patterns-)
4. [Stack Tecnologico](#stack-tecnologico-)
5. [Installazione e Avvio](#installazione-e-avvio-)
6. [Team di Sviluppo](#team-di-sviluppo-)
---

## Panoramica 🔭
TicketFlow risolve le complessità della gestione cinematografica attraverso un'architettura robusta e un'interfaccia utente intuitiva ("User-Centric"). Il sistema permette una gestione granulare delle sale e degli spettacoli, prevenendo sovrapposizioni orarie e garantendo la coerenza dei dati transazionali.

L'applicazione segue rigorosamente il pattern MVC (Model-View-Controller), garantendo una netta separazione tra la logica di business, l'interfaccia grafica e la persistenza dei dati.
---

## Funzionalità Chiave 🚀
Il sistema gestisce tre livelli di utenza con permessi distinti:

👤 **Area Cliente (User)**
* Browsing Intelligente: Ricerca avanzata di film per titolo o genere.

* Prenotazione Visuale: Selezione interattiva dei posti in sala con feedback in tempo reale sulla disponibilità.

* Smart Pricing: Calcolo dinamico del prezzo (es. applicazione automatica sconto studenti tramite Strategy Pattern).

* Pagamento: Simulazione di checkout e pagamento elettronico sicuro.

👔 **Area Manager**
* Gestione Palinsesto: Creazione, modifica e rimozione degli spettacoli.

* Controllo Integrità: Algoritmo intelligente per la prevenzione di sovrapposizioni ("overlap") di orari nelle sale.

* Gestione Sale: Configurazione della capienza e layout delle sale cinematografiche.

🛡️ **Area Admin**
* User Management: Supervisione completa delle anagrafiche utenti.

* Sicurezza: Gestione dei permessi e monitoraggio degli accessi.
---

## Architettura e Design Patterns 🏗
Il cuore di TicketFlow è costruito seguendo le best practices dell'ingegneria del software per garantire manutenibilità ed estensibilità.

**Design Patterns Utilizzati:**
* MVC (Model-View-Controller): Struttura base del progetto per disaccoppiare la logica dalla UI (JavaFX).

* DAO (Data Access Object): Astrazione completa dell'accesso al database per rendere il codice indipendente dal tipo di storage.

* Factory Method: Utilizzato in DaoFactory per centralizzare la creazione delle istanze DAO.

* Facade: La classe TicketFlowService funge da unico punto di accesso per la logica di business complessa, semplificando le chiamate dai controller.

* Strategy: Implementato nel calcolo dei prezzi (es. ScontoStudenti) per permettere variazioni dinamiche delle tariffe senza modificare il codice core.

* Singleton: Gestione univoca della connessione al database (DbConnection).
---

## Stack Tecnologico 🛠
|Categoria|Tecnologia|Dettagli|
|---------|----------|--------|
|Linguaggio|Java 17|Core logic e Backend|
|GUI Framework|JavaFX 21|Interfaccia utente (FXML + CSS)|
|Build Tool|Maven|	Gestione dipendenze e ciclo di vita|
|Database|	SQLite	|RDBMS Embedded (nessuna configurazione server richiesta)|
|Testing|	JUnit 5|	Unit Testing per logica di business|
|Librerie|	SLF4J|	Logging facade|
---

## Installazione e Avvio 💻
**Prerequisiti**
* JDK 17 o superiore installato.
* Maven 3.x installato.

**Passaggi**
1. Clona il repository:
```
git clone https://github.com/tuo-username/TicketFlow.git
cd TicketFlow
```
2. Compila il progetto e scarica le dipendenze:
```
mvn clean install
```
3. Esegui i test (Opzionale ma consigliato):
```
mvn test
```
4. Avvia l'applicazione:
```
mvn javafx:run
```
- **Nota Database:** Al primo avvio, l'applicazione inizializzerà automaticamente il database SQLite (ticketflow.db) e le relative tabelle tramite la classe SchemaInit.
---

## Team di Sviluppo 👥 
Progetto realizzato dal gruppo TicketFlow per l'esame di Ingegneria del Software.
|Nome|Ruolo|Matricola|Focus|
|----|-----|---------|-----|
|Stefano Bellan|Developer|20054330|Logica Manager, Gestione Sale/Spettacoli|
|Luca Franzon|Developer|20054744|Gestione Acquisti, Pagamenti, Registrazione|
|Timothy Giolito|Developer|20054431|Facade Service, Ricerca, Infrastruttura Base|

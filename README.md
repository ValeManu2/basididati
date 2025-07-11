# Sistema di Gestione Prenotazioni e Vendite – Studio Tecnoacustica

Questo progetto nasce con l’obiettivo di digitalizzare le attività quotidiane dello Studio Tecnoacustica, uno studio medico specializzato in diagnosi uditive e fornitura di dispositivi acustici personalizzati.  
Attraverso un’applicazione web moderna e sicura, il sistema sostituisce le attuali procedure cartacee e telefoniche, migliorando l’efficienza organizzativa e l’esperienza dell’utente.  
Il sistema è basato su un database relazionale SQL, progettato per garantire coerenza e integrità dei dati.

---

## Indice

- [Modello Entità/Relazione](#modello-entitàrelazione)
- [Funzionalità Principali](#funzionalità-principali)
- [Tecnologie Utilizzate](#tecnologie-utilizzate)
- [Installazione](#installazione)
- [Configurazione del Database](#configurazione-del-database)
- [Utilizzo](#utilizzo)
- [Licenza](#licenza)

---

## Modello Entità/Relazione

Il sistema gestisce tre tipologie di utenti (**Pazienti**, **Medici/Audioprotesisti**, **Amministratori**) e una serie di entità correlate come dispositivi, appuntamenti, ordini e ricette.  
Le relazioni sono progettate per essere consistenti e normalizzate.  
Le entità principali sono:

- **Utente** (con ruolo: paziente, medico, admin)
- **Ricetta**
- **Prenotazione**
- **Prodotto**
- **Ordine / Dettaglio Ordine**

---

## Funzionalità Principali

L’applicazione offre un’esperienza completa per pazienti, medici e personale:

- Registrazione e Login con verifica email (OTP), validazione sicura e ruoli.
- Prenotazione Visite con calendario interattivo e conferme via email.
- Visualizzazione Medici Disponibili: elenco aggiornato dei professionisti.
- Catalogo Prodotti: dispositivi acustici con immagini, descrizioni e prezzo.
- Carrello e Checkout: carrello dinamico, conferma ordine, dettaglio vendita.

---

## Tecnologie Utilizzate

- **Python + Django**: backend e gestione ORM
- **MySQL / MariaDB**: database relazionale
- **HTML5 / CSS3 / JavaScript**: frontend interattivo
- **Bootstrap**: UI moderna e responsive
- **FullCalendar.js**: gestione visuale delle prenotazioni
- **Email OTP System**: verifica sicurezza account

---

## Installazione

Clonare il progetto:

```bash
git clone https://github.com/tuo_utente/studio-tecnoacustica.git
cd studio-tecnoacustica
```

Creare e attivare ambiente virtuale:

```bash
python -m venv venv
source venv/bin/activate  # oppure .venv\Scripts\activate.bat su Windows
```

Installare le dipendenze:

```bash
pip install -r requirements.txt
```

---

## Configurazione del Database

Nel file `settings.py` configurare la sezione DATABASES:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'tecnoacustica',
        'USER': 'root',
        'PASSWORD': 'tuapassword',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```

Creare un database MySQL (es. `tecnoacustica`).

Eseguire le migrazioni:

```bash
python manage.py makemigrations
python manage.py migrate
```

---

## Utilizzo

Dopo la configurazione, eseguire i seguenti comandi:

```bash
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```

Accedere all’app da [http://127.0.0.1:8000](http://127.0.0.1:8000)

### Esempi Utente

- Visualizzare prodotti e disponibilità
- Aggiungere al carrello
- Prenotare visita da calendario
- Ricevere codice OTP e verificare account
- Consultare storico ordini e prenotazioni

### Esempi Admin/Staff

- Visualizzare e modificare lo stato delle prenotazioni
- Gestire inventario e disponibilità
- Visualizzare vendite, ricette e report

---

## Licenza

Questo progetto è distribuito con licenza MIT.

---

> **README** generato automaticamente sulla base della documentazione `basiDidati.pdf` e codice incluso in `tecnoacustica.zip`.

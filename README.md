# Laravel Project

Dit is een [Laravel](https://laravel.com/) project dat draait op PHP en MySQL. Volg de onderstaande stappen om het project lokaal op te zetten en te draaien.

---

## 🚀 Vereisten
Zorg ervoor dat je de volgende software geïnstalleerd hebt:

- **PHP** (>= 8.1)
- **Composer** (Dependency Manager voor PHP)
- **MySQL** (of een andere ondersteunde database)
- **Node.js** en **npm** (voor front-end assets)
- **Git** (voor versiebeheer)

---

## 📂 Installatie-instructies

Volg deze stappen om het project lokaal draaiend te krijgen:

### 1. Clone het project
```bash
git clone https://github.com/FlorisROC/Laravel-CRUD.git 
cd <repository-naam>
```

### 2. Installeer dependencies
```bash
composer install
npm install
```

### 3. Maak een `.env` bestand
Maak een `.env` bestand door het voorbeeldbestand te kopiëren:
```bash
cp .env.example .env
```
Pas de instellingen aan, zoals de databaseconfiguratie, zodat deze overeenkomen met jouw lokale omgeving.

### 4. Genereer de applicatiesleutel
```bash
php artisan key:generate
```

### 5. Database instellen
Maak een nieuwe database aan in MySQL en stel de naam in in het `.env` bestand:
```
DB_DATABASE=laravel_db
DB_USERNAME=je_gebruikersnaam
DB_PASSWORD=je_wachtwoord
```

Voer daarna de migraties uit om de tabellen aan te maken:
```bash
php artisan migrate
```

Optioneel: Voeg voorbeeldgegevens toe met seeders:
```bash
php artisan db:seed
```

### 6. Start de ontwikkelserver
```bash
php artisan serve
```
De server draait nu op [http://127.0.0.1:8000](http://127.0.0.1:8000).

---

## 📦 Assets bouwen
Bouw de front-end assets met **Vite**:
- Voor ontwikkeling:
  ```bash
  npm run dev
  ```
- Voor productie:
  ```bash
  npm run build
  ```

---

## 🐳 Optioneel: Gebruik Laravel Sail (Docker)
Als je Docker gebruikt, kun je Laravel Sail gebruiken:
1. Installeer Sail:
   ```bash
   composer require laravel/sail --dev
   ```
2. Start de containers:
   ```bash
   ./vendor/bin/sail up
   ```
3. Gebruik Sail-commando's (bijvoorbeeld):
   ```bash
   ./vendor/bin/sail php artisan migrate
   ```

---

## 🛠️ Handige commando's
- **Cache vernieuwen**:
  ```bash
  php artisan config:cache
  php artisan route:cache
  php artisan view:cache
  ```
- **Testen uitvoeren**:
  ```bash
  php artisan test
  ```
- **Logbestanden bekijken**:
  ```bash
  tail -f storage/logs/laravel.log
  ```

---

## 📝 Licentie
Dit project is gelicentieerd onder de [MIT-licentie](LICENSE).

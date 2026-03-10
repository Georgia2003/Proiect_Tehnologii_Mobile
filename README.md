
# Proiect Tehnologii Mobile

## Descriere proiect

Acest proiect reprezintă o aplicație mobilă dezvoltată cu **Flutter** pentru disciplina **Tehnologii Mobile**.
Aplicația permite utilizatorilor să descopere diferite **modele de manichiură**, să aleagă serviciul dorit și să își facă **programări online la salon**.

Aplicația va consuma **servicii web (REST API)** pentru a obține informații despre modelele de unghii și serviciile disponibile și va utiliza **SQLite** pentru stocarea locală a anumitor date (ex: favorite sau programări salvate).

Scopul aplicației este să ofere o interfață mobilă prin care utilizatorii pot:

* vizualiza modele de unghii
* explora diferite tipuri de servicii de manichiură
* vedea detalii despre fiecare model sau serviciu
* salva modele preferate
* crea un cont de utilizator
* realiza programări online
* efectua plata serviciilor înainte de programare

---

# Conceptul aplicației

Aplicația va funcționa ca o platformă de **descoperire și programare pentru servicii de manichiură**.

Pe pagina principală vor fi afișate **modele de unghii** sub formă de carduri cu imagini.

Fiecare model poate conține informații precum:

* tipul de manichiură
* stilul modelului
* nivelul de complexitate
* durata estimată a realizării
* prețul serviciului
* descrierea modelului

Utilizatorul poate selecta un model pentru a vedea mai multe detalii și pentru a realiza o **programare la salon**.

Aplicația permite și salvarea modelelor preferate pentru a putea fi accesate ulterior.

---

# Structura aplicației

Aplicația va avea următoarele ecrane principale:

## 1. Home Page

Pagina principală va afișa mai multe **modele de unghii disponibile**.

Fiecare element din listă va conține:

* imagine reprezentativă
* numele modelului
* tipul de manichiură (ex: clasică, semi-permanentă, construcție gel)
* preț orientativ
* un buton pentru vizualizarea detaliilor

Această pagină permite utilizatorului să exploreze rapid diferite stiluri de manichiură.

---

## 2. Pagina de detalii a modelului

Această pagină va conține informații complete despre modelul selectat.

Informațiile pot include:

* descrierea modelului
* tipul de serviciu
* durata estimată a procedurii
* prețul
* recomandări privind întreținerea manichiurii

Pe această pagină utilizatorul va avea opțiunea de a:

* salva modelul la **favorite**
* continua către **programare**

---

## 3. Pagina de programare

Această pagină va permite utilizatorului să realizeze o **programare online** pentru serviciul dorit.

Exemple de informații colectate:

* nume
* email / telefon
* tipul de serviciu (semi-permanent, clasic, construcție etc.)
* data și ora programării
* observații suplimentare

După completarea formularului, utilizatorul poate continua către **plata online a serviciului**.

Datele pot fi trimise către un serviciu web sau salvate temporar local.

---

## 4. Pagina de favorite

Utilizatorul poate salva anumite **modele de unghii preferate** pentru a le consulta ulterior.

Aceste date vor fi salvate local folosind **SQLite**, astfel încât aplicația să demonstreze utilizarea unei baze de date locale.

---

## 5. Pagina de cont utilizator

Aplicația va permite utilizatorilor să își creeze un **cont personal**.

Prin intermediul contului, utilizatorii pot:

* vizualiza programările realizate
* gestiona preferințele
* salva modele favorite

---

# Structura tehnică a proiectului

Codul aplicației este organizat în interiorul folderului **lib** folosind o structură modulară.

```text
lib
 ├── models
 │   └── nail_model.dart
 │
 ├── services
 │   ├── api_service.dart
 │   └── database_service.dart
 │
 ├── screens
 │   ├── home_page.dart
 │   ├── nail_details_page.dart
 │   ├── booking_page.dart
 │   └── favorites_page.dart
 │
 ├── widgets
 │   └── nail_card.dart
 │
 └── main.dart
```

### Explicația folderelor

**models**
Conține modelele de date ale aplicației (ex: modelul unui design de unghii).

**services**
Conține logica pentru:

* apelarea serviciilor API
* gestionarea bazei de date SQLite.

**screens**
Conține ecranele principale ale aplicației.

**widgets**
Conține componente UI reutilizabile (ex: carduri pentru afișarea modelelor de unghii).

**main.dart**
Punctul de pornire al aplicației.

---

# Distribuirea sarcinilor în echipă

Pentru dezvoltarea proiectului, sarcinile pot fi împărțite astfel:

**Membru 1**

* configurarea proiectului
* navigarea între ecrane
* structura generală a aplicației

**Membru 2**

* implementarea listei de modele de unghii
* integrarea API pentru încărcarea datelor

**Membru 3**

* implementarea paginii de detalii
* design UI pentru prezentarea modelelor

**Membru 4**

* implementarea SQLite
* salvarea modelelor favorite

---

# Rularea aplicației

Pentru rularea aplicației:

```bash
git clone <repository>
cd Proiect_Tehnologii_Mobile/mobile_app
flutter pub get
flutter run
```

---

# Tehnologii utilizate

* Flutter
* Dart
* REST API
* SQLite
* Git / GitHub

---

💡 Dacă vrei, îți pot face și:

* **o versiune puțin mai “profesională” pentru README (care ia puncte mai multe la proiect)**
* **ideea de API fake pentru modele de unghii**
* **schema de bază de date SQLite pentru favorite și programări** (profesorii cer foarte des asta).

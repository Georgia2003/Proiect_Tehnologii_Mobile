# Proiect_Tehnologii_Mobile


# Proiect Tehnologii Mobile

## Descriere proiect

Acest proiect reprezintă o aplicație mobilă dezvoltată cu **Flutter** pentru disciplina **Tehnologii Mobile**.
Aplicația va permite utilizatorilor să descopere și să planifice **călătorii organizate**, să vizualizeze detaliile acestora și să se înscrie la diferite experiențe turistice.

Aplicația va consuma **servicii web (API)** pentru a obține informațiile despre călătorii și va utiliza **SQLite** pentru stocarea locală a anumitor date (ex: favorite sau înscrieri salvate local).

Scopul aplicației este să ofere o interfață mobilă prin care utilizatorii pot:

* vizualiza mai multe călătorii disponibile
* căuta sau explora destinații
* vedea detalii complete despre o călătorie
* consulta criteriile de participare
* salva călătorii favorite
* trimite o cerere de înscriere

---

# Conceptul aplicației

Aplicația va funcționa ca o platformă de **planificare și descoperire a călătoriilor organizate**.
Pe pagina principală vor fi afișate mai multe călătorii sub formă de carduri cu imagini atractive.

Fiecare călătorie va conține informații detaliate precum:

* destinația
* durata excursiei
* programul zilnic (dimineață, prânz, seară)
* activitățile incluse
* mesele incluse
* cerințe de participare
* documente necesare (dacă este cazul)
* recomandări privind îmbrăcămintea sau echipamentul
* intervalul de vârstă recomandat

Utilizatorul poate selecta o călătorie pentru a vedea toate detaliile și pentru a se înscrie.

---

# Structura aplicației

Aplicația va avea următoarele ecrane principale:

## 1. Home Page

Pagina principală va afișa mai multe călătorii disponibile.

Fiecare element din listă va conține:

* imagine reprezentativă
* numele destinației
* durata călătoriei
* locația
* un buton pentru vizualizarea detaliilor

Această pagină permite utilizatorului să exploreze rapid mai multe opțiuni de călătorie.

---

## 2. Pagina de detalii a călătoriei

Această pagină va conține informații complete despre excursia selectată.

Informațiile pot include:

* descrierea călătoriei
* durata
* programul pe zile sau pe intervale (dimineață / prânz / seară)
* mesele incluse
* activitățile planificate
* criteriile de participare
* vârsta recomandată
* echipamentul sau îmbrăcămintea necesară
* documentele necesare (ex: pașaport)

Pe această pagină utilizatorul va avea și opțiunea de a se înscrie.

---

## 3. Pagina de înscriere

Această pagină va permite utilizatorului să completeze un formular pentru participarea la o călătorie.

Exemple de informații colectate:

* nume
* vârstă
* email / telefon
* data dorită pentru excursie
* observații suplimentare

Datele pot fi trimise către un serviciu web sau salvate temporar local.

---

## 4. Pagina de favorite / rezervări

Utilizatorul poate salva anumite călătorii preferate pentru a le consulta ulterior.

Aceste date vor fi salvate local folosind **SQLite**, astfel încât aplicația să demonstreze utilizarea unei baze de date locale.

---

# Structura tehnică a proiectului

Codul aplicației este organizat în interiorul folderului **lib** folosind o structură modulară.

```text
lib
 ├── models
 │   └── travel.dart
 │
 ├── services
 │   ├── api_service.dart
 │   └── database_service.dart
 │
 ├── screens
 │   ├── home_page.dart
 │   ├── travel_details_page.dart
 │   ├── registration_page.dart
 │   └── favorites_page.dart
 │
 ├── widgets
 │   └── travel_card.dart
 │
 └── main.dart
```

### Explicația folderelor

**models**
Conține modelele de date ale aplicației (ex: modelul unei călătorii).

**services**
Conține logica pentru:

* apelarea serviciilor API
* gestionarea bazei de date SQLite.

**screens**
Conține ecranele principale ale aplicației.

**widgets**
Conține componente UI reutilizabile (ex: carduri pentru afișarea călătoriilor).

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

* implementarea listei de călătorii
* integrarea API pentru încărcarea datelor

**Membru 3**

* implementarea paginii de detalii
* design UI pentru prezentarea informațiilor

**Membru 4**

* implementarea SQLite
* salvarea călătoriilor favorite

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

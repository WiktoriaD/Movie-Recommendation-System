# System rekomendacji filmów

Zaawansowany system rekomendacji filmów, który implementuje i porównuje filtrowanie kolaboracyjne oraz filtrowanie oparte na treści. Projekt został wzbogacony o dane z zewnętrznego API i zintegrowany z chmurową bazą danych NoSQL - MongoDB Atlas.

## Opis projektu

Celem projektu było stworzenie kompleksowego systemu rekomendacji, który demonstruje różne techniki modelowania i inżynierii danych. Projekt został zrealizowany jako praca dyplomowa na studiach podyplomowych z zakresu Big Data.

Główne zaimplementowane funkcjonalności:
* **Filtrowanie kolaboracyjne (Collaborative Filtering):** Rekomendacje oparte na podobieństwie ocen pomiędzy użytkownikami.
* **Filtrowanie oparte na treści (Content-Based Filtering):** Zaawansowany model rekomendujący filmy na podstawie ich "DNA" - atrybutów takich jak gatunek, tagi, reżyser, obsada i słowa kluczowe.
* **Integracja z API:** Skrypt automatycznie wzbogaca dane o filmach, pobierając dodatkowe informacje z The Movie Database (TMDb).
* **Wdrożenie w chmurze:** Wyniki działania modelu (pre-kalkulowane rekomendacje) są zapisywane w bazie MongoDB Atlas, symulując architekturę gotową do użycia przez aplikację webową.

---

## Użyte technologie

Projekt został zrealizowany z wykorzystaniem następujących narzędzi i bibliotek:

* **Język:** Python (wersja 3.11.7 użyta do dewelopmentu)
* **Główne biblioteki:**
    * `pandas` - do manipulacji i analizy danych.
    * `scikit-learn` - do budowy modeli (TF-IDF, podobieństwo cosinusowe).
    * `requests` - do wykonywania zapytań do zewnętrznego API.
    * `python-dotenv` - do zarządzania zmiennymi środowiskowymi.
    * `pymongo` - jako sterownik do komunikacji z bazą MongoDB.
    * `matplotlib` & `seaborn` - do wizualizacji danych.
* **Baza danych:** MongoDB Atlas (M0 Free Tier).
* **Środowisko:** Jupyter Notebook.

---

## Instalacja i uruchomienie

Aby uruchomić projekt lokalnie i odtworzyć wyniki, postępuj zgodnie z poniższymi krokami.

```bash
# Klonowanie repozytorium
git clone [https://github.com/WiktoriaD/Movie-Recommendation-System.git](https://github.com/WiktoriaD/Movie-Recommendation-System.git)
cd Movie-Recommendation-System

# Utwórz środowisko wirtualne o nazwie 'venv'
python -m venv venv

# Aktywuj środowisko
# Na Windows:
venv\Scripts\activate
# Na macOS/Linux:
source venv/bin/activate

# Zainstaluj wymagane biblioteki
pip install -r requirements.txt

# Projekt wymaga dostępu do API oraz bazy danych. Stwórz w głównym folderze projektu plik o nazwie .env i uzupełnij go swoimi danymi, wzorując się na poniższym szablonie
API_KEY="TWOJ_KLUCZ_DO_TMDB"
DB_STRING="TWÓJ LINK DO CLUSTRA"

# Po poprawnej instalacji i konfiguracji, uruchom serwer Jupyter Lab lub Jupyter Notebook
jupyter lab

# Analiza danych pogodowych i klasyfikacja opadów

Projekt typu Data Science oparty na danych meteorologicznych z systemu "Pogodynka". Celem projektu była predykcja intensywności opadów atmosferycznych na podstawie różnych warunków pogodowych przy użyciu algorytmów uczenia maszynowego.

## 📁 Dane

- `pogodynka_zbilansowana.csv` – dane treningowe (przygotowane, czyste dane z 38 kolumnami).
- `pogodynka_test_clean.csv` – dane testowe (osobny zbiór do walidacji końcowej modelu).

Dane zostały załadowane do **SQL Server**, a następnie odczytane w **Jupyter Notebook** za pomocą `pyodbc`.

---

## ⚙️ Użyte technologie

- Python (Jupyter Notebook)
- Pandas, NumPy, Seaborn, Matplotlib
- Scikit-learn
- XGBoost
- SQL Server (dane źródłowe)
- Git, GitHub

---

## 🧠 Użyte algorytmy ML

1. **Random Forest Classifier**
2. **XGBoost Classifier**
3. **KNeighbors Classifier**

Modele uczono na danych z `pogodynka_zbilansowana.csv`, a testowano na `pogodynka_test_clean.csv`.

---

## 📊 Wyniki i wizualizacje

### Macierze Pomyłek

![Confusion Matrix](figures/confusion_matrices.png)

---

### Feature Importance (XGBoost)

![Feature Importance](figures/feature_importance.png)

---

## 📈 Metryki

| Model                | Accuracy | Precision | Recall | F1-score |
|---------------------|----------|-----------|--------|----------|
| Random Forest        | 0.877848 | 0.875355  | 0.877848 | 0.871267 |
| XGBoost              | 0.869295 | 0.864977  | 0.869295 | 0.865011 |
| K-Nearest Neighbors  | 0.783027 | 0.760084  | 0.783027 | 0.760751 |

---
## 📂 Struktura katalogów


---

## ✅ Wnioski

- Najlepsze wyniki osiągnął model **XGBoost**, który dzięki analizie ważności cech potwierdził istotny wpływ temperatury, deficytu punktu rosy oraz wielkości zachmurzenia na występowanie opadów.
- Model KNN był najmniej efektywny, co może być skutkiem dużej liczby zmiennych binarnych i braków w normalizacji.
- Projekt można rozszerzyć o:
  - Próbę regresji ilościowej opadu (nie tylko klasyfikację)
  - Integrację danych z nowych lokalizacji
  - Automatyzację modelowania (AutoML)

---

## 🙋‍♂️ Autor

**Rafał Karpowicz**  
Projekt wykonany jako część portfolio Data Science

GitHub: [@RafalKarpowicz](https://github.com/RafalKarpowicz)

---


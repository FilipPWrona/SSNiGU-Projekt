# Projekt Końcowy: Klasyfikacja Obrazów z Wykorzystaniem CNN

## Opis Projektu
Projekt zrealizowany w ramach przedmiotu **Sztuczne Sieci Neuronowe i Głębokie Uczenie**. Głównym celem jest zaprojektowanie, zaimplementowanie i zbadanie właściwości Konwolucyjnych Sieci Neuronowych (CNN) w praktycznym zadaniu klasyfikacji wieloklasowej.

Do wykonania zadania wybrano referencyjny zbiór danych **CIFAR-10** obejmujący kolorowe obrazy o rozdzielczości 32x32 pikseli. Model został zbudowany w środowisku **PyTorch**.

## Zawartość Projektu (Notatnika Jupyter)
W przygotowanym pliku `projekt.ipynb` znajdziesz obszerną dokumentację odpowiadającą wytycznym z sylabusa (m.in. Pkt. 2, 3, 4, 7 i 10), która obejmuje:
- Uzasadnienie wyboru problemu oraz narzędzi.
- Sposób przygotowania danych (preprocessing, augmentacje z pakietu `torchvision`).
- Definicję elastycznej architektury **Konwolucyjnej Sieci Neuronowej (CNN)** z wykorzystaniem warstw w pełni połączonych (`Linear`), splotowych (`Conv2d`) oraz normalizacji (Batch Normalization).
- Implementację algorytmu wstecznej propagacji błędu (Backpropagation) wraz z logowaniem historii loss i accuracy.
- Przeprowadzenie **3 eksperymentów porównawczych**:
  - Model Bazowy Płytki (Optymalizator Adam)
  - Model Głęboki (Optymalizator Adam)
  - Model Bazowy Płytki (Optymalizator klasyczny SGD z momentum)
- Ewaluację z **wizualizacją wyników** (Krzywe nauki, analizę błędnych predykcji, wizualizację map cech aktywacji dla warstw splotowych).
- Ostateczne wnioski i analizę **ograniczeń systemów Głębokiego Uczenia**.

## Uruchomienie
1. Upewnij się, że posiadasz zainstalowane biblioteki m.in. `torch`, `torchvision`, `matplotlib` i `numpy`. Notatnik w pełni wykorzystuje potencjał sprzętowy dzięki automatycznej alokacji urządzenia (wspiera wsparcie m.in. dla rdzeni CUDA np. w akceleratorach RTX).
2. Uruchom wszystkie komórki w pliku `projekt.ipynb` (Opcja `Run All`).
3. Zbiór CIFAR-10, jeżeli nie jest obecny, zostanie w tle **pobrany automatycznie** (`download=True`). Nie trzeba załączać zewnętrznych folderów.

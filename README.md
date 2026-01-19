# spa-simple-power-analysis-simulation
Symulacja podstaw ataku Simple Power Analysis (SPA) – projekt edukacyjny z cyberbezpieczeństwa.
# Podstawy Simple Power Analysis (SPA) – symulacja
## Opis projektu

Projekt edukacyjny przedstawiający podstawy ataku Simple Power Analysis (SPA) (side-channel attack) poprzez symulację przebiegów poboru mocy podczas wykonywania uproszczonego algorytmu kryptograficznego.

Celem projektu było:

pokazanie, jak implementacja zależna od klucza może ujawniać informacje poprzez pobór mocy,

przeprowadzenie symulowanego ataku SPA,

wdrożenie mechanizmów obronnych (stałoczasowość + maskowanie),

porównanie wyników dla środowisk Windows i Linux.

Projekt wykonano w ramach przedmiotu Sprzętowe aspekty cyberbezpieczeństwa – ćwiczenie nr 5.

## Zakres

W projekcie zrealizowano:

symulację przebiegów poboru mocy na podstawie modelu Hamming Weight (z dodanym szumem),

implementację wersji podatnej algorytmu (zależność od bitu klucza),

wizualną analizę wykresów SPA,

implementację wersji zabezpieczonej:

constant-time

maskowanie danych (boolean masking)

porównanie wyników przed i po obronie.

## Technologie

Python 3

NumPy

Matplotlib

## Uruchomienie projektu
1) Instalacja zależności
pip install numpy matplotlib

2) Uruchomienie skryptu

Przykładowo:

python spa_attack.py


lub (wersja z obroną):

python spa_defense.py


Nazwy plików mogą się różnić w zależności od wersji (Windows/Linux) — w repozytorium znajdują się osobne pliki dla symulacji ataku i obrony.

## Wyniki

W wersji podatnej możliwe było wizualne rozróżnienie przebiegów poboru mocy zależnych od bitu klucza.

Po zastosowaniu mechanizmów obronnych:

przebiegi stały się do siebie bardzo podobne,

różnica średnich wartości poboru mocy spadła do poziomu porównywalnego z szumem,

skuteczność SPA została znacząco ograniczona.

## Mechanizmy obronne

W celu ograniczenia skuteczności SPA zastosowano:

stałoczasowość (constant-time) – stała liczba operacji niezależnie od klucza,

maskowanie danych (boolean masking) – przetwarzanie danych w postaci zamaskowanej,

dodatkowy szum w symulacji dla lepszego odwzorowania warunków rzeczywistych.

## Autorzy

Emilia Zaręba

Katarzyna Zieleniewska

## Uwaga

Projekt ma charakter edukacyjny i symulacyjny – nie zawiera rzeczywistych pomiarów poboru mocy sprzętu.

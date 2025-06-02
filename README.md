# quantum-vertex-cover

Questo progetto esplora la risoluzione del problema del Vertex Cover, un classico problema NP-hard, utilizzando approcci sia classici che quantistici. In particolare, viene illustrata la formulazione del Vertex Cover come problema di ottimizzazione combinatoria e la sua mappatura in un Hamiltoniano quantistico, preparatoria per l'applicazione di algoritmi come QAOA (Quantum Approximate Optimization Algorithm) e VQE (Variational Quantum Eigensolver).

Il progetto serve come esempio pratico per comprendere come problemi di ottimizzazione difficili possono essere affrontati nel contesto del Quantum Computing.

## Contenuti

*   **Introduzione al Vertex Cover**: Descrizione del problema e della sua importanza.
*   **Formulazione Hamiltoniana**: Dettagli su come il problema del Vertex Cover viene trasformato in un Hamiltoniano quantistico (formulazione Ising/QUBO).
*   **Funzioni di Utilità**: Funzioni di supporto per la visualizzazione, validazione e valutazione delle soluzioni.
*   **Definizione del Grafo**: Creazione di un grafo d'esempio su cui applicare gli algoritmi.
*   **Risoluzione Classica**: Implementazione di un risolutore classico (OR-Tools CP-SAT) per ottenere una soluzione ottima di riferimento.
*   **Implementazione Quantistica (VQE/QAOA)**: 

## Problema del Vertex Cover

Dato un grafo non orientato \( G = (V, E) \), un **vertex cover** è un sottoinsieme di vertici \( C ⊆ V \) tale che ogni arco \( (u, v) \in E \) abbia almeno uno dei due estremi in \( C \). L'obiettivo è trovare il vertex cover di dimensione minima.

## Formulazione Quantistica

Il problema viene mappato in un Hamiltoniano \( H = Hₐ + Hᵦ \), dove:
*   \( Hₐ \) è un termine di penalità che garantisce che ogni arco sia coperto.
*   \( Hᵦ \) è un termine di costo che mira a minimizzare il numero di vertici selezionati.

Le variabili binarie \( xᵥ ∈ \{0, 1\} \) per ogni vertice sono mappate su variabili di spin \( sᵥ ∈ \{-1, +1\} \).

## Installazione
Le installazioni sono già incluse nel notebook per comodità.

## Utilizzo

1.  Clona questo repository: bash git clone cd
2.  2.  Apri il notebook `Progetto.ipynb` in Google Colab.
3.  Esegui le celle del notebook per installare le dipendenze, definire il grafo e risolvere il problema in modo classico.
4.  (Aggiungerai qui le istruzioni specifiche per eseguire le parti quantistiche quando saranno pronte).

## Riferimenti

*   Lucas, A. (2014). Ising formulations of many NP problems. Frontiers in Physics. (Citato nel notebook)
*   Documentazione di PennyLane
*   Documentazione di Qiskit

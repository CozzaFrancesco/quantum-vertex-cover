# quantum-vertex-cover

Questo progetto esplora la risoluzione del problema del Vertex Cover, un classico problema NP-hard, utilizzando approcci sia classici che quantistici. In particolare, viene illustrata la formulazione del Vertex Cover come problema di ottimizzazione combinatoria e la sua mappatura in un Hamiltoniano quantistico, preparatoria per l'applicazione di algoritmi come QAOA (Quantum Approximate Optimization Algorithm) e VQE (Variational Quantum Eigensolver).

Il progetto serve come esempio pratico per comprendere come problemi di ottimizzazione difficili possono essere affrontati nel contesto del Quantum Computing.

## 📌 Indice

- [Problema del Vertex Cover](#vertex-cover)
- [Formulazione Quantistica](#formulazione-quantistica)
- [Installazione](#installazione)
- [Utilizzo](#utilizzo)
- [Struttura del Codice](#struttura-del-codice)
- [Risultati](#risultati)
- [Riferimenti](#riferimenti)
- [Licenza](#licenza)

## 🔍 Vertex Cover

Dato un grafo non orientato \( G = (V, E) \), un **vertex cover** è un sottoinsieme di vertici \( C ⊆ V \) tale che ogni arco \( (u, v) \in E \) abbia almeno uno dei due estremi in \( C \). L'obiettivo è trovare il vertex cover di dimensione minima.

**Applicazioni**:
- Progettazione di reti
- Bioinformatica
- Cybersecurity
- Scheduling e logistica

## ⚛️ Formulazione Quantistica

Il problema viene mappato in un Hamiltoniano quantistico:

\[ H = Hₐ + Hᵦ \]

Dove:
- \( Hₐ = A \sum_{(u,v) \in E} (1 - x_u)(1 - x_v) \) (termine di penalità)
- \( Hᵦ = B \sum_{v \in V} x_v \) (termine di costo)

Le variabili binarie \( x_v \) sono mappate su qubit mediante:
\[ x_v = \frac{1 + s_v}{2}, \quad s_v \in \{-1, +1\} \]

## 💻 Installazione

1. Clona il repository:
```bash
git clone https://github.com/tuo-username/quantum-vertex-cover.git
cd quantum-vertex-cover
```

## 🚀 Utilizzo
- Apri il notebook Progetto.ipynb in Jupyter o Google Colab
- Esegui le celle in ordine per:
   Definire il grafo di esempio
   Visualizzare il grafo
  Risolvere il problema con approccio classico (OR-Tools CP-SAT)
  Implementare la soluzione quantistica (VQE/QAOA)
- Analizza i risultati comparando le soluzioni classiche e quantistiche

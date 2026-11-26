# Architecture Transformer

Notebooks pédagogiques pour explorer les modèles de séquences et les modèles de langage avec PyTorch et Transformers.

## Parcours conseillé

| Ordre | Notebook | Sujet |
| --- | --- | --- |
| 1 | [RNN](notebooks/sequence_models/RNN.ipynb) | Prédire une série sinusoïdale avec un réseau récurrent simple. |
| 2 | [LSTM](notebooks/sequence_models/LSTM.ipynb) | Réaliser la même prédiction avec une mémoire LSTM. |
| 3 | [Transformer](notebooks/sequence_models/Transformer.ipynb) | Utiliser un encodeur Transformer et des positions apprises. |
| 4 | [BERT](notebooks/language_models/BERT.ipynb) | Prédire un token masqué avec BERT multilingue. |
| 5 | [GPT](notebooks/language_models/GPT.ipynb) | Générer du texte avec GPT-2. |

Chaque notebook est autonome : exécuter ses cellules dans l'ordre, du début à la fin.

## Deuxième partie : exercices corrigés

| Exercice | Notebook | Contenu |
| --- | --- | --- |
| 1 | [Prévision électrique](notebooks/exercises/01_energy_transformer.ipynb) | EnergyTransformer, validation chronologique, MAE/RMSE en kW et deux références. |
| 2 | [Mini-GPT](notebooks/exercises/02_mini_gpt.ipynb) | Modèle causal par caractères entraîné depuis zéro, test de causalité et comparaison des températures. |
| 3 | [Mini-BERT](notebooks/exercises/03_mini_bert.ipynb) | Modèle bidirectionnel par mots, masquage 80/10/10, test du padding et exactitude de validation. |

Les solutions incluent le code, les résultats d'exécution, les graphiques et les réponses aux questions.
Le [corpus original](notebooks/exercises/corpus.txt) est partagé par les exercices 2 et 3.
Pour l'exercice 1, télécharger le jeu [Individual Household Electric Power Consumption sur UCI](https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption)
et décompresser `household_power_consumption.txt` à la racine du dépôt. Ce fichier volumineux reste local.
Les exercices utilisent uniquement la bibliothèque standard, NumPy, Matplotlib et PyTorch, déjà prévus dans l'environnement.
L'entraînement s'exécute sur CPU ou sur CUDA si disponible ; sa durée dépend du matériel.

## Installation

Prérequis : Python 3.11 ou supérieur et [uv](https://docs.astral.sh/uv/).

```sh
uv sync --locked
```

Ouvrir un notebook dans VS Code avec les extensions Python et Jupyter, puis sélectionner l'interpréteur du dossier `.venv` comme noyau.

Les notebooks RNN, LSTM et Transformer génèrent leurs données avec PyTorch. Les notebooks BERT et GPT téléchargent leurs modèles préentraînés au premier lancement et nécessitent alors une connexion Internet.
=======

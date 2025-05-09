# Comparaison des architectures RNN

Projet comparant les performances de SimpleRNN, LSTM et GRU sur l'analyse de sentiments (dataset IMDB).

## Structure
```
.
├── Comparaison_RNN_LSTM_GRU.ipynb          # Notebook Jupyter
├── models/                                 # Modèles sauvegardés
└── README.md                               # Ce fichier
```

## Prérequis
- Python 3.8+
- Jupyter Notebook
- Bibliothèques :
  ```bash
  pip install tensorflow matplotlib numpy
  ```


## Dataset
- IMDb dataset from tensorflow.keras.datasets.imdb
- 50,000 movie reviews (25k for training, 25k for testing)
- Labels: 1 for positive, 0 for negative
- Limited vocabulary: Top 5,000 most frequent words


## Utilisation
1. Exécuter le notebook :
   ```bash
   jupyter notebook Comparaison_RNN_LSTM_GRU.ipynb
   ```
2. Les modèles sont sauvegardés dans `models/` pour éviter un nouvel entraînement à chaque exécution du code (gain de temps).

## Résultats Attendus
| Architecture | Val Accuracy | Temps/Epoch |
|--------------|-------------|------------|
| SimpleRNN    | ~80-82%     | 45s        |
| LSTM         | ~87-89%     | 1min       |
| GRU          | ~86-88%     | 55s        |

## Exemple de Sortie
```python
=== Prédictions LSTM ===
"This movie was a masterpiece..." → POSITIF (0.92)
"I've never seen something so..." → NEGATIF (0.08)
```
## 📚 Références

#### **Documentation Officielle**
1. [TensorFlow Keras RNN Documentation](https://www.tensorflow.org/api_docs/python/tf/keras/layers/RNN)
2. [IMDB Dataset Documentation](https://www.tensorflow.org/api_docs/python/tf/keras/datasets/imdb)

#### **Articles Fondamentaux**
- Hochreiter, S., & Schmidhuber, J. (1997). [Long Short-Term Memory](http://www.bioinf.jku.at/publications/older/2604.pdf)  
  *(Paper original sur les LSTM)*
- Cho et al. (2014). [Learning Phrase Representations using RNN Encoder-Decoder](https://arxiv.org/abs/1406.1078)  
  *(Introduction des GRU)*

#### **Tutoriels Recommandés**
- [Understanding LSTM Networks](https://colah.github.io/posts/2015-08-Understanding-LSTMs/) (Christopher Olah)
- [Keras RNN Guide](https://keras.io/guides/working_with_rnns/)

#### **Livres**
- Géron, A. (2022). *Hands-On Machine Learning with Scikit-Learn, Keras and TensorFlow* (Ch. 15)
- Chollet, F. (2021). *Deep Learning with Python* (Ch. 6)

#### **Citations des Librairies**
```bibtex
@misc{tensorflow2015-whitepaper,
  title={ {TensorFlow}: Large-Scale Machine Learning on Heterogeneous Systems},
  url={https://www.tensorflow.org/},
  note={Software available from tensorflow.org},
  author={Google Research},
  year={2015}
}
```

#### **Dataset Citation**
```bibtex
@article{maas2011imdb,
  title={Learning Word Vectors for Sentiment Analysis},
  author={Maas, Andrew L. and Daly, Raymond E. and Pham, Peter T. and Huang, Dan and Ng, Andrew Y. and Potts, Christopher},
  journal={ACL},
  year={2011}
}
```
## Licence
MIT

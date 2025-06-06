# Guida all'utilizzo del notebook
Puoi eseguire il comando
  ```console
  pip install -r requirements.txt
  ```
per installare i moduli necessari.  
Per ottenere il notebook a partire dal file `ml_vademecum.py`, vedi il paragrafo 'Conversioni' di seguito.

### Perché utilizziamo Jupytext?
Jupytext permette, tra le altre cose, di convertire qualsiasi notebook Jupyter in un file `.py` costituito solo dal contenuto effettivo del notebook e privo di tutti i metadati che i file `.ipynb` si trascinano dietro. In questo modo, versioniamo solo ciò che è strettamente necessario.

## Utilizzo di Jupytext
### Conversioni
- Da `.ipynb` a  `.py` :
  
  ```console
  jupytext --to py notebook.ipynb 
  ```
- Da `.py` a  `.ipynb` :
  
  ```console
  jupytext --to notebook notebook.py
  ```
### Sincronizzazione
Jupytext permette di creare una coppia sincronizzata di notebook ipynb/py, e offre una modalità `--sync` che aggiorna automaticamente il file meno recente della coppia.  
Per convertire `notebook.ipynb` in una coppia sincronizzata di notebook ipynb/py:
```console
jupytext --set-formats ipynb,py notebook.ipynb
```
Per aggiornare il file meno recente della coppia (non importa quale dei due viene specificato):
```console
jupytext --sync notebook.ipynb
```

[Qui](https://jupytext.readthedocs.io/en/latest/using-cli.html) si trova una serie di comandi utili, tra cui quelli presentati.


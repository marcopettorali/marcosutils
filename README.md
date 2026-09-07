# Marco's Utils

Repository contenitore per alcune utility mantenute come Git submodule.

## Repository inclusi

- [probdist](https://github.com/marcopettorali/probdist)
- [editplot](https://github.com/marcopettorali/editplot)

## Clone

```bash
git clone --recurse-submodules https://github.com/marcopettorali/marcosutils.git
```

Se hai gia clonato la repo senza submodule:

```bash
git submodule update --init --recursive
```

## Aggiornamento submodule

Per aggiornare i submodule al commit piu recente del branch configurato:

```bash
git submodule update --remote --merge
git commit -am "Update submodules"
```

## Modificare la lista

La lista dei repository inclusi e definita in `.gitmodules`.

Per aggiungere una nuova repo:

```bash
git submodule add https://github.com/owner/repo.git repo
git commit -m "Add repo submodule"
```

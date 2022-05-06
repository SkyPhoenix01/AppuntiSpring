# Spring Boot

## Tabelle

### Professori

| ID | Name | Cognome | login |
| - | - | - | - |
| 41 | Francesco | Rossi | francescoRossi |


### Classi

| ID | Codice | Titolo |
| - | - | - |
| 02 | 2020 - 2021 | FullStack Developer |

### ProfessoriClassi

| ID | IdProfessore | IdClasse |
| - | - | - |
| 01 | 41 | 02 |

### Studenti

| ID | Name | Cognome | Login | idClasse |
| - | - | - | - | - |
| 05 | Gianluigi | Verdi | gianVerdi | 02 |
---
---

## Chiamate REST

### Login :heavy_check_mark:
---

### Lista Classi *Per la seleziona classi* :heavy_check_mark:
---

facciamo una chiamata GET con **idProfessore** e stampiamo tutte le classi che hanno il professore come docente
<!-- 
| idClasse | nomeClasse |
|-|-|
| 02 | FullStack Developer | -->

```json
    [
        {
            "idClasse": "02",
            "nomeClasse": "FullStack Developer"
        }
    ]
```


### Lista Repos :heavy_check_mark:
---
facciamo una chiamata POST con **loginProfessore**, **token** e facciamo una chiamata a GitHub per avere tutti i repos poi confrontiamo il campo login dei vari repos con i login degli **Studenti** la lista dovrà essere 

```json
    [
        {
            "idRepo": 01,
            "name": "Gianluigi",
            "surname": "Verdi",
            "login": "gianVerdi",
            "class": 02,
            "repoName": "prova",
            "link": "prova.com",
            "totaleCommit": 3,
            "creationDate": "2021-04-05",
            "lastUpdate": "2021-04-05"
        }
    ]
```

*P.S* per il totale commit facciamo una chiamata a GitHub per avere la lista dei commit e stampiamo il numero dei commit

### Lista Commit
---
```json
    [
        {
            "idRepo": 01,
            "name": "gianluigi",
            "surname": "Verdi",
            "repoName": "prova",
            "login": "gianVerdi",
            "creationDate": "2021-04-05",
            "lastUpdate": "2021-04-05",
            "commit": [
                {
                    "html_url": "www.commit.com",
                    "committer": {
                        "name": "gianluigi",
                        "email":"gianVerdi@email.com",
                        "date": "2022-05-05"
                    },
                    "message": "provaCommit"
                }
            ]
        }
    ]
```






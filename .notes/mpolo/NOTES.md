Info da slides:
The project consists in the design, development, and assessment of an ML system dealing with one "problem" chosen among a few options (examples).
the student delivers a description, not the software
the description is evaluated for clarity, technical soundness, (amount of) results

---

Un altro ragazzo di DSSC (penso del secondo anno) aveva cominciato progetto su twitter. Non so se può essere utile:
    * info [qui](https://docs.google.com/document/d/12KHF62Q4d9CncrE5ZiuP6Bd91HJf8jwq8Y7btIzUmtA/edit)
    * repo [qui](https://github.com/mechanapoleon/TwitterSentimentAnalysis)

---

3 file?? (OUTDATED):
1 preprocessing.ipynb
1 ?.ipynb for modelling and evaluation
1 .py for usage

anzi meglio IMO:
* 1 (o più) script/notebook per scaricare tweet (no input, dataset raw come output (più dataset?))
* 1 notebook dove si fa feature eng, assessment, e poi training su tutto dataset (unico input il dataset (o più dataset) raw, unico output il modello )
* 1 script per usare il modello (input il modello, output testuale)
---

fasi design pag 46 slides

---

imo solo assessment della learning technique $(f'_{learn}, f'_{predict})$ con cross validation e poi training su tutto dataset una volta finito "tuning". Ma usiamo random forest classifier perché easy è miglior punto di partenza stando alle slides. Quindi non serve neanche tuning hyperparameters (ok quelli di default) e la cosa migliore è sfruttare il tempo a disposizione per migliorare dataset e feature engineering.

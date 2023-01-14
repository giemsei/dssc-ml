Info da slides:
The project consists in the design, development, and assessment of an ML system dealing with one "problem" chosen among a few options (examples).
the student delivers a description, not the software
the description is evaluated for clarity, technical soundness, (amount of) results

Nostro progetto:
The goal is to build a tool for predicting how popular will be a tweet about food. There is no data available for this problem: the student is hence required to obtain it, if the proposed solution is based on data (likely it will be!)

---

Un altro ragazzo di DSSC (penso del secondo anno) aveva cominciato progetto su twitter. Non so se può essere utile:
    * info [qui](https://docs.google.com/document/d/12KHF62Q4d9CncrE5ZiuP6Bd91HJf8jwq8Y7btIzUmtA/edit)
    * repo [qui](https://github.com/mechanapoleon/TwitterSentimentAnalysis)

---

* fasi design pag 46 slides
* preprocessing pag 352 slides

---

Imo solo assessment della learning technique $(f'_{learn}, f'_{predict})$ con cross validation e poi training su tutto dataset una volta finito "tuning". Ma usiamo random forest classifier perché easy e miglior punto di partenza stando alle slides. Quindi non serve neanche tuning hyperparameters (ok quelli di default) e la cosa migliore è sfruttare il tempo a disposizione per migliorare dataset e feature engineering

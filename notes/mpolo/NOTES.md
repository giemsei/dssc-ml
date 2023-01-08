Info da slides:
The project consists in the design, development, and assessment of an ML system dealing with one "problem" chosen among a few options (examples).
the student delivers a description, not the software
the description is evaluated for clarity, technical soundness, (amount of) results

Nostro progetto:
The goal is to build a tool for predicting how popular will be a tweet about food. There is no data available for this problem: the student is hence required to obtain it, if the proposed solution is based on data (likely it will be!).

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
preprocessing pag 352 slides

---

imo solo assessment della learning technique $(f'_{learn}, f'_{predict})$ con cross validation e poi training su tutto dataset una volta finito "tuning". Ma usiamo random forest classifier perché easy è miglior punto di partenza stando alle slides. Quindi non serve neanche tuning hyperparameters (ok quelli di default) e la cosa migliore è sfruttare il tempo a disposizione per migliorare dataset e feature engineering.

---
da definire cosa è un tweet e cosa significa popular:

possibile definizione di popular:
media pesata like e retweet (eventualmente con pesi binari se semplifica, quindi solo like o solo retweet) diviso numero follower di chi lo scrive. Risultato messo in categorie (es.: low, medium, high popularity)

3 categorie basta e avanzano (già bene se si ottengono risultati così). definiscile così: prendi tutti i tweet del dataset e dividi like/retweet di ognuno per numero follower, ordini per valori ottenuti e dividi in 3 parti uguali ottenendo 3 range. Poi sistemi leggermente i range per ottenere numeri belli. Es se medium è tra 0.008032 e 0.031991, fai 0.008 e 0.032 cioè 8 e 32 like/retweet ogni mille follower, oppure 0.01 e 0.03 cioè 1 e 3 ogni 100 follower.

Ma non è detto che in media scalino linearmente con numero follower, potrebbero scalare linearmente con il suo logaritmo o con il quadrato, ecc. cioè bisognerebbe normalizzare dividendo per g(num_follower), ma g non la conosciamo e dobbiamo provare a ricavarla fittando tipo modello lineare num_follower vs media like per molti utenti (magari prima vedi graficamente).

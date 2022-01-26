# Decision-Trees-Random-Forest-loan-data

L'arbre 🌳 de décision est une méthode qui est simple pour classifier n'importe quel type de données. Cependant, ils souffrent d'une mauvaise capacité de généralisation (la capacité  à bien prédire sur les données de test). Pour combler cette lacune, une forêt de décision est un ensemble d'arbres de décision qui ont appris sur des échantillons de données différents (66% des données de l'ensemble d'apprentissage en général pour chacun-aléatoirement sélectionnés pour chaque arbre) et avec un ensemble de features différent pour chacun (sélectionné au hazard pour chaque arbre parmis l'ensemble des features disponibles). Une fois l'ensemble des arbres entrainés, ils procèdent à un vote pour prédire la classe d'une nouvelle donnée et la décision de la forêt de décision est alors la classe qui a reçu la majorité des votes. Plus le nombre d'arbres qui compose la forêt de décision est grand et plus le modèle est souple en général.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DiouaneAbdallah/Decision-Trees-Random-Forest-loan-data/blob/main/DecisionTreesRandomForest.ipynb)

Pour ce projet, nous allons travailler sur une dataset publique disponible sur [www.lendingclub.com](www.lendingclub.com). Lending club connecte les gens qui ont besoin d'argent (emprunteurs) avec les gens qui ont de l'argent (investisseurs). Etant donné, que vous êtes un investisseur, vous allez certainement investir dans les gens qui ont de grandes chances de vous rendre votre argent. Nous allons essayer de créer un modèle qui va vous aider à le faire.

Lending club a eu une année 2016 très lucrative avec plus de 500 millions de $ de profit.

Jetons donc un coup d'oeuil sur le données.

Nous allons utiliser les données de prêt entre 2007 et 2018en essayant de prédire et de classifier si un emprunteur particulier a remboursé son emprunt en totalité ou pas. Vous pouvez télécharger les données [ici](https://www.lendingclub.com/info/download-data.action) ou utiliser tout simplement le fichier csv. Le fichier csv est déjà nettoyé. 

Les colonnes représentes:
* credit.policy: 1 si le client répond aux critère de garantie de lendingclub.Com et 0 sinon
* purpose: L'objet de l'emprunt(qui prend les valeurs "credit_card":carte de crédit, "debt_consolidation": remboursement de dettes, "educational": éducation, "major_purchase": grand achat, "small_business": petit projet, and "all_other": tout autre besoin)
* int.rate: Le taux d'intérêt de l'emprunt, comme proportion (0.11 correpond à 11 %). Les emprunteurs qui sont jugés à risque ont un taux d'intérêt plus grand. 
* installment: Les mensualités payées par l'emprunteur si le crédit est approuvé.
* log.annual.inc: Le revenu annuel déclaré par l'emprunteur.
* dti: La proportion de la dette par rapport au revenu (dette/revenu annuel)
* fico: un score de crédit concernant l'emprunteur
* days.with.cr.line: Le nombre de jours pendant lesquels un emprunteur a eu une ligne de crédit
* revol.bal: Le montant impayé pendant un cycle pour une carte de crédit
* revol.util: La fraction du montant de la ligne de crédit utilisé par rapport au montant total disponible
* inq.last.6mths: Le nombre de demande de renseignement remplis par l'emprunteur pour obtenir un prêt les 6 derniers mois
* delinq.2yrs: le nombre de fois que l'emprunteur a dépasse la date limite de payement pendant les 2 dernières années
* pub.rec: Le nombre de documents publics concernant l'emprunteur (faillite, impôts, procès)

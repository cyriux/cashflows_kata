# cashflows_kata

A kata to learn finance fundamentals while coding, in the purest Domain-Driven Design spirit

# Introduction Text supposedly from a Finance Encyclopedia


Avec les factures émises on projette des encaissements attendus.

Avec celles reçues ou les bons de commande on projette les décaissements.

On peut ajouter des prédictions (par exemples projections de ventes).

Avec les mouvements projetés on calcule l’échelle de trésorerie.

Si y’a des excès ou des trous alors on doit prévoir d’aller sur le marché pour placer ou emprunter. 

Si des mouvements dans des devises non internes alors il faut prévoir des changes.

Puis avec les relevés bancaires on a les mouvements réels à comparer avec le prévu. 

Par dessus tout ça on peut optimiser et simuler des scénarios pour anticiper des risques. Et on peut évaluer la performance financière.

--
La finance de marché c’est l’autre côté : quand un client a un besoin (épargner / emprunter / changer des devises / lisser des flux / se protéger d’un risque incertain alors le client demande au sales un devis

Le sales passe au trader qui donne le prix

Si le client accepte alors on confirme, puis on livre le produit financier. 

Ensuite c’est comme de l’épicerie : il faut racheter ce qu’on a vendu (hedging, ou couverture). 

Mais comme les produits ont une durée (comme des assurances), il faut s’occuper de calculer et payer / recevoir les flux des produits au fil du temps aussi.


# Potential Sub-domains (and contexts)

- Sales predictions
- Sales
- Invoicing
- Procurement
- Customer Bookkeeping
- Treasury Management
- FX Change Management
- Financial Optimization
- Financial Simulation
- Risk Hedging


# Preliminary Questions

- Read the text, suggest potential bounded contexts out of it
- Identify the 2-4 main concepts for each
- Discuss about how to implement the whole thing, across all the various sub-domains/contexts  

# Kata steps

Let's start gentle and familiar.

## Book-keeping

"Account" of "Cashflows"
cashflow = {amount}

cashflow addition
balance = sum of all cashflows overall
merge of sub-accounts


## Treasury Management

"CashflowSequence" of "Cashflows"
cashflow = {date, amount}

cashflow addition only for the same date
merge of sequences
daily balances, within a 3-week time window


## Valuating a business line to be sold - Discounting 

// TBD


# Going further


## FX Change Management
 
cashflow addition only for the same date and currency
merge of sequences
weekly balances, over the next 4 weeks


## Fiscal Optimization

cashflow addition only for the same date and nature
merge of sequences
annual balance by nature


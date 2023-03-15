# HDH Graph Databases

Run deze instructie:

- vanaf een OND
- zonder Pulse
- zonder Caleidos, dus via een hotspot


## Installatie repo

- clone de repo van github
- `poetry install`

## Installatie Neo4j Desktop

- installeer Neo4J Desktop via https://neo4j.com/download/
- start neo4j en voeg de key toe die je krijgt op de download pagina
- maak nieuw project
- Voeg Local DBMS toe via Add
- Start DBMS

- Voeg remote DBMS toe met de volgende credentials
  - NEO4J_URI=neo4j+s://<to be disclosed during hdh>.databases.neo4j.io
  - NEO4J_USERNAME=neo4j
  - NEO4J_PASSWORD=<to be disclosed during hdh>
  - AURA_INSTANCENAME=form13


Bekijke https://docs.google.com/presentation/d/1WvPzs_JEh8uuKEAQGecH1rUd1NoRzqZIKc-hQkuBdXQ/edit?usp=sharing

## Upload en browse data

Bekijk https://docs.google.com/presentation/d/1O6Oy_GbDYYCvQanUyUCl30hQdSsy9kKL53Jgl23Nnsk/edit?usp=sharing

Volg de instructies op https://github.com/neo4j-partners/hands-on-lab-neo4j-and-vertex-ai/tree/main/Lab%203%20-%20Moving%20Data
met de lokale dbs en stop bij "A Year of Data".

Wij hebben "A Year of Data" voor je gereed gezet op de remote DBMS; de lokale dbms is te klein.
## Exploratie

Open Bloom van de Remote DBMS via Neo4j Desktop en volg de instructies op
- https://github.com/neo4j-partners/hands-on-lab-neo4j-and-vertex-ai/tree/main/Lab%204%20-%20Exploration
- exploring_cypher.ipynb
- exploring_pandas.ipynb

## Graph Data Science

Bekijk https://docs.google.com/presentation/d/133tXAH--V7Uvyd0Ylhs08_xDEPfl64uvaNNdxeHVpvk/edit?usp=sharing

- Volg embeddings.ipynb
- Nu is het moment gekomen om onze graph embeddings aan het voorspellingsmodel toe te voegen en te proberen te
  voorspellen welke holdings door de vermogensbeheerders zullen worden geschrapt. Gebruik je favoriete classifier
  en creativiteit! :)
- Deze code kan je waarschijnlijk helpen met het opschonen en voorbereiden van de
  data: https://github.com/neo4j-partners/neo4j-sec-edgar-form13/blob/main/featurize/featurize.py
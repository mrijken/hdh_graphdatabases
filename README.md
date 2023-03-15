# HDH Graph Databases

## Installatie

Run deze instructie:

- vanaf een OND
- zonder Pulse
- zonder Caleidos, dus via een hotspot

### Installatie repo

- clone de repo van github XXX
- `poetry install`

### Neo4j sandbox & AuraDB

- ga naar https://sandbox.neo4j.com
- maak een account

#### AuraDB
- Niet start een nieuwe project maar click grijs knopje "Start Free on AuraDB" aan de rechterkant
- klick door "start free"
- je moet inloggen met de sandbox wachtword
- aan de linkerkant kies AuraDS instances (AuraDS, niet DB) en click een "new instance" knopje

- geef de volgende waarden op:
    - Instance name = form13
    - Number of nodes = 500000
    - Number of relationships = 1000000
    - tick "Node Embedding" plaatje aan

- click door naar calculate estimate en verder create instance
    - je kan gevraagd worden om de Credit Card gegevens in te vullen (zal niet gecharged worden)
- vergeet niet de DB wachtwoord te kopieren

### Upload de data
- als de DB instance is aangemaakt en draait, klik dan op het query knopje - dat opent de query-editor in het nieuwe browservenster
- heir heb je de DB wachtwoord nodig om connectie te maken
- als connectie is gelukt, kan je de data uploaden, volg dan deze instructies https://github.com/neo4j-partners/hands-on-lab-neo4j-and-vertex-ai/tree/main/Lab%203%20-%20Moving%20Data

### Graph Data Exploration
- om visuele (graph) data exploratie te doen, click het "Bloom" knopje op de DB console pagina
- volg deze instructies: https://github.com/neo4j-partners/hands-on-lab-neo4j-and-vertex-ai/blob/main/Lab%204%20-%20Exploration/README.md

### Node Embeddings

- open en run de `node_embeddings.ipynb` notebook om de graph embeddings aan te maken
- als je klaar bent en de `embedding.csv` is opgeslagen, kan je de AuraDB instance stoppen
- ga terug naar de AuraDB console window en druk rood prullenbak knopje
- controleer of de DB instance is vernietigd (er zijn geen instanties meer zichtbaar op de pagina)

### Data Science
- Nu is het moment gekomen om onze graph embeddings aan het voorspellingsmodel toe te voegen en te proberen te voorspellen welke holdings door de vermogensbeheerders zullen worden geschrapt. Gebruik je favoriete classifier en creativiteit! :)
- Deze code kan je waarschijnlijk helpen met het opschonen en voorbereiden van de data: https://github.com/neo4j-partners/neo4j-sec-edgar-form13/blob/main/featurize/featurize.py
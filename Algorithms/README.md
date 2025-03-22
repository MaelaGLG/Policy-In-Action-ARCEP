
## Algorithmes

### Algorithme Google Scholar 

Nous avons développé un premier algorithme en Python qui effectue une recherche automatisée sur Google Scholar en utilisant des paramètres facilement modifiables. L'algorithme calcule la pertinence des articles en identifiant les mots communs entre le sujet d'intérêt (la requête) et le titre des articles scientifiques. Les articles sont ensuite triés, et le score de pertinence est combiné avec l'année de publication et le nombre de citations pour déterminer l'ordre des résultats. Pour chaque article sélectionné, l'algorithme webscrape et nettoie le texte complet de l'abstract via Selenium. Finalement, les résultats sont exportés sous forme de tableau récapitulatif dans un fichier Excel téléchargeable à la fin du document. 

### Algorithme NewsAPI 

Le deuxième algorithme en Python que nous avons développé effectue une recherche automatisée d'articles d'actualité en utilisant l'API de NewsAPI avec des paramètres facilement modifiables. Il récupère les articles correspondant aux mots-clés spécifiés et extrait leurs métadonnées (titre, langue, source, date de publication, lien). Les articles sont ensuite triés par date de publication pour afficher les résultats les plus récents en priorité. Il récupère le texte intégral de chaque article et filtre automatiquement les articles dont le contenu est trop court ou inaccessible afin d'améliorer la qualité des résultats. Enfin, les articles valides sont exportés sous forme de fichier Excel.
___


## Algorithms

### Google Scholar Algorithm

We have developed a first Python algorithm that performs an automated search on Google Scholar using easily modifiable parameters. The algorithm calculates the relevance of the articles by identifying the common words between the topic of interest (the query) and the titles of the scientific articles. The articles are then sorted, and the relevance score is combined with the publication year and the number of citations to determine the order of the results. For each selected article, the algorithm webscrapes and cleans the full abstract text using Selenium. Finally, the results are exported as a summary table in a downloadable Excel file at the end of the document.

### NewsAPI Algorithm

The second Python algorithm we developed performs an automated search for news articles using the NewsAPI API with easily modifiable parameters. It retrieves articles matching the specified keywords and extracts their metadata (title, language, source, publication date, link). Articles are then sorted by publication date to display the most recent results first. It retrieves the full text of each article and automatically filters out articles whose content is too short or inaccessible to improve the quality of the results. Finally, valid articles are exported as Excel files.

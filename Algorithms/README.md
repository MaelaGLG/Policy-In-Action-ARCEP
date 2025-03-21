
## Algorithmes

### Algorithme Google Scholar 

Nous avons développé un algorithme en Python qui effectue une recherche automatisée sur Google Scholar en utilisant des paramètres facilement modifiables. L'algorithme calcule la pertinence des articles en identifiant les mots communs entre le sujet d'intérêt (la requête) et le titre des articles scientifiques. Les articles sont ensuite triés, et le score de pertinence est combiné avec l'année de publication et le nombre de citations pour déterminer l'ordre des résultats. Pour chaque article sélectionné, l'algorithme webscrape et nettoie le texte complet de l'abstract via Selenium. Finalement, les résultats sont exportés sous forme de tableau récapitulatif dans un fichier Excel téléchargeable à la fin du document. 

### Algorithme NewsAPI 

Nous avons également développé un autre algorithme en Python qui effectue celui-ci une recherche automatisée d'articles d'actualité en utilisant l'API de NewsAPI avec des paramètres facilement modifiables. L'algorithme récupère les articles correspondant aux mots-clés spécifiés et extrait leurs métadonnées (titre, langue, source, date de publication, lien). Les articles sont ensuite triés par date de publication pour afficher les résultats les plus récents en priorité. Pour enrichir l'analyse, l'algorithme tente de récupérer le texte intégral de chaque article en utilisant la bibliothèque newspaper3k. Les articles dont le contenu est trop court ou inaccessibles sont automatiquement filtrés afin d'améliorer la qualité des résultats. Enfin, les articles valides sont exportés sous forme de fichier CSV, contenant les informations essentielles ainsi que le texte complet des articles sélectionnés. Un aperçu des premiers résultats est également affiché directement en sortie du script.

___


## Algorithms

### Google Scholar Algorithm

We have developed a Python algorithm that performs an automated search on Google Scholar using easily modifiable parameters. The algorithm calculates the relevance of the articles by identifying the common words between the topic of interest (the query) and the titles of the scientific articles. The articles are then sorted, and the relevance score is combined with the publication year and the number of citations to determine the order of the results. For each selected article, the algorithm webscrapes and cleans the full abstract text using Selenium. Finally, the results are exported as a summary table in a downloadable Excel file at the end of the document.

### NewsAPI Algorithm

We have also developed another Python algorithm that performs an automated search for news articles using the NewsAPI with easily adjustable parameters. The algorithm retrieves articles matching the specified keywords and extracts their metadata (title, language, source, publication date, and link). The articles are then sorted by publication date to prioritize the most recent results. To enhance the analysis, the algorithm attempts to retrieve the full text of each article using the newspaper3k library. Articles with content that is too short or inaccessible are automatically filtered out to improve result quality. Finally, the valid articles are exported as a CSV file, containing essential information along with the full text of the selected articles. A preview of the first results is also displayed directly in the script output.

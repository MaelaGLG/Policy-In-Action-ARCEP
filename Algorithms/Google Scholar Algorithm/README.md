# Collection of Articles using Google Scholar

### Author: Maela Guillaume-Le Gall

---

Ce code effectue une recherche automatisée sur Google Scholar en utilisant les paramètres définis dans la première section **"Configuration"**. L'algorithme calcule la pertinence des articles en identifiant les mots communs entre la requête et le titre de l'article. Les articles sont ensuite triés, et le score de pertinence est combiné avec l'année de publication et le nombre de citations pour déterminer l'ordre des résultats. Pour chaque article sélectionné, l'algorithme webscrape et nettoie le texte complet de l'abstract via Selenium. Finalement, **les résultats sont exportés sous forme de tableau dans un fichier Excel téléchargeable à la fin du document.**

Les paramètres de **Configuration** peuvent être facilement modifiés dans la première cellule de code :
- requête = **query**
- nombre d'articles à récupérer = **NUM_FETCH**
- année minimale = **MIN_YEAR**
- nombre d'articles à exporter = **NUM_SELECT**

*Le nombre d'articles à récupérer doit toujours être supérieur au nombre d'articles à exporter, car certains articles peuvent être exclus s'ils sont antérieurs à la date minimale (MIN_YEAR) ou en raison de mécanismes anti-bot. Il est recommandé d'indiquer un NUM_FETCH supérieur d'au moins un tiers à NUM_SELECT.*

---

This code performs an automated search on Google Scholar using the parameters defined in the first **"Configuration"** section. The algorithm calculates the relevance of articles by identifying the common words between the query and the article title. The articles are then sorted, and the relevance score is combined with the publication year and the number of citations to determine the order of the results. For each selected article, the algorithm webscrapes and cleans the full abstract text using Selenium. Finally, **the results are exported as a table in a Excel file downloadable at the end of the document.**

The **Configuration** parameters can be easily modified in the first code cell:
- query = **query**
- number of articles to fetch = **NUM_FETCH**
- minimum publication year = **MIN_YEAR**
- number of articles to export = **NUM_SELECT**

*The number of articles to fetch should always be greater than the number of articles to export, as some articles may be excluded if they are older than the minimum date (MIN_YEAR) or due to anti-bot mechanisms. It is recommended to set NUM_FETCH to at least one third more than NUM_SELECT.*


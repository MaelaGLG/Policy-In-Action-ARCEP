
# Collection of Articles using NEWSAPI

### Authors: Julian Rojas & Rafaël Mourouvin

---

Ce script effectue une recherche automatisée d'articles d'actualité sur l'impact environnemental de l'intelligence artificielle en utilisant l'API de NewsAPI. Il récupère des articles en anglais et en français selon les mots-clés spécifiés.  

L'algorithme extrait les métadonnées des articles (Title, Source, Raw Date, Parsed Date, Link) et les classe par ordre chronologique grâce à la variable `SORT_BY="publishedAt"`. Ensuite, il tente de récupérer le texte intégral de chaque article via la fonction `get_full_article_text(url)`, qui utilise la bibliothèque **newspaper3k**.  

Les articles dont le contenu est trop court ou inaccessibles sont automatiquement filtrés grâce à la condition `df_articles[~df_articles["Full Article Text"].str.startswith("Error fetching article")]` afin de garantir la qualité des résultats.  

Les résultats finaux sont sauvegardés sous forme de fichier **CSV** (`ai_environmental_impact_articles_FULLTEXT.csv`) contenant les informations essentielles ainsi que le texte complet des articles valides. L'affichage des premiers résultats est également proposé en sortie du script via `print(df_articles[['Parsed Date', 'Language', 'Title', 'Source', 'Link', 'Full Article Text']].head(40))`.  

**Paramètres de configuration dans le code**  

- **Mots-clés de recherche** :`QUERY_EN = "AI environmental impact"` en anglais et `QUERY_FR = "impact environnemental de l'IA"` en français.  
- **Langues analysées** : `LANGUAGES = {"en": QUERY_EN, "fr": QUERY_FR}` (Anglais et Français).  
- **Nombre d'articles récupérés par requête** : `PAGE_SIZE=60`.  
- **Critère de tri des résultats** : `sortBy="publishedAt"`, pour classer les articles du plus récent au plus ancien.  
- **Filtrage des articles invalides** : `df_articles[~df_articles["Full Article Text"].str.startswith("Error fetching article")]`.  
- **Exportation des résultats** : `df_articles.to_csv(OUTPUT_FILENAME, index=False, encoding='utf-8-sig')`.  

---

This script performs an automated search for news articles on the environmental impact of artificial intelligence using the NewsAPI. It retrieves articles in English and French based on the specified keywords.

The algorithm extracts metadata from the articles (Title, Source, Raw Date, Parsed Date, Link) and sorts them chronologically using the variable `SORT_BY="publishedAt"`. Then, it attempts to retrieve the full text of each article through the function `get_full_article_text(url)`, which uses the **newspaper3k** library.

Articles with content that is too short or inaccessible are automatically filtered using the condition `df_articles[~df_articles["Full Article Text"].str.startswith("Error fetching article")]` to ensure the quality of the results.

The final results are saved as a **CSV** file (`ai_environmental_impact_articles_FULLTEXT.csv`), containing essential information along with the full text of valid articles. The first results are also displayed as script output using `print(df_articles[['Parsed Date', 'Language', 'Title', 'Source', 'Link', 'Full Article Text']].head(40))`.

**Configuration parameters in the code**

- **Search keywords** : `QUERY_EN = "AI environmental impact"` in english and `QUERY_FR = "impact environnemental de l'IA"` in french.
- **Analyzed languages** : `LANGUAGES = {"en": QUERY_EN, "fr": QUERY_FR}` (English and French).
- **Number of articles retrieved per query** : `PAGE_SIZE=60`.
- **Sorting criterion** : `sortBy="publishedAt"`, to order articles from most recent to oldest.
-  **Filtering invalid articles** : `df_articles[~df_articles["Full Article Text"].str.startswith("Error fetching article")]`.
- **Exporting results**  : `df_articles.to_csv(OUTPUT_FILENAME, index=False, encoding='utf-8-sig')`.

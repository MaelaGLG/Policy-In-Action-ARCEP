Collection of Articles using NEWSAPI

Ce script effectue une recherche automatisée d'articles d'actualité sur l'impact environnemental de l'intelligence artificielle en utilisant l'API de NewsAPI. Il récupère des articles en anglais et en français selon les mots-clés spécifiés.  

L'algorithme extrait les métadonnées des articles (Title, Source, Raw Date, Parsed Date, Link) et les classe par ordre chronologique grâce à la variable `sortBy="publishedAt"`. Ensuite, il tente de récupérer le texte intégral de chaque article via la fonction `get_full_article_text(url)`, qui utilise la bibliothèque **newspaper3k**.  

Les articles dont le contenu est trop court ou inaccessibles sont automatiquement filtrés grâce à la condition `df_articles[~df_articles["Full Article Text"].str.startswith("Error fetching article")]` afin de garantir la qualité des résultats.  

Les résultats finaux sont sauvegardés sous forme de fichier **CSV** (`ai_environmental_impact_articles_FULLTEXT.csv`) contenant les informations essentielles ainsi que le texte complet des articles valides. L'affichage des premiers résultats est également proposé en sortie du script via `print(df_articles[['Parsed Date', 'Title', 'Source', 'Link', 'Full Article Text']].head(20))`.  

**Paramètres de configuration dans le code**  

- **Mots-clés de recherche** : `"AI environmental impact"` (`query="AI environmental impact"`) pour l'anglais et `"impact environnemental de l'IA"` (`query="impact environnemental de l'IA"`) pour le français.  
- **Langues analysées** : `language="en"` (anglais) et `language="fr"` (français).  
- **Nombre d'articles récupérés par requête** : `pageSize=20`.  
- **Critère de tri des résultats** : `sortBy="publishedAt"`, pour classer les articles du plus récent au plus ancien.  
- **Filtrage des articles invalides** : `df_articles[~df_articles["Full Article Text"].str.startswith("Error fetching article")]`.  
- **Exportation des résultats** : `df_articles.to_csv("ai_environmental_impact_articles_FULLTEXT.csv", index=False, encoding='utf-8-sig')`.  

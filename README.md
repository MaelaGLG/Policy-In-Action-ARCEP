# Policy In Action DEPP-ARCEP : L'Impact Environmental de l'IA

Ce projet est le fruit d'une collaboration entre le MSc&T "Data and Economics for Public Policy" (École Polytechnique, ENSAE & Télécom Paris) et l'ARCEP (Autorité de régulation des communications électroniques, des postes et de la distribution de la presse).

Dans ce cadre, un défi a été proposé aux étudiant·es du master : évaluer l'impact environnemental de l'IA et développer des outils pour actualiser ces connaissances en intégrant les nouvelles publications sur le sujet.

## Les algorithms

### Algorithme Google Scholar

Nous avons développé un premier algorithme en Python qui effectue une recherche automatisée sur Google Scholar en utilisant des paramètres facilement modifiables. L'algorithme calcule la pertinence des articles en identifiant les mots communs entre le sujet d'intérêt (la requête) et le titre des articles scientifiques. Les articles sont ensuite triés, et le score de pertinence est combiné avec l'année de publication et le nombre de citations pour déterminer l'ordre des résultats. Pour chaque article sélectionné, l'algorithme webscrape et nettoie le texte complet de l'abstract via Selenium. Finalement, les résultats sont exportés sous forme de tableau récapitulatif dans un fichier Excel téléchargeable à la fin du document. 

### Algorithme NewsAPI 

Le deuxième algorithme en Python que nous avons développé effectue une recherche automatisée d'articles d'actualité en utilisant l'API de NewsAPI avec des paramètres facilement modifiables. Il récupère les articles correspondant aux mots-clés spécifiés et extrait leurs métadonnées (titre, langue, source, date de publication, lien). Les articles sont ensuite triés par date de publication pour afficher les résultats les plus récents en priorité. Il récupère le texte intégral de chaque article et filtre automatiquement les articles dont le contenu est trop court ou inaccessible afin d'améliorer la qualité des résultats. Enfin, les articles valides sont exportés sous forme de fichier Excel.


## La revue de littérature 

Nous avons réalisé une revue de la littérature qui analyse, à partir de l'état de l'art actuel, les effets environnementaux de l'IA. Pour ce faire, nous avons appliqué la méthodologie Life Cycle Assessment (LCA), qui couvre l’ensemble des étapes du cycle de vie d’un produit ou d’un processus. Son objectif est de quantifier et comparer les impacts environnementaux d’un système tout au long de son existence, depuis l’extraction des matières premières jusqu'à son traitement en fin de vie, en passant par ses phases d’utilisation, d’entretien et de transport.

Toutes les sources utilisées sont disponibles dans le dossier associé.

1. **Introduction**

2. **Impacts environnementaux négatifs directs de l’IA**
   - 2.1. Production
   - 2.2. Transport
   - 2.3. Phase d’utilisation
   - 2.4. Fin de vie des équipements

3. **Impacts environnementaux négatifs indirects de l’IA**
   - 3.1. Effets rebond matériels
   - 3.2. Effets rebond économiques
   - 3.3. Effets rebond sociétaux

4. **Contributions environnementales positives de l’IA**
   - 4.1. Efficacité énergétique dans les bâtiments et les processus industriels
   - 4.2. Intégration des énergies renouvelables
   - 4.3. Agriculture durable et de précision
   - 4.4. Gestion intelligente des déchets
   - 4.5. Surveillance environnementale et conservation de la biodiversité

5. **Considérations futures et stratégies d'atténuation**
   - 5.1. Cadres réglementaires
   - 5.2. Mécanismes de transparence
   - 5.3. Apports des sciences comportementales
   - 5.4. Tendances durables émergentes

6. **Conclusion**


## **Contributions**

Si vous souhaitez suggérer des améliorations, n’hésitez pas à nous contacter aux adresses suivantes :

- Julian Rojas-Rojas - julian.rojas@polytechnique.edu
- Maela Guillaume-Le Gall - maela.guillaume-le-gall@polytechnique.edu
- Rafaël Mourouvin - rafael.mourouvin@polytechnique.edu

## **Remerciements**

Nous tenons à remercier l'équipe de l'ARCEP pour avoir proposé ce défi et pour les feedbacks apportés au fil du projet. Par ailleurs, ce projet a été réalisé dans le cadre du MSc&T in Data and Economics for Public Policy et nous tenons à remercier nos directeurs de master, Pierre Boyer et Franck Malherbet, pour avoir organisé ce challenge avec l'ARCEP et pour leur suivi du projet.

## **Structure des fichiers**

```
├── README.md  
├── LICENSE <- Licence du dépôt (par défaut, MIT)  
├── Algorithms  
│   ├── Google Scholar Algorithm <- Algorithme de recherche d’articles académiques  
│   └── NewsAPI Algorithm <- Algorithme d'articles d'actualité
├── Literature review  
│   ├── Sources Articles <- Articles académiques et rapports institutionnels utilisés  
│   └── Final Report <- Rapport final et tableau récapitulatif des impacts environnementaux  

```
___


# Policy In Action DEPP-ARCEP: The Environmental Impact of AI

This project is the result of a collaboration between the MSc&T "Data and Economics for Public Policy" (École Polytechnique, ENSAE & Télécom Paris) and ARCEP (French Regulatory Authority for Electronic Communications, Postal Services, and Press Distribution).

As part of this initiative, a challenge was proposed to master's students: evaluate the environmental impact of AI and develop tools to continuously update this knowledge based on new publications

## The algorithms

### Google Scholar Algorithm

We have developed a first Python algorithm that performs an automated search on Google Scholar using easily modifiable parameters. The algorithm calculates the relevance of the articles by identifying the common words between the topic of interest (the query) and the titles of the scientific articles. The articles are then sorted, and the relevance score is combined with the publication year and the number of citations to determine the order of the results. For each selected article, the algorithm webscrapes and cleans the full abstract text using Selenium. Finally, the results are exported as a summary table in a downloadable Excel file at the end of the document.


### NewsAPI Algorithm

The second Python algorithm we developed performs an automated search for news articles using the NewsAPI API with easily modifiable parameters. It retrieves articles matching the specified keywords and extracts their metadata (title, language, source, publication date, link). Articles are then sorted by publication date to display the most recent results first. It retrieves the full text of each article and automatically filters out articles whose content is too short or inaccessible to improve the quality of the results. Finally, valid articles are exported as Excel files.


## Literature Review

We conducted a literature review assessing, based on the current state of research, the environmental effects of AI. To do so, we applied the Life Cycle Assessment (LCA) methodology, which aims to cover all stages of a product or process’s life cycle. The goal is to quantify and compare the environmental impacts of a system throughout its entire existence, from raw material extraction to its end-of-life treatment (landfilling, recycling…), including use, maintenance, and transportation phases.
All sources used are available in the associated folder.

Review Structure:

**1. Introduction**

**2. Direct Negative Environmental Impacts of AI**
2.1. Production
2.2. Transportation
2.3. Operation Phase
2.4. End-of-Life of Equipment

**3. Indirect Negative Environmental Impacts of AI**
3.1. Material Rebound Effects
3.2. Economic Rebound Effects
3.3. Societal Rebound Effects

**4. Positive Environmental Contributions of AI**
4.1. Energy Efficiency in Buildings and Industrial Processes
4.2. Renewable Energy Integration
4.3. Sustainable and Precision Agriculture
4.4. Intelligent Waste Management
4.5. Environmental Monitoring and Biodiversity Conservation

**5. Future Considerations and Mitigation Strategies**
5.1. Regulatory Frameworks
5.2. Transparency Mechanisms
5.3. Insights from Behavioral Sciences
5.4. Emerging sustainable trends

**6. Conclusion**



## **Contributions**

If you have suggestions for improvements, feel free to contact us at the following addresses:


- Julian Rojas-Rojas - julian.rojas@polytechnique.edu
- Maela Guillaume-Le Gall - maela.guillaume-le-gall@polytechnique.edu
- Rafaël Mourouvin - rafael.mourouvin@polytechnique.edu

## **Acknowledgments**

We would like to thank the ARCEP team for proposing this challenge and for the feedback they provided throughout the project. In addition, this project was carried out as part of the MSc&T in Data and Economics for Public Policy and we would like to thank our Master's supervisors, Pierre Boyer and Franck Malherbet, for organising this challenge with ARCEP and for monitoring the project.

## **File Structure**

```
├── README.md  
├── LICENSE <- Repository license (default: MIT)  
├── Algorithms  
│   ├── Google Scholar Algorithm <- Academic article retrieval algorithm  
│   └── NewsAPI Algorithm <- News Articles Algorithm   
├── Literature review  
│   ├── Sources Articles <- Academic papers and institutional reports used  
│   └── Final Report <- Final report and summary table of environmental impacts  

```

# EmoDIFT
A dataset for multi-label emotion detection in french tweets

## Description:
The EmoDIFT dataset was created as part of the CATCH project, funded by the ANR and the Normandy region (AAP ANR RA-SIOMRI 2021). The aim is to design tools for automatically understanding written testimonies from a population affected by the health and environmental fallout of an industrial incident. The case study for this project is the fire at the Lubrizol plant in Rouen on 19 September 2019.

This dataset includes tweets collected with the Twitter microblogging platform API, over a period corresponding to the 15 months following the fire at the Lubrizol plant in Rouen, i.e. from 19/09/2019 to 31/12/2020. It has then be compiled following three steps:
- the collection of over 90,496 tweets containing the word "Lubrizol"
- a filtering step to retain the 1,2508 tweets from the population affected
- the manual annotation of a random selection of 2,350 tweets

These 2,350 tweets have then been labelled for multi-label emotion recognition tasks by a human annotators. Each tweet have been annotated by three different annotators, each of which being instructed to read and to evaluate tweets with the goal of identifying a maximum of three emotions from a predefined set of emotion labels. If the emotions expressed within the tweet belong to multiple emotion registers, the annotator is required to rank them in order of importance. This order is based on the predominance of expressed emotions within the tweet. Specifically, the label associated with the dominant emotion is assigned a value of 1, while the second and third most dominant emotions are assigned values of 2 and 3, respectively. The ultimate goal of the annotation is to identify expressions of opinion, whether they are explicit (I’m scared), or implicit (Those are hydrocarbons in there, that’s dangerous), taking only the semantic information into consideration.

The predefined emotions labels has been selected from the second tier of Plutchik’s model of emotions. The following 6 emotions has been used: *anger*, *disgust*, *fear*, *surprise*, *sadness*, and *mistrust*. In addition, *irony* has been included as an optional label since irony has been shown to be an important clue for emotion classification. Furthermore, the labels *neutral* and *inexploitable* have been added to allow annotators to identify tweets that do not express any particular emotion or that are not relevant to our case study (for example, a tweet from a news media that has not been filtered in the pre-processing phase).

The final step has consisted to merge the three human annotations of each tweet to transforme emotions ranks into a level of presence. We do not give here the formula used for that purpose, but refer the reader to the article cited at the bottom of this note for more details.

## Contributors:
- Usman MALIK, LITIS lab., Univ Rouen Normandy, France (usmanmalik57@gmail.com)
- Hugo LEROGERON, Saagie, France (hugo.lerogeron@saagie.com)
- Leshanshui YANG, Saagie, France (leshanshui.yang@saagie.com)
- Simon BERNARD, LITIS lab., Univ Rouen Normandy, France (simon.bernard@univ-rouen.fr)
- Roman PICOT-CLEMENTE, Saagie, France (romain@saagie.com)
- Clément CHATELAIN, LITIS lab., INSA Rouen Normandy, France (clement.chatelain@insa-rouen.fr)
- Alexandre PAUCHET, LITIS lab., INSA Rouen Normandy, France (alexandre.pauchet@insa-rouen.fr)
- Jérôme CORTINOVIS, Atmo Normandie, France (jerome.cortinovis@atmonormandie.fr)

## Acknowledgments:
This work is part of the CATCH project (ANR-21-SIOM-0011), co-financed by the French National Research Agency (ANR) and by the the Normandy region through the RA-SIOMRI 2021 funding program.

## Article to cite
### Plain text
U. Malik, S. Bernard, A. Pauchet, C. Chatelain, R. Picot-Clémente and J. Cortinovis, "Pseudo-Labeling With Large Language Models for Multi-Label Emotion Classification of French Tweets," in IEEE Access, vol. 12, pp. 15902-15916, 2024, doi: 10.1109/ACCESS.2024.3354705. 

### Bibtex
````{verbatim}
@article{emodift,  
  author={Malik, Usman and Bernard, Simon and Pauchet, Alexandre and Chatelain, Clément and Picot-Clémente, Romain and Cortinovis, Jérôme},  
  journal={IEEE Access},  
  title={Pseudo-Labeling With Large Language Models for Multi-Label Emotion Classification of French Tweets},  
  year={2024},  
  volume={12},  
  number={},  
  pages={15902-15916},  
  doi={10.1109/ACCESS.2024.3354705}  
}
````

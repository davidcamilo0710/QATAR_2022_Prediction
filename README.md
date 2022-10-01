![16366925243845 (1)](https://user-images.githubusercontent.com/60159274/193369854-51e7c21f-228d-47b5-9b04-a0d39f37dd19.jpg)
<img width="1348" alt="Screen Shot 2022-09-30 at 3 15 39 PM" src="https://user-images.githubusercontent.com/60159274/193369758-9105f128-a3b1-4d06-9c21-361c327a69ff.png">

# World Cup QATAR 2022 Prediction: Project Overview

## Resources Used

## Data preparation and dataset creation

* Both datasets l1 and l2 were prepared for analysis and the creation of the training dataset of the Machine learning model. The preparation consists of fixing the na's values and removing the information of the teams that will not participate in the cup.

* From dataset L1, create training dataset l3 and inference dataset l4. l3 contains the names of the teams facing each other, the FIFA ranking of each team, and the rating of both teams' defense, midfield, and offense. On the other hand, the inference dataset contains the qualification of each team on its last FIFA date.

## EDA

From datasets l1 and l2, the notebooks n1 and n2 answer the questions listed below. These questions allow us to get an idea of the favorites to win the cup according to statistics.

* Which National soccer teams have the best offence?

![download-12](https://user-images.githubusercontent.com/60159274/193368513-18266a41-cef3-4dac-9273-dfecc0357b3e.png)

* Which National soccer teams have the best defence?

![download-8](https://user-images.githubusercontent.com/60159274/193368518-889e1672-d759-4e80-85e6-6de64f6f3e1c.png)

* Which National soccer team have the best midfield?

![download-11](https://user-images.githubusercontent.com/60159274/193368515-2a046f68-61a2-421d-9e74-b0420bd452e9.png)

* Which teams have the highest winning percentage?

![download-6](https://user-images.githubusercontent.com/60159274/193368516-68e21bf6-bc91-4759-80d9-767271dc0636.png)

* Who are the best players in Qatar 2022?

![download-2](https://user-images.githubusercontent.com/60159274/193378980-b2302754-6514-449d-b890-cce0a716a519.png)

* What are the most promising teams?

![download-5](https://user-images.githubusercontent.com/60159274/193368544-11f6f51f-2a2d-4812-af89-4eed5e71763d.png)

* Does it have any advantage to be the local team?

This question is fundamental. The graph below shows that the home teams win more than 50% of the home games. This is due to different reasons, e.g., the familiarity with the field of play, the movement that the visiting teams must make, the feeling of territoriality, the support of the public, and innumerable factors. When the Colombian National Team visits the Maracana stadium to play against Brazil, they tend to lose the match or draw. However, they tend to tie or win when Colombia is local in the Metropolitano stadium. For this reason, to predict the result of the matches from a Machine Learning model, I must define the home team and the visiting team.

![download-7](https://user-images.githubusercontent.com/60159274/193368561-dd1398c8-dcad-4575-b3aa-2f4a30719444.png)

## Modeling and Tuning

The n3 notebook aims to train the Machine learning model that will predict the outcome of the World Cup matches. This notebook chooses one ML model to predict the group stage matches and another for the knockout stage. the difference is that the result of the group stage matches can be a loss, a draw, or a win. On the other hand, in the direct elimination stage, there is only defeat or victory. The best model for each stage is chosen among the algorithms:

* Random Forest
* Ada Boost Classifier
* XGB Boost
* Neural Networks

The XGB Boost model presents the best performance in both stages. Therefore it is tuned, validated, and exported as a pipeline to perform easy inferences.

* Confusion matrix of the group stage model tuned and validated

![download-10](https://user-images.githubusercontent.com/60159274/193368594-3d6f69a8-cc6c-456c-9408-a2ebc1f72ee1.png)

* Confusion matrix of the knockout stage model tuned and validated

![download-9](https://user-images.githubusercontent.com/60159274/193368596-cbd0a492-7399-49af-be28-bd6c4a014694.png)

## Predictions

Finally, notebook n4 uses the inference datasets and the trained models to predict the World Cup matches and thus find the winner of the World Cup. It is essential to mention that to choose who is the home team in each World Cup match, use dataset l5, which provides the potential of each team; therefore, the team with more significant potential will be the home team.

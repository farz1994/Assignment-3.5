# Assignment-3.5
Assignment 3.5
Import the Titanic Dataset from the link Titanic Data Set.
Perform the following:
a. Is there any difference in fares by different class of tickets?
Note - Show a boxplot displaying the distribution of fares by class

Yes, the Fare is highest for first class tickets, moderate for second class and lowest for the third class.

boxplot(fare~pclass,data= titanic_dataset, main="Fare vs Pclass",xlab="Class",ylab="Fare",col=topo.colors(3))


b. Is there any association with Passenger class and gender?
Note – Show a stacked bar chart

No, there is no association with Pclass and Gender

library(ggplot2)
ggplot(titanic_dataset, aes(x = pclass, fill = factor(sex))) +
  geom_bar(stat='Count', position='stack') +
  labs(x = 'Pclass')

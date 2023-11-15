# Data_115
data set project
NFL <- read.csv("NFL_Yards_2022.csv")
linearNFL <- lm(Yards~Received, NFL)
summary(linearNFL)
ggplot(NFL, aes(x=Yards,y=Received)) +geom_point(color="blue") +geom_smooth(method="lm",formula=y~x,color='green') +labs(title = "Avg. Recieving yards by NFL teams")

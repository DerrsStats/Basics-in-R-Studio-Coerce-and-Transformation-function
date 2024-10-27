# Basics-in-R-Studio-Coerce-and-Transformation-function

# Coerce and Transformation function

#coercing from matrix to dataframe

stan=matrix(data=c(1,3,4,5,7,8),nrow=2,ncol=3,byrow = "true")

stan

stan.dataframe=as.data.frame(stan)

stan.dataframe

class(stan.dataframe)

stan.dataframe$v4=c(10,7)

stan.dataframe

#coercing from dataframe to list

stan.list= as.list(stan.dataframe)

stan.list

class(stan.list)

stan.list$v5="Dera"

stan.list

#Tranform function and how to use it

(brain<-subset(mtcars,carb==1,select=c(2,3,4,5)))

brain

class(brain)

brain$new=100:106

brain

transform(brain,old=cyl+new)

transform(brain, young=disp-hp)

transform(brain,fresh=disp)

(bye<-transform(brain,fresh=1-disp))

bye

bye=transform(bye,best=54:60)

bye

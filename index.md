# Header 01
## Header 02
### Header 03
#### Header 04
##### Header 05
###### Header 06

![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)

```
#The following code presents plotting issues on 'main', 'labels' and 'abline'
getwd()
name<-c('A','B','C','D','E','F','G','H','I')
id<-c(1,2,3,4,5,6,7,8,9)
marks_before<-c(15,11,3,15,18,2,3,5,8)
marks_after<-c(16,7,10,17,12,12,14,10,14)
attendance<-c(12,8,9,13,11,10,10,11,13)

df<-cbind.data.frame(name,id,marks_before,marks_after,attendance)

#pdf('attendance',title='Attendance',h=10,w=7)
par(mfrow=c(2,1))
with(df,plot(attendance,marks_before),
     main=c('R=',cor(df$marks_before,df$attendance)),
     xlab='Attendance',
     ylab='Marks before curriculum',
     abline(lm(marks_before~attendance,data=df))
)


with(df,plot(attendance,marks_after),
     main=c('R=',cor(df$marks_after,df$attendance)),
     ylab='Marks after curriculum',
     xlab='Attendance',
     abline(lm(marks_after~attendance,data=df))
)

#mtext='Evaluation of attendance effect on students marks'
#dev.off()

```

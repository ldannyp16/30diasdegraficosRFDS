# 30diasdegraficosRFDS
Create bar graph with ggplot

library(ggplot2)
poblacionssp<-read.table("D:/Econometrics/Poblacion_SSP.txt")
poblacionssp

colnames(poblacionssp)<-c("Fecha","S_servicios")
colnames(poblacionssp)
names(poblacionssp)
attach(poblacionssp)

summary(poblacionssp)


ggplot(data=poblacionssp, aes(x=Fecha,y=S_servicios)) + geom_bar(stat="identity",color="ROYALBLUE")+
  xlab("Año ")+
  ylab("Porcentaje de hogares sin acceso a servicios públicos")+
  ggtitle("Hogares en centros poblados y dispersos sin acceso a servicios públicos en Colombia")

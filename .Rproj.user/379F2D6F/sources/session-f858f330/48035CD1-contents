
## Load all geos
geos <- read.csv("./Datos/Geos_info.csv")

## Select only relevant columns
geos <- geos[,c(1,2,35,37)]
geos <- geos[(geos$Site == "Cueva de la Cocina" & 
               geos$Type.Fortea == "G18. Triángulo con dos lados cóncavos (tipo Cocina)") | 
               (geos$Site == "Cova Or"),]
geos <-na.omit(geos[geos$Reliability == 100,])

## randomly reduce dataset to ease the location of landmarks
set.seed(1)
geos <- geos[unique(round(runif(120,1,nrow(geos)))),]

## Save current data
write.csv(geos,"./Datos/geos_less.csv")

## Move .jpgs to current folder. Change paths as convenient

#index <- geos$ID

#for (i in 1:length(index)){
#  file.copy(from = paste0("/media/alfredo/1TB/Storage/INVESTIGACIO/TESIS/data/Z_TOT_ORDENAT/",index[i],"/GeoMorph/",index[i],".jpg"),
#                          to = paste0("./Shapes/",index[i],".jpg"), overwrite = TRUE)
#}


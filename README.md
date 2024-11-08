# Text mining
Dette repository indeholder digitale værktøjer til text mining, og er målrettet studerende uden eller med begrænset kendskab til programmering. Værktøjerne er udarbejdet som Shiny Apps, så brugerne kan benytte sig af dem via et genkendeligt interface uden at skulle konfronteres med den bagvedliggende kode. Værktøjerne kan derved ses som en indgangsvinkel for studerende, der ønsker at prøve kræfter med text mining. 

I denne version af værktøjet kan studerende mv. lære at bruge nogle af de forskellige funktioner, der er kendeteget ved text mining samt stifte bekendskab til forskellige visualiseringer, der relaterer sig hertil. Formålet med dette er at afmystificere text mining som analysetilgang og -værktøj, hvor visualiseringer og genkendelighed er i hovedsædet. I corpora mappen findes en række pre-klargjorte datasæt, såkaldte corpora, der alle indeholder en række tekster indenfor forskellige kategorier. Heriblandt eventyr af H.C Andersen og Brødrende Grimm samt romaner af Jane Austen. Her åbner de forskellige corpora op for forskellige analyser, hvor elementer som oversættelse mellem sprog, udvikling over tid, genre mm. kan spille ind. Her kan brugeren let skifte mellem de forskellige copora og tekster samt mellem de forskellige analyseredskaber og visualiseringer. Vi anbefaler at studerende mv. anvender de pre-klargjorte datasæt til at blive fortrolige med materialet og funktionerne, inden de selv prøver kræfter med værktøjet på deres eget data. Studerende mv. kan selv uploade en enkelt fil eller flere filer, der derefter fungerer som corpus til text mining. Her vil brugerne kunne anvende værktøjet til hurtigt at skabe overblik over en eller flere tekster i et corpus. Dette kan være en indgangsvinkel til videre analyse eller på anden vis fungere som et eksplorativt værktøj, der er med til at bidrage til nye måder at anskue tekster og corpora på. 

## Corpora
I denne mappe findes en række data, der relaterer sig til Text Mining. Hvert corpus stammer fra Det Kgl. Bibliotek eller Project Gutenberg og er uden for ophavsret. Se mere om Project Gutenberg her: https://www.gutenberg.org/ 

## Stopwords
I denne mappe findes henholdsvis en engelsk og en dansk stopordsliste. Det er her muligt at se, indholdet af de to stopordslister, der anvendes i text mining applikationen. 

## Sådan tilgås materialet
Det er muligt at køre text mining applikationen på to måder. Den ene måde er via Posit Cloud, hvor applikationen tilgås fra en browser og den anden måde er at køre det lokalt på ens egen computer.

## Tilgå materialet via en browser
### 1. Gå til Posit Cloud
Ønsker du at tilgå materialet fra en browser, skal du blot følge dette link: https://posit.cloud/plans/free. Her skal du enten oprette en gratis profil eller logge ind, hvis du allerede har en bruger.

### 2. Kør programmet
1. Lav et nyt RStudio projekt via 'New project' knappen
2. Lav et nyt R script under 'Files' --> 'New file'
3. Skriv følgende kode i scriptet:  
``` 
# Her tilgås pakkerne, der skal bruges for, at køre applikationen. Pakkerne udvider basisfunktionaliteten i R og gør det blandt andet muligt at åbne og arbejde med applikationer med en brugergrænseflade, hvilket er tilfældet med ShinyTextMining 
library(shiny)
library(thematic)
library(readtext)
library(writexl)
library(DT)
library(tidyverse)
library(tidytext)
library(quanteda)
library(quanteda.textstats)
library(ggraph)
library(igraph)
library(ggwordcloud)
library(tidygraph)

# Her fortæller vi R, at vi ønsker at åbne applikationen ShinyTextMining, der ligger på Github under AUL-Arts-Digital-Lab 
runGitHub("ShinyTextMining", "AUL-Arts-Digital-Lab")
```
4. Kør koden ved at trykke shift, ctrl og enter
5. Du kan nu tilgå text mining applikationen

## Tilgå materialet lokalt
### 1. Installer R
Download den nyeste version af R ned på din computer. Husk at vælg en version, der passer til din computers styresystem. R er et ’sprog’ vi skal bruge til at programmere med.
<br> R kan downloades her: https://posit.co/download/rstudio-desktop/
### 2. Installer RStudio
Download den nyeste version af RStudio ned på din computer. Husk at vælg en version, der passer til din computers styresystem. RStudio er selve applikationen, hvori vi skriver vores kode. Det er RStudio vi åbner, når vi skal programmere.
<br> RStudio kan downloades her: https://posit.co/download/rstudio-desktop/

### 3. Kør programmet
1. Lav et nyt R script under filer/files 
2. Skriv følgende kode:  
``` 
# Her tilgås pakkerne, der skal bruges for, at køre applikationen. Pakkerne udvider basisfunktionaliteten i R og gør det blandt andet muligt at åbne og arbejde med applikationer med en brugergrænseflade, hvilket er tilfældet med ShinyTextMining 
library(shiny)
library(thematic)
library(readtext)
library(writexl)
library(DT)
library(tidyverse)
library(tidytext)
library(quanteda)
library(quanteda.textstats)
library(ggraph)
library(igraph)
library(ggwordcloud)
library(tidygraph)

# Her fortæller vi R, at vi ønsker at åbne applikationen ShinyTextMining, der ligger på Github under AUL-Arts-Digital-Lab 
runGitHub("ShinyTextMining", "AUL-Arts-Digital-Lab")
```
3. Kør koden ved at trykke shift, ctrl og enter
4. Du kan nu tilgå text mining applikationen

<img src="./TextMining.png" width="400"/>

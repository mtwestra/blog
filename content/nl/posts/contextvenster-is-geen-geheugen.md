+++
date = '2026-06-10T09:00:00+02:00'
draft = false
title = 'Het contextvenster is geen geheugen'
tags = ['llm', 'architectuur']
+++

Een van de meest voorkomende misvattingen die ik zie bij teams die beginnen te bouwen met taalmodellen, is het behandelen van het contextvenster als geheugen. Dat is het niet. Het lijkt meer op een whiteboard — uiterst nuttig zolang het voor je staat, maar zodra je de kamer uit loopt, is het weg.

Het contextvenster is eindig, duur en vluchtig. Elke token die je erin stopt kost geld bij het inlezen en vertraagt de uitvoer bij het genereren. En als het gesprek eindigt, verdwijnt alles wat erin stond. Het model heeft niets geleerd van jullie uitwisseling. Morgen herinnert het zich jou niet.

Dit heeft enorme gevolgen voor productontwikkeling. Als je een AI-assistent wilt die jouw geschiedenis kent, moet je die geheugenlaag zelf bouwen — doorgaans een combinatie van een vectordatabase voor semantisch ophalen en gestructureerde opslag voor feiten die exact moeten kloppen. Het taalmodel is dan een redeneermotor die werkt op wat je ophaalt en in de prompt injecteert.

De teams die de beste AI-producten bouwen, begrijpen deze architectuur helder. Ze denken na over wat er moet blijven bestaan, hoe ze het efficiënt ophalen, en wat elke keer opnieuw geconstrueerd kan worden. Het contextvenster is een krachtig hulpmiddel. Het is gewoon geen archiefdoos.

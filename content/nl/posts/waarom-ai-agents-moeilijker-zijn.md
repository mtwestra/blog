+++
date = '2026-06-01T09:00:00+02:00'
draft = false
title = 'Waarom AI-agents moeilijker zijn dan ze lijken'
tags = ['agents', 'llm']
+++

Iedereen bouwt momenteel AI-agents. De demo's zijn indrukwekkend: een taalmodel browst het web, schrijft code, stuurt e-mails, plant vergaderingen. Het ziet eruit als magie. Maar als je ooit geprobeerd hebt er een te implementeren in een echte productieomgeving, weet je dat de kloof tussen demo en betrouwbaar product enorm is.

Het kernprobleem is dat taalmodellen probabilistisch zijn. Ze voeren een plan niet deterministisch uit — ze samplen uit een verdeling van waarschijnlijke volgende tokens. Meestal levert dat iets zinnigs op. Maar ketting genoeg van die stappen aan elkaar, en de staartrisico's stapelen zich op. Een agent met vijf stappen die bij elke stap 95% betrouwbaar is, heeft slechts 77% kans om zonder fout te voltooien. Bij tien stappen daalt dat naar 60%.

Dit is geen reden om het op te geven. Het is een reden om zorgvuldig te ontwerpen: houd lussen kort, voeg checkpoints toe, maak fouten herstelbaar, en houd een mens in de loop voor alles wat consequenties heeft. De teams die betrouwbare agents opleveren, zijn niet de teams met de krachtigste modellen — het zijn de teams die de agent behandelen als een nieuwe medewerker in de eerste week, niet als een autonoom orakel.

De vereiste mentale omschakeling is aanzienlijk. We zijn gewend aan software die óf werkt óf een foutmelding gooit. Agents introduceren een derde categorie: plausibel fout. De intuïtie opbouwen om dat te herkennen — voordat het schade aanricht — is de echte engineering-uitdaging van dit moment.

---
title: FAQ
description: Ofte stilte spørsmål med svar.
weight: 50
---

Svar på noen av de vanligste spørsmålene om tjenester 3.0.


### Finnes det en beskrivelse av tjenester 3.0?

> Ja, på overordnet nivå så har vi [fire målsettinger](../goals), og en veldig overordnet beskrivelse av [arkitekturen](../architecture).  
> Mer dokumentasjon vil legges ut når vi nærmer oss release av en "minimum testbar versjon".


### Når kan vi ta i bruk tjenester 3.0?

> Nå som noe finansiering ser ut til å være på vei så vil vi kunne starte realisering av [målsettingene](../goals) for 3.0. 
> Det å tilgjengeliggjøre og oppdatere tjenester 3.0 fortløpende fremover, for å få kontinuerlig feedback, er ønsket måte å jobbe på.  
>
> Se [siste status](../status) for detaljer.


### Kan man gjenbruke noe fra skjema basert på InfoPath, eller må man starte helt på nytt?

> Tjenester 3.0 vil støtte eksisterende dataformater (XSD) fra [SERES](https://altinnett.brreg.no/no/SERES/) og [OR]((https://w2.brreg.no/oppgaveregisteret/spesifikasjon_etatsliste.jsp)),
> noe som betyr at alle grensesnitt (mottak, preutfylling, innsending, etc) vil kunne gjenbrukes uten
> endringer i tjenesteeiers fagsystemer eller [sluttbrukersystemer](https://altinnett.brreg.no/no/Sluttbrukersystemer/).
> Kall mot dagens [mappere](/docs/guides/tul/vedlegg/mappere/) og interne tjenester skal også fortsatt fungere, selv om vi på sikt ønsker å fase ut mappere til fordel for noe bedre.  
>
> Vi har også vurdert muligheten for å lage et verktøy som automatisk konverterer fra InfoPath til tjenester 3.0, helt eller delvis.  
> Etter diskusjoner med diverse tjenesteutviklere, så har det kommet frem at man sannsynligvis uansett vil ønske å forbedre brukergrensesnitt, og forenkle tekster og logikk når man går over til responsive
> tjenester som skal fungere også på mobil. Det å utvikle et konverteringsverktøy er ikke utelukket, men det må gi en reell verdi for tjenesteeierne.

### Finnes det noen retningslinjer for å lette overgangen fra InfoPath?

> - Lag enkle og fornuftige modeller (XSD) som inneholder så mye som mulig av datatyper, begrensninger, etc. istedenfor å kode disse selv.
> - Benytt regelmotor (XML) istedenfor C# i InfoPath for logikk (særlig for kompliserte skjema).
> - Lag gode og korte tekster som har en større sjanse for å fungere også på små skjermer.
> - Vurder om store tabeller (antall kolonner) egentlig er nødvendig.


### Vil vi kunne utvikle eget brukergrensesnitt og kun benytte API'ene i Altinn?

> Ja. API'ene til Altinn vil fortsatt fungere som før, og tjenester 3.0 vil løfte API'ene til en kanal som er likestilt med portal også ved utvikling og testing av tjenester.
> Det vil også legges til rette for å kunne eksponere *alle* ressurser som utvikles som API, f.eks. tekst-ressurser, metadata, semantiske koblinger, valideringer, etc.

### Vil det forsvinne funksjonalitet som finnes i dagens plattform?

> I utgangspunktet nei, så fremt det ikke er funksjonalitet som ikke benyttes, eller som ikke gir mening lengre.  
> De første versjonene av tjenester 3.0 vil ikke inneholde all funksjonalitet, da de viktigste egenskapene vil leveres først og videre utvikling vil gjøres basert på feedback.


### Er tjenester 3.0 prioritert?

> Ja. Tjenester 3.0 er helt sentral for å kunne realisere de fire satsingsområdene i [Altinn-strategien](https://altinnett.brreg.no/no/Altinn/Altinn-strategi/).
> I tillegg er tjenester 3.0 definert som ett av hovedproduktene i Altinn, og er dermed sentral også i Altinn [produktstrategi](https://altinnett.brreg.no/no/Altinn/Altinn-strategi/).  


### Hva slags teknologi benyttes i tjenester 3.0?

> Se [oversikten over programvare](../architecture#programvare) (vil revideres).


### Når vil den gamle InfoPath-løsningen fases ut?

> Enten når alle "aktive" InfoPath-skjema er migrert over til 3.0, eller når support for InfoPath i SharePoint Server
> avsluttes ([2023](https://support.microsoft.com/en-us/lifecycle/search?alpha=sharepoint%202013), ev.
> [2026](https://support.microsoft.com/en-us/lifecycle/search?alpha=sharepoint%202016) hvis vi oppgraderer til SharePoint 2016).  
> De [siste ryktene](https://redmondmag.com/articles/2017/10/03/sharepoint-server-2019-infopath-support.aspx) tyder på at støtte
> for InfoPath også vil inkluderes i SharePoint 2019, noe som betyr at support sannsynligvis kan forlenges helt til 2029 hvis vi oppgraderer.
> 
> [Support for InfoPath](https://support.microsoft.com/en-us/lifecycle/search?alpha=infopath) er også en faktor,
> men denne virker å forlenges hver gang støtten for InfoPath i SharePoint forlenges.
>
> Rent økonomisk i forhold til driftskostnader så vil det være fordelaktig å fase ut den gamle løsningen så snart som mulig,
> men det vil selvsagt ikke kunne gjøres før alle tjenesteeiere er klare.

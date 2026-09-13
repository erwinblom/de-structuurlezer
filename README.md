> **Verhuisd naar Open-source AI Skills NL.** Deze losse repository is gearchiveerd en wordt niet meer bijgewerkt. Gebruik voortaan [de actuele skill](https://github.com/erwinblom/open-ai-skills-nl/tree/main/skills/tekstploeg/de-structuurlezer).
>
> De oorspronkelijke instructies, voorbeelden en versiegeschiedenis blijven hier beschikbaar. De nieuwe versie is inhoudelijk vergeleken, maar is niet in alle werkwijzen identiek. Zie [de vergelijking en migratiekeuzes](MIGRATIE.md).

# De Structuurlezer

> Vind waar je tekst van zijn eigen lijn afwijkt.

De Structuurlezer is een Nederlandstalige AI-skill die conceptteksten vóór publicatie controleert op hoofdlijn, volgorde en redenering. De skill wijst alleen structuurproblemen aan die aan een concrete passage of overgang zijn te koppelen.

De tekst wordt niet automatisch herschreven of herordend. Je krijgt een compact structuurrapport met de zichtbare hoofdlijn, maximaal vijf belangrijke signalen en maximaal drie prioriteiten.

## Wat de skill doet

- benoemt de zichtbare hoofdlijn in maximaal twee zinnen;
- controleert of passages aantoonbaar bijdragen aan die lijn;
- signaleert dwaalsporen, volgordeproblemen, redeneringsgaten en dubbel werk;
- koppelt ieder signaal aan een concrete passage of overgang;
- onderscheidt structuur van stijl, feiten en vermoedelijke lezersreacties;
- zegt eerlijk wanneer geen duidelijk structuurprobleem is gevonden.

## Wat de skill niet doet

- de volledige tekst automatisch herschrijven of herordenen;
- moeilijke zinnen als structuurprobleem behandelen;
- claims factchecken;
- voorspellen hoe een publiek zal reageren;
- een nieuwe bedoeling of redenering voor de schrijver verzinnen;
- alle vier de categorieën kunstmatig vullen.

## Bestanden

- `SKILL.md`: de volledige instructie voor de AI-assistent;
- `voorbeelden/`: een voorbeeldopdracht en verkorte voorbeelduitvoer;
- `LICENSE`: MIT-licentie.

## Installeren

### Omgeving met skills

1. Download deze repository via **Code → Download ZIP** of clone hem met Git.
2. Plaats de map in de lokale skillsmap van je AI-omgeving.
3. Herstart de omgeving of begin een nieuwe taak als nieuwe skills niet direct zichtbaar worden.
4. Vraag de assistent om `De Structuurlezer` te gebruiken.

De precieze skillsmap verschilt per product. De kern is steeds hetzelfde: `SKILL.md` moet als instructiebestand beschikbaar zijn voor de assistent.

### Omgeving zonder skillsmap

Voeg `SKILL.md` toe aan de projectkennis of kopieer de inhoud naar de vaste instructies van je assistent. Je kunt de werkwijze ook per gesprek meegeven als bijlage.

## Gebruik

Geef de volledige concepttekst mee en bijvoorbeeld deze opdracht:

```text
Gebruik De Structuurlezer voor deze tekst.

[tekst]
```

Met extra context wordt het oordeel preciezer:

```text
Gebruik De Structuurlezer voor deze nieuwsbrief.
Doel: uitleggen waarom kleine AI-tools nuttiger kunnen zijn dan één groot systeem.
Gewenste actie: de lezer probeert één tool uit.

[tekst]
```

## De uitkomst

De Structuurlezer levert een `Structuurrapport` met:

1. de zichtbare hoofdlijn;
2. maximaal vijf concrete structuursignalen;
3. per signaal het type en het effect op de lijn;
4. maximaal drie problemen onder `Eerst oplossen`;
5. geen automatische herschrijving.

De vier mogelijke signalen zijn:

| Type | Betekenis |
| --- | --- |
| Dwaalspoor | Een passage opent een zijlijn die niet zichtbaar bijdraagt |
| Volgordeprobleem | Noodzakelijke uitleg of context staat te laat |
| Redeneringsgat | Een conclusie mist een zichtbare tussenstap |
| Dubbel werk | Twee passages vervullen dezelfde functie zonder voortgang |

## Aanpassen aan je eigen werk

Maak bij voorkeur eerst een kopie en pas daarna `SKILL.md` aan. Handige instellingen om persoonlijk te maken:

1. **Tekstsoort** — voeg vaste aandachtspunten toe voor essays, nieuwsbrieven, memo's of hoofdstukken.
2. **Aantal signalen** — verlaag het maximum voor korte teksten of verhoog het voorzichtig voor lange hoofdstukken.
3. **Vaste context** — geef doel, hoofdvraag, doelgroep en gewenste actie standaard mee.
4. **Uitvoer** — maak de uitleg compacter, maar behoud de vier probleemtypen.

Behoud bij aanpassingen in elk geval deze veiligheidsregels:

- geen nieuwe bedoeling of inhoud verzinnen;
- ieder signaal aan een concrete passage of overgang koppelen;
- structuur niet verwarren met stijl, feiten of publieksreacties;
- geen kunstmatige kritiek produceren;
- de brontekst niet automatisch wijzigen.

## Goede test

Test een aangepaste versie ten minste op:

1. een logisch opgebouwde tekst zonder wezenlijk structuurprobleem;
2. een tekst met een onverbonden anekdote;
3. een conclusie die een redeneringsstap overslaat;
4. uitleg die pas verschijnt nadat zij nodig was;
5. twee passages die hetzelfde structurele werk doen.

De skill slaagt als hij echte problemen vindt zonder stijlvoorkeuren of gezochte kritiek als structuurfout te presenteren.

## Bijdragen

Verbeteringen, praktijktests en voorbeelden zijn welkom. Houd bijdragen algemeen bruikbaar: voeg geen persoonlijke paden, accounts, abonnementen of projectnamen toe aan de publieke skill.

## Licentie

MIT. Je mag de skill gebruiken, aanpassen en verspreiden met behoud van de licentietekst.

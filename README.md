# Game of Thrones: Great Houses

In dit afsluitend labo wordt de inhoud van de verschillende hoofdstuken gecombineerd.
Het is de ideale voorbereiding op het examen, dat o.a. zal bestaan uit een vergelijkbaar praktisch gedeelte.

Er zijn in de startsituatie van het labo reeds enkele branches aanwezig:
* **master**
* **dev**
* enkele **feature** branches

Op de **master** branch vind je de opgave van het labo.
Tijdens de uitwerking van het labo, zal je verschillende **feature** branches naar **dev** mergen (zowel reeds bestaande als nog aan te maken feature branches).
De **master** branch wordt enkel aangepast op het einde van het labo.

### Aanvullende toetsen

**Opgelet:** bij dit labo horen **TWEE** aanvullende toetsen op Leho:
1. De eerste toets maak je **VOOR** je aan het labo begint. Hierin worden enkele inzichtsvragen gesteld over de **startsituatie** van het labo. Eventueel kan je wel al de remote repo van het labo **clonen** naar je lokale pc, als je liever via Git Bash de nodige opzoekingen doet binnen de repo dan op GitHub.
2. De tweede toets maak je zoals gewoonlijk **na** afronden van het labo.

Je kan/mag de aanvullende toetsen steeds afleggen gebruik makend van alle bronnen (cursusmateriaal, labo, online bronnen, ...).

### Deel 1: remote repo clonen

- [ ] Open de Git Bash Console op de locatie waar je dit labo wil gaan clonen. Dit kan via een rechtermuisklik op de locatie in kwestie en vervolgens de keuze **Git Bash Here** te selecteren.
- [ ] Zorg ervoor dat de startsituatie *(deze repository)* van het labo op jouw pc **gecloned** wordt. Maak hiervoor gebruik van het passende git commando. 
- [ ] Ga **na het clonen** via de Console naar de gecloonde repository. Dit kan/mag je uiteraard ook doen door de nieuwe aangemaakt folder aan te klikken en hier opnieuw een Git Bash console te openen via de **Git Bash Here** optie.
>**Tip!** Controleer voor je verder werkt of je al dan niet in de juiste git repository zit! Je kan dit snel visueel vaststellen in je console.

### Deel 2: issues aanmaken

- [ ] Maak voor elk van de reeds aanwezige **feature** branches een issue aan op GitHub. Geef de issues een duidelijke titel.

>**Tip!** Voor de branch **feature/house-stark** kan je de issue bv. als titel **House Stark** geven.

### Deel 3: verwijderen reeds gemergde feature branch

In de startsituatie is een van de aanwezige feature branches eigenlijk al gemerged naar **dev**.

- [ ] Zoek uit (via Git Bash of op GitHub) welke van de feature branches al naar **dev** werd gemerged.
- [ ] Voer het gepaste git commando uit in je Git Bash console om deze feature branch te verwijderen uit je **remote** repo.

>**Tip!** Indien je de betreffende branch intussen ook lokaal had uitgecheckt, voer dan gerust ook het gepaste git commando uit om deze branch ook lokaal terug te verwijderen. Als je de branch nooit lokaal uitcheckte, hoef je ze uiteraard ook niet te verwijderen lokaal, want dan heeft ze daar nooit bestaan.

- [ ] Sluit het **issue** (manueel) af dat bij deze feature branch hoort.

### Deel 4: House Baratheon

- [ ] Ga lokaal in Git Bash naar de branch **feature/house-baratheon**.
- [ ] Download de afbeelding (PNG) met het [embleem van House Baratheon](https://www.kindpng.com/picc/m/455-4550587_storms-end-game-of-thrones-houses-game-of.png) naar je lokale PC.
- [ ] Maak een map aan in de root van je repo met de naam `houses/`.
- [ ] Plaats de afbeelding die je gedownload hebt in deze map `houses/` en verander de naam naar `baratheon.png`.
- [ ] Open het bestand `README.md` (bv. in Visual Studio code). Voeg onderaan deze regel toe:

```
![](houses/baratheon.png)
```

- [ ] Bewaar je wijziging, maar **wacht** nog even om een commit te maken.
- [ ] Voer het gepaste git commando uit om een overzicht te krijgen van de wijzigingen die klaar staan in de working directory.

Je zal zien dat de wijziging aan `README.md` getoond wordt, maar de toegevoegde afbeelding `houses/baratheon.png` **niet**.
Dit komt door de reeds aanwezige gitignore, die alle bestanden behalve Markdown bestanden in de map `houses` uitsluit.

- [ ] Open de **gitignore** file (bv. in Visual Studio code).
- [ ] Voeg een regel toe zodat ook alle bestanden met extensie `.png` in de map `houses` opgenomen worden in het versiebeheer.
- [ ] Pas de regel commentaar bovenaan de gitignore aan in lijn met deze wijziging.
- [ ] Bewaar de aanpassingen aan de **gitignore**.
- [ ] Voer opnieuw hetzelfde git commando als hierboven uit om na te gaan welke wijzigingen klaar staan in de working directory. Nu zou je drie wijzigingen moeten zien:
  - Aanpassing aan `README.md`.
  - Aanpassing aan de **gitignore**.
  - Toevoeging van afbeelding `houses/baratheon.png`.

- [ ] Commit deze drie wijzigingen naar je lokale repo (samen in één commit). **Verwijs in je commit message naar de bijhorende issue op GitHub**, op zo'n manier dat deze issue **automatisch afgesloten zal worden** zodra we de commit in de master branch zullen mergen.
- [ ] Synchroniseer naar de remote repository op GitHub.

- [ ] **Open** op GitHub een **pull request** om de branch **feature/house-baratheon** in **dev** te mergen.
- [ ] Je zal zien dat er een merge conflict onstaat in de pull request. **!! WACHT** nog even om dit op te lossen en de pull request effectief te mergen, daar komen we later op terug.
- [ ] Ken jezelf toe als *assignee* van de pull request.

### Deel 5: House Greyjoy

Alhoewel er geen feature branch aanwezig is voor House Greyjoy, werd de beschrijving hiervan per ongeluk wel toegevoegd op een andere, foute branch.

- [ ] Maak voor House Greyjoy een **issue** aan op GitHub.
- [ ] Zoek uit op welke branch de beschrijving van House Greyjoy werd toegevoegd aan `README.md` en in welke commit.
      Noteer de **commit hash** van deze commit. Je kan dit via Git Bash lokaal doen, of op GitHub.

- [ ] Maak lokaal een nieuwe branch **feature/house-greyjoy** vanaf **dev** en ga meteen naar deze nieuwe branch.
- [ ] Voer een git commando uit om de commit waarin de beschrijving van House Greyjoy werd toegevoegd aan `README.md` over te zetten naar deze branch `feature/house-greyjoy`. **Opgelet:** dit zal een conflict veroorzaken, we lossen dit straks op.

>**Tip!** Als onderdeel van dit commando heb je de commit hash nodig die je eerder noteerde.

- [ ] Het overzetten van de commit naar de nieuwe branch **feature/house-greyjoy** veroorzaakt een **conflict**.
      Dit komt omdat de betreffende commit gebaseerd is op een andere git geschiedenis dan deze op de huidige branch.
      We kunnen dit conflict oplossen net zoals we een merge conflict oplossen bij het mergen van twee branches.

- [ ] Los het conflict in `README.md` op (bv. in Visual Studio Code). We willen de beschrijving van House Stark en House Greyjoy behouden.
      De flarden van de beschrijving van House Lannister die meekomen in het conflict, willen we **niet** behouden.

- [ ] Bewaar je aanpassingen in `README.md` en commit je oplossing van het conflict.
      Laat je indien nodig inspireren door de voorstellen die git geeft om de juiste commando's te vinden om de conflictoplossing af te ronden.

- [ ] Synchroniseer je nieuwe lokale branch **feature/house-greyjoy** naar de remote op GitHub.

>**Tip!** Denk eraan dat je hier iets extra moet doen omdat de nieuwe lokale branch nog niet bestaat op de remote.

- [ ] Keer lokaal terug naar de branch waarop de overgezette commit oorspronkelijk (en foutief) werd doorgevoerd.
- [ ] Gebruik het gepaste git commando om deze commit op die foute branch ongedaan te maken **met behoud van de reeds bestaande git geschiedenis**.
- [ ] Synchroniseer de branch naar de remote.

- [ ] Open op GitHub een **pull request** om de branch **feature/house-greyjoy** te mergen in **dev**.
- [ ] Verifieer dat er **geen** merge conflict onstaat in de pull request, maar **WACHT** nog even om deze pull request verder af te werken, daar komen we zo meteen op terug.
- [ ] Ken jezelf toe als *assignee* van de pull request.
- [ ] Link **op GitHub** deze pull request aan het issue van House Greyjoy.

>**Tip!** In de cursus wordt niet expliciet vermeld hoe je een issue manueel aan een pull request kan koppelen op GitHub (we deden het daar enkel via de commit message).
Zoek even uit hoe je de link rechtstreeks op GitHub kan leggen. Kijk even welke knoppen en invulvelden er allemaal zijn op de pull request pagina.

### Deel 6: pull requests afwerken

Er staan nu twee pull requests open op GitHub.
 
- [ ] Ga naar de pull request die **feature/house-baratheon** zal mergen in **dev**.
- [ ] Verifieer dat er een conflict wordt gesignaleerd in de pull request.
- [ ] Los het conflict op **via GitHub**. Het conflict is ontstaan omdat vanuit parallele branches zowel de uitleg van House Stark als House Baratheon werd toegevoegd aan `README.md`. We willen beide secties in de README behouden, onder elkaar. Let er ook op dat de afbeelding met het embleem van House Baratheon niet verloren gaat.
- [ ] Werk vervolgens de pull request af zodat de merge effectief uitgevoerd wordt.

Nu staat er nog maar één pull request open.
Deze bevatte oorspronkelijk geen conflict t.o.v. van **dev**, maar door de eerste pull request in **dev** te mergen is de situatie veranderd.

- [ ] Ga naar de pull request die **feature/house-greyjoy** zal mergen in **dev**.
- [ ] Verifieer dat ook hier nu een merge conflict ontstaat, waardoor de pull request niet zomaar gemerged kan worden.

We gaan dit conflict **lokaal** in Git Bash oplossen.

- [ ] Ga lokaal naar de **dev** branch.
- [ ] Breng deze lokale **dev** branch up to date met de wijzigingen die op de remote gebeurden (door de eerste PR te mergen).
- [ ] Ga lokaal nu naar de branch **feature/house-greyjoy**.
- [ ] Merge **LOKAAL** de branch **dev** in **feature/house-greyjoy**.
- [ ] Bij deze merge zou nu ook hetzelfde conflict moeten ontstaan dat reeds door GitHub in de pull request was gesignaleerd.
- [ ] Los het merge conflict lokaal op. We willen gewoon dat de beschrijving van zowel House Stark, Baratheon als Greyjoy mooi onder elkaar in de `README.md` komen.
- [ ] Bewaar je wijziging die het conflict oplost.
- [ ] Commit je wijziging naar de lokale git repo.
- [ ] Synchroniseer de branch **feature/house-greyjoy** nu naar de remote.

Het conflict is nu opgelost! Dat zou ook zichtbaar moeten zijn in de pull request.

- [ ] Ga op GitHub naar de nog openstaande pull request die **feature/house-greyjoy** in **dev** zal mergen.
- [ ] Verifieer dat het merge conflict verholpen is en dat de pull request nu probleemloos kan afgewerkt worden.
- [ ] Werk de pull request af zodat de merge ook effectief plaatsvindt.

### Deel 7: release van dev naar master

- [ ] Maak nu een laatste pull request op GitHub, die de branch **dev** zal mergen in **master**.
- [ ] Ken jezelf als *assignee* toe aan de pull request.
  
Ook hier ontstaat weer een conflict, omdat de README op **master** de instructies voor het labo bevat, terwijl op **dev** hier de beschrijving van House Baratheon, Stark en Greyjoy in terechtgekomen is.

- [ ] Los het conflict op. Kies zelf of je het deze keer via GitHub doet of lokaal. Als resultaat willen we de instructies van het labo (die oorspronkelijk op **master**) stonden volledig **overschrijven** met de beschrijving van de Houses (die binnenkomen via **dev**).
- [ ] Werk de pull request af zodat **dev** effectief in **master** wordt gemerged.


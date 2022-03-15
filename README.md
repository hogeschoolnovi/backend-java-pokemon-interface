## Inleiding

Je hebt inmiddels geleerd hoe je relaties, overerving en abstracte klassen moet toepassen, dit hebben we uitgebreid met wat meer kennis. Zo weet je nu wat acces modifiers, keywords, overloading enzo nog veel meer. In het backend landschap
worden deze concepten vaak uitgelegd aan de hand van dieren of andere levende wezens. Dus in plaats van de standaard
hond of kat te kiezen, passen wij deze concepten toe op het onderwerp Pokèmon!

## Opdrachtbeschrijving

Je gaat een applicatie programmeren waarmee een speler via de commandline een spel kan spelen. Degenen die bekend zijn met Pokèmon weten
dat deze altijd een _type_ hebben (sterker nog: Pokèmon kunnen meerdere types tegelijk zijn, maar om het niet te moeilijk
te maken, maken we gebruik van één type per Pokèmon). Voorbeelden van deze typen zijn: Fire 🔥, Water 🌊, Grass 🌿 en
Electric ⚡. Daarnaast gaan we een gym maken en een trainer, zodat de applicatie interactief kan worden.

Naast hun type, hebben Pokèmon natuurlijk bepaalde eigenschappen met elkaar gemeen. Daarom maken we gebruik van een
Super klasse. Ook gaan we kijken om gebruik te maken van overloading, polymorfisme en een interface.

![Pokemon!](./assets/pokemon.JPG)

## Randvoorwaarden

De applicatie moet voldoen aan het volgende:

- Een `abstract` Super klasse met minimaal 5 `private` `final`  variabelen,  5 `private`variabele, 1 constructor, 6 getters en 1 setter;
- 4 subklassen die, naast alles dat ze erfen, zelf ook minimaal 2 `private` `final` variabelen, 1 constructor, 4 methodes,  1 getter bevatten.
- Een `main`-klasse met een `main`-methode;
- Een `interface` met 11 methodes
- Een implementatie van de `interface` waarin alle methodes worden overschreven met een `@Override`
- 2 normale klassen met minimaal 8 variabelen, constructor, getters en setters

### Afwijkjing van werkwijze

Omdat jullie inmiddels wat verder gevorderd zijn met het programeren met `Java` gaan we jullie laten ervaren hoe het kan zijn om samen een 
applicatie in elkaar te zetten. Jullie krijgen hierbij een deel van de code van ons. Deze code wordt bijgeleverd in een apparte klassen met instructies zodat jullie deze op de juiste plaats kunnen zetten in app. 
Dit betekend ook dat een groot deel van de methodes al benoemt zullen zijn. Dit is nodig om straks een werkende interactieve applicatie te hebben! 

## Stappenplan
Het is uitdagender om jouw eigen stappenplan te maken, maar als je niet weet waar je wil beginnen kun je dit stappenplan volgen.
1. Maak de volgende klassen aan:
   - Pokemon (`abstract`)
   - FirePokemon
   - GrassPokemon
   - ElectricPokemon
   - GrassPokemon
   - PokemonGym (`interface`)
   - PokemonGymImpl
   - PokemonGymOwner
   - PokemonTrainer
   - WaterPokemon
2. In de klasse Variabelen staan verschillende variabelen met tips. Plaats deze in de juiste klassen, die je zojuist hebt aangemaakt en geef deze de juiste datatype.
3. Geef alle variabelen getters en setters als ze in de juiste klasse staan.
4. In de klasse Methodes staan de methodes die minimaal gebruikt moeten worden binnen de applicatie. Verplaats deze naar de juiste klassen
5. De aanval methodens moeten de volgende eigenschappen hebben:
  - een `system.out.println` en laat deze vertellen wie, wie aanvalt met welke aanval(concatenation met variablen)
  - een beslissingstructuur die kijkt welk type de vijand heeft
  - aan de hand van de beslissingstructuur moet de vijand hp punten verliezen (per type verschilt het aantal puntn)
  - een `system.out.println` die aangeeft wat de aanval voor effect heeft
  - vergeet de hp van de vijand niet te verlagen
  - sluit de methode af met een `system.out.println` die de resteren hp waarde weergeeft van de vijand
6. De volgende methodes hebben nog een extra functie
  - rainDance heeft geen effect op electric Pokemons maar geeft een `system.out.println` met de boodschap: has no effect on (vijand)
  - rainDance levert een hp boost aan vijanden grass types
  - tunder levert een hp boost aan electric Pokemons
  - leechSeed trekt hp van de vijand af en geeft deze hp aan de aanvallende Pokemon terug
7. In de interface plaatsen we de methodes zonder uitwerking. Dus alleen het returntype, naam, datatypes van de parameters en de parameters van de methode.
8. In de implementatie van de interface zetten we gehele methodes. Vergeet de `@Override` niet.


## Bonusopdrachten

1. Kunnen jullie de variable food met het juiste datatype toevoegen aan de juiste klasse(n)? En een methode die de pokemon voert, wat de hp een boost geeft?
2. Kunnen jullie het spel aanpassen dat je in plaats van een aanval doet, het pokemonvoedsel naar de pokemon gooit. Als deze voeding de juiste is van het type pokemon, de pokemon een hp boost geven?
3. Op dit moment kun je het spel oneindig spelen. Is er een manier om te zorgen dat als de pokemon geen hp meer heeft, de pokemon niet meer gebruikt kan worden? Tenzij het spel opnieuw gestart wordt.

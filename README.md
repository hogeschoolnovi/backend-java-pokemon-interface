## Inleiding

Je hebt geleerd hoe je relaties, overerving en abstracte klassen moet toepassen. Ook weet je nu meer over: access modifiers, keywords, overloading, klassen, methoden en nog veel meer. In het backend landschap
worden deze concepten vaak uitgelegd aan de hand van dieren of andere levende wezens. In deze opdracht passen wij de scope, overloading, keywords en interfaces toe op Pokémons!

## Opdrachtbeschrijving

Je gaat een applicatie programmeren waarmee een speler via de commandline een spel kan spelen. Degenen die bekend zijn met Pokémon weten
dat deze altijd een _type_ hebben (sterker nog: Pokémon kunnen meerdere types tegelijk zijn, maar om het niet te moeilijk
te maken, maken we gebruik van één type per Pokémon). Voorbeelden van deze typen zijn: Fire 🔥, Water 🌊, Grass 🌿 en
Electric ⚡. Daarnaast gaan we een gym maken en een trainer, zodat de applicatie interactief kan worden.

Naast hun type, hebben Pokémon natuurlijk bepaalde eigenschappen met elkaar gemeen. Daarom maken we gebruik van een
**super** klasse. Ook gaan we kijken naar overloading, polymorfisme en een interface.


![Pokemon!](./assets/pokemon.JPG)


### Afwijking van werkwijze

Omdat jullie inmiddels wat verder gevorderd zijn met het programmeren met 
`Java` gaan we jullie laten ervaren hoe het is om samen een 
applicatie in elkaar te zetten. Jullie krijgen daarom een deel van de code van
ons. Jullie krijgen de Main klasse en de PokemonGym klasse.
Deze twee klassen hoeven jullie niet meer aan te passen.
Ze staan echter wel vol met foutmeldingen. Deze foutmeldingen mogen jullie weg werken
door klassen, methodes, variabelen, abstracte klassen en interfaces te maken (en soms een import).
De code in de PokemonGym fungeert als een soort van "game engine". Deze code hoef je niet te begrijpen, maar het is leuk om te bestuderen.
De Methodes en Variabelen klassen bevatten hints voor deze opdracht en zullen verder
geen deel uitmaken van de uiteindelijke applicatie.

#### Klassen naamgeving

Omdat we de belangrijkste functionaliteit al voor je hebben uitgewerkt, is het belangrijk dat je jouw
klassen de juiste namen geeft. Kijk daarom goed in [Methodes.java](./src/Methodes.java), [Main.java](./src/Main.java) en [PokemonGymImpl.java](./src/PokemonGymImpl.java). 
Daar worden alle klassenamen gebruikt.
Door de methodes in [Main](./src/Main.java) en [PokemonGymImpl](./src/PokemonGymImpl.java) 
goed te lezen, kun je voor de meeste methodes en variabelen al afleiden in welke klassen die moeten komen te staan.

#### Methodes en variabelen verdelen

In deze opdracht hoef je zelf geen methodes of variabelen te bedenken. (Tenminste, niet totdat je aan de bonusopdrachten gaat werken.) 
We hebben bijna alle methodes al voor je in [Methodes.java](./src/Methodes.java) gezet, behalve getters en setters.
De methodes die hier niet staan, waaronder constructors, kun je afleiden uit [Main](./src/Main.java) en [PokemonGymImpl](./src/PokemonGymImpl.java).
We hebben een aantal variabelen die je nodig hebt, beschreven in [Variabelen.java](./src/Variabelen.java), 
maar je kunt ze ook afleiden uit de getters, setters en constructors die in [Main](./src/Main.java) en [PokemonGymImpl](./src/PokemonGymImpl.java) worden aangeroepen.
Het enige wat je nog moet doen is de methodes en variabelen in de juiste klasse(n) zetten. 
De variabelen uit [Variabelen.java](./src/Variabelen.java) moet je meestal nog een type geven en instantiëren, maar bij sommigen hebben we dat ook al gedaan.

### De aanval methodes

De aanval methodes moeten de volgende eigenschappen hebben:
- een `system.out.println` die vertelt wie wie aanvalt met welke aanval (concatenation met variabelen, b.v.: "Bulbasaur attacks Charizard with leafStorm");
- een beslissingsstructuur die kijkt welk type de vijand heeft;
- aan de hand van de beslissingsstructuur moet de vijand hp punten verliezen (per type verschilt het aantal punten);
- een `system.out.println` die aangeeft wat de aanval voor effect heeft (concatenation met variabelen, b.v.: "Charizard loses 15 hp");
- vergeet de hp van de vijand niet te verlagen;
- sluit de methode af met een `system.out.println` die de resteren hp waarde weergeeft van de vijand;

De volgende methodes hebben nog een extra functie:
- `rainDance` heeft geen effect op electric Pokemons maar geeft een `system.out.println` met de boodschap: "has no effect on (vijand)";
- `rainDance` levert een hp boost aan vijanden grass-types;
- `thunder` levert een hp boost aan electric Pokemons;
- `leechSeed` trekt hp van de vijand af en geeft deze hp aan de aanvallende Pokémon terug;


### Spel logica

Bij Pokémons is het zo dat het type bepalend is voor hoe zwaar de schade is. Hieronder vind je een overzichtje voor een logica van schade bij aanvallen:
- Het type fire🔥 doet de meeste schade aan grass-pokémons🌿, daarna aan water-pokémons🌊, dan de electric-pokémons⚡ en het minste bij fire-pokémons🔥.
- Het type grass🌿 doet de meeste schade aan electric-pokémons⚡, daarna aan fire-pokémons🔥, dan de water-pokémons🌊 en het minste bij grass-pokémons🌿.
- Het type electric⚡ doet de meeste schade aan water-pokémons🌊, daarna aan grass-pokémons🌿, dan de fire-pokémons 🔥en het minste bij electric-pokémons⚡.
- Het type water🌊 doet de meeste schade aan fire-pokémons🔥, daarna aan electric-pokémons⚡, dan de grass-pokémons🌿 en het minste bij water-pokémons🌊.

## Randvoorwaarden

De applicatie moet voldoen aan het volgende:

- Je mag geen code toevoegen, aanpassen of verwijderen uit de `Main` en `PokemonGymImpl` klassen, behalve de nodige imports.
- Een `abstract` super klasse  met 5 `private` `final`  variabelen,  1 `private`variabele, 1 constructor, 6 getters en 1 setter;
- 4 subklassen die, naast alles dat ze erven, zelf ook minimaal 2 `private` `final` variabelen, 1 constructor, 4 methodes, 1 getter bevatten;
- Een `Main`-klasse met een `main`-methode;
- Een `interface` met 11 methodes;
- Een implementatie (-Impl) van de `interface` waarin alle methodes worden overschreven met een `@Override`;
- 2 "normale" klassen. Waarvan een klasse met 8 variabelen, constructor, getters en setters. De andere klasse extends de eerste klasse en heeft zelf nog 1 variabele, een getter, setter en een constructor die enkel de super aanroept. 


## Stappenplan
Let op: het is uitdagender om jouw eigen stappenplan te maken. Als je niet zo goed weet waar je moet beginnen, kun je onderstaand stappenplan gebruiken:
1. Loop door [Main](./src/Main.java) en [PokemonGymImpl](./src/PokemonGymImpl.java) en los alle foutmeldingen op door klassens, variabelen en methodes aan te maken en af en toe iets te importeren.
2. Kijk in [Variabelen.java](./src/Variabelen.java) of daar nog niet-geimplementeerde variabelen staan. Plaats deze in de juiste klassen, die je zojuist hebt aangemaakt en geef ze de juiste datatypen.
3. Geef alle variabelen getters en setters als ze in de juiste klasse staan.
4. Doe hetzelfde voor [Methodes.java](./src/Methodes.java).
5. Implementeer de aanval methodes zoals hierboven beschreven. Let daarbij ook op de bijzondere gevallen `raindance`, `thunder` en `leechSeed`.
6. Plaats de methodes in de interface plaatsen zonder uitwerking. Dus alleen het returntype, naam, datatypes van de parameters en de parameters van de methode.


## Bonusopdrachten

1. Voeg de variabele ‘food’ met het juiste datatype toe aan de juiste klasse(n). Voeg ook een methode toe waarbij de hp van de Pokémon een boost krijgt wanneer hij gevoerd wordt.
2. Pas het spel aan zodat je het pokémonvoedsel naar de Pokémon gooit voor een aanval, in plaats van een aanval doet. Als dit voedsel het juiste type is voor dit type Pokémon, zal het de Pokémon een boost geven. 
3. Op dit moment kun je het spel oneindig spelen. Pas het spel aan zodat een Pokémon die geen hp meer heeft, niet meer gebruikt kan worden, tenzij het spel opnieuw wordt opgestart.


## Tip

Let goed op welke tips en advies IntelliJ je geeft!

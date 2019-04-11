<h1>Chef's Apprentice</h1>

Disclaimer: Dette er et GitLab-prosjekt som er flyttet til GitHub

Chef’s Apprentice er en applikasjon der brukere skal kunne finne matoppskrifter basert på søk etter ingredienser. Applikasjonen skal også gi en interaktiv opplevelse der brukere skal kunne legge ut egne oppskrifter, og lese oppskrifter av anerkjente kokker. 

<h2>Motivasjon</h2>

Tanken bak applikasjonen er å redusere dagens matsvinn samt minimere sult i Norge. Applikasjonen skal gjøre hverdagen lettere ved at det skal bli enklere å bruke opp ingredienser en har liggende i kjøleskapet. 

<h2>Build status og test coverage</h2>

![badges](https://user-images.githubusercontent.com/37066508/55951646-0f97e100-5c58-11e9-8459-23dc917c5b7f.png)

<h2>Skjermbilder</h2>

![forside](https://user-images.githubusercontent.com/37066508/55951648-0f97e100-5c58-11e9-960b-966bceee67d5.PNG)

Forside

![write-recipe](https://user-images.githubusercontent.com/37066508/55951654-10307780-5c58-11e9-984c-2d25165bbeef.PNG)

Skriv nye oppskrifter

<h2>Kodekonvensjoner</h2>

Det er fulgt ordinære konvensjoner i Java fra [JavaPractices](http://www.javapractices.com/home/HomeAction.do) som er foreslått i faget TDT4140. Hver klasse og hver metode har tilhørende doc-comments med konsistent navngivning.
 
<h2>Teknologier/rammeverk</h2>

* Maven
* JavaFX
* JFoenix
* JDBC
* Java 11
* JUnit 4


<h2>Egenskaper</h2>

* Ulike brukertilganger
* Bruk av tredjepart API for henting av oppskrifter
* Mulighet for å legge inn egne oppskrifter
* “Verifiserte” oppskrifter

 
<h2>Installasjon</h2>

Vi anbefaler bruk av Intellij til videreutvikling. 
For å komme i gang kan en klone repoet fra GitLab.

Deretter åpner en prosjektet i Intellij som et Maven-prosjekt. 
Intellij vil foreslå å importere nye settings fra pom.xml. 

Klikk “import new settings”.

Så må en sette opp en egen mySQL-database. Denne kan kjøres på feks. localhost.

Vi har lagt ved et sql-script: `gruppe79.sql` for å opprette databasen etter en har satt opp mysql.

Naviger til prosjektnavn/ChefsApprentice/src/main/java/sample/DBconnector.java og legg inn dine database-credentials.

I Intellij gå til File->Settings->Build, Execution, Deployment->Build Tools->Maven->Runner 

og huk av Delegate IDE build/run actions to maven.

Naviger til prosjektnavn/ChefsApprentice/src/main/java/sample/ og kjør MainBackEnd.java.

Naviger til prosjektnavn/ChefsFrontEnd/src/main/java/sample/ og kjør Main.java.

Gratulerer! Applikasjonen kjører!
 
<h2>Tester</h2>

Vi benytter oss av JUnit 4. 

Tester ligger under modulnavn/src/test/java/
Disse kjøres hver gang en bygger med Maven.

<h2>Brukermanual</h2>

[Se Wiki-siden](https://github.com/Kobrestad/ChefsApprentice/wiki)

<h2>Bidra</h2>

Dersom en ønsker å bidra kan en forke og lage merge-requests.

Ønsker en å ta applikasjonen ut i produksjon må en lage en egen mySQL-database.

Dette kan gjøres med sql-scriptet `gruppe79.sql` som ligger i repositorien vår.

Gjør en dette må en selv gå inn i ChefsApprentice/src/java/sample/DBConnector 
og endre Database-credentials slik at din egen database kan benyttes.

<h2>Credits</h2>

[TheMealDB.com](https://www.themealdb.com/api.php) for oppskriftsdatabase.

<h2>Lisens</h2>

Copyright 2019 Gruppe 79 TDT4140, NTNU

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

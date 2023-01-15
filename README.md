# edu-crud-jdbc

## Beskrivning

>I kursen DB2022 på IT-Högskolan skulle vi efter kursens slut redovisa våra färdigheter i SQL, Normalisering samt Java mot en relationsdatabas. Detta är min redovisning från denna kurs. Parallellt med kursen på It-högskolan läste jag även av eget fördjupningsintresse kursen “Mastering SQL (Using MySql, Java and Go) på Udemy.

### Under kursen på IT-Högskolan lärde jag mig 

#### Databaser
>Design av relationsdatabaser. SQL-syntax för att ta fram, sätta ihop och organisera bland data. DDL: Skapa och ändra tables. DML: Uppdatera och eliminera tables. DQL: Välja ut specifik data i en databas. DCL: Ändra och upphäva användares rättigheter i databasen.**TCL**: Hantera transaktioner. 
Skapa SQL scripts. ACID. Vikten av konsistens och hur man med hjälp av Normalisering (1NF - 3NF) skyddar konsistensen genom att ta bort/eliminera anomalier och på så vis undvika redundant data.
#### Utveckling mot relationsdatabaser med Java
>Skapa och förstå javaapplikationer som nyttjar relationsdatabaser. Bädda in SQL i javakod och göra förfrågningar mot databas. Göra CRUD-applikationer. Skapa Springbootapplikationer för att komma åt JPA. Jdbc Interfaces: Konstruera javakod med Driver Manager, Driver, Connection, Statement, Prepare statement och Result set. JUnit: Som ett alternativt sätt att köra kod. Unit test Lifecycle. Test, BeforeEach, AfterEach, AfterAll, AfterEach.
#### Mermaid och Lucidchart
>Konstruera Entity-Relationship Diagram som illustrerar relationer i databasen. Konstruera flödesscheman.
#### Vi/Vim, Gradle och Bash 
>Vi för att snabbt göra små förändringar i filer via terminalen. Gradle för att skapa nya javaprojekt med, köra och testa dessa med bashkommandon. Dependency Management, låna mjukvara till styrfil från gradle/maven repository för att få en driver. Bash för snabb hantering av filer. 
#### Docker
>Hur man kan få tillgång till en utvecklingsmiljö utan att behöva installera en faktisk databas och arbeta med ett Relationship Database Management system som MySQL eller en dokumentdatabas (MongoDB) och ha många databaser igång samtidigt. Importera kommaseparerat data till en extern maskin och köra sql scripts i en extern maskin. Docker lifecycle: Run, create/rm, start/stop, pause/unpause
#### Markdown och git
>Dokumentering av projekt med ett tidsbestämt språk och version control. 

####  Entity Relationship Diagram

```mermaid
erDiagram
    Student ||--o{ Phone : has
    Student }|--o| Grade : has
    Student ||--o{ StudentSchool : attends
    School ||--o{ StudentSchool : enrolls
    Student ||--o{ StudentHobby : has
    Hobby ||--o{ StudentHobby : involves

  Student {
        int StudentId
        string Name
        int GradeId
    }
      Phone {
        int PhoneId
        int StudentId
        tinyint IsHome 
        tinyint IsJob
        tinyint IsMobile
        string number
    }
       School {
        int SchoolId
        string name
        string City
    }
        StudentSchool {
        int StudentId
        int SchoolId
    }
      Hobby {
        int HobbyId
        string name
    }
    StudentHobby {
        int StudentId
        int HobbyId
    }
     Grade {
        int GradeId
        string name
    }
```

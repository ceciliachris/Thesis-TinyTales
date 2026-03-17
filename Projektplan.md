# Projektplan för Examensarbete

**Ditt namn:** Cecilia Christiansson  
**Din handledare:** William Enander

## 1. Projektöversikt

### 1.1 Projekttitel

_Utveckling av en AI‑driven applikation för att generera barnanpassade sagor med illustrationer_

### 1.2 Projekttyp

- [X] Utvecklingsprojekt (bygga en applikation/system)
- [ ] Forskningsprojekt (undersöka och analysera ett ämne)
- [ ] Hybridprojekt (kombinerar utveckling med forskning)

### 1.3 Sammanfattning (max 200 ord)

_Detta projekt går ut på att utveckla en mobilapplikation som med hjälp av generativ AI kan skapa korta, barnanpassade sagor med tillhörande illustrationer.
Användaren ska kunna välja ålder, tema eller själv beskriva vad sagan ska handla om.
Applikationen kommer att byggas med en Java/Spring Boot‑backend som integreras med AI‑modeller för text- och bildgenerering,
samt en mobil frontend utvecklad i React Native (via Expo). Projektet kommer om tiden tillåter även att inkludera möjlighet att spara sagor i en databas och,
stöd för röstinmatning och uppläsning._

_Syftet är att undersöka hur AI kan användas för att generera barnvänligt innehåll, samt bygga en fungerande prototyp som demonstrerar funktionaliteten.
Resultatet kommer att analyseras med fokus på språknivå, struktur och bildrelevans._

## 2. Bakgrund och Problemformulering

### 2.1 Bakgrund

_Generativa AI‑modeller har på senare år fått förmågan att skapa både text och bilder baserat på användarinmatning. Detta öppnar för nya typer av digitala 
verktyg som automatiskt kan producera innehåll som tidigare krävde manuellt arbete, såsom sagor, illustrerade berättelser och pedagogiskt material. 
Barnsagor är en särskild kategori av text som kräver anpassning av ordval, berättarstruktur, längd och ton efter barnets ålder. Även illustrationerna 
behöver vara begripliga, relevanta och åldersanpassade. Trots att AI‑modeller kan generera kreativt innehåll saknas lättillgängliga prototyper som kombinerar 
åldersanpassad text, tema‑val, talbaserad input och AI‑genererade bilder i ett sammanhållet system. Det skapar ett relevant tekniskt problem: Hur väl kan AI hantera 
åldersanpassning, och hur bra är bilderna i förhållande till sagans innehåll? Detta projekt utforskar denna fråga genom att bygga en prototyp i Java som genererar
sagor och bilder baserat på användarens val._

### 2.2 Problemformulering

_Hur kan en Java‑applikation generera barnanpassade sagor med hjälp av AI, och hur väl kan AI anpassa språk, 
struktur och bildinnehåll efter olika åldersgrupper och teman?_

### 2.3 Syfte och Mål

**Syfte:** 

_Syftet med detta projekt är att utveckla en prototyp som genererar korta barnanpassade sagor med tillhörande AI‑illustrationer 
och att utvärdera kvaliteten i de texter och bilder som genereras. Lärdom om hur det fungerar med att implementera AI, 
hur hårt man kan reglera den för att inte skicka opassande sagor och bilder._

**Specifika mål:**

- _Mål 1: Utveckla en Java‑baserad backend som kan kommunicera med en AI‑modell för textgenerering._
- _Mål 2: Implementera generering av AI‑baserade bilder som matchar sagans innehåll._
- _Mål 3: Skapa ett enkelt användargränssnitt där användaren kan välja ålder, tema och eventuellt prata in en kort beskrivning._
- _Mål 4: Generera 5–10 sagor och analysera språknivå, struktur och bildrelevans._
- _Mål 5: Identifiera begränsningar och risker med AI‑genererat innehåll för barn._

### 2.4 Avgränsningar

- Ingen djupgående pedagogisk analys av barns språkutveckling.
- Ingen användarstudie eller testning på barn.
- Ingen fullständig boklayout eller publiceringsplattform.
- Ingen egen träning av AI‑modell, endast existerande API används. (Behöver dock kunna begränsas i hur den genererar sagor och bilder)
- Begränsat antal sagor ca 5–10st för analys.
- Fokus ligger på funktionalitet, inte avancerad UI‑design.

## 3. Teknisk Specifikation (för utvecklingsprojekt)

### 3.1 Teknisk Stack

- **Frontend:**
    - React Native (via expo för snabbare utveckling och enkel testning på mobil)

- **Backend:**
    - Java, Spring Boot (REST-API för text och bildgenerering)

- **Databas:**
    - MongoDB eller PostgreSQL  

- **Övrigt:**
    - AI‑API för textgenerering
    - AI‑API för bildgenerering
    - Möjlighet att använda lokala öppna AI‑modeller (t.ex. via Ollama) för att undvika API‑kostnader.
    - Ev. Web Speech API för tal‑till‑text
    - JUnit för tester
    - GitHub för versionshantering och projekthantering

### 3.2 Funktionella Krav

_Lista de viktigaste funktionerna som systemet ska ha_

- Användare ska kunna välja ålder på mottagaren
- Användare ska kunna välja tema eller skriva eget tema
- Systemet ska generera en saga baserat på input
- Systemet ska generera 1–3 bilder kopplade till sagan
- Resultatet ska presenteras i ett enkelt gränssnitt
- Användaren ska kunna ge röstinput (valfritt)
- Systemet ska kunna spara genererade sagor i en databas (valfritt)
- Systemet ska kunna läsa upp sagor (valfritt)

### 3.3 Icke-funktionella Krav

- **Prestanda:** _Appen ska generera text inom 10 sekunder_
- **Säkerhet:** _Ingen personlig data lagras_
- **Stabilitet:** _Appen ska hantera fel utan att krascha_
- **Användbarhet:** _UI ska vara enkelt att förstå både för förälder och barn_
- **Tillgänglighet:** _Texten ska vara läsbar på både mobil, surfplatta och dator_

## 4. Metod och Genomförande

### 4.1 Utvecklingsmetod

_Github project, kommer att arbeta i sprintar som är 1 vecka för att tydligt kunna följa hur långt jag har kommit i arbetet.
Lägga upp många och tydliga issues. Göra många små commits_

### 4.2 Arbetsprocess

_Beskriv steg-för-steg hur du planerar att genomföra projektet:_

1. _Fas 1: Kravanalys och design_
    - Definiera vilka AI-API:er som ska användas
    - Design av endpoints och databasstruktur
    - Skapa en enkel UI-skiss

2. _Fas 2: Utveckling av grundfunktioner_
    - Implementera backend-logik för textgenerering
    - Implementera bildgenerering
    - Skapa grundläggande UI för input och visning av saga och bilder

3. _Fas 3: Implementation av avancerade funktioner_
    - Implementera röstinput (om det finns tid)
    - Implementera sparfunktion i databas (om det finns tid)
    - Implementera uppläsning av sagor (om det finns tid)

4. _Fas 4: Testning och debugging_
    - Enhetstestning av backend-komponenter
    - Manuell testning av hela flödet från input till genererad saga
    - Åtgärda buggar och förbättra prestanda

5. _Fas 5: Dokumentation och slutrapport_
    - Sammanställa metod, resultat och analys i rapporten
    - Färdigställa dokumentation av kod och användning
    - Förbereda presentation av projektet

### 4.3 Verktyg och Resurser

- **Utvecklingsverktyg:**
    - IntelliJ IDEA (backendutveckling i Java/Spring Boot)
    - Visual Studio Code (frontendutveckling i React Native)
    - Github (versionshantering)

- **Testverktyg:**
    - JUnit för enhetstester i backend
    - Manuell testning av UI och flöde i mobilapp

- **Projekthantering:** _(t.ex. Trello, Jira, GitHub Projects)_
    - GitHub Projects för att organisera issues och sprintar

- **Externa resurser:**
    - Dokumentation för valda AI-modeller
    - Eventuella bibliotek för tal-till-text i React Native



## 5. Tidsplan

### 5.1 Milstolpar

| Vecka | Milstolpe                      | Leverabler                       |
|-------|--------------------------------|----------------------------------|
| 1     | _Kravanalys och systemdesign_  | _Mockups, API-struktur_          |
| 1-2   | _Grundläggande backend_        | _Textgenereing fungerar_         |
| 2-3   | _Bildgenereing och UI_         | _Prototyp klar_                  |
| 3     | _Testning och analys_          | _Genererade sagor, anteckningar_ |
| 4     | _Slutrapport och presentation_ | _Färdig rapport, powerpoint_     |

### 5.2 Tidsallokering

- **Timmar per vecka:** _35-40 timmar_
- **Total beräknad arbetstid:** _140-160 timmar_

## 6. Riskanalys

| Risk                                                                  | Sannolikhet | Påverkan | Åtgärd                                                                                |
|-----------------------------------------------------------------------|-------------|----------|---------------------------------------------------------------------------------------|
| _Tekniska problem med API_                                            | _Medel_     | _Hög_    | _Identifiera alternativa API:er_                                                      |
| _Tidsbrist_                                                           | _Hög_       | _Medel_  | _Reducera funktionsomfattning_                                                        |
| _Tar för lång tid att generera bilder_                                | _Hög_       | _Hög_    | _Begränsa till endast en bild_                                                        |
| _AI genererar olämpligt innehåll_                                     | _Medel_     | _Hög_    | _Implementera filter och begränsningar_                                               |
| _AI försöker att generera bilder av upphovsrättsskyddade karaktärer_  | _Hög_       | _Hög_    | _Prompt‑sanering: AI instrueras att ersätta sådana figurer med originella karaktärer_ |
| _Lokala AI‑modeller kan ha varierande prestanda beroende på hårdvara_ | _Medel_     | _Medel_  | _Använd mindre modeller eller fallback till moln‑API vid behov_                       |

## 7. Utvärdering och Testning

### 7.1 Testplan

Projektet kommer att testas genom en kombination av tekniska tester och kvalitativ analys:

- **Enhetstestning:**  
  Test av backend‑komponenter och API‑endpoints (t.ex. att rätt input ger ett korrekt AI‑anrop).

- **Integrationstestning:**  
  Test att backend korrekt kommunicerar med AI‑modell för både text och bildgenerering.

- **Funktionstestning (manuell):**  
  Genomföra fullständiga flöden i applikationen för att verifiera att åldersval, tema och resultatvisning fungerar utan fel.

- **Kvalitativ innehållsanalys:**  
  Generera 5–10 sagor och utvärdera språknivå, struktur och bildrelevans i relation till vald åldersgrupp.

### 7.2 Framgångskriterier

- Kriterium 1: Systemet genererar sagor utan fel inom en rimlig tid
- Kriterium 2: Bilderna är relevanta för sagans innehåll
- Kriterium 3: Språket är anpassat utifrån vald åldersgrupp
- Kriterium 4: Prototypen fungerar i sin helhet

## 8. Referenser och Källor_Lista relevanta källor, dokumentation, tutorials och annan litteratur som du planerar att använda._

- Dokumentation för vald AI‑modell (text och bild)
- Java / Spring Boot dokumentation
- React Native och Expo dokumentation
- MongoDB eller PostgreSQL dokumentation
- Artiklar och tutorials om generativ AI och prompt‑design
- AI‑assistans under utvecklingsprocessen (t.ex. felsökning och kodförslag)
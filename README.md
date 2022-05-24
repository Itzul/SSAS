# Flyg med SSAS
#### Itzul L. Vergara

## Intro

Efter att har skapat mitt StarSchema är det dags att börja bygga kuben! I grunduppgiften skapar vi en Multidimensional modell. 

Det finns tre stora delar:
* Data Source Views 
* Dimensions 
* Cube


## Data Source Views

<img width="461" alt="image" src="https://user-images.githubusercontent.com/19158658/170114442-6066c22d-8954-4daf-9468-5341d52a3c7d.png">

Jag skapade två *Named edited calculation*  för att testa, en kopplade Routes (origin.State med destiny.State) och den andra kopplade Carrier (CarrierID med Description). 

## Dimensions

<img width="596" alt="image" src="https://user-images.githubusercontent.com/19158658/170115371-d73762e2-3a39-467a-b155-c24944aa64ea.png">

För att ha lämpliga dimensioner bytte jag några detaljer: nu finns två hierarkier i datum: År,kvartal, månad, dag. och År, vecka, dag. Samt två i Routes : Origin, destiny. CarrierID är inte gömt men den visar Description istället. 

## Cube 
<img width="674" alt="image" src="https://user-images.githubusercontent.com/19158658/170116384-05d1f4f6-2f31-4811-9577-cd11f103c04c.png">

Kuben är klar, några measures har adderats! Men i automatisk räkning finns inte medelvärde med så jag var tvungen att skapa det med *caluculations*:

<img width="762" alt="image" src="https://user-images.githubusercontent.com/19158658/170119389-06dc096d-0c6e-483a-bc35-f8e2597fb45b.png">


## Multidimensional modell vs Tabular modell


Multidimensional model introducerades innan Tabular modellen 2010 vs 2016. Tabular är mycket snabbare och enklare men kräver också mer RAM. Fördelar med multidimensional är att den kan hantera mycket mer data och göra mer komplicerade measures. Den här tabellen förklara enklare: 

<img width="657" alt="image" src="https://user-images.githubusercontent.com/19158658/170120506-b35c51b3-15ac-4326-a206-9ec117532109.png">



# Stort Tack!


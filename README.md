# SSAS
#### Itzul L. Vergara

## Intro

Efter att har skapat mitt StarSchema nu är dags att börja bygga kuben! I grunduppgiften skapar vi en Multidimensional modell. 

Det finns tre stora delar:
* Data Source Views 
* Dimensions 
* Cube


## Data Source Views

<img width="461" alt="image" src="https://user-images.githubusercontent.com/19158658/170114442-6066c22d-8954-4daf-9468-5341d52a3c7d.png">

Jag skapade två *Named edited calculation* där för att testa, med en kopplade  Routes: origin.State och destiny.State med en '-' och en för att koppla Carrier ID samt Description som Carrier. 

## Dimensions

<img width="596" alt="image" src="https://user-images.githubusercontent.com/19158658/170115371-d73762e2-3a39-467a-b155-c24944aa64ea.png">

För att ha lämpliga dimensioner bytte några detaljer: nu finns två hierarkier i datum: År,kvartal, månad, dag. och År, vecka, dag. Samt två i Routes : Origin, destiny. CarrierID är inte gömt men den visar Description istället. 

## Cube 
<img width="674" alt="image" src="https://user-images.githubusercontent.com/19158658/170116384-05d1f4f6-2f31-4811-9577-cd11f103c04c.png">

Kuben är nästan klar, några measures har varit adderat! Men i automatisk räkning finns inte medelvärde då var jag tvungen att skapa med *caluculations*:

<img width="704" alt="image" src="https://user-images.githubusercontent.com/19158658/170118165-f26ddc6a-d691-4489-be89-6230f1fe4fa8.png">

### Kuben är  klar! 


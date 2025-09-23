# Mini signalizacijos sistema su Arduino

## Projekto aprašymas
Šis projektas imituoja paprastą signalizacijos sistemą. Sistema aptinka judesį naudodama PIR jutiklį ir įjungia garsinį bei vizualinį signalą (buzzer ir LED). Tokios sistemos gali būti naudojamos patalpų apsaugai ar automatiniam judesio aptikimui.

## Naudoti komponentai
- Arduino Uno
- PIR judesio jutiklis
- LED su rezistoriumi (220 Ω)
- Buzzer
- Breadboard
- Jungiamieji laidai

## Schema
Komponentų sujungimas:
- PIR OUT → D2  
- LED → D12 (per rezistorių į GND)  
- Buzzer → D13  
- Maitinimas: 5V ir GND iš Arduino  

![Schema](HW1.png)  

## Programinė dalis
Naudojau Arduino IDE / Tinkercad aplinką. Kodas nuskaito PIR jutiklio signalą ir pagal jį įjungia arba išjungia LED bei buzzer. (Visas kodas yra "main" faile).

## Kas veikia / kas neveikė
Kas veikia: Dabar viskas veikia puikiai, sistema aptinka signalą, įjungia LED ir buzzer, o po judesio pabaigos išjungia.
Kas neveikė: Buvo taip, jog buvau ne taip, kaip reikia sujungęs porą laidų, todėl tik paleidus simuliaciją, Buzzer'is veikdavo be perstojo (visą laiką pypdavo).

## Ateities patobulinimai
- Pridėti LCD ekraną, kuris rodytų, kiek kartų aptiktas judesys.
- Prijungti Wi-Fi modulį, kad praneštų apie judesį telefonu.
- Vietoje paprasto buzzerio naudoti garsinė sireną.

## Išvada
Projektas pademonstravo, kaip galima sujungti sensorių ir aktuatorių naudojant Arduino. Sistema veikia kaip paprasta signalizacija, tinkama mokumuisi ir pagrindiniams automatizacijos principams suprasti.

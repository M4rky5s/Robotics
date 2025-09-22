1. Projekto pavadinimas - Mini signalizacijos sistema su Arduino

2. Šis projektas imituoja paprastą signalizacijos sistemą. Sistema aptinka judesį naudodama PIR jutiklį ir įjungia garsinį bei vizualinį signalą (buzzer ir LED). Tokios sistemos gali būti naudojamos patalpų apsaugai ar automatiniam judesio aptikimui.

3. Dizainas:
     Naudoti komponentai:
       Arduino Uno
       PIR judesio jutiklis
       LED su rezistoriumi
       Buzzer
       Breadboard Mini + jugiamieji laidai
     Schenma:
       PIR -> D2, LED -> D12, Buzzer -> D13, maitinimas iš Arduino (5V, GND).
     Veikimo principas:
       Kai PIR aptinka judesį, LED užsidega ir buzzer pradeda skleisti garsą. Kai judesys nebeaptinkamas - sistema nutils.

4. Programinė dalis:
     Naudojau Arduino IDE / Tinkercad aplinką. Kodas nuskaito PIR jutiklio signalą ir pagal jį įjungia arba išjungia LED bei Buzzer. (Kodo pavyzdys yra pateiktas "main" faile).

5. Kas veikia / kas neveikė:
     Kas veikia: Dabar viskas veikia puikiai, sistema aptinka signalą, įjungia LED ir buzzer, o po judesio pabaigos išjungia.
     Kad neveikė: Buvo taip, jog buvau ne taip, kaip reikia sujungęs porą laidų, todėl tik paleidus simuliaciją, Buzzer'is veikdavo be perstojo (visą laiką pypdavo).

6. Ateities patobulinimai:
     Pridėti LCD ekraną, kuris rodytų, kiek kartų aptiktas judesys.
     Prijungti Wi-Fi modulį, kad praneštų apie judesį telefonu.
     Vietoje paprasto buzzerio, naudoti garsesnę sireną.

7. Išvada:
     Projektas pademonstravo, kaip galima sujungti sensorių ir aktuatorių naudojant Arduino. Sistema veikia kaip paprasta signalizacija, tinkama mokumuisi ir pagrindiniams automatizacijos principams suprasti.

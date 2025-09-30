# Mini signalizacijos sistema su Arduino

## Projekto aprašymas
Šis projektas imituoja paprastą signalizacijos sistemą. Sistema aptinka judesį naudodama PIR jutiklį ir įjungia garsinį bei vizualinį signalą (buzzer ir RGB LED(aptikus signala - Raudona spalva, neaptinkant signalo - žalia spalva). Išjungti signalizaciją galima tik suvedus teisingą slaptažodį, kitu atvėju signalizacija taip ir neišsijungs, kol nebus įvestas teisingas slaptažodis. Tokios sistemos gali būti naudojamos patalpų apsaugai ar automatiniam judesio aptikimui.

## Naudoti komponentai
- Arduino Uno
- PIR judesio jutiklis
- RGB LED
- Rezistoriai
- Buzzer
- Breadboard
- LCD 16x2 (I2C)
- Mygtukas (Pushbutton)
- Keypad 4x4
- Jungiamieji laidai

## Schema
Komponentų sujungimas:
- PIR OUT → D8  
- RGB LED → D12, D11, D10 (per rezistorių į GND)  
- Buzzer → D13
- LCD I2C: Arduino GND → GND, 5V → VCC, A4 → SDA, A5 → SCL
- Keypad: ROWS → D7, D6, D5, D4. COLS → D3, D2, D1, D0.
- Maitinimas: 5V ir GND iš Arduino  

![Schema](HomeWork1.png)  

## Programinė dalis
Naudojau Arduino IDE / Tinkercad aplinką. Priklausomai nuo sistemos būsenos (ji OFF ar ON) kodas nuskaito PIR jutiklio signalą ir pagal jį įjungia RGB LED bei buzzer. Prasidėjus alarmui, reikia suvesti teisingą PIN kodą, kad sistema nustotų pypti. Suvedus teisingą PIN, naudojantis mygtuku, sistemą galima įjungti arba išjungti. (Visas kodas yra "main" faile).

## Kas veikia / kas neveikė
Kas veikia: Dabar viskas veikia puikiai, tik pradėjus simuliaciją, LCD I2C įsijungia, jeigu sistema aptinka signalą, įjungia RGB LED (raudona spalva) ir buzzer, norint juos išjungti reikia suvesti teisinga slaptažodį naudojantis Keypad (visą vedamą slaptažodį rodo ekrane). Suvedus teisingą slaptažodį, sistema išsijungia, alarmas išsijungia, paspaudus mygtuką, sistemą galima vėl įjungti ir laukti judesio. (Kol judesio neaptinkama ir sistema įjungta, RGB LED lemputė šviečia žaliai).
Kas neveikė: Iš karto tik prijungus LCD I2C ekraną prie Arduino, jis neveikė, nerodė nieko, tai teko googl'inti kur buvo problema. Taip pat buvo, jog neveikė buzzeris, bet ten buvo problema tokia, kad buvau neteisingai sujungęs buzzerio laidus.

## Ateities patobulinimai
- Manau galima būtų kažkaip pridėti papildomus jutiklius, kurie tikrintų ar pvz. patalpos durys ir langai yra uždaryti ar ne. Ir jeigu neuždaryti, Alarmas neveiktų.
- Prijungti Wi-Fi modulį, kad praneštų apie judesį telefonu.
- Vietoje paprasto buzzerio naudoti garsinė sireną.

## Išvada
Projektas pademonstravo, kaip galima sujungti RGB LED, PIR sensorių, LCD I2C ekraną, mygtuką bei keypad ir sukonstruoti kažką naudingo. Sistema veikia kaip paprasta signalizacija, tinkama mokymuisi ir pagrindiniams automatizacijos principams suprasti.

<video loop src="FirstHWDemo.mp4" width="600">video</video>

# BG bron

## Voor Dexcom gebruikers  


### Dexcom G5 of G6 met xDrip+  


* Als het nog niet ingesteld is, download dan [xdrip](https://github.com/NightscoutFoundation/xDrip) en volg de instructies voor nightscout ([G4 zonder 'share'](http://www.nightscout.info/wiki/welcome/nightscout-with-xdrip-wireless-bridge), [G4 met 'share'](http://www.nightscout.info/wiki/welcome/nightscout-with-xdrip-and-dexcom-share-wireless), [G5](http://www.nightscout.info/wiki/welcome/nightscout-with-xdrip-and-dexcom-share-wireless/xdrip-with-g5-support)).
* In xdrip ga naar Settings > Interapp Compatibility > Broadcast Data Locally en selecteer ON.
* In xdrip ga naar Instellingen > Interapp settings > Accepteer Lokaal uitgezonden en selecteer UIT.
* Als je AndroidAPS wilt gebruiken om te kalibreren ga dan in xdrip naar Instellingen > Interapp settings > Accept Calibrations en selecteer OP. Je kunt ook de opties bekijken in Instellingen > Minder vaak voorkomende instellingen > Advanced Calibration Settings.
* Selecteer xdrip in ConfigBuilder (instellingen in AndroidAPS).

### Dexcom G5 of G6 met de aangepaste Dexcom app  


* Download de apk van <https://github.com/dexcomapp/dexcomapp>, en kies de versie die je nodig hebt (mg/dl of mmol/l versie, voor G5 of G6).
* Stop sensor en verwijder de originele Dexcom app, als dat nog niet gedaan is.
* Installeer de gedownloade apk
* Start sensor
* Selecteer Dexcom G5 App (patched) in ConfigBuilder (instelling in AndroidAPS).

### Dexcom G4 met OTG kabel ('traditionele' Nightscout)  


* Als dit nog niet is ingesteld download dan Nightscout Uploader app vanuit de Play Store en volg de instructies op [Nightscout](http://www.nightscout.info/wiki/welcome/basic-requirements).
* In AndroidAPS Preferences enter your Nightscout website and API secret.
* Selecteer NSClient in ConfigBuilder (setting in AndroidAPS).

## Voor Libre gebruikers met Bluetooth-adapter  


Om je Libre te gebruiken als een CGM die elke 5 minuten nieuwe BG waarden krijgt, moet je eerst een NFC naar Bluetooth adapter kopen, zoals:

* MiaoMiao-Reader <https://www.miaomiao.cool/>
* Blukon Nightrider <https://www.ambrosiasys.com/howit>
* BlueReader <https://bluetoolz.de/blueorder/#home>
* Sony Smartwatch 3 (SWR50) als Auslesetool <https://github.com/pimpimmi/LibreAlarm/wiki/>

### Libre met xDrip+  


* Als nog niet is ingesteld dan download xdrip en volg de instructies op: [LimiTTEer](https://github.com/JoernL/LimiTTer), [Libre Alarm](https://github.com/pimpimmi/LibreAlarm/wiki) or [BlueReader](https://unendlichkeit.net/wordpress/?p=680&lang=en)([Hardware](https://bluetoolz.de/wordpress/)).
* In xdrip ga naar Settings > Interapp Compatibility > Broadcast Data Locally en selecteer ON.
* In xdrip ga naar Instellingen > Interapp settings > Accepteer Lokaal uitgezonden en selecteer UIT.
* Als je AndroidAPS wilt gebruiken om te kalibreren ga dan in xdrip naar Instellingen > Interapp settings > Accept Calibrations en selecteer OP. Je kunt ook de opties bekijken in Instellingen > Minder vaak voorkomende instellingen > Advanced Calibration Settings.
* Selecteer xdrip in ConfigBuilder (instellingen in AndroidAPS).
* Voor G5 native-mode in xDrip, ga naar Instellingen > Cloud Upload >> REST API > Extra options > Append source info to device en selecteer ON.

### Libre met Glimp  


* If not already set up then download Glimp and follow instructions on [Nightscout](http://www.nightscout.info/wiki/welcome/nightscout-for-libre).
* Selecteer Glimp in ConfigBuilder (instellingen in AndroidAPS).

## Voor Eversense gebruikers  


De makkelijkste manier om de Eversense te gebruiken met AndroidAPS is om de aangepaste [Eversense app](https://github.com/BernhardRo/Esel/blob/master/apk/mod_com.senseonics.gen12androidapp-release.apk) te installeren (en de originele app eerst te verwijderen).

**Waarschuwing: door de oude app te verwijderen zullen jouw lokaal opgeslagen (glucose)gegevens ouder dan een week, ook worden verwijderd!**

Om jouw gegevens vervolgens in AndroidAPS te krijgen, moet je [ESEL installeren](https://github.com/BernhardRo/Esel/blob/master/apk/esel.apk) en "Send to AAPS and xDrip" (Stuur naar AAPS en xDrip) in ESEL aanzetten. Ook moet je "MM640g" kiezen als BG bron in de [Configuratie Builder](../Configuration/Config-Builder.md) in AndroidAPS. As the BG data from Eversense can be noisy sometimes, it is good to enable "Smooth Data" in ESEL, which is better than enabling "Always use short average delta instead of simple delta" in AAPS.

Een andere instructie voor het gebruik van xDrip+ met Eversense vind je [hier](https://github.com/BernhardRo/Esel/tree/master/apk).

## Voor MM640g of MM630g gebruikers  


* If not already set up then download [600SeriesAndroidUploaer](http://pazaan.github.io/600SeriesAndroidUploader/) and follow instructions on [Nightscout](http://www.nightscout.info/wiki/welcome/nightscout-and-medtronic-640g).
* In 600 Series Uploader ga naar Instellingen > Send to xdrip+ en selecteer ON (vinkje).
* Selecteer MM640g in ConfigBuilder (Instelling AndroidAPS).

## Voor PocTech CT-100 gebruikers  


* Installeer PocTech App
* Selecteer PocTech App in ConfigBuilder (instelling in AndroidAPS).

## For users of other CGM uploaded to Nightscout  


If you have any other CGM set up that sends your data to [Nightscout](http://www.nightscout.info) then  


* In AndroidAPS Preferences enter your Nightscout website and API secret.
* Selecteer NSClient in ConfigBuilder (setting in AndroidAPS).
## Cel programu
Katalog zawiera program testujący działanie stosu Bluetooth.
https://infocenter.nordicsemi.com/index.jsp?topic=%2Fcom.nordic.infocenter.sdk5.v14.2.0%2Fexamples_ble.html&cp=4_0_0_4_2

Zadanie to: 
- podłączyć na komputerze w Lab_l2.1 po UART  NRF52, odebrać jakiś napis z terminala (kod z poprzednich zajęć!) i odesłać przesłaną ramkę po BLE jako ADVERTISING.
- z aplikacji nasłuchającej skopiować odebrane bajty, przeanalizować ramkę w postacic RAW i sprawdzić czy udało się przesłać poprawne watości.


## Opis
Po uruchomieniu urządzenie powinno być widoczne dla skanerów BLE (np. aplikacji nRF Connect dla systemu Android).
https://play.google.com/store/apps/details?id=no.nordicsemi.android.mcp&hl=pl

Pakiety BLE logowane są w snifującej aplikacji dziąłającej na RPi jako "sink" i można je sobie obejrzeć w przeglądarce pod adresem:
http://192.168.1.107:5000/api/transmission

Proszę znaleźć tam pakiet przesłany ze swojego progarmu i ustalić czy odebrane dane zostały przesłane jako ciąg znaków wystawionych po URAT z terminala komputera w laboratorium do którego podłączony został NRF52_DK. 

Pomocne narzdzia...
echo 'wklej odebrany payload (ascii)' > payload
hexdump -C payload
xxd  -r -p payload > payload.bin
cat payload.bin
xxd payload.bin


https://devzone.nordicsemi.com/tutorials/b/bluetooth-low-energy/posts/ble-advertising-a-beginners-tutorial
http://developer.nordicsemi.com/
http://developer.nordicsemi.com/nRF5_SDK/doc/

https://www.silabs.com/community/wireless/bluetooth/knowledge-base.entry.html/2017/02/10/bluetooth_advertisin-hGsf
https://www.silabs.com/community/wireless/bluetooth/knowledge-base.entry.html/2017/11/14/bluetooth_advertisin-zCHh
 

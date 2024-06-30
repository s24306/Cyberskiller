> ##  W katalogu domowym użytkownika alice znajduje się przechwycony ruch sieciowy zaszyfrowany protokołem WPA pod nazwą file.pcap. Użytkownik Bob, który wysłał plik file.pcap użytkownikowi Alice, nagrał ruch sieciowy podczas przesyłania odpowiedzi do zadania w celu późniejszego przeanalizowania szyfrowanego ruchu. Z racji, że Bob wykorzystał protokół TLS, poprosił administratora serwera o klucz prywatny wykorzystywany w tym protokole. Niestety, zapisując nagrywany ruch Bob nie był świadom, że wśród nagranych pakietów znajduje się również klucz prywatny serwera. Odszyfruj ruch sieciowy WPA oraz TLS w celu uzyskania odpowiedzi. Do złamania protokołu WPA wykorzystaj słownik 10k najpopularniejszych haseł 10k-most-common.txt.

W ramach zadania otrzymujemy adres IP serwera i dane logowania  
Po zalogowaniu się do systemu znajdziemy plik pcap  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/7d1f16b5-1497-4d3a-bb7b-f31adc172cbc)  

Pobierzmy go na naszą maszynę  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/074d4f89-5ac1-490e-9738-83a525cf134e)

Gdy otworzymy plik, naszym oczom ukaże się SSID boba - `Bob_AP`  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/e4e294e1-e34e-423b-a000-c50a47172b4d)  

Spróbujmy scrakować jego hasło za pomocą aircrack-ng  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/73c12ee6-7b37-48ac-bc09-335094d193bc)  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/179b4dd2-2700-4024-87aa-e44ed1880812)  

Hasło udało nam się znaleźć w mniej niż sekundę.  
Rozszyfrujmy więc komunikację WPA.  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/8a9a79b0-ab9b-4e03-b244-95bfd1ded97e)  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/da1cc623-f937-4fe6-8de7-9e345af1032e)  

Dzięki temu jesteśmy teraz w stanie zobaczyć komunikację TLS  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/b6bf7b05-82df-40ce-b2a0-29ac676cfc0e)  

Na samym dole pakietów znajdziemy jeden, który zawiera w sobie klucz prywatny boba  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/d046eb74-1f62-4161-ae1e-17853c1f6197)

Wyeksportujmy go  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/7a709a90-5c03-47c6-aa91-9e89f8cdf29e)  

Teraz, gdy mamy już klucz prywatny zapisany w pliku key.pem, dodajmy do do kluczy rsa dla TLS  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/9bbf8c01-37b1-4789-ba81-91581225b242)  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/6c5d0efa-3313-489f-987b-515a33cc9183)  

Powinna ukazać nam się rozszyfrowana komunikacja po http, jeśli tak się nie stało, być może trzeba zrestartować wiresharka  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/2116e9e4-b2ff-4b4f-a743-5517ca25e507)  

Follow -> http stream pozwoli nam ujrzeć pakiet w przystępnej formie i uzyskać odpowiedź  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/27b0064b-1e75-40c6-a896-868e13a958c4)


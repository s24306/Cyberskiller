> ## Na maszynie uruchomiony jest pewien kontroler w postaci aplikacji WWW. Twoim zadaniem jest odnalezienie podatności oraz wykorzystanie jej za pomocą odpowiedniego modułu metasploit. Odpowiedź do zadania znajduje się w katalogu domowym użytkownika root.

W ramach zadania dostajemy IP maszyny.  
Po przeskanowaniu nmapem zauważymy, że aplikacja działa na porcie 8080  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/fbb02d41-9eab-4d62-89a2-dc62f6d15262)  

Po wejściu na ten adres w przeglądarce naszym oczom ukaże się aplikacja Unifi  
![Screenshot from 2024-06-23 15-58-28](https://github.com/s24306/Cyberskiller/assets/91730770/fc36736e-9ee0-43e2-9401-f7ad1a852b58)  

Znajdźmy w msfconsole exploit, które nam pomoże w dostaniu się do systemu  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/94c76da4-9da2-4955-bc79-ccad7efa8cde)  

Po skonfigurowaniu modułu i uruchomieniu go, znajdziemy naszą odpowiedź do zadania  
![Screenshot from 2024-06-23 18-28-04](https://github.com/s24306/Cyberskiller/assets/91730770/076956cd-61d7-444f-8355-e87e3c41be6a)

> ##  Na maszynie uruchomiony został serwer DNS. Jedna z wielu subdomen, która skonfigurowana jest na serwerze, zawiera odpowiedź do zadania. Główną domeną jest local. Twoim zadaniem jest odnalezienie wspomnianej subdomeny za pomocą enumeracji. 

W ramach zadania dostajemy adres IP serwera DNS.  
Znajdźmy w msfconsole moduł, który pomoże nam go enumerować.  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/1b4de8e9-bda4-439f-824b-b056cb4129bd)

Ustawiamy opcje w module, włączamy oczywiście bruteforce i uruchamiamy.  
Możemy zobaczyć, że znaleziona została subdomena 8.local  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/94997851-48c7-424f-b076-86b77f82322e)

Niech moduł teraz przeszuka wszystko pod 8.local  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/81f0c251-8e6f-4560-b88b-dee990703ccb)

Znaleźliśmy kolejną subdomenę 02.8.local, powtarzamy proces i znajdujemy odpowiedź  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/1a99434f-7a3c-406a-9f7c-8df2c08a395c)

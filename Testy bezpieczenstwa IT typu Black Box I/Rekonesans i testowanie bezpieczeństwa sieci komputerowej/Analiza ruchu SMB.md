> ## Na serwerze działa usługa, która zapisuje plik z odpowiedzią przy użyciu Samby. Wystarczy tylko dobrze się wsłuchać i poznasz odpowiedź!

W ramach zadania otrzymujemy adres IP, oraz dane logowania do serwera  
Po zalogowaniu się sprawdźmy, czy mamy uprawnienia sudo do jakiegoś programu  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/1565c486-c7d3-4bbc-86c3-55cbdae18c0e)  

Z racji, iż wiemy, że chcemy wyeksploitować sambę, sprawdźmy czy możemy odczytać plik konfiguracyjny  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/cc683f2d-6111-4196-8fbd-a052235a677a)  

Widzimy, że mamy share w /var/smb, dostęp do tych plików ma tylko i wyłącznie użytkownik bob, ale możemy przejrzeć co tam jest  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/a6ae3c27-c47f-44b5-8f68-cf2a9b452da9)  

Wiemy, gdzie jest plik z odpowiedzią, oraz mamy dostęp do sudo poprzez tcpdump.  
Zobaczmy, czy możemy znaleźć eskalację uprawnień na [gtfobins](https://gtfobins.github.io/)  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/acd99814-df53-4c21-a5d8-ca6653a49ad4)  

Użyjmy znaalezionego przez nas exploita  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/64ad1b65-112b-4f05-8944-f4f70746ea85)

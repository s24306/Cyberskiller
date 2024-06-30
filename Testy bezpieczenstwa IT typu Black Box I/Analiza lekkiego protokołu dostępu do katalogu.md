> ## Masz możliwość podniesienia uprawnień jednego z narzędzi. Użyj go, żeby przeanalizować protokół dostępu do katalogu, który działa na serwerze. Odpowiedź do zadania znajduje się w atrybucie obiektu cn=secret,dc=cyberskiller,dc=com.

W ramach zadania otrzymujemy adres IP i dane logowania  
Po zalogowaniu znów mamy dostęp do tcpdump.  Tym razem użyjmy go zgodnie z przeznaczeniem i przechwyćmy ruch, który się odbywa na serwerze.  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/c99c3235-df5d-447d-b4b6-1a92e07fe97f)  

Pobierzmy plik do analizy za pomocą scp na naszą maszynę  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/8db873ed-8dea-423f-9057-6e4bdee69984)  

Otwórzmy nasz plik w wiresharku i znajdźmy pakiet zawierający interesujące nas atrybuty za pomocą Edit -> Find packet.  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/13dfbc97-9335-483e-8885-13e764603228)  

Naszą odpowiedź zobaczymy po rozwinięciu LDAPa  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/a1bae381-d11a-47bf-b4b8-c4992159b78e)

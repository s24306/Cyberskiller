> ## Na maszynie uruchomiona jest prosta aplikacja webowa, umożliwiająca wgranie pliku na serwer. Twoim zadaniem jest wgrać wykonywalny payload meterpreter w celu uzyskania powłoki użytkownika bob. W katalogu domowym użytkownika bob pozostawiono informacje na temat konta użytkownika jenny. Twoim zadaniem jest uzyskać dostęp do konta jenny. Odpowiedź znajdziesz w katalogu domowym tego użytkownika w pliku secret.txt.

W ramach zadania dostajemy adres IP maszyny, na której uruchomiona jest aplikacja web.  
Możemy zacząć od przygotowania payloadu meterpretera w msfvenom  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/c0cfd1bd-539d-40ef-a203-85e7b346970d)  

Wybierzmy multi/handler w msfconsole, ustawmy payload i odpalmy  
![Screenshot from 2024-06-23 14-34-43](https://github.com/s24306/Cyberskiller/assets/91730770/7d6e20ee-ae4d-4991-a5bd-f3368bc99c15)

Teraz, gdy nasłuchiwanie jest już włączone, możemy zuploadować nasz payload  
![Screenshot from 2024-06-23 14-08-16](https://github.com/s24306/Cyberskiller/assets/91730770/e1904db3-3c3b-4512-b867-d17e43709be6)

Po dostaniu się na serwer, możemy znaleźć dane logowania dla jenny  
![Screenshot from 2024-06-23 14-39-54](https://github.com/s24306/Cyberskiller/assets/91730770/2e363e59-7878-493b-be02-ca2ff5f4c969)

Wrzućmy naszą sesję meterpretera w tło i znajdźmy moduł, który pomoże nam zalogować się na konto jenny  
![Screenshot from 2024-06-23 14-12-58](https://github.com/s24306/Cyberskiller/assets/91730770/b530a6b4-6dd2-40a0-a6e8-d1ffbcb9fc53)

Ustawmy potrzebne dane i rozpocznijmy eksploitację  
![Screenshot from 2024-06-23 14-57-37](https://github.com/s24306/Cyberskiller/assets/91730770/a8709fcc-6a39-453b-acb8-7f1ec71793ca)

Po dostaniu się do systemu znajdziemy odpowiedź  
![Screenshot from 2024-06-23 14-58-47](https://github.com/s24306/Cyberskiller/assets/91730770/ba47a18b-0210-41ea-ba5d-41f6b7a3cfb8)

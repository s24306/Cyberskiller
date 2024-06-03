> ## Na maszynie uruchomiony został serwer SMTP. Twoim zadaniem jest odnalezienie dwóch nazw użytkowników, którzy posiadają konta na serwerze. Jeden z użytkowników posiada hasło takie samo jak jego login. Wyślij wiadomość e-mail do użytkownika o prostym haśle z konta drugiego użytkownika. Po wysłaniu wiadomości odpowiedź do zadania znajdzie się w katalogu domowym użytkownika o słabym haśle. Do znalezienia nazw użytkowników wykorzystaj wordlistę znajdującą się w repozytorium CyberSkiller userlist.txt.

W ramach zadania dostajemy adres IP serwera, oraz listę użytkowników w formacie txt.  
Przeprowadźmy wpierw skan nmapem  
![Screenshot from 2024-06-03 11-57-08](https://github.com/s24306/Cyberskiller/assets/91730770/a5eee61a-f85a-4cfc-94c0-b2774aef41b8)

Znajdźmy w msfconsole auxiliary, który pomoże nam znaleźć użytkowników smtp  
![Screenshot from 2024-06-03 12-13-39](https://github.com/s24306/Cyberskiller/assets/91730770/5e6e6a83-aafd-4d31-87a2-484e1a46aaa2)

Skonfigurujmy opcje, załączmy listę użytkowników z zadania i rozpocznijmy skan  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/8a2a72bd-3f2f-4f7b-b286-2a3c395f3ff2)

Udało nam się znaleźć dwóch użytkowników: chlo i nicola.  
Spróbujmy teraz połączyć się z ssh używając tego samego loginu i hasła  
![Screenshot from 2024-06-03 11-56-53](https://github.com/s24306/Cyberskiller/assets/91730770/630d3f0c-3591-4aaa-b5fa-0fb68d35db89)

Dostaliśmy się na konto chlo, jedyne co nam pozostaje to wysłać do niej maila jako nicola  
![Screenshot from 2024-06-03 12-18-22](https://github.com/s24306/Cyberskiller/assets/91730770/d4f93d92-a68e-4047-bb3b-72e3af3fb407)

Możemy teraz na koncie chlo odczytać maila, którego dopiero co wysłaliśmy, jak i odpowiedź do zadania  
![Screenshot from 2024-06-03 12-19-36](https://github.com/s24306/Cyberskiller/assets/91730770/faae3c33-2c6e-4a7e-996d-9eec249fc7b9)

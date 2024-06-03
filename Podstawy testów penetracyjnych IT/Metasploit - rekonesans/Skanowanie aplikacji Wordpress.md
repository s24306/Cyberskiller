> ##  Na maszynie uruchomiony został blog, wykorzystujący aplikację Wordpress. Użytkownik CyberSkiller zainstalował kilka motywów do swojego bloga, niestety jeden z nich jest źle skonfigurowany. W folderze motywu został także dodany plik z możliwymi hasłami użytkownika CyberSkiller. Wykorzystaj wordlistę small-themes.txt do znalezienia błędnego motywu, a następnie znajdź hasło do konta użytkownika CyberSkiller.
 
W ramach zadania dostajemy adres IP serwera WWW.  
Z racji, iż mamy działać na theme'ach w wordpressie, znajdźmy taki właśnie moduł  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/b660a028-c13c-47bd-9071-d86fa42e6323)

Po ustawieniu zmiennych i uruchomieniu modułu nic nam nie zwrócono. Po przeczytaniu dokładniej, należy wyłączyć "exploitable".  
Pluginy też możemy wyłączyć, z racji że nas nie interesują.  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/608376ed-868f-48f8-b21a-76128a6d4bdb)

Udając się pod "http://10.34.40.127/wp-content/themes/" i sprawdzając każdy znaleziony theme po kolei znajdziemy plik z hasłami  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/345046df-e2d8-40dd-93f1-6609ed12520b)
![image](https://github.com/s24306/Cyberskiller/assets/91730770/f0f2d0bf-fd18-4d7a-bd92-3752e857e67b)

Teraz możemy użyć modułu, który pozwoli nam dostać się na konto admina  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/d66b7755-cb02-4844-93ab-c5ef77c7c805)

Po zalogowaniu się do wordpressa ujrzymy odpowiedź  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/24c13d9d-4603-4c92-8dd4-c10a37db4003)

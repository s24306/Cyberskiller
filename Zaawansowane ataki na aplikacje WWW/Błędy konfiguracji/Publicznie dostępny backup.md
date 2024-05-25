W ramach zadania dostajemy dostęp do web serwera. Wiemy, że plik secret.txt znajduje się w jednym z podkatalogów katalogu głównego serwera.  
Sprawdzamy podkatalogi za pomocą gobustera  
![Screenshot from 2024-05-25 16-41-50](https://github.com/s24306/Cyberskiller/assets/91730770/6b2bce7e-b7cb-4f97-ac9f-2c1fd6403868)

Widzimy, że znaleziony został katalog backups, ale nie możemy go przeglądać.  
Sprawdzimy jeszcze raz za pomocą gobustera katalog /backups, ale tym razem z szukaniem rozszerzeń, np. zip  
![Screenshot from 2024-05-25 16-56-26](https://github.com/s24306/Cyberskiller/assets/91730770/bf268103-8bb8-4154-9c75-1f39bbb2be81)

Odkrywamy plik backup.zip  
Po jego pobraniu znajdziemy flagę  

![image](https://github.com/s24306/Cyberskiller/assets/91730770/86e8b7d3-fbd5-45ab-8c4e-146f57beab57)

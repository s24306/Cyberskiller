> ##  W katalogu domowym użytkownika bob znajduje się paczka zip, zawierająca plik secret.txt. Twoim zadaniem jest wygenerowanie wykonywalnego payloadu za pomocą narzędzia msfvenom. Wykorzystaj w tym celu jeden z dostępnych modułów meterpreter. Po wygenerowaniu pliku uruchom nasłuchiwanie na przychodzące połączenie w programie metasploit w celu uzyskania sesji powłoki użytkownika bob. Do wysłania pliku wykorzystaj serwis webapp dostępny za pomocą protokołu http.

W ramach zadania dostajemy adres web, pod który należy się udać, gdzie przekażemy nasz payload do umieszczenia na maszynie Boba.   
![image](https://github.com/s24306/Cyberskiller/assets/91730770/94302edd-f0a1-4fdf-9a49-5dd5aec844f0)  

Z racji, iż wymagane jest od nas wykorzystanie meterpretera, wyszukmy taki właśnie payload w msfvenom  
![Screenshot from 2024-06-02 21-11-35](https://github.com/s24306/Cyberskiller/assets/91730770/cf77d10d-2967-40e1-bb03-b031d463ded7)  

W msfconsole używamy exploit/multi/handler i ustawiamy taki sam payload jak w msfvenom  
![Screenshot from 2024-06-02 21-12-17](https://github.com/s24306/Cyberskiller/assets/91730770/66c67dd2-8c8c-4545-b6e2-5e724ab1df17)  

Gdy dostaniemy się do systemu, możemy za pomocą meterpretera uzyskać dostęp do shella. Niestety użytkownik nie ma zainstalowanego unzipa, abyśmy mogli odczytać zawartość archiwum.  
![Screenshot from 2024-06-02 21-12-57](https://github.com/s24306/Cyberskiller/assets/91730770/e12d616d-6f7a-4702-b091-7180e07896ac)  

Wychodzimy więc z shella, używamy wbudowanej komendy meterpretera "download" i rozpakowujemy paczkę u siebie, dzięki czemu możemy uzyskać odpowiedź do zadania.  
![Screenshot from 2024-06-02 21-13-17](https://github.com/s24306/Cyberskiller/assets/91730770/8b22a325-b0ae-408b-b7f8-7d422483b7e4)  

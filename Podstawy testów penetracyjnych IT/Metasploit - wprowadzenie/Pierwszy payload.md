> ## W katalogu domowym użytkownika bob znajduje się plik secret.txt, zawierający odpowiedź do zadania. Twoim zadaniem jest wygenerowanie wykonywalnego payloadu za pomocą narzędzia msfvenom. Wykorzystaj w tym celu moduł payload/linux/x64/shell_reverse_tcp. Po wygenerowaniu pliku uruchom nasłuchiwanie na przychodzące połączenie w programie metasploit w celu uzyskania sesji powłoki użytkownika bob. Plik wgraj za pomocą uruchomionej aplikacji web dostępnej za pomocą protokołu http.
> 
W ramach zadania dostajemy adres web, pod który należy się udać, gdzie przekażemy nasz payload do umieszczenia na maszynie Boba.  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/83062fb3-a532-43e3-84b7-979cb4069ac1)

Tworzymy payload za pomocą msfvenom   
![Screenshot from 2024-06-02 19-15-48](https://github.com/s24306/Cyberskiller/assets/91730770/fe3a13ec-69f9-49c2-9de4-839f1f0f0526)  


Uruchamiamy msfconsole, wybieramy exploit/multi/handler i uruchamiamy go. Po zuploadowaniu payloadu otrzymamy połączenie  
![Untitled](https://github.com/s24306/Cyberskiller/assets/91730770/a9e1af3f-4a6e-4817-b0e3-97a652502869)

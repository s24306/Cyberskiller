> ## Zaloguj się do serwera za pomocą SSH. Odpowiedź do zadania znajduje się w szyfrowanym ruchu sieciowym, który masz możliwość podsłuchać, w czym może pomóc uruchomiona aplikacja WWW.

W ramach zadania otrzymujemy adres IP i dane logowania.  
Po zalogowaniu się na serwer możemy przechwycić odbywającą się komunikację za pomocą tcpdump  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/cefc5570-99bd-4dff-8dea-cad5de1ca0e0)

Warto odnotować na przyszłość, że mamy uprawnienia sudo  
Pobierzmy plik na naszą maszynę  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/7c2205cc-c88d-4256-9c47-e6dc55b1f579)  

Po otworzeniu pcapa zauważymy, że cały ruch jest szyfrowany  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/dc04890a-68c1-4d49-9d0c-4899c0dbc5b4)  

Będziemy potrzebować klucza prywatnego, aby go odszyfrować, jednakże w samym pcapie go nie znajdziemy.  
Wróćmy do zdalnej maszyny i sprawdźmy jakie procesy na niej działają  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/9ab681db-a6de-4568-a2db-7b38829ed915)  

Możemy zauważyć, iż klucz prywatny jest w folderze roota i ma nazwę key.pem  
Wiemy z wcześniej, że mamy uprawnienia sudo do tcpdump.  
Możemy wykorzystać exploit z [gtfobins](https://gtfobins.github.io/), aby odczytać jego zawartość  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/25a75fc8-9fae-406b-afb1-f415bc030a66)  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/674d11dd-aa8c-49b4-9d94-d50499885d44)  

Zapiszmy odczytany klucz do pliku i użyjmy go do odszyfrowania TLS w wiresharku, dodając go do kluczy RSA   
![image](https://github.com/s24306/Cyberskiller/assets/91730770/e46b3f68-93eb-4dfb-8056-a7917dda0ae8)  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/7193ecd1-a4e0-43e8-a9f5-9b5b7d5547ab)  

Zobaczymy, że odszyfrował nam się ruch HTTP, odczytajmy go więc za pomocą Follow -> HTTP Stream  
![Screenshot from 2024-06-30 14-20-09](https://github.com/s24306/Cyberskiller/assets/91730770/c9e03096-073b-4868-827d-319c3229c62a)  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/37829138-40da-40ac-aba0-55ee1c6b04c2)

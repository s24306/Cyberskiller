> ##  Posiadasz dostęp do serwera obsługującego prostą stronę WWW. Aplikacja posiada funkcjonalność wgrywania plików zdefiniowanych przez użytkownika. Wiedząc, że odpowiedź zadania znajduje się w pliku secret.txt w katalogu uploads, wgraj odpowiedni plik, który umożliwi dostęp do zawartości tego pliku.

W ramach zadania otrzymujemy adres IP aplikacji internetowej  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/49618fbc-cce2-4c75-9846-bbee426ae687)  

Spreparujmy odpowiedni plik, w którym umieścimy prostą komendę w php i zuploadujmy go  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/56213ee8-d7ee-4af6-8b7f-445254513900)

Teraz, gdy przejdziemy do /uploads/a.php, naszym oczom ukaże się taki błąd  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/ac472f3d-317f-4bb3-a639-ef4dc0b36d46)  

Oznacza to nie tylko, że udało nam się wgrać plik, ale i również to, że działa  
Przekażmy komendę do cmd `/uploads/a.php?cmd=ls`  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/d3eb54a0-e9e3-4b0c-905f-b63da2634b99)  

Odczytajmy odpowiedź do zadania  
`/uploads/a.php?cmd=cat secret.txt`  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/e97f9ed7-db2b-4220-868a-07af20dcf76d)

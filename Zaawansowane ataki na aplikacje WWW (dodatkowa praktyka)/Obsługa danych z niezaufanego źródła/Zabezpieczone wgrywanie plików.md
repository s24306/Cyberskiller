> ## Posiadasz dostęp do web serwera obsługującego prostą stronę HTTP. Aplikacja posiada funkcjonalność wgrywania plików zdefiniowanych przez użytkownika. Wiedząc, że aplikacja posiada zabezpieczenie przed wgrywaniem plików php oraz że plik z odpowiedzią do zadania znajduje się w katalogu uploads i posiada on losową nazwę, wgraj odpowiedni plik, który umożliwi odczytanie odpowiedzi do zadania.  

W ramach zadania dostajemy adres IP aplikacji webowej, pozwalajcej na uploadowanie plików.  
![Screenshot_2024-06-25_07-27-59](https://github.com/s24306/Cyberskiller/assets/91730770/ac629eaf-6842-4f62-94e3-050ee7b8af89)  

Aby wyświetlić zawartość folderu uploads, przygotujemy plik php  
![Screenshot_2024-06-25_07-33-46](https://github.com/s24306/Cyberskiller/assets/91730770/72ab8eaa-a49c-4626-8975-48d42b91f702)  

Przy uploadzie pliku php, dostaniemy informację zwrotną, że nasz plik ma zły typ i nie zostanie wrzucony  
![Screenshot_2024-06-25_07-28-44](https://github.com/s24306/Cyberskiller/assets/91730770/fadc6e1b-4990-4cef-8507-fe1268344532)

Możemy to ominąć w bardzo prosty sposób, używając w przeglądarkowej zakładce "Network" opcji "Edit and Resend", gdzie zmienimy Content-Type na taki, który nie jest blokowany, jak np. text/plain  
![Screenshot_2024-06-25_07-29-35](https://github.com/s24306/Cyberskiller/assets/91730770/78f55812-dbbb-4815-a39b-d56985b90134)  

Po przejściu do uploads/[nazwa_pliku].php nic nam się jednak nie ukaże. Prawdopodobnie w pliku .htaccess jest wyłączone wykonywanie php.  
Możemy temu z łatwością zaradzić poprzez zuploadowanie pustego pliku .htaccess, który zastąpi obecny na serwerze.  
Po zuploadowaniu i ponownym wywołaniu naszego pliku php, ukaże nam się zawartość folderu  
![Screenshot_2024-06-25_07-27-44](https://github.com/s24306/Cyberskiller/assets/91730770/e4f62330-5f82-4ebd-9cd4-e5e579dba45a)  

Po przeklejeniu nazwy pliku, którego nazwa ta jest losowa, otrzymamy odpowiedź do zadania  
![Screenshot_2024-06-25_07-27-20](https://github.com/s24306/Cyberskiller/assets/91730770/86d327dd-bdae-48a0-b137-99a3d8dd9cb0)  

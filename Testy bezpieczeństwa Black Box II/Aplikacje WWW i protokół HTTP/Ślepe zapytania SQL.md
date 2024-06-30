> ##  Posiadasz dostęp do serwera obsługującego prostą stronę HTTP. Aplikacja posiada zaimplementowany mechanizm wyszukiwarki. Wykorzystując podatność wstrzyknięć SQL typu Blind, wydobądź z bazy danych hasło użytkownika CS. Podpowiedź: Nazwa tabeli użytkowników to accounts. Nazwy kolumn w tabeli accounts to id, account_username, account_password. Hasło użytkownika stanowi odpowiedź do zadania i ma standardowy format, czyli rozpoczyna się od wielkiej litery C, po której jest druga wielka litera i 10 cyfr.

W ramach zadania otrzymujemy adres IP, pod którym znajduje się podatna wyszukiwarka  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/02544166-6a05-47dd-932b-907e41318fea)  

Użyjmy specjalne spreparowanego zapytania. Wiemy, że pierwsze znaki hasła dla użytkownika CS to "CS", po których następuje 10 cyfr.  
Zacznijmy je enumerować, zaczynając od 0.  
`a" union select account_username from accounts where account_username = 'CS' and account_password like '%CS0%'; -- a`  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/1addc9a2-1673-4a41-9637-0a910c5c91b9)  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/7c668b95-077a-48d5-9041-94e9318bd6a7)  

Jak widzimy, w bazie danych nie ma hasła, które zaczyna się od "CS", po którym następuje 0.  
Sprawdźmy inne kombinacje  
Przy "CS2" dostajemy informację zwrotną, iż hasło z takim ciągiem znaków istnieje, dla takiego użytkownika. 
![image](https://github.com/s24306/Cyberskiller/assets/91730770/bfe9c520-b355-4e2d-aa37-a3cb2ea9d2d0)

Na tym etapie nie pozostaje nam nic innego, jak:  
a) Wstukiwać po jednej cyfrze i sprawdzać czy trafiliśmy
b) zautomatyzować proces np. za pomocą pythona  
Gdy uzyskamy CS i ciąg 10 cyfr, które istnieje w systemie - to odpowiedź do zadania

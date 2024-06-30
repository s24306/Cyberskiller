> ## Na serwerze działa szyfrowany serwer IMAP. Odpowiedź znajduje się w skrzynce odbiorczej użytkownika alice.

W ramach zadania dostajemy adres IP oraz dane do logowania.  
Z racji, że mamy się połączyć z szyfrowanym imapem, użyjemy openssl  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/8290e344-8071-4d2b-968d-2c8c31d24b1f)  

Aby dowiedzieć się, jak się poruszać po imapie, przeczytajmy przykładowy dialog na [wikipedii](https://en.wikipedia.org/wiki/Internet_Message_Access_Protocol#Dialog_example).  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/24e50cc9-cb54-41f8-b35c-b4e61ac5da31)  

Tagi [A001, A002, etc.] służą tylko serwerowi, żeby wiedział na co odpowiada, można ciągle używać tego samego i nic złego się nie stanie  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/35cc5d3b-4625-4ebe-8c0b-216767700e25)  

Wiadomość otrzymaliśmy zakodowaną base64, więc ją odkodujmy  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/a56f38ad-d2f3-44f8-84c7-2e3c292ee9cc)

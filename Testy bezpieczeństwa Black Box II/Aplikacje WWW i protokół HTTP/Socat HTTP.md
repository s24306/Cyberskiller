> ##  Zaloguj się do systemu za pomocą SSH. Działa tam lokalny demon HTTP. Za pomocą narzędzia socat odpytaj ten demon o odpowiedź HTTP, a znajdziesz w niej odpowiedź do zadania. Być może do uzyskania odpowiedzi będzie należało użyć innej metody...

W ramach zadania dostajemy adres IP i dane do logowania.  
Po zalogowaniu się na serwer, użyjmu socata do połaczenia się z daemonem.  
Aby uzyskać odpowiedź musimy wysłać zapytanie GET  
`GET / HTTP/1.1`  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/27038bdd-22eb-4209-bc75-0880a6ac974d)

> ## Na serwerze znajdziesz tajną wiadomość ukrytą w pliku, który jest obrazkiem. Przejdź po tym pliku i odczytaj wiadomość.

W ramach zadania otrzymujemy adres serwera oraz dane logowania  
Po zalogowaniu się znajdziemy plik.  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/9c4f76e1-a5df-490c-9a0c-7412946bd56e)  

Pobierzmy go na naszą maszynę za pomocą scp  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/42b26efe-10b5-4c79-94ef-c789b1211888)  

Jeśli podejrzymy plik, zobaczymy kod - niestety nie jest to odpowiedź, a podpucha  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/b0efbf17-5446-4ba9-9d2c-8d1d5e563d5f)  

file, exiftool i hexdump nic nam nie dały  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/44e7d7fc-2392-4918-b294-aea9979dbc0e)  

Jeśli spróbujemy binwalka, to ukaże nam się archiwum gzip.  
Wypakujmy wszystko z naszego pliku  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/497b43b6-7798-453f-893a-0c570762f9d5)  

W folderze z wyekstraktowanymi danymi widzimy archiwum 140.gz. Rozpakujmy je  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/1980f3ca-f172-4583-aa31-4abaff2bc51d)  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/c72fa1d0-8778-44bf-8a44-cd21169bc444)  

Gdy sprawdzimy wypakowany plik, okaże się, iż jest to plik tekstowy.  
Przeczytajmy go więc  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/5fef1b6c-0a71-44dd-ab48-06f5314490ee)

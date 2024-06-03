> ##  Na maszynie uruchomiony został serwis WWW. Twoim zadaniem jest znalezienie ukrytego folderu, który zawiera odpowiedź do zadania. Wykorzystaj framework metasploit oraz wordlistę, znajdującą się w repozytorium CyberSkiller directory-list-2.3-medium.txt. W ramach zadania dostajemy adres IP serwera, oraz listę użytkowników w formacie txt.  

Przeprowadźmy wpierw skan nmapem  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/0ba5b6d5-dc9f-4d6b-ad0c-8fa094718340)

Znajdźmy w msfconsole auxiliary, który pomoże nam listować katalogi  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/433db3b0-f397-4a84-960f-f4419d1aef7c)

Jak widzimy, trochę tego jest, więc postarajmy się bardziej zawęzić nasze poszukiwania  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/b4849ebf-638e-4d57-961b-ad1b1a055d48)

Skonfigurujmy opcje, załączmy listę katalogów z zadania i rozpocznijmy skan  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/1fdbb936-b9a3-4614-a334-d8965fe7e902)

Możemy po kolei zacząć sprawdzać linki.  
Pod /web znajdziemy jeden plik tekstowy, który niestety nie zawiera w sobie nic ciekawego  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/d1ce7b23-c361-4acd-b079-cd1e990ab853)

W /pics znajdziemy plik TODO.txt, w którym mamy informację o nietypowej nazwie katalogu  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/a97397fb-0e53-44d9-82ed-48356dc9bfe2)

Gdy przejdziemy do niego z poziomu paska adresu, ukaże nam się secret.txt  
![image](https://github.com/s24306/Cyberskiller/assets/91730770/f5872b98-d3f5-48ae-86c8-a03ab9328c9e)

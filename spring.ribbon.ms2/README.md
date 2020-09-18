# spring.ribbon.ms2
loadbalancing avec Ribbon sans eureka.  

ms2 + Ribbon
--- ms2 instance 1 ( port 8200 )
--- ms2 instance 2 ( port 8201 )
				  
http://localhost:8080/getmicro2


Notice : 
- Démarrer 2 instances du serveur spring.ribbon.ms2  en changeant le port, l'un 8200 et l'autre 8201. 
- Démarrer spring.ribbon.ms.loadbalancing
- Accèder l'URL http://localhost:8080/getmicro2, l'algorithme par défautl de loadbalancing tapera tantot une instance puis l'autre.
La page HTML affichera "Currently hitting instance running on port: 8200" ou "Currently hitting instance running on port: 8201"

Référence:
https://www.studytonight.com/post/load-balancing-spring-boot-microservices-using-netflixs-ribbon 
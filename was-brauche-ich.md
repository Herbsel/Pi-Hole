Kurz: Das weiß ich auch nicht :-D Aber so kurz möchte ich es nicht halten. Zuallererst, ein PiHole ist in erster Linie dazu gedacht Werbung auszufiltern und eventuel etwas Tracking und Seiten die Ransomware verbreiten.

Sprich, ein PiHole Filtert DNS Anfragen. Was ein PiHole nicht kann, ist weiterverzweigte Aufrufe verweigern die mit DNS nichts zu tun haben. Mails filtern, Netzwerkverkehr überwachen, Videos auf Schadcode untersuchen. Wenn du nicht weißt was ein DNS Server ist und DNS Anfragen sind, solltest du dich zuallerst [darin einlesen](https://www.elektronik-kompendium.de/sites/net/0901141.htm)

Nun weiß hoffentlich jeder was ein DNS Server ist und macht. Die Quellen zu PiHole Listen betragen alleine bei Github zum Zeitpunkt des Schreibens ca. 352 Repositorys mit jeweils teilweise dutzenden Listen. Dazu noch die anderweitig im Netz Auftauchenden.

Noch einmal, DNS blockt keinen Verkehr, er ist ausschließlich für DNS zuständig! Um Traffic, Netzwerkstream, Ports usw. zu kontrollieren, braucht es eine Firewall wie die ONSense! Dort könnt ihr per GeoIP Blocking ein- und ausgehenden Verkehr blocken und mit Listen wie der Firehol Level1 List auch einkommenden Traffic blocken.

![Titel](https://user-images.githubusercontent.com/53258295/116553216-30443980-a8fa-11eb-9588-e51621fd3d89.png)

**Wir bauen uns unser eigenes Filternet

Bigdata, Überwachung (Tracking), jede smarte Glühbirne sendet mittlerweile nach Hause. Zudem alle Smartphones und deren Apps. Täglich gibt es hunderte, wenn nicht tausende neue Seiten mit Ransomware, Schadware die euch Cryptominer unterjubeln wollen. Immer mehr Botnetze wie Emotet und Co. Wir sind schon lange nicht mehr in der Lage manuell zu arbeiten und dem Verstand alles zu überlassen. Vieles arbeitet im verborgenen ohne dass wir es am PC, Laptop oder Smartphone mitbekommen.

PiHole das schwarze Loch für Werbung, so der Slogan des PiHole. Zeitweise gab es in Blogs, bei Youtuber und im Netz einen wahren Hype um dieses System. Die Vorgehensweise dabei ist schlicht einfach wie simpel.

PiHole arbeitet als DNS Resolver, d.H. ihr geb auf der OPNSene den PiHole als DNS Server an und verteilt diesen per DHCP und zukünftig fragt ihr diesen an, statt dem bösen 8.8.8.8 von Google. (Am besten auf der OPNSense den kompletten Port 53 Verkehr auf den PiHole lenken)

Einen Schritt weiter geht es, wenn noch der Unbound konfiguriert wird. Damit arbeitet PiHole als Recursiver DNS Server. D.h. den Zwischenschritt, wenn eine IP unbekannt ist und standardmäsßig ein DNS Server des ISPs, Google, Cloudflare etc. gefragt wird fällt weg und der PiHole fragt selber deim DNS Rootserver an.

Zum Filtern werden [Listen](https://github.com/topics/pihole-blocklists) hinterlegt (von github oder whatelse) in denen IPs bzw. Domains hinterlegt sind. Zum Beispiel hinterlegst du fakeshop24.de im PiHole. Rufst du nun mit deinem Smartphone fakeshop24.de auf, wird die DNS Anfrage an PiHole geschickt und dieser sieht, dass es einen Match mit der Blacklist gibt. Genau da greift der Filter und PiHole antwortet mit 0.0.0.0 quasi dem Äquivalent von /dev/null bei Linux.

Das Ganze hat gleich mehrere Vorteile. Die Anfragen werden schon vor dem Verlassen des eigenen Netzes gefiltert, kommen also schon gar nicht nach draußen. Das spart Traffic. Dadurch bekommen diverse Werbeanbieter schon gar nicht in den Genuss deiner Daten. Das gleiche gilt für DNS Anbieter wie 8.8.8.8 (Google), da ihr Diese gar nicht mehr anfragt, sondern ihr direkt den Rootserver fragt. Dadurch kann euer Internet Service Provider, oder DNS Server wie der von Google kein Profil von euch erstellen.

1. Traffic gespart da Anfragen direkt in Nirvana geleitet werden
2. ISP / Google / DNS-Server Anbieter können kein Profil von euch erstellen
3. DNS Sperren wie der der Clearingstelle Urheberrecht im Internet (CUII) greifen nicht
4. Werbung diverser Smartphoneapps wird kostenlos (ohne diesen ganzen 3,99€ Pro-Versionen. Wobei "Pro" dann ohne Werbung heißt. Ein Thema für sich) herausgefiltert

Natürlich ist dies ein zweischneidiges Schwert und die andere Seite der Medallie ist die, dass viele Dienste ihr Geld mit Werbung verdienen. Ich persönlich habe auch nichts gegen Werbung an sich, aber wenn eine Internetseite zu 50% aus Werbung besteht, wird es mir zu viel.

Ich sehe den Sinn und Zweck von Werbung, aber diese hat einfach einen unaushaltbaren Zustand an Masse gewonnen. Zudem gibt es diverse Trackingdienste und -Anbieter die versuchen aus einem Nutzer einen gläsernen Menschen zu machen. Wenn hier die Politik nicht reagiert, muss man sich selbst um seine Datenautonomie kümmern.

Diese Firmen argumentieren gerne mit personalisierte Werbung. Doch mal Hand aufs Herz (jedem Leser, diese Unternehmen machen es ohnehin nicht) vor dem Internet gab es Werbung im TV, Radio, Zeitung und evtl. Post die ebenso unpersonalisiert war. Nur weil es jetzt die digitalen Mittel dafür gibt, heißt das nicht, dass ich dem automatisch zustimme. Und wenn jemand mit meinen Daten Geld verdient, möchte ich gefälligst von diesem Kuchen etwas ab haben. Und ich rede hier von Geld, nicht von virtuellen Cookies.

Mal in blanken Zahlen. ich filtere momentan 9.643.127!! unique Domains / IPs mit 144 (funktionierenden) Listen, davon sind alleine 5.700.000!! Einträge pornografische Inhalte. Das bedeutet, doppelte Einträge sind durch den PiHole schon kummuliert. Bei dieser schieren Masse könnte man verzweifeln. Und mein gefiltertes Netz funktioniert nahelos Problemlos. Jetzt stell dir vor, wie gläsernen du tatsächlich für die verschiedensten Anbieter und Dienste bist.

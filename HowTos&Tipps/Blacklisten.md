# blacklists

Ich persönlich filtere lieber zu viel als zu wenig und korrigere false positives per Whitelist aus. Ausnahmsweise finde ich Duplikate in verschiedensten Listen auch eher positiv. Die Listen werden ohnehin kommuliert und jeder Eintrag bleibt am Ende nur einmal in der Datenbank. Geht eine Liste allerdings offline und das kommt sehr häufig vor, dann wird diese Domain dennoch weiterhin aufgenommen. Jeder kann sich natürlich auch ein Monitoring einrichten und die offline Gegangenen sofort ersetzen. Jedoch habe ich in meiner Freizeit besseres zu tun als adhoc auf solche Vorkommnisse zu reagieren.

Hier folgt eine auserwählte Liste an Blacklists die ich sehr empfehlen kann.

**SemperVideo**

Wer SemperVideo bei Youtube noch nicht kennt, hat etwas verpasst. Er / Sie hat / haben eine Liste auf die Beine gestellt, die es in sich haben.

[PiHole Listen von SemperVideo](https://github.com/RPiList/specials)

Deren eignen (teilw. kommulierte) Listen in Gruppen findet ihr dort
[SemperVideos own Lists](https://github.com/RPiList/specials/tree/master/Blocklisten)

Grundsätzlich könnte ich an dieser Stelle schon aufhören, da sie ihren Job wirklich genial machen. Dazu für den deutschsprachigen Raum. Schau dir auch die Regex Sachen an, die du manuell hinterlegen musst. Gerade für Punycode Adressen am Smartphone sehr sinnvoll!

In der
specials/Blocklisten/readme.md ist eine Auflistung welche Liste was blockt.

**Botnetze**
[Botnetzliste](https://feodotracker.abuse.ch/downloads/ipblocklist_recommended.txt)

**NSA Blocklist inkl. gov Domains** (am besten in der Firewall auch eingehend blocken. Schützt natürlich nicht 100%ig)
[NSA Blocklist](https://raw.githubusercontent.com/Cauchon/NSABlocklist-pi-hole-edition/master/HOSTS%20(including%20excessive%20GOV%20URLs)

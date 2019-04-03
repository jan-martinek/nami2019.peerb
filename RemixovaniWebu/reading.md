Přebírání dat dostupných na webu třetími stranami je významnou součástí fungování webu. Příkladem mohou být vyhledávače jako je [Google](http://google.com) či [Seznam](http://seznam.cz) nebo vkládání obsahu ze sociálních sítí a videoserverů.

Obsah je možné skládat do jednoho celku různými způsoby. Profesionální řešení, které musí spolehlivě fungovat (jako prodejní či informační služba), bude nejspíše pracovat přímo na serveru a bude využívat především strojově čitelných zdrojů dat. My si vyzkoušíme skládání zdrojů přímo ve webovém prohlížeči: pomocí prvku iframe, skriptů či specifických HTML prvků.

Přečtěte si článek [Hacking, Mashing, Gluing: Understanding Opportunistic Design](http://webremix.org/readings/hackingmashinggluing.pdf), který vysvětluje některé motivace za „lepením“ webů dohromady. Autoři používají technický slovník: některé kapitoly můžete přeskočit. Nejpřístupnější a snad i nejzajímavější jsou závěrečné kapitolky na posledních třech stranách — od mezititulku *„Mashing as a design activity“* (s. 52).

Na webu se běžně setkáte s předgenerovanými elementy `embed`, `iframe`, `script` nebo složitějším kódem (často kvůli tomu, aby lépe fungoval v různých prohlížečích). Obsah ke vkládání najdete například na [Twitteru](http://twitter.com) (tweety), [Youtube](http://youtube.com) (videa), [Facebook](http://facebook.com) (statusy, odznaky, like tlačítka aj.), [Disqus](http://disqus.com) (modul pro vkládání komentářů ke článkům), [Flickr](http://.com) (fotky, fotoalba), [Soundcloud](http://soundcloud.com) a [Spotify](http://spotify.com) (playlisty, skladby), [Google Calendar](http://calendar.google.com) (kalendáře), [Slideshare](http://slideshare.com) (prezentační slajdy) a další. 

> **Tip:** Rozdíl mezi `embed` a `iframe` je poměrně hezky popsaný na [Stack
Overflow](http://stackoverflow.com/questions/16660559/difference-between-iframe-embed-and-object-elements/21115112#21115112).  

> S iframe se dnes potkáte spíše méně často (kvůli zásadním problémům s
vyhledávači a díky rozšíření skriptování na straně serveru). Prvek se využívá
při přidávání funkcionality z externího zdroje (například [lajkovací tlačítka
Facebooku](https://developers.facebook.com/docs/plugins/like-button), diskusní
pluginy jako je [Disqus](https://disqus.com) apod.).
### Šablonování v Hugo

Šablony znáte z kancelářských aplikací: několika kliky můžete změnit podobu
celého dokumentu (ať už článku napsaného ve Wordu nebo slajdy v Powerpointu).
Krom toho, že si můžete vybrat připravenou šablonu, můžete si je též vytvořit
— tímto směrem se vydáme s Hugo. Uplatníme při tom naše předchozí znalosti
CSS a HTML.


#### Šablony

V námi používaném základu pro Hugo je několik souborů, které **určují, jak bude
vypadat výsledný web**:
  
- soubor `static/css/style.css` obsahuje CSS styly

- složka `layouts/` obsahuje HTML šablony, z nichž se web skládá
  - `_default/baseof.html` obsahuje **obecnou HTML šablonu**, kterou sdílejí všechny stránky na webu a vkládají se do ní všechny ostatní šablony
  - `_default/list.html` je šablonou pro seznamy článků — jde například o archiv článků
  - `_default/single.html` a `post/single.html` obsahují **HTML šablony pro stránky příspěvků** — obecná stránka jako je /about, resp. datovaný příspěvek ve složce /post — (všimněte si shody názvů složek)
  - `index.html` je šablonou pro obsah domovské stránky
  
Je důležité si na toto dělení zvyknout – přednastavené umístění konkrétních souborů nám [může usnadnit práci](https://en.wikipedia.org/wiki/Convention_over_configuration). Proklikejte si stránky a seznamte se s tím, jak jednotlivé soubory vypadají.

Povšimněte si především těchto věcí:

- **šablonovacích značek**, které obsahují příkazy a proměnné (`{{ … }}`)

- **značky `{{ .Content }}`** ve všech šablonách krom té základní – zde Hugo vloží HTML
pro konkrétní typ stránky, které vygeneruje z Markdownu (tedy např. `about.md`).

Šablony se automaticky skládají dohromady — algoritmus trochu složitější, ale to podstatné je napsáno výše — existují základní šablony ve složce `_default` a pak konkrétní, které se hledají dle typu stránky (domovská stránka: index, archiv: list, příspěvek: single) a složky, kam patří — takže příspěvek ve složce `content/post` se vygeneruje pomocí šablony `layouts/post/single.html`.


#### Parametry webu a stránek

V šablonách můžete krom obsahu stránky pracovat s proměnnými, které jsou definovány v souboru `config.yaml` anebo v záhlaví konkrétní stránky (v souboru `*.md`). Ty jsou k nalezení v proměnných `.Site.Params` a `.Params`. Ve stránce tedy může být napsáno např.:

    ---
    title: My First Post
    date: 2017-02-20T15:26:23-06:00
    author: Josef Novák
    ---

Pro vypsání autora pak stačí do šablony vložit například:

    <p>Autor článku: {{ .Params.author }}</p>

Pro detaily a seznam automaticky dostupných proměnných se mrkněte [do dokumentace](https://gohugo.io/variables/).

Šablony umožňují mnoho dalšího — například podmíněné konstrukce a jiné příkazy. **Pro naše základní potřeby by však měl stačit tento úvod.**

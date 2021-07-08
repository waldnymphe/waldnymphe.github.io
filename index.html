<!DOCTYPE html>
<html lang="de">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="bulma/css/bulma.min.css">
    <script>
        const whTooltips = {
            colorLinks: true,
            iconizeLinks: true,
            renameLinks: true
        };
    </script>
    <script src="https://wow.zamimg.com/widgets/power.js"></script>
    <title>Berufeliste</title>
</head>

<body>
    <h1 id="server" class="title"></h1>
    <section id="guild" class="section p-3">
    </section>
</body>

</html>

<script>
    loadURL("waldnymphe_alchemy.json", onDataLoaded);

    function createProfessionList(profession, playerID) {
        let categories = sortCategories(profession.recipes);
        let container = document.createElement("div");

        categories.forEach((element, key, map) => {
            let category = document.createElement("div")
            category.classList.add("category", "section", "pl-2");

            title = document.createElement("h3");
            title.classList.add("title", "is-5");
            title.innerHTML = key;

            category.appendChild(title);


            element.forEach((element, key, map) => {
                //create recipe
                console.log(element);

                let recipe = createElement("div", "");
                recipe.classList.add("recipe", "card", "pb-5");

                let title = createElement("p", "", createWowHeadLink(element.name, element.id)); //todo: link zu wowohead
                //https://tbc.wowhead.com/item=22866

                title.classList.add("card-header-title");

                recipe.appendChild(title);

                let zutaten = createElement("ul", "");
                zutaten.classList.add("pl-5");

                element.items.forEach((item) => {
                    let li = createElement("li", "", item.num + " " + createWowHeadLink(item.name, item.id));
                    zutaten.appendChild(li);
                });

                recipe.appendChild(zutaten);

                category.appendChild(recipe);
            });

            container.appendChild(category);
        });

        document.getElementById(playerID).appendChild(container);
    }

    function createWoWHeadTooltip(name, id) {
        let link = "https://de.tbc.wowhead.com/item=" + id;
        return "<a href='" + link + "' data-wowhead= 'item=" + id + "' class='q3'>" + name + "</a>";
    }

    function createWowHeadLink(name, id) {
        let link = "https://de.tbc.wowhead.com/item=" + id;
        return "<a href='" + link + "' target='_blank'>" + name + "</a>";
    }

    function createElement(type, id, innerHTML = "") {
        let ele = document.createElement(type);
        ele.id = id;
        ele.innerHTML = innerHTML;
        return ele;
    }

    function sortCategories(recipes) {
        let categories = new Map();

        recipes.forEach(element => {
            if (!categories.get(element.categorie)) {
                categories.set(element.categorie, new Map());
            }

            let item = {
                name: element.name,
                id: element.id,
                num: element.num,
                categorie: element.categorie,
                spellId: element.spellId,
                items: element.items
            }
            categories.get(element.categorie).set(item.name, item);
        });
        return categories;
    }

    function createPlayer(playerName, guildName, profession) {
        let guild = document.getElementById("guild");

        let guildTitle = document.createElement("h1");
        guildTitle.classList.add("title", "is-4");
        guildTitle.innerHTML = guildName;

        let playerEle = document.createElement("section");
        playerEle.id = playerName;
        playerEle.classList.add("section", "p-3");

        let playerTitle = document.createElement("h1");
        playerTitle.classList.add("title", "is-5");
        playerTitle.innerHTML = playerName;

        let playSubtitle = document.createElement("h2");
        playSubtitle.classList.add("subtitle");
        playSubtitle.innerHTML = profession.name + ", " +
            profession.specializationName +
            ", " +
            profession.level;

        playerEle.appendChild(playerTitle);
        playerEle.appendChild(playSubtitle);

        guild.appendChild(guildTitle);
        guild.appendChild(playerEle);

        createProfessionList(profession, playerName);
        //document.getElementById("player").innerHTML = player + " (" + guild + ")";
    }

    function onDataLoaded(data) {
        data = JSON.parse(data);
        var server = data.server;
        var player = data.player;
        var guild = data.guild;
        var profession = data.profession;

        document.getElementById("server").innerHTML = server;
        createPlayer(player, guild, profession);
    }

    function loadURL(url, callBack) {
        var xhr = new XMLHttpRequest();
        xhr.open("GET", url, true);
        xhr.setRequestHeader("Accept", "application/json");
        xhr.onloadend = onLoadEnd(xhr, callBack);
        xhr.send();
    }

    function onLoadEnd(request, callBack) {
        return function() {
            var status = request.status;
            var result = String(request.response);
            if (status >= 200 && status < 300) callBack(result);
        };
    }
</script>

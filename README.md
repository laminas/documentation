# Documentation

> ## 🇷🇺 Русским гражданам
> 
> Мы, участники Laminas, родились и живем в разных странах. У многих из нас есть друзья, родственники и коллеги как в России, так и в Украине. Некоторые из нас родились в России. Некоторые из нас живут в России. У некоторых бабушки и дедушки сражались с фашистами во Второй мировой войне. Здесь никто не поддерживает фашизм.
> 
> У одного из нас есть украинская родственница, которая спаслась из дома вместе с сыном. Поезд задержался из-за бомбежки на дороге впереди. У нас есть друзья, которые прячутся в бомбоубежищах. Мы с тревогой ждем весточки от них после воздушных налетов, которые беспорядочно наносят удары и попадают по больницам, школам, детским садам и домам. Мы не берем это из каких-либо СМИ. Мы наблюдаем это напрямую.
> 
> Вы доверяете нам достаточно, чтоб использовать наши программы, и мы просим вас довериться нам вновь. Мы нуждаемся в помощи. Выходите и протестуйте против этой бесполезной войны. Остановите кровопролитие. Скажите "Нет войне!"
> 
> ## 🇺🇸 To Citizens of Russia
> 
> We at Laminas come from all over the world. Many of us have friends, family and colleagues in both Russia and Ukraine. Some of us were born in Russia. Some of us currently live in Russia. Some have grandparents who fought Nazis in World War II. Nobody here supports fascism.
> 
> One team member has a Ukrainian relative who fled her home with her son. The train was delayed due to bombing on the road ahead. We have friends who are hiding in bomb shelters. We anxiously follow up on them after the air raids, which indiscriminately fire at hospitals, schools, kindergartens and houses. We're not taking this from any media. These are our actual experiences.
> 
> You trust us enough to use our software. We ask that you trust us to say the truth on this. We need your help. Go out and protest this unnecessary war. Stop the bloodshed. Say "stop the war!"

This repository exists for the purpose of planning and organizing documentation 
changes and milestones for the Laminas Project and related subproject, and to show how to setup and update the documentation locally.

## Setup

To prepare your local development environment to build the documentation locally, follow the steps below:

1. [Install MkDocs](https://www.mkdocs.org/#installation) and all of its dependencies (The installation description for MkDocs also includes the installation of Python.)
2. Install the [Python PyMdown Extensions](https://facelessuser.github.io/pymdown-extensions/installation/#installation_1)

## Building the Documentation Locally

To build the documentation locally, follow the steps below:

1. Clone `laminas/documentation-theme` inside your development branch, by running: `git clone git://github.com/laminas/documentation-theme.git`
2. Build the documentation by running: `./documentation-theme/build.sh -u https://docs.laminas.dev/<your project>/`, swapping `<your project>` for the path of the package you’re working on, e.g., `https://docs.laminas.dev/laminas-hydrator`.

### Viewing Generated Documentation

To view the generated documentation, after building it, open `docs/html/index.html`.
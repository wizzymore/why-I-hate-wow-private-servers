# Почему я ненавижу большинство частных серверов WoW.

*Автор [Francesco Borzi'](https://github.com/FrancescoBorzi) ака Shin*

Почему на пиратских серверах WoW до сих пор так много багов, хотя они существуют уже много лет?

![Wow-facepalm](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-facepalm.jpeg)

Не стоит волноваться, это не очередная лекция об авторских правах на Blizzard.
Я просто хочу объяснить, почему я ненавижу большинство пиратских серверов [World of Warcraft](https://ru.wikipedia.org/wiki/World_of_Warcraft).

## Введение

Я увлекаюсь эмуляцией WoW с 14 лет. 
Помню, что в первый раз, когда я присоединился к одному из этих "особых миров", было много багов, но ты по крайней мере играл бесплатно. 
Знаете, в то время у меня не было ни цента, так что у меня не было альтернативы.

В 15 лет я начал задаваться вопросом, как на самом деле работают и могут существовать пиратские серверы, особенно с технической точки зрения. 
Может быть, кто-то украл код у [Blizzard](https://ru.wikipedia.org/wiki/Blizzard_Entertainment)? 
Не знаю, в то время я был еще молод и неопытен! Несмотря на это, я начал тратить на это время и, с помощью моего старого друга (Fabio), 
мне наконец-то удалось установить сервер WoW на свой собственный компьютер.

Тогда я даже не представлял, как много удовольствия и знаний я получил благодаря этому волшебному миру.
Это может прозвучать странно, но этот мир все еще очаровывает меня сейчас, как взрослого человека, в определённый момент я даже посвятил этой теме свою 
[диссертацию магистра по информатике](https://community.trinitycore.org/topic/13025-just-thank-you-wow-emulation).

![wow-emulation-thesis](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-emulation-thesis.jpeg)

И всё же: **Я ненавижу большинство пиратский серверов и я действительно хочу объяснить почему.**

## Немного технических терминов

![Wow-sleeping](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-sleeping.jpg)

Для того, чтобы вы поняли мою точку зрения, мне необходимо остановиться на небольшой технической особенности о рабочих процессов WoW, которую я постараюсь объяснить на пальцах.

### Как работает оригинальный World of Warcraft

На программном уровне есть две программы, которые можно считать основными действующими лицами этой игры:

- **ПРИЛОЖЕНИЕ КЛИЕНТ** - Это и есть "World of Warcraft", установленный каждым игроком на своем компьютере для доступа к игре;

- **ПРИЛОЖЕНИЕ СЕРВЕР** - Это программа, которая работает на серверных машинах

Процесс очень простой: все Клиенты (игроки) соединяются с сервером для того, чтобы взаимодействовать друг с другом. Клиент знает адрес сервера, так как он хранится в известном файле "**realmlist.wtf**" (поэтому вам нужно изменить этот файл, чтобы переключиться на другой сервер).

![Client-server](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/client-server.png)

### Как работает частный сервер World of Warcraft

При игре на пиратских серверах все точно также. Разница только в программном обеспечении, которое используется на серере.

![Wow-Defias](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-defias.jpg)

**КЛИЕНТ**. У каждого есть доступ к оригинальному клиенту World of Warcraft. 
Вы можете легко получить его, купив или скачав онлайн. 
Именно его вы будете использовать для игры на официальном сервере. 
Очевидно, что разные пиратские серверы имеют разные версии клиентов(BC,WoTLK,Cataclysm и.т.д), но это всегда оригинальный клиент. 
Нужно лишь внести небольшое изменение в файл "realmlist.wtf", заменив адрес ретейла(офа) на адрес пиратского сервера. Вот и все.

**СЕРВЕР**. Это совсем другое. 
Никто за пределами Blizzard не имеет доступа к оригинальному программному обеспечению, которое управляет официальными серверами World of Warcraft. 
Так что эти приложения полностью отличаются от оригинального.

### Обратная разработка (обратная инжинерия/реверс-инжиниринг)

![Reverse engineering](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/reverse-engineering.jpeg)

Каждое программное обеспечение, которое работает на пиратских серверах, было создано с помощью метода "обратной инженерии/реверс-инжиниринга", 
что, простыми словами, означает "я пытаюсь написать программу, имитирующую поведение другой программы, не глядя на исходный код".

Теперь вопрос в том, кто реализовал эту программу и когда это произошло?

#### Отступление от авторских прав

*Весь защищенный авторским правом материал (изображения, звуки, 3D модели, логотипы и т.д. ...) находится внутри клиентского приложения.
Серверное приложение содержит только цифры и тексты. Поэтому использование его в образовательных целях абсолютно легально.*

## Неофициальные серверные приложения WoW

Кто создает программы, которые работают на частных серверах WoW (обычно называемых "эмуляторами")? И как они это делают?

### Сложность

![Complex](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/complex.jpg)

Не нужно быть экспертом, чтобы понять, что написание серверного приложения для MMORPG с таким большим размахом, как World of Warcraft, это уж точно не игрушки.

Blizzard - большая компания с тысячами сотрудников. Написание программы, "имитирующей" работу их серверного приложения, безусловно, 
не просто и нецелесообразно для одного человека (или небольшой группы программистов).
*Примечание переводчика: однако Blizzard разработывала WoW не всей тысячей, всего над сервером и клентов трудилось человек 200 или около того.*

И дело не только в сложности. Давайте подумаем об очень простых, но повторяющихся задачах, таких как добавление в мир каждого NPC, 
включая каждую единицу их лута с собственным процентом шансов и т.д... 
Потрясающая работа в принципе. Не говоря уже обо всех очень сложных задачах, требующих часов изучения и тестирования, таких как механика заклинаний, механика босса и т.п.

Одним словом... даже самый лучший программист в мире не смог бы выполнить всю эту работу самостоятельно.

Тем не менее, существуют пиратские серверы, и программное обеспечение, которое заставляет их работать. 
И некоторые пиратские серверы теперь могут предложить качественную игру, которая недалека от оригинала (здесь я имею в виду в основном старые дополнения).

Как это возможно?

### MaNGOS и открытый исходных код

> Если у вас есть яблоко, и у меня - яблоко, и мы обменяемся этими яблоками, то у нас с вами все равно будет по одному яблоку. 
Но если у вас есть идея, у меня есть идея, и мы обменяемся этими идеями, то у каждого из нас будет две идеи. (Джордж Бернард Шоу)

Для простоты: программа с открытым исходным кодом - это программа, код которой публичный.

В контексте пиратских серверов, открытый исходный код играет фундаментальную роль.

Некоторые геймеры-ветераны, возможно, помнят, что когда-то качество игры на пирастких серверах было действительно плохим, почти ничего не работало.
Например, если бы вы были разбойником в инвизе, вы могли стать мишенью для любого, кто написал `/target nickname`. 
Угадайте, какой класс я выбрал для своего первого персонажа...

![Mangos-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/mangos-logo.gif)

Настоящей революцией стал [MaNGOS](https://ru.wikipedia.org/wiki/MaNGOS) - проект с открытым исходным кодом, созданным в 2005 году, 
целью которого было предоставление серверного приложения для World of Warcraft.
*Примечание переводчика: до MaNGOS был WoWEmu и другие, но всех их объединяло то, что это был лютый треш.*

Хорошей новостью как и силой MaNGOS было то, что его код как открытого приложения был полностью публичным, 
и любой пользователь со всего мира мог изучить его и внести свой вклад 
(как в плане добавления или исправления игровой механики, так и в плане сообщения об ошибках).

Только таким образом, благодаря вкладу многих добровольцев разных национальностей, удалось разработать серверное приложение, 
способное эмулировать World of Warcraft с более высоким качеством игры.

В 2009 году родился еще один важный проект [TrinityCore](https://www.trinitycore.org/), основанный на MaNGOS.
*Примечание переводчика: тут есть небольшая ирония, а заключается она в том, что группа разработчиков MaNGOS устала от проверок их кода* 
*лидерами проэкта MaNGOS, т.к. это по их инению затягивало исправления багов,спеллов,талантов,квестов(что так и было, но проблему нужно не просто исправить,*
*а сделать это качественно, например не добавив новых),
*а в итоге тринити пришли к тому же самому из-за чего ушли :D*

![Trinitycore-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/trinitycore-logo.png)

На сегодняшний день подавляющее большинство частных серверов работают на серверных приложениях (ядрах), основа которых MaNGOS/TrinityCore.

С годами родились [различные проекты](http://mangosrumors.org/best-wow-emulator-2020/), и они были основаны на коде MaNGOS/TrinityCore, 
который в основном варьируется в зависимости от поддерживаемой версии WoW.
Например [AzerothCore](https://www.azerothcore.org/) для 3.3.5, 
[OregonCore](https://github.com/OregonCore) для 2.4.3, 
[SkyFire](https://www.projectskyfire.org/) для 5.4.8, 
[CMaNGOS](https://cmangos.net/) для Classic/TBC/WOTLK и многих других .... 
Все они основаны на MaNGOS и/или TrinityCore.

*Примечание переводчика: на самом деле CMaNGOS это тот же MaNGOS, только continued, парни не сошлись во взглядах на дальнейшую разработку
после ухода основых лидеров VladimirMangos и TheLuda*

![Azerothcore-authserver](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/azerothcore-authserver.png)

### Справка

Пиратские серверы достигли такого качества только благодаря большому комьюнити, 
которое внедряло все больше и больше игровых возможностей на протяжении многих лет (с 2005 года по сегодняшний день).

Сегодня любой опытный пользователь ПК может легко установить сервер WoW, даже не будучи программистом.

## Открытый исходный код против пиратских серверов

![Alice-and-bob](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/alice-and-bob.jpg)

### Гипотетический сценарий

Предположим, что у Алисы и Боба есть частный сервер, и давайте предположим, что они находятся на одной и той же версии игры.
И Алиса, и Боб хотят выпустить новый контент для своих игроков, который до сих пор был закрыт, потому что боссы `A`, `B`, `C` и `D` довольно багованые.

- Алиса очень хороший разработчик и может исправить обоих боссов `A` и `B`.
- Боб все еще новичок и исправляет только босса `C`.

### В идеальном мире

Алиса и Боб работают вместе и обмениваются исправлениями. В результате, оба их сервера будут иметь отлично заскриптованых боссов `A`, `B` и `C`.
Кроме того, Алиса и Боб объединят свои усилия для работы над `D`.

В результате, игроки на обоих серверах очень довольны, потому что они получают полностью рабочий контент.

### В реальном мире

Алиса и Боб - соперники, поэтому они ведут войну друг против друга. На сервере Алисы работают только боссы `А` и `B`. В то время как на сервере Боба работает только `C`.
Некоторые игроки перемещаются с сервера Боба на сервер Алисы. Сервер Боба закрывается через некоторое время. Некоторые игроки на сервере Алисы перестают играть, потому что устают всегда ходить только на босов `А` и `В`, потому что `С` и `D` не работают.

В результате, игроки на обоих серверах менее довольны, чем в предыдущем сценарии. Алиса заработала на донатах игроков больше, чем Боб.

### Лицензия эмуляторов WoW

На самом деле, код MaNGOS/TrinityCore (и их производных проектов) выпускается под [лицензией GNU GPL](https://en.wikipedia.org/wiki/GNU_General_Public_License).

Простыми словами, в этой лицензии сказано следующее: пользуйтесь исходным кодом, чтобы делать все, что хотите, не платя за это ничего, 
до тех пор, пока любые изменения в исходном коде выпускаются под той же самой лицензией.
По существу, лицензия этих проектов требует от тех, кто ими пользуется, публиковать любые изменения в сообществе.

Конечно, большинство пирастких серверов используют эту лицензию как **туалетную бумагу**. 
Иначе не было бы никакого пиратского сервера, который работает лучше, чем другие.

![Toilet-paper](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/toilet-paper.jpg)

## Ложь о пиратских серверах

Вот список лжи, которую администраторы многих пирастких серверов WoW продолжают рассказывать своим игрокам:

### Мы написали это ядро сами

Ложь! Нет никакой разницы, сколько изменений внес лично ты, все равно за основу взят проект MaNGOS.

Может быть, вы и сделали некоторые улучшения, но большая часть кода все еще принадлежит MaNGOS/TrinityCore.

Может быть, вы действительно хороши и переписали большую часть кода за эти годы. Тем не менее, вы начали с MaNGOS. 
Без него на старте у вас не работала бы даже авторизация.

### "Мы починили X"

В подавляющем большинстве случаев никто ничего не исправлял относительно взятой основы(MaNGOS/TrinityCore).
Они только что скачали исправления, исходящие от сообщества разработчиков ПО с открытым исходным кодом, и применили их к своему ядру.
Но при этом вся слава достается им.

### "Мы (реально) починили X"

Некоторые пиратские серверы действительно исправляют вещи самостоятельно. Часто у них есть специальные команды разработчиков, которым платят деньги, 
поступающие от донатов игроков.

Большинство из них не делятся этими исправлениями с сообществом разработчиков.

Лицензия GPL на эмулятор, которыми вы пользуетесь для запуска своего сервера, просит вас делиться исправлениями, 
но вы все равно не делаете этого. Поэтому я вас ненавижу.

![Pinocchio](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/pinocchio.jpeg)

## "Оправдания" частных серверов.

### "Я держу исправления в секрете, чтобы сделать мой сервер лучше, чем другие"

Хорошо, чемпион. Попробуйте подумать об этом: если бы ВСЕ разработчики делали как вы, ни вас, ни вашего пиратского сервера не существовало бы.

Почему? Да потому, что не существовало бы ни MaNGOS (ни TrinityCore, ни AzerothCore и т.д. ...).
Эти проекты существуют благодаря разработчикам, которые, в отличие от вас, поделились своим кодом.

Если бы все разработчики сохраняли свой код приватным, у нас не было бы приличного эмулятора WoW, и вы просто не смогли бы открыть свой пирасткий сервер, 
потому что не было бы никакого программного обеспечения.

### "Если бы я поделился своими исправлениями, конкуренты украли бы их"

Нечего "воровать". Они не могут "украсть" этот код, потому что он не "принадлежит" тебе. Да, даже если ты действительно его написал.

Философия открытого исходного текста ясна: вы можете пользоваться этим кодом бесплатно, при условии, что любое его изменение ДОЛЖНЫ быть обнародовано.

Разве вы не согласны? Хорошо. Тогда не используйте открытый исходный код и пишите свой собственный эмулятор WoW с нуля.

## Как это влияет на игроков

![Wow-Dranei-crying](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-dranei-crying.jpg)

Я прекрасно понимаю, что вся эта история с этикой и лицензиями для среднестатистического игрока World of Warcraft имеет очень мало значения.
Игроки просто хотят играть на стабильном и хорошо отлаженном сервере, их не очень волнует, сотрудничает этот сервер с открытым исходным кодом или нет.

Но... попробуйте на мгновение взглянуть на это с другой точки зрения.

Разработчики проектов с открытым исходным кодом (MaNGOS, TrinityCore, AzerothCore и т.д. ...) в основном не заботятся о том, что делают пирасткие серверы.
Конечно, как разработчика вас бесит, что какой-то случайный администратор сервера получает деньги за вашу работу, но в конце концов это не меняет вашу жизнь.
Многие разработчики с открытым исходным кодом делают это просто для развлечения и обучения.

На самом деле, если бы ВСЕ частные серверы сотрудничали с открытым исходным кодом, жизнь игроков полностью изменилась бы!
В этом случае, каждый сервер сможет обеспечить гораздо лучший игровой опыт для любого аддона(BC WOTLK и.т.д). 
Пример Алисы и Боба, упомянутый выше, может быть применен и в этом случае.

Однако реальность такова: по всему миру существует множество пирастких серверов, каждый из которых всегда работает над одними и теми же проблемами, 
гоняясь за тем, чтобы сделать их быстрее и лучше.
Если бы они сотрудничали друг с другом, они могли бы избежать ненужной работы и иметь больше времени сил. 
И могли бы достичь гораздо большего.

*Примечание: качество (конкуренция) между пиратскими серверами должно состоять не только из работоспособности контента, а еще и из других факторов, таких как умение их администраторов управлять ими(серверами).
Сообщество также играет фундаментальную роль, как и в случае с серверами Blizzard (которые с технической точки зрения все равны)*.

Если пиратский сервер закрывается, а его разработчики не поделились своей работой, то эта работа(фиксы) будет потеряна навсегда.

## Разоблачение лжи

### Официальный список авторов

Самое интересное, что все проекты на базе MaNGOS полностью публичны, поэтому можно точно проверить, кто в них участвовал.

В результате, все списки вкладчиков этих проектов абсолютно общедоступны, и ЛЮБОЙ может проверить, кто в действительности что исправил.

Нампример:

- Официальный список вкладчиков MaNGOS: https://github.com/cmangos/mangos-wotlk/blob/master/AUTHORS.md
- Официальный список участников TrinityCore: https://github.com/TrinityCore/TrinityCore/blob/3.3.5/AUTHORS
- Официальный список вкладчиков AzerothCore: https://github.com/AzerothCore/azerothcore-wotlk/graphs/contributors

PS: вы можете найти автора этой статьи во всех этих списках
*Примечение переводчика: как одного так и второго переводчика можно найти в AzerothCore(Winfidonarleyan и Viste). Viste можно было бы найти и впервых двух, но он тогда был мудаком и не делился фиксами :D*
### Официальный список коммитов (изменений)

Любой проект с открытым исходным кодом (обычно размещаемый на GitHub) имеет список коммитов, реализованных разными разработчиками. 
Для каждого коммита есть как автор, так и дата его создания.

Очень легко проверить эту информацию, просто откройте официальный репозиторий любого эмулятора. 

Например, "TrinityCore github" или "AzerothCore github" и просто взгляните.
- [TrinityCore. Версия клиента 3.3.5a](https://github.com/TrinityCore/TrinityCore/commits/3.3.5)
- [AzerothCore. Версия клиента 3.3.5a](https://github.com/azerothcore/azerothcore-wotlk/commits/master)

Вы увидите, того кто что-нибудь сделал. Вы увидите все строки кода, их авторов, комментарии других разработчиков и так далее. 
Вы увидите все. Больше никакой лжи!

## Что я могу сделать как игрок?

Мой совет - играйте и поддерживаете на пиратских серверы, которые сотрудничают с открытым исходным кодом, несмотря на тип расширения и эмулятор, который они используют. 
*Примечание переводчика: А от тех кто не поддерживаете БЕГИТЕ, они конечно молодцы, что починили что-то, но поступают не по христиански*

Или, по крайней мере, избегайте тех серверов, которые выдают чужую работу за свою, удаляя авторские права оригинала.

### Узнать больше о свободном программном обеспечении

- https://www.gnu.org/software
- https://www.fsf.org/about/what-is-free-software

## Спасибо

Особая благодарность *Лауре Бартиромо*

### Спасибо за помощь в переводе

- Игроку с сервера wowka.su **Luna**
- [@Viste](https://github.com/Viste) за более детализированую информацию

*Примечание от Viste: сомнительная помощь, т.к. когда я увидел этот текст он выглядел как после google переводчика... пришлось поредачить, что я тоже сделал не очень качественно простите, но было мало времени, из-за чего текст все еще похож на машинный перевод* 




# De ce urăsc majoritatea serverelor private de WoW

*Scris de Francesco Borzi' aka Shin / Tradus de Ouizzy @wizzymore*

De ce sunt atât de multe probele în serverele private de WOW, deși sunt pe zone de atât de mulți ani?

![Wow-facepalm](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-facepalm.jpeg)

Nu te îngrijora, aceasta nu este o lectură de copyright legată de Blizzard.
Doar vreau să explic de ce urăsc majoritate serverelor private de [World of Warcraft](https://en.wikipedia.org/wiki/World_of_Warcraft).

## Introducere

Sunt fascinat de emularea WoW încă de când aveam 14 ani. Îmi amintent că prima dată când am intrat pe un "server special", erau o multime de buguri, dar puteai să te joci pe gratis cel puțin. N-aveam niciun ban în acea perioadă, deci, nu aveam altă alternativă.

La 15 ani am început să mă întreb cum functionează de fapt serverele private și cum pot să existe, în special dintr-o perspectivă tehnică. A furat cumva cineva codul de la [Blizzard](https://ro.wikipedia.org/wiki/Blizzard_Entertainment)? Nu aveam nici o idee - eram atât de tânăr și ne-experimentat în acea perioadă! Totuși, am început să ma prostesc și, cu ajutorul unui prieten vechi (Fabio), am reușit în sfârșit să instalez un server de WoW la mine pe PC.

Pe vremea aceea nici nu îmi puteam imagina câtă satisfacere o să primesc și câte lucruri o să învăt datorită acestei lumi magice.

Poate suna ciudat, dar această lume încă mă fascinează, ca un adult, la un moment, mi-am dedicat întreaga [Licență de Master în Știința Calculatoarelor pe acest subiect](https://community.trinitycore.org/topic/13025-just-thank-you-wow-emulation).

![wow-emulation-thesis](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-emulation-thesis.jpeg)

Dar, totuși: **Urăsc majoritatea serverelor private și chiar vreau să înțelegi de ce.**

## Câțiva termeni tehnici

![Wow-sleeping](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-sleeping.jpg)

Ca să poți să-mi înțelegi punctul de vedere, trebuie să te învăț cateva termene tehnice despre procesul funcțional WoW, pe care încerc să le pun în cele mai simple cuvinte.

### Cum funcționează originalul World of Warcraft

La nivelul de software, sunt două programe pe care le poți considera actorii principali ai jocului:

- **APLICAȚIA CLIENT** - care este actualul "World of Wacraft" instalat de către toți jucătorii pe calculatoarele lor ca să poată accesa jocul;

- **APLICAȚIA SERVER** - programul care funcționează pe servere specializate.

Procesul este foarte simplu: toți Clienții (jucătorii) se conectează la Server ca să poată interacționa cu alți jucători. Clientul știe adresa serverului, cum este memorată în faimosul fișier "**realmlist.wtf**" (de asta trebuie să modifici acest fișier ca să te poți schimba pe alt server)

![Client-server](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/client-server.png)

### Cum funcționează serverele private de WoW

Când te joci pe servere private, principiul este același. Diferența este doar software-ul pe care îl folosești.

![Wow-Defias](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-defias.jpg)

**CLIENTUL**. Toată lumea are acces la clientul original de World of Warcraft. Poți să il obții ușor dacă cumperi clientul sau îl descarci de pe internet. Acest program este exact același program pe care l-ai folosii să te joci pe serverele oficiale. Desigur, diferite servere private au cliente cu versiuni diferite, dar mereu folosesc clientul original. Tu doar trebuie să faci o mică schimbare în fișierul "realmlist.wtf", înlocuind adresa serverului de retail cu adresa serverului privat. Și asta e cam tot.

**SERVER**. This is completely different. Nobody outside Blizzard has access to the original software that runs the official World of Warcraft servers. So these applications are completely different from the original one.
**SERVER**. Asta este o diferență completă. Nimeni înafară de Blizzard nu are acces la software-ul original care rulează serverele oficiale de World of Warcraft. Deci aceste aplicații sunt complet diferite de cele originale.

### Reverse engineering

![Reverse engineering](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/reverse-engineering.jpeg)

Toate software-urile care rulează servere private au fost create prin tehnica de "inginerie inversă", care, în cuvinte simple, înseamnă "Încerc să scriu un program care imitează comportamentul altui program, fără să mă uit la codul original".

Întrebarea acum este: cine a implementat acest software și când s-a întâmplat?


#### Digression about the copyright

*The entire copyrighted material (images, sounds, 3D models, logos, etc ...) is located inside the client application.
The server application contains only numbers and texts. Therefore, it is absolutely legal if you use it for educational purposes.*

## Unofficial WoW server applications

Who creates the software applications that run WoW's private servers (commonly called "emulators")? And how did they do it?



### Complexity

![Complex](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/complex.jpg)

You don't need to be an expert to understand that writing a server application for an MMORPG with such a big scope like World of Warcraft is certainly not child's play.

Blizzard is a big company with thousands of employees. Writing a program that "imitates" the operation of their server application is certainly not trivial or feasible for a single individual (or a small group of programmers).

And it's not just a matter of complexity. Let's think of very trivial but repetitive tasks, like adding every single NPC into the world, including every single item of their loot with its own percentage of chance, etc.. . A terrific job basically. Not to mention all the very complex tasks that require hours of study and testing, such as spell mechanics, boss mechanics, etc.

In short .... not even the best programmer in the world could be able to do all this work on her/his own.

Yet there are private servers, and the software that makes them run. And some private servers are now able to offer a game quality that is not far from the original one (here I refer mainly to the old expansions).

How is that possible?

### MaNGOS and the open source development model

> If you have an apple and I have an apple and we exchange these apples then you and I will still each have one apple. But if you have an idea and I have an idea and we exchange these ideas, then each of us will have two ideas. (George Bernard Shaw)

Just to make it simple: an open source program is a program whose code is public.

In the context of private servers, the open source plays a fundamental role.

Some veteran gamers may remember that once the game quality on private servers was really bad. Almost nothing worked.
For example, if you were a rogue in stealth you could be targeted by anyone who wrote `/target Yourname`. Guess which class I chose for my first character ...

![Mangos-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/mangos-logo.gif)

The real revolution was [MaNGOS](https://it.wikipedia.org/wiki/MaNGOS), an open source project created in 2005, whose purpose was to provide a server application for World of Warcraft.
The great news of MaNGOS, as well as its strength, was the fact that as an open source application, its code was completely public, and any user from all over the world could study it and offer their own contribution (both in terms of adding or fixing game mechanics, but also in terms of reporting bugs).

Only in this way, thanks to the contribution of many volunteers of different nationalities, it was possible to develop a server application capable of emulating World of Warcraft with a higher game quality.

In 2009 another important project was born [TrinityCore](https://www.trinitycore.org/), based on MaNGOS.

![Trinitycore-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/trinitycore-logo.png)

To date, the overwhelming majority of private servers run on MaNGOS/TrinityCore-based applications.

Over the years, [different projects](http://mangosrumors.org/best-wow-emulator-2020/) were born, and they were based on the MaNGOS/TrinityCore code, which mainly vary according to the supported WoW version.
For example [AzerothCore](https://www.azerothcore.org/) for 3.3.5, [OregonCore](https://github.com/OregonCore) for 2.4.3, [SkyFire](https://www.projectskyfire.org/) for 5.4.8, [CMaNGOS](https://cmangos.net/) for Classic/TBC/WOTLK, and many others ... All of them based on MaNGOS and/or TrinityCore.

![Azerothcore-authserver](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/azerothcore-authserver.png)

### Recap

So the private servers have reached such a quality only thanks to the many contributors who have implemented more and more game features over the years (from 2005 to today).

Today any experienced PC user can easily install a WoW server, without even being a programmer.

## Open source vs private servers

![Alice-and-bob](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/alice-and-bob.jpg)

### Hypothetical scenario

Suppose that Alice and Bob have a private server each, and let's assume they are on the same version of the game.
Both Alice and Bob want to release a new content to their players, which has been closed so far because the bosses `A`,` B`, `C` and` D` are quite buggy.

- Alice is a very good developer and can fix both bosses `A` and` B`
- Bob is still a beginner and only fixes the boss `C`

### In an ideal world

Alice and Bob work together and exchange their fixes. As a result, both of their servers will have perfectly fixed bosses `A`,` B` and `C`.
In addition, Alice and Bob will join forces in order to work on `D` as well.

As a result, the players on both servers are very happy because they play a completely fixed content.

### In the real world

Alice and Bob are rivals and so they wage war against each other. In Alice's server, only bosses `A` and` B` work. While in Bob's server only `C` works.
Some players move from Bob's server to Alice's one. Bob's server closes after a while. Some of Alice's server players stop playing because they get tired of always doing only `A` and` B` because `C` and` D` don't work.

As a result, the players on both servers are less happy than in the previous scenario. Alice made more money through player donations than Bob did.

### The license of the WoW emulators

Actually, the MaNGOS/TrinityCore code (and their derivated projects) is released under the [GNU GPL license](https://en.wikipedia.org/wiki/GNU_General_Public_License).

In simple words, this license says the following: use the code to do whatever you want, without paying anything, as long as any modification to the original code is also released under the same license.
Basically, the license of these projects requires those who use them to publish any changes to the public.

Of course, most private servers use this license as **toilet paper**. Otherwise, there should be no private server that is "better fixed" than others.

![Toilet-paper](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/toilet-paper.jpg)

## The lies about the private servers

Here it is a list of lies that the administrators of many WoW private servers keep telling to their players:


### "We wrote this core"

Fake news. It doesn't matter how many changes "you" made. However, you started with a MaNGOS-based project.

Maybe you've made some improvements, but most of the code is still MaNGOS/TrinityCore's.

Maybe you are really good and you have rewritten most of the code over the years. Still, you started from MaNGOS. Without it, on day 1 you wouldn't even have got the login feature working.

### "We have fixed X"

In the vast majority of cases, none of them has really fixed anything.
They have just downloaded the fixes coming from the open source community and applied them to their core.
Still they take all credits.

### "We (really) fixed X"

Some private servers really fix stuff on their own. They often have dedicated development teams that are paid with the money coming from players' donations.

Most of them do not share these fixes with the development community.

Well, the community that gave (for free) the software you are using to run your server is asking you to share them, but you still keep it private. So I hate you anyway.

![Pinocchio](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/pinocchio.jpeg)

## The "justifications" of private servers


### "I keep them private to make my server a special place, better than the others"

Alright champ. Try to think about this: if ALL the developers did like you, neither you nor your private server would exist.

Why? Simply because neither MaNGOS (nor TrinityCore, AzerothCore, etc ...) would exist.
These projects exist thanks to developers who, unlike you, shared their code.

If all devs kept their code private, we would have no decent WoW emulator and you just couldn't open your private server, because there wouldn't be any software available.


### "If I shared my fixes, the competition would steal them"

There is nothing to "steal". They can't "steal" that code because it doesn't "belong" to you. No, not even if you really wrote it.

The open source philosophy is clear: you can use that code for free, provided that any modification of it MUST be made public.

Oh don't you agree? Alright. Then don't use any open source code and write your own WoW emulator from scratch.

## How this affects players

![Wow-Dranei-crying](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-dranei-crying.jpg)

I totally understand that this whole story about ethics and licenses matters very little to the average World of Warcraft player.
Players just want to play on a stable and well-fixed server, they don't care much whether this server collaborates with open source or not.

But... try for a moment to see it from another perspective.

Developers of the open source projects (MaNGOS, TrinityCore, AzerothCore, etc ...) basically don't care much about what private servers do.
Of course, as a developer it pisses you off to see some random server administrator taking credits for your work, but in the end it doesn't change your life.
Many open source developers just do it for fun and educational purposes.

Actually, if ALL private servers collaborated with open source, the players’ lives would change completely!
You know, in that case, every server would provide a much better game experience for any expansion. The example of Alice and Bob mentioned before can be applied to this case as well.

However, the reality is just that: there are many private servers around the world, each of them always works on the same things, racing to do them sooner and better.
If they collaborated with each other instead, they would avoid doing unnecessary work and would have more time and workforce. So they would surely be able to achieve much more.

*Note: the quality (and competition between) private servers should not be (only) about of fixing, but also about other factors such as its administrators’ skills in managing it. The quality of the community also plays a fundamental role, just as it happens in Blizzard servers (which are all equal from a technical perspective).*

If a private server closes, and its developers have not shared their work, that work will be lost forever.

## Exposing lies

### Official authors list

The most interesting thing is that all the MaNGOS-based projects are completely public, so it is possible to accurately verify who contributed to them.

As a result, all the contributors list of these projects are absolutely public and ANYONE can verify who actually fixed what.

For example:

- Official list of MaNGOS contributors: https://github.com/cmangos/mangos-wotlk/blob/master/AUTHORS.md
- Official list of TrinityCore contributors https://github.com/TrinityCore/TrinityCore/blob/3.3.5/AUTHORS
- Official list of AzerothCore contributors https://github.com/AzerothCore/azerothcore-wotlk/graphs/contributors

PS: you can find the author of this article in all these lists

### Official commits list

Any open source project (generally hosted on GitHub) has the list of commits realised by the different developers. For each commit, both the author and the date are there.

It is very easy to verify this information, just open the official repository of any emulator. Google for example "TrinityCore github" or "AzerothCore github" and just have a look.

You will see who-does-really-what. You will see all the lines of code, their authors, other devs’ comments, etc. You will see everything. No more lies!


## What can I do as a player?

My advice is you play/support private servers that collaborate with open source, in spite of the type of expansion and emulator they use.

Or, at least, avoid those servers that peddle other people's work on their own, removing the credits from the original authors.

**NEW:** in 2021 the new project [ChromieCraft](https://www.chromiecraft.com/about) has been launched, featuring a fully open-source server with a progressive-twink taste.

![ChromieCraft logo](https://avatars1.githubusercontent.com/u/68329413?s=400&u=084b35243e0aed1becd6a67fa88717eb8c1674d8&v=4)

### Learn more about free software

- https://www.gnu.org/software/software.en.html
- https://www.fsf.org/about/what-is-free-software


## Thanks

Special thanks to *Laura Bartiromo*

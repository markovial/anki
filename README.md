## My Current Anki Plugins

* [Add Table                     ](https://ankiweb.net/shared/info/1237621971) : Add tables to anki cards
* [Advanced Browser              ](https://ankiweb.net/shared/info/874215009)  : Add column sorting
* [AwesomeTTS                    ](https://ankiweb.net/shared/info/1436550454) : Add audio to anki cards
* [Browser TableEditor           ](https://ankiweb.net/shared/info/831846358)  : Display Table and editor side by side
* [Colorful Hierarchical Tags    ](https://ankiweb.net/shared/info/594329229)  : Add hirearchical tags
* [CrowdAnki                     ](https://ankiweb.net/shared/info/1788670778) : Import and export deck as JSON
* [Custom Background             ](https://ankiweb.net/shared/info/1210908941) : Rice Anki UI
* [Duplicate and Reorder         ](https://ankiweb.net/shared/info/1114271285) : Create cards by duplicating existing
* [Enhance main window           ](https://ankiweb.net/shared/info/877182321)  : Rice Anki UI
* [Highlight Search Results      ](https://ankiweb.net/shared/info/225180905)  : Highlight search results
* [Mini Format pack              ](https://ankiweb.net/shared/info/295889520)  : More formatting options
* [Minimal Flat Big Buttons      ](https://ankiweb.net/shared/info/1042429613) : Rice Anki UI
* [More Deck stats and time left ](https://ankiweb.net/shared/info/1556734708) : Display time stats on home screen
* [Remaining time for anki 21    ](https://ankiweb.net/shared/info/1508357010) : Display time stats on review screen
* [Review Heatmap                ](https://ankiweb.net/shared/info/1771074083) : Display heatmap for reviews
* [Search Bar                    ](https://ankiweb.net/shared/info/1251668918) : Add search bar to reviewer and editor
* [Vim answer shortcuts          ](https://ankiweb.net/shared/info/1197299782) : Vim shortcuts to answer


## NOTES on COLLABORATION

I tried open sourcing and public collab using github + anki. I don't really like the current status of remote collaboration. In my experience, if you want a large group of people to collaborate you have to reduce the barriers as much as possible. It has to be as simple as - here is a link , edit/comment on the column you feel like needs to be changed. I want the work flow to look something like this :

* Editing remotely is done to a shared file (e.g. google sheets)
* Editing locally is done in Anki
* In both cases you read from github directly making the github file the main "source of truth".

* To publish changes use [GithubSheets](https://github.com/Max-Makhrov/GitHub-Sheets-gs) (or something similar for whatever service you are using) with an authentication token
* To publish changes from Anki , clicking sync would export deck as Json/CSV/XML/... this would create a pull request to github.
* If you are a recognized editior (i.e. have an authentication token) the pull request gets auto accepted = auto sync.

* Both sheets and anki reflect changes automagically since they are reading and editing the same file.
* It's not live and editior permissions can be mananged by choosing to share sheets link/permission or the github authentication token.

This doesn't seem achievable unless anki itself integrates with github or some other versioning service. The closest thing to this seems like Anki Remote Decks.

Current things that irk me :

* [CrowdAnki](https://github.com/Stvad/CrowdAnki) : Each deck has to be in a seperate repo which I don't like
* CrowdAnki : The repo name has to be the same as the local deck name which I don't like
* CrowdAnki : Editing suggested be done in to JSON file , not user friendly at all.
* [BrainBrew](https://github.com/ohare93/brain-brew) : No idea on what exactly the yaml recipies are ... ?
* [Anki Remote Decks](https://github.com/c-okelly/anki-remote-decks) : Creates a new seperate class of deck 'remote decks' and all remote decks are subdecks. Cannot rename/move the deck.

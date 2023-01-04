## My Current List of Anki Plugins

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

This doesn't seem achievable unless anki itself integrates with github or some other versioning service.

Current things that irk me :

* [CrowdAnki](https://github.com/Stvad/CrowdAnki) : Each deck has to be in a seperate repo which I don't like
* CrowdAnki : The repo name has to be the same as the local deck name which I don't like
* CrowdAnki : Editing suggested be done in to JSON file , not user friendly at all.
* [BrainBrew](https://github.com/ohare93/brain-brew) : No idea on what exactly the yaml recipies are ... ?
* [Anki Remote Decks](https://github.com/c-okelly/anki-remote-decks) : Creates a new seperate class of deck 'remote decks' and all remote decks are subdecks. Cannot rename. Not a fan.

|                                                                                     |                                        |
| :--                                                                                 | :--                                    |
| [Advanced Browser](https://ankiweb.net/shared/info/874215009)                       |                                        |
| [Anki Zoom](https://ankiweb.net/shared/info/538879081)                              |                                        |
| [AwesomeTTS](https://ankiweb.net/shared/info/1436550454)                            |                                        |
| [Change Interface Font]()                                                           |                                        |
| [Custom Background Image and Gear Icon](https://ankiweb.net/shared/info/1210908941) |                                        |
| [Customize Sidebar]()                                                               |                                        |
| [Enhance main window](https://ankiweb.net/shared/info/877182321)                    |                                        |
| [Hierarchical Tags 2](https://ankiweb.net/shared/info/594329229)                    |                                        |
| [Image Occlusoin Enchanged for Anki 21](https://ankiweb.net/shared/info/1374772155) |                                        |
| [Japanese Support](https://ankiweb.net/shared/info/3918629684)                      |                                        |
| [Kanji Colorizer stroke order diagrams](https://ankiweb.net/shared/info/1964372878) |                                        |
| [Mini Format pack](https://ankiweb.net/shared/info/295889520)                       |                                        |
| [Minimal Flat Big Buttons](https://ankiweb.net/shared/info/1042429613)              |                                        |
| [More Deck stats and time left](https://ankiweb.net/shared/info/1556734708)         |                                        |
| [Remaining time for anki 21](https://ankiweb.net/shared/info/1508357010)            |                                        |
| [Review Heatmap](https://github.com/glutanimate/review-heatmap#installation)        |                                        |
| [Vim answer shortcuts](https://ankiweb.net/shared/info/1197299782)                  |                                        |
| [No Distractions](https://ankiweb.net/shared/info/1049863218)                       | Remove Unneccesary junk from screen    |
| [Highlight Search Results](https://ankiweb.net/shared/info/225180905)               |                                        |
| [Collapsible Fields](https://ankiweb.net/shared/info/1896168623)                    |                                        |
| [Search Bar](https://ankiweb.net/shared/info/1251668918)                            | Adds search bar to reviewer and editor |
| [CrowdAnki](https://ankiweb.net/shared/info/1788670778)                             | Import and export deck as JSON         |
| [Duplicate and Reorder](https://ankiweb.net/shared/info/1114271285)                 | Duplicate existing cards               |
| [Browser](https://ankiweb.net/shared/info/831846358)                                | Table and editor side by side          |
| [Add Table](https://ankiweb.net/shared/info/1237621971)                             |                                        |


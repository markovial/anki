
## Todo
* Get the german deck working , with full export import cycle tested
* Delete all images from Deutsch decks , and replace with open source / cited images
* Readme - add process for easy new deck onboarding


## Export your deck

How does a deck go from anki to git ? :

|             |                          |                                                                 |
| :--         | :--                      | :--                                                             |
| CrowdAnki   | Export Deck as json file | Export as CrowdAnki JSON representation                         |
| Brain-Brew  | Unpack json into csv     | brainbrew init <br /> brainbrew run recipes/anki_to_source.yaml |
| LibreOffice | Edit fields in csv       | data/src/deckname.csv                                           |
| Git         | Publish                  | git push                                                        |

## Import a new deck
|            |                            |                                           |
| --         | :--                        | :--                                       |
| Git        | Get from github            | git pull                                  |
| Brain-Brew | Convert csv to json        | brainbrew run recipes/source_to_anki.yaml |
| CrowdAnki  | Import Deck from json file | Import from disk (import build folder)    |

## Making Contributions

Edit the csv files in : data/src , using either excel or libreoffice or
whatever you want. Then push the changes to git.

You don't have to edit only in the csv format. You can just do all your edits
in Anki itself , and export using CrowdAnki. These changes will still be
reflected. It just depends on what you are more comfortable with. I was just
showing one possible workflow.

## Dependencies

[Python 3.7+](https://www.python.org/) \
[pip](https://pypi.org/project/pip/) \
[pipenv 2021.11.23+](https://pypi.org/project/pipenv/) \
[Brain-Brew 0.3.6+](https://github.com/ohare93/brain-brew) \
[CrowdAnki Plugin](https://ankiweb.net/shared/info/1788670778)


If you have newer versions , make sure to edit the Pipfile in the root
dierctory with your version numbers. To check version numbers use :

python --version \
pip --version \
pipenv --version \
brainbrew --version

The above commands also help to validate that everything is installed and
working correctly.

## Folder and File structure :

**build** 

* **build** : Contains folders than can be imported by or are exported by CrowdAnki.
These folders contain all the deck data represented as a json file. The
CrowdAnki plugin can import the folders inside build and transform them into
Anki usable decks. Similarly , if changes are made in anki , to commit them to
github , you export the deck using the CrowdAnki plugin into this build folder.

* **recipes** : Contains yaml files. These files contain the instrucitons that dictate
how to transform the json files into csv files and vice versa. These are used by
brain-brew to change json files into csv files for easy editing and vice versa.

Running brainbrew run recipes/source_to_anki.yaml will convert current csv's
located in source to CrowdAnki readable json format inside build folder.

* **src** : Contains csv files that have all the actual data for the anki deck.
Editing is done in csv cause they are easier to deal with / format / edit than
json or within Anki directly.

## NOTES

I had problems with the brain-brew installation. I installed it fine , but I
couldnt run the init from the commandline , with error being command not found.
I got around it by doing : 

$HOME/.local/bin/brainbrew init 

, but a longer term soulution would be to add this directory to path. Ill do it
later though , cause for now its working ...

## TO CREATE A NEW COLLABORATABLE ANKI PROJECT

1. Export Deck as crowdanki file
1. run brainbrew init <folder_name> in folder
1. ... ?
1. profit

Export to folder : $HOME/Git/anki/
Import from folder :  $HOME/Git/anki/Art/build


```
$HOME/.local/bin/brainbrew init $HOME/Git/anki/Art
$HOME/.local/bin/brainbrew run $HOME/Git/anki/Art/recipes/source_to_anki.yaml
```

```
brainbrew init
```

it initalizes inside the folder that you are running the command from , so make sure you have cd'd into the right place before running the command.

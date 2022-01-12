# anki
Anki decks that I wish to collaborate on.

How does a deck go from anki to git ? :

EXPORT
CrowdAnki : Export Deck as json file
Brain-Brew : Convert json into csv
Git : Edit fields in csv and push using git

IMPORT
Git : pull from github
Brain-Brew : Convert csv to json
CrowdAnki : Import Deck from json file


You don't have to edit only in the csv format. You can just do all your edits in
Anki itself , and export using CrowdAnki. These changes will still be reflected.
It just depends on what you are more comfortable with. I was just showing one
possible workflow.

Dependencies :

python 3.7+
pip
pipenv 2021.11.23+ : pypi.org/project/pipenv/
Brain-Brew 0.3.6+  : github.com/ohare93/brain-brew 
CrowdAnki Plugin   : ankiweb.net/shared/info/1788670778

If you have newer versions , make sure to edit the Pipfile in the root dierctory with your version numbers. To check version numbers use :

python --version
pip --version
pipenv --version
brainbrew --version

The above commands also help to validate that everything is installed and working correctly.


file structure :

build : Contains folders than can be imported by or are exported by CrowdAnki.
These folders contain all the deck data represented as a json file. The
CrowdAnki plugin can import the folders inside build and transform them into
Anki usable decks. Similarly , if changes are made in anki , to commit them to
github , you export the deck using the CrowdAnki plugin into this build folder.

recipes : Contains yaml files. These files contain the instrucitons that dictate
how to transform the json files into csv files and vice versa. These are used by
brain-brew to change json files into csv files for easy editing and vice versa.

Running brainbrew run recipes/source_to_anki.yaml will convert current csv's
located in source to CrowdAnki readable json format inside build folder.

src : Contains csv files that have all the actual data for the anki deck.
Editing is done in csv cause they are easier to deal with / format / edit than
json or within Anki directly.



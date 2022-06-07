# HelloFlask
Découverte des gestionnaires et outils dev Poetry/pyenv/flask

#Installation et utilisation de Pyenv

etape1: update de sudo apt-get
sudo apt-get update

etape2: installation de librairies
sudo apt-get install make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev
libffi-dev liblzma-dev

etape3: installation de Pyenv à partir d'un script
curl https://pyenv.run | bash

etape4: ajout de lignes au fichier bashrc
# Load pyenv automatically
export PYENV_ROOT="$HOME/.pyenv"
command -v pyenv >/dev/null || export
PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"
# Load pyenv-virtualenv automatically
eval "$(pyenv virtualenv-init -)"

Attention mettre en commentaires entre les balises de 'conda initialise' pour éviter les conflits entre conda et pyenv


A partir de là pyenv est opérationnel!!

pyenv versions => python existant (en général au moins la version system)

pyenv install --list => affiche toutes les versions possibles

pyenv install miniconda3-4.7.12 => ajout d'un gestionnaire d'environnement

pyenv virtualenv <version python> <nom_environnement> => Création d'un environnement virtuel

pyenv activate <nom_environnement> => activation de l'environnement virtuel

pyenv global <version python> => permet de dire quelle version est utilisée par défaut 

python local <version python préférée> <version python> => dans le dossier du projet à venir, on spécifie la version avec laquelle on veut travailler. Crée un fichier .python -version qui contient le numéro de version choisie











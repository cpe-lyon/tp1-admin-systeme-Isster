# **Exercice 2:** Prise en main de l'interprétateur de commande

## Manuel

### 1) Identifier le rôle de which

Après avoir tapé la commande:

<code></br>
man which
</code>

On se rend compte que la commande **which** permet de localiser une commande ou un binaire.
</br>

### 2) Quand on consulte cette page, comment peut-on rechercher, par exemple, le mot option? 

Il suffit de tapper la commande:

<code></br>
man which
</code>

Puis la commande:

<code></br>
/option
</code>
</br>

### 3) Comment quitte-t-on le manuel ? 

Il suffit pour celà de tapper:
<code></br>
q
</code>
</br>

### 4) Chaque section du manuel a une première page, qui présente le contenu de la section. Aﬀicher la première page de la section 6; de quoi parle cette section?

Après avoir tappé la commande:
<code></br>
man 6 intro
</code>
</p>

Puis j'ai vu que dans la description, que la section 6 du manuel montre tout les jeux et applications amusantes disponible sur le système.
</br>

## Navigation dans l’arborescence des fichiers

### 1) Allez dans le dossier /var/log

Il suffit de tapper la commande:
<code></br>
cd /var/log
</code>
</br>

### 2) Remontez dans le dossier parent (/var) en utilisant un chemin relatif 

Il suffit de tapper la commande:
<code></br>
cd ..
</code>
</br>

### 3) Retournez dans le dossier personnel 

Il suffit de tapper la commande:
<code></br>
cd ..
</code>
</br>

### 4) revenez au dossier précédent (/var) 

Il suffit de tapper la commande:
<code></br>
cd /var
</code>
</br>

### 5) Essayez d’accéder au dossier /root; que se passe-t-il? 
Il faut tapper la commande:
<code></br>
cd /root
</code>
Mais en tant qu'utilisateur, on ne peut pas accéder au dossier administrateur car nous ne possédons pas les droits.
</br>

### 6) Essayez la commande sudo cd /root; que se passe-t-il? Expliquez  

Après avoir tapper la commande:
<code></br>
cd /root
</code></br>
On nous montre que nous n'avons pas les permissions avec "**Permission denied**"

### 7) A partir de votre dossier personnel, créez l’arborescence suivante
Il faut tapper la commande:
<code></br>
mkdir nom
</code></br>
Pour créer un dossier. </br>

Il faut tapper la commande:
<code></br>
touch nom
</code></br>
Pour créer un fichier.
</br>

### 8) Revenez dans votre dossier personnel; à l’aide de la commande rm, essayez de supprimer Fichier1, puis Dossier1; que se passe-t-il? 

En essayant d'utiliser la commande <code>rm Dossier1/Fichier1</code> ou <code>rm dossier1 </code>. On ne peux pas supprimer le dossier cependant le fichier sera supprimé si l'on utilise un chemin relatif.

### 9) Quelle commande permet de supprimer un dossier? 

Pour supprimer un dossier il faut tapper la commande:
<code>rmdir Dossier1 </code></br>

### 10) Que se passe-t-il quand on applique cette commande à Dossier2? 

 On ne peut pas car il y a des sous dossiers et des fichiers à l'intérieur.</br>

### 11) Comment supprimer en une seule commande Dossier2 et son contenu?

Il faut tapper la commande:
<code>rm -r Dossier2 </code></br>

## Commandes importantes

### 1) Quelle commande permet d’aﬀicher l’heure? A quoi sert la commande time? 

Afin d'afficher l'heure il faut tapper la commande:
<code>date </code></br>

La commande <code>time</code> permet d'éxecuter les programmes et determine les ressources utilisées par les commandes.</br>

### 2) Dans votre dossier personnel, tapez successivement les commandes ls puis la; que peut-on en déduire sur les fichiers commençant par un point? 

Les fichiers commençant par un point sont des fichiers cachés.</br>

### 3) Où se situe le programme ls? 
Il se situe dans le dossier usr/bin/
</br>

### 4) Que fait la commande ll? 
La commande <code>ll</code> permet de lister les fichiers et dossiers ainsi que leurs droits.
</br>

### 5) Quelle commande permet d’aﬀicher les fichiers contenus dans le dossier /bin? 

La commande permettant d'afficher les fichiers contenus dans le dossier /bin est: <code>ls usr/bin/</code>

### 6) Que fait la commande ls ..? 
La commande <code>ls</code> permet de lister les fichiers et dossiers du repertoire précédant.
</br>

### 7) Quelle commande donne le chemin complet du dossier courant?

Il s'agit de la commande: <code>pwd</code>
</br>

### 8) Que fait la commande echo 'yo' > plop exécutée 2 fois?
Cette commande permet de créer un fichier nommé plop. Puis une fois créer, il inscrit dans le fichier ce qui est écrit entre '' soit yo.
</br>

### 9) Que fait la commande echo 'yo' >> plop exécutée 2 fois? 
Cette commande permet de créer un fichier nommé plop. Puis une fois créer, il inscrit dans le fichier ce qui est écrit entre '' soit yo. Mais si on le fait 2x alors yo sera écrit à la suite du premier yo.
</br>

### 10) A quoi sert la commande file ? Essayez la sur des fichiers de types différents.
La commande **file** permet de déterminer le type de fichier en dehors de son extension.
</br>

### 11) Créez un fichier toto qui contient la chaîne Hello Toto ! ; créer ensuite un lien titi vers ce fichier avec la commande ln toto titi. Modifiez à présent le contenu de toto et affichez le contenu de titi : qu’observe-t-on ? Supprimez le fichier toto ; quelle conséquence cela a-t-il sur titi ?

Afin de créer le fichier toto qui contient la chaine "Hello Toto", il faut faire la commande: </br>
<code>echo "Hello Toto !" > Toto </code></br>
Apres avoir effectué le lien, lorsque l'on modifie le contenu de Toto, le contenu de Titi aussi change par conrte si l'on supprime le dossier Toto le dossier Titi quand à lui reste inchangé.</br>

### 12) Créez à présent un lien symbolique tutu sur titi avec la commande ln -s titi tutu. Modifiez le contenu de titi ; quelle conséquence pour tutu ? Et inversement ? Supprimez le fichier titi ; quelle conséquence cela a-t-il sur tutu ?

Après avoir créer un lien symbolique entre Titi et tutu, lorsque l'on modifie le contenu de titi, le contenu de tutu y est également changé de la même façon. De plus lorsque titi est supprimé, alors tout le contenu de tutu est supprimé également.
</br>

### 13) Affichez à l’écran le fichier /var/log/syslog. Quels raccourcis clavier permettent d’interrompre et reprendre le défilement à l’écran ?

Les raccourcis clavier permettant de stoper le defilement puis de reprendre sont:</br>
**Ctrl + s** Pour stoper le défilement </br>
**Ctrl + q** Pour reprendre le defilement </br>

### 14) Affichez les 5 premières lignes du fichier /var/log/syslog, puis les 15 dernières, puis seulement les lignes 10 à 20.

Afin d'afficher les 5 premières lignes du fichier il faut tappé la commande:
<code> head -5 /var/log/syslog </code></br>
Puis les 15 dernières:
<code> tail -15 /var/log/syslog </code></br>
Enfin les lignes 10 à 20 :
<code> head -n 10 /var/log/syslog | tail -n 20 </code></br>

### 15) Que fait la commande dmesg | less ?
La commande dmesg | less permet de voir la mémorie tampon utilisé par le noyau pour les messages (Page par page).

### 16) Affichez à l’écran le fichier /etc/passwd ; que contient-il ? Quelle commande permet d’afficher la page de manuel de ce fichier ?
Le fichier /etc/passwd contient tout ce qui concernent les utilisateurs (par ex: login, mot de passe...).</br>
La commande qui permet d'afficher la page de manuel de ce fichier est: <code>man passwd </code>.</br>

### 17) Affichez seulement la première colonne triée par ordre alphabétique inverse
Afin d'afficher la première colonne triée apr ordre alphabetique inverse, il faut tapper:
<code>sort +0 -r /etc/passwd</code></br>

### 18) Quelle commande nous donne le nombre d’utilisateurs ?
Pour voir le nombre d'utilisateurs il faut tapper la commande:
<code>wc -l /etc/passwd</code></br>

### 19) Combien de pages de manuel comportent le mot-clé conversion dans leur description ?
Après avoir tappé la commande: 
<code>man -k conversion </code> on voit que le mot-clé conversion apparait dans 4 pages de manuel.</br>

### 20) A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine
Pour celà, il suffit de tapper la commande: 
<code>find / -name passwd </code></br>

### 21) Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier ~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial /dev/null
Il faut pour cela tapper la commande:
<code>find / -name passwd > ~/list_passwd_files.txt 2>> /dev/null </code></br>

### 22) Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu précédemment
Apres avoir tappé la commande: 
<code>grep ll </code> on sait que l'alias ll est defini dans les options de grep. (Marqué grep[Option])</br>

### 23) Utilisez la commande locate pour trouver le fichier history.log
Après avoir tapper la commande: 
<code>locate history.log</code></br>
Le fichier history.log apparait selon le chemin suivant: /var/log/apt/history.log. </br>

### 24) Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il ? Pourquoi ?
Une fois le dossier créer, lorsque l'on essaye de le localiser il n'apparait pas.






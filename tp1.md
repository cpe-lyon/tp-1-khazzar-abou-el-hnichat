Question 1 :  
*A l’aide du manuel, identifiez le rôle de la commande which*  
**ca renvoie le chemin des fichiers executé dans l'environnement courant si ces arguments ont été données dans un interpréteur de commande**

Question 2 :  
*Quand on consulte une page du manuel, comment peut-on rechercher un terme (par exemple, chercherle termeoptiondans la page de manuel dewhich?*  
**pour chercher dans le manuel on fais le man ensuite dessus on fait le /avec le mot qu'on cherche et ensuite n pour passer au prochain mot trouvé et majuscule n pour revenir en arrière**  

Question 3 :  
*Comment quitte-t-on le manuel?*  
**on quitte le manuel en faisant q**  

Question 4 :
*Chaque sectiondu manuel a une première page, qui présente le contenu de la section. Aﬀicher lapremière page de la section 6; de quoi parle cette section?*  
**on doit faire man 6 intro et on retrouve des info sur eux, économiseurs d’écran, gadgets...**  

  
Navigation dans l’arborescence des fichiers1    
1.*allez dans le dossier /var/log*  **cd /var/lo**
2.*remontez dans le dossier parent (/var) en utilisant un chemin relatif* **cd ..**  
3.*retournez dans le dossier personnel*
**cd ~ ou cd $HOME**
4. *revenez au dossier précédent (/var)sans utiliser de chemin*
**cd -**
5.*essayez d’accéder au dossier /root; que se passe-t-il?*
**L'ordinateur a refusé car je ne possède pas les droits de lecture**  
6.*essayez la commande sudo cd /root; que se passe-t-il? Expliquez*  
**Il a refusé car cd est une commande et non un programme, il faut élever ses droits en faisant sudo -i et ensuite faire la commande**  
7.*à partir de votre dossier personnel, créez l’arborescence suivante:*  
**mkdir Dossier1 + cd Dossier1/ + touch Fichier1 + cd ~
mkdir Dossier2/ + cd Dossier2/ + mkdir Dossier2.1 + cd .. + mkdir Dossier2.2 + cd Dossier2.2 + touch Fichier2.1 + touch Fichier2.2 (pour consulter le résultat la cmd tree**  
8.*revenez dans votre dossier personnel; à l’aide de la commande rm, essayez de supprimer Fichier1, puisDossier1; que se passe-t-il?*  
**Le Fichier1 n'a pas pu etre supprimé car on est pas dans son repertoire (Dossier1); et le dossier1 non car c'est un repertoire et il faut utiliser la commande rmdir**  
9.*quelle commande permet de supprimer un dossier?*  
**rmdir**  
10.*que se passe-t-il quand on applique cette commande à Dossier2?*  
**On ne peut pas car le dossier n'est pas vide**  
11.*comment supprimer en une seule commande Dossier2 et son contenu?*  
**rmdir -r** 
**COMMANDES IMPORTANTES**  
1.*Quelle commande permet d’aﬀicher l’heure? A quoi sert la commandetime?*  
**date et la commande time permet d'afficher le temps d'execution d'une certaine commande**  
2.*Dans votre dossier personnel, tapez successivement les commandes ls puis la; que peut-on en déduire sur les fichiers commençant par un point?*  
**ls affiche les fichiers et dossier non cachés alors que la permet d'afficher aussi les fichier commencant par un point qui sont des fichier caché cela permet de dissimuler des éléments permet de protéger des fichiers de manipulations involontaires et d’alléger l’affichage des dossiers dans lesquels ils sont stockés.**  
3.*Où se situe le programme ls?*
**Dans le dossier /bin**
4.*Essayez la commande ll. Existe-t-il une entrée de manuel pour cette commande? Utilisez les commandes alias ou alias pour en savoir plus sur la nature de cette commande.*
**non il n'existe pas de manuel pour ll; cette commande correspond a la commande ls -alF qui permet d'afficher les contenants du dossier ou l'on se trouve avec leurs droits,taille,créateur,date+heur de création,nom**  
5.*Quelle commande permet d’aﬀicher les fichiers contenus dans le dossier/bin?*  
**ls /bin**  
6.*Que fait la commande ls ..?*  
**Ca affiche le contenu du repertoire d'avant**  
7.*Quelle commande donne le chemin complet du dossier courant?*  
**La commande est pwd**  
8.*Que fait la commande echo 'yo' > plop exécutée 2 fois?*  
**ca créé un fichier plop avec le mot yo ecrit a la premiere ligne, la deuxieme execution remplace le yo par un yo donc le fichier reste inchangé**  
9.*Que fait la commande echo 'yo' >> plop exécutée 2 fois?*  
**ca cree un fichier plop avec yo et ansuite la deuxieme execution ajoute a la ligne le mot yo tout cela grâce au '>>'**  
10.*A quoi sert la commande file? Essayez la sur des fichiers de types différent*  
**Il affiche le type de contenu du fichier**  
11.*Créez un fichier toto qui contient la chaîne Hello Toto !; créer ensuite un lien titi vers ce fichier avec la commande ln toto titi. Modifiez à présent le contenu de toto et aﬀichez le contenu de titi:qu’observe-t-on? Supprimez le fichiertoto; quelle conséquence cela a-t-il sur titi?*  
**echo 'Hello Toto !' > toto, ensuite, ln toto titi, lorsque l'on modifie le fichier toto, le fichier titi est automatiquement modifié, lorsque tot est supprimé alors titi n'est pas impacté**  
12.*Créez à présent un lien symbolique tutu sur titi avec la commandeln -s titi tutu. Modifiez lecontenu detiti; quelle conséquence pourtutu? Et inversement? Supprimez le fichiertiti; quelleconséquence cela a-t-il surtutu?*  
**tutu se met a jour lors de la modification de titi; pareille pour l'inverse, lorsqu'on supprime titi, tutu devient vide**  
13.*Aﬀichez à l’écran le fichier/var/log/syslog. Quels raccourcis clavier permettent d’interrompre et reprendre le défilement à l’écran?*  
**pour interrompre l'écran Ctrl+s et pour reprendre Ctrl+q**  
14.*Aﬀichez les 5 premières lignes du fichier/var/log/syslog, puis les 15 dernières, puis seulement leslignes 10 à 20*  
**Pour aﬀichez les 5 premières lignes du fichier/var/log/syslog: head -n 5  ''/var/log/syslog''; et les 15 dernieres: tail -n 15 ''/var/log/syslog'' et enfin pour afficher les lignes 10 à 20 : head -n 10 /var/log/syslog | tail-n 20 /var/log/syslog**  
15.*Que fait la commande dmesg | less?*  
**Afficher page par page le tampon des messages du noyau: dmesg affiche le tampon et less page par page**  
16.*Aﬀichez à l’écran le fichier/etc/passwd; que contient-il? Quelle commande permet d’aﬀicher la pagede manuel de ce fichier?*  
**il contient tout les utilisateurs du sytème avec 
    nom de l'utilisateur pour l'identification sur le système (login),
    mot de passe crypté,
    numéro d'utilisateur (uid),
    numéro de groupe d'utilisateur par défaut (gid). Tout utilisateur est affecté à un et un seul groupe de base. Il peut, par ailleurs, faire partie d'un grand nombre d'autres groupes.
    nom complet ; ce champ peut contenir de nombreuses informations, il correspond à un champ de remarque,
    répertoire de base de l'utilisateur,
    programme à lancer au démarrage (programme de base), généralement un interpréteur de commande (shell). La durée de vie de ce processus correspond à celle de la session utilisateur, c'est à dire que la session de l'utilisateur se terminera avec le processus. Il est possible de préciser ici tout type de programme, ce qui permet de limiter le champ d'action d'un utilisateur (en le connectant directement au programme qu'il doit utiliser, par exemple).**  
17.*Aﬀichez seulement la première colonne triée par ordre alphabétique inverse*  












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

  
*Navigation dans l’arborescence des fichiers1*  
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
8.





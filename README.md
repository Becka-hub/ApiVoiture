Bonjour j'ai n'est pas mis du react dans ce projet car j'ai n'ais pas eu beaucoup de temps pour apprendre du react et faire le test en même temps ,
mais j'ai fini l'api rest pour les fonctionner demander

# Test React Symfony

-J'ai utiliser Symfony 5.3.12
-Lexik/JWT 2.14 pour l'authentification


## Tables

J'ai utilisé 3 tables pour cet api rest

-Car:
   id,name,mark,number
   
-User:
   id,email,password
   
-Comment:
   id,comment,fk_car,fk_user

## Structure

Src:

   -Controller:
              Auth:
                   -AuthController = controlleur pour l'authentification
              Secure:
                   -CarController = controller pour le table car
                   -CommentController = controller pour la table comment
              Full:
                   -FullControlleur = controlleur pour la table car
                   
   -Service:
              -service = un fichier qui contient des services des controllers
              
   -Shared:   
              -Message = un fichier qui contient des messages pour chaques controllers
              -Reponses = Un fichier qui contient des reponses pour chaques controllers
              
   -DataFixtures:
              -AppFixtures= Un fichier qui contient un fixture pour la table car
              
              
              
## URL

 -Dans AuthController:
 
   -127.0.0.1:8000/auth/login = Pour le connexion des utilisateurs
   -127.0.0.1:8000/auth/register = Pour le registrement des utilisateurs
   
   
 -Dans FullControlleur:
 
   -127.0.0.1:8000/full/car = Pour afficher les cars pour les utilisateurs non connecter
   
   
 -Dans CarController: ses url a besion d'un token
 
   -127.0.0.1:8000/api/car/carList = Pour afficher les cars pour les utilisateurs connectés
   -127.0.0.1:8000/api/car/carSingle/{id} = Pour afficher un seul car pour les utilisateurs connectés
   
 
 -Dans CommentController: ses url a besion d'un token
 
   -127.0.0.1:8000/api/comment/commentList = Pour afficher les comments pour les utilisateur connecter
   -127.0.0.1:8000/api/comment/commentSingle/{id} = Pour afficher un seul comment pour les utilisateurs connectés
   -127.0.0.1:8000/api/comment/commentSave = Pour l'ajout des comments pour les utilisateurs connectés
   -127.0.0.1:8000/api/comment/commentDelete/{id} = Pour la supression des comments pour les utilisateurs connectés
   
   
 
   

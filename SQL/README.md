
# SQL Injection

## Définition
Une SQL Injection permet d'injecter du SQL dans une requête non sécurisée.

## Exemple vulnérable
    ```php
    $login = $_POST["login"];
    $query = "SELECT * FROM users WHERE login = '$login'";
Un attaquant peut entrer :
' OR '1'='1

## Correction (requêtes préparées)
    $stmt = $pdo->prepare("SELECT * FROM users WHERE login = ?");
    $stmt->execute([$login]);
    
## Contre-mesures
- Utiliser des requêtes préparées
- Ne jamais concaténer les entrées utilisateur
- Limiter les permissions SQL
  

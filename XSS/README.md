# XSS (Cross-Site Scripting)

## Définition
Le XSS permet à un attaquant d'injecter du JavaScript malveillant dans une page web.

## Exemple vulnérable
    <input type="text" name="msg">
    <p>Message : <?php echo $_GET["msg"]; ?></p>
Si l'utilisateur entre :

    <script>alert("XSS")</script>
Le script s'exécute.

## Correction
    echo htmlspecialchars($_GET["msg"]);
    
## Contre-mesures
- Échapper toutes les entrées utilisateur
- Utiliser htmlspecialchars()
- Filtrer les tags <script>
- Utiliser un CSP (Content Security Policy)

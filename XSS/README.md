# XSS (Cross-Site Scripting)

## Définition
Le XSS permet à un attaquant d'injecter du JavaScript malveillant dans une page web.

## Exemple vulnérable
```html
<input type="text" name="msg">
<p>Message : <?php echo $_GET["msg"]; ?></p>

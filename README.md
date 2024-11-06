<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hello World</title>
</head>
<body>

<h1>Hello World!</h1>

<script>
var pageTitle = document.title; // Stocke le titre de la page original

// Fonction appelée lorsque la fenêtre perd le focus (l'utilisateur change d'onglet)
function handleTabBlur() {
  document.title = 'Revient!'; // Change le titre quand l'utilisateur quitte l'onglet
}

// Fonction appelée lorsque la fenêtre récupère le focus (l'utilisateur revient à l'onglet)
function handleTabFocus() {
  document.title = pageTitle; // Rétablit le titre original quand l'utilisateur revient
}

// Écouteur d'événements pour détecter lorsque la fenêtre perd le focus
window.addEventListener('blur', handleTabBlur);

// Écouteur d'événements pour détecter lorsque la fenêtre récupère le focus
window.addEventListener('focus', handleTabFocus);
</script>

</body>
</html>

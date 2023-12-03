# PHP-dans-un-fichier-HTML
<!DOCTYPE html>
<html>
<head>
  <style>
    p {
      margin: 0;
    } </style>
</head>
<body>
<?php
  // Tableau associatif d'utilisateurs avec leurs informations
  $tab = [[56, 12], [5, 26]];
  $utilisateurs = [
      ["nom" => "Marie", "age" => 23, "couleur" => "rouge"],
      ["nom" => "Fatou", "age" => 22, "couleur" => "rose"],
      ["nom" => "Anta", "age" => 21, "couleur" => "vert"]
  ];

  // Parcourir le tableau des utilisateurs
  echo "<br>AFFICHAGE AVEC BOUCLE FOREACH<br>";
  foreach ($utilisateurs as $utilisateur) {
      $nom = $utilisateur["nom"];
      $age = $utilisateur["age"];
      $couleur = $utilisateur["couleur"];

      // Convertir la couleur en anglais pour le CSS
      $colorStyle = "";
      switch ($couleur) {
          case "rouge":
              $colorStyle = "red";
              break;
          case "rose":
              $colorStyle = "pink";
              break;
          case "vert":
              $colorStyle = "green";
              break;
          default:
            // On ne connait pas cette couleur
            break;
      }

      // Afficher le message de bienvenue
      echo "<p>Bonjour $nom, tu as $age ans et ta couleur est le <span style=\"color:$colorStyle\">$couleur</span>.<p>";
  }

  echo "<br>AFFICHAGE AVEC BOUCLE WHILE<br>";
  $index = 0;
  while ($index < count($utilisateurs)) {
    $utilisateur = $utilisateurs[$index];

    $nom = $utilisateur["nom"];
    $age = $utilisateur["age"];
    $couleur = $utilisateur["couleur"];

    // Convertir la couleur en anglais pour le CSS
    $colorStyle = "";
    switch ($couleur) {
        case "bleu":
            $colorStyle = "blue";
            break;
        case "rouge":
            $colorStyle = "red";
            break;
        case "vert":
            $colorStyle = "green";
            break;
    }

    echo "Bonjour $nom, tu as $age ans et ta couleur est le <span style=\"color:$colorStyle\">$couleur</span>.<br>";

    $index++;
  }

  echo "<br>AFFICHAGE AVEC BOUCLE FOR<br>";
  for ($i = 0; $i < count($utilisateurs); $i++) {
    $utilisateur = $utilisateurs[$i];
    $nom = $utilisateur["nom"];
    $age = $utilisateur["age"];
    $couleur = $utilisateur["couleur"];

    // Convertir la couleur en anglais pour le CSS
    $colorStyle = "";
    switch ($couleur) {
        case "bleu":
            $colorStyle = "blue";
            break;
        case "rouge":
            $colorStyle = "red";
            break;
        case "vert":
            $colorStyle = "green";
            break;
    }

    // Afficher le message de bienvenue
    echo "Bonjour $nom, tu as $age ans et ta couleur est le <span style=\"color:$colorStyle\">$couleur</span>.<br>";
  }

?>
</body>
</html>

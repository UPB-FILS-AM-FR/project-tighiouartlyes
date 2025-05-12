<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
</head>
<body>

<h2>Projet Arduino : Contrôle d'un Moteur Pas à Pas avec LEDs et Potentiomètre</h2>
<h3> Nom : TIGHIOUART</h3> <h3> Prénom : Lyes</h3>

<h3>1. Description du Projet</h3>
<p>Ce projet a pour but de contrôler la vitesse d’un moteur pas à pas (28BYJ-48) à l’aide d’un potentiomètre connecté à une carte Arduino UNO.
  Trois LEDs (rouge, jaune, verte) sont utilisées pour afficher visuellement la plage de vitesse du moteur : faible, moyenne et élevée.</p>
<p>Le potentiomètre permet à l’utilisateur de faire varier une tension analogique que l’Arduino convertit en valeur de vitesse.
  Cette vitesse est ensuite transmise au moteur via le module ULN2003, qui agit comme interface de puissance.
  Les LEDs s’allument automatiquement en fonction de la vitesse détectée.</p>

<h3>2. Motivation du Projet</h3>
<ul>
  <li>Comprendre le fonctionnement d’un moteur pas à pas.</li>
  <li>Apprendre à utiliser un potentiomètre pour un contrôle analogique.</li>
  <li>Visualiser des données physiques (vitesse) par un système lumineux simple.</li>
  <li>S’initier à l’interconnexion entre composants (driver, moteur, LEDs).</li>
</ul>


<h3>3. Architecture Fonctionnelle</h3>
<p>Le système est divisé en trois parties principales :</p>
<ul>
  <li><strong>Entrée utilisateur</strong> : potentiomètre</li>
  <li><strong>Traitement</strong> : Arduino UNO (lecture analogique, calcul vitesse, commande LEDs)</li>
  <li><strong>Sortie</strong> : moteur pas à pas via ULN2003 + LEDs pour affichage</li>
</ul>

<pre>
[ Potentiomètre ] --(analogique)--> [ Arduino UNO ]
                                   |--> [ LED indicatrices ]
                                   |--> [ ULN2003 Driver ] --> [ Moteur 28BYJ-48 ]
</pre>
<h3>4. Composants Utilisés</h3>
<table>
  <thead>
    <tr>
      <th>Composant</th>
      <th>Quantité</th>
      <th>Rôle</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Arduino UNO</td><td>1</td><td>Microcontrôleur central</td></tr>
    <tr><td>Moteur pas à pas 28BYJ-48</td><td>1</td><td>Actionneur de mouvement</td></tr>
    <tr><td>ULN2003 Driver</td><td>1</td><td>Interface entre Arduino et moteur</td></tr>
    <tr><td>Potentiomètre 10kΩ</td><td>1</td><td>Contrôle de vitesse analogique</td></tr>
    <tr><td>LED rouge</td><td>1</td><td>Indicateur vitesse faible</td></tr>
    <tr><td>LED jaune</td><td>1</td><td>Indicateur vitesse moyenne</td></tr>
    <tr><td>LED verte</td><td>1</td><td>Indicateur vitesse élevée</td></tr>
    <tr><td>Résistances 220Ω</td><td>3</td><td>Limitation de courant LEDs</td></tr>
    <tr><td>Breadboard</td><td>1</td><td>Montage sans soudure</td></tr>
    <tr><td>Fils Dupont (M-M) et (M-F)</td><td>17</td><td>Connexions internes</td></tr>
    <tr><td>Câble USB</td><td>1</td><td>Programmation + alimentation Arduino</td></tr>
  </tbody>
</table>

</body>
</html>

Déclaration des constantes :
apiKey : C’est la clé API pour accéder à l’API OpenWeatherMap.
apiUrl : C’est l’URL de base de l’API OpenWeatherMap.
searchBox, searchBtn, weatherIcon : Ce sont des références à des éléments HTML sur la page. searchBox est la zone de texte où vous tapez le nom de la ville, searchBtn est le bouton pour lancer la recherche, et weatherIcon est l’endroit où l’icône météo sera affichée.
Fonction checkWeather(city) : Cette fonction est appelée lorsque vous cliquez sur le bouton de recherche. Elle prend en paramètre le nom de la ville que vous avez tapé dans la zone de texte.
Elle commence par faire une requête à l’API OpenWeatherMap avec le nom de la ville et la clé API.
Si la réponse a un statut 404 (ce qui signifie que la ville n’a pas été trouvée), elle affiche un message d’erreur et cache les informations météo.
Si la réponse est valide, elle convertit la réponse en JSON et utilise ces données pour mettre à jour les informations météo sur la page.
Gestion des icônes météo : Selon le temps qu’il fait (nuageux, clair, pluvieux, etc.), une icône différente est affichée. Les icônes sont stockées dans le dossier “images”.
Écouteur d’événements : Un écouteur d’événements est ajouté au bouton de recherche. Lorsque vous cliquez sur le bouton, la fonction checkWeather est appelée avec la valeur actuelle de la zone de texte.
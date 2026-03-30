# tp-docker-image

En faisant les tests, on remarque que le multistage est moins lourd que le classic.
L'image classic pèse environ 1.1G0 et l'image multistage pèse environ 240Mo.

Le multi-stage est plus léger car on utilise slim comme image finale qui est une version allégée de node. Ensuite avec npm ci --omit=dev on installe uniquement les dépendances nécessaires pour faire tourner l'application.

Pour optimiser encore plus on pourrait utiliser alpine à la place de slim pour être encore plus léger.

Déployer son site Gatsby-Ghost avec Docker et Traefik
= 

Article et explication : https://www.grottedubarbu.fr/gatsby-ghost-docker-traefik/

1. Cloner le dépôt

2. Lancer Traefik et Ghost :
`docker-compose up -d traefik && docker-compose up -d ghost_cms`

3. Récupérer votre clé API Ghost.

4. Modifier `gatsby/.ghost.json`

5. Lancer le site statique :
`docker-compose up -d ghost_static`
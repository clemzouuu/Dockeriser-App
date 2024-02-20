# Étape de construction
FROM node:lts

# Définition du répertoire de travail dans le conteneur
WORKDIR / .

# Copie de tous les fichiers dont les dépendances  
COPY / .
RUN npm install

# Construction de l'application
RUN npm run build
EXPOSE 3000
CMD ["node", "build"]

#SvelteKit fourni un serveur web, donc est "suffisant". Est utile jusqu'au déploiement de l'app
#Utile de rajouter ngnix pour les performances, peut gérer plusieurs clients, pour la sécurité (limitation du taux de requêtes,gère les certificats ssl), pour la production


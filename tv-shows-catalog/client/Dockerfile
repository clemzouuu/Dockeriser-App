# Étape de construction 
FROM node:lts-alpine

# Définition du répertoire de travail dans le conteneur
WORKDIR / app

# Copie de tous les fichiers dont les dépendances 
COPY . .
RUN npm install

# Construction de l'application
RUN npm run build
EXPOSE 3000
CMD ["node", "build"]


#Utile de rajouter ngnix pour les performances, peut gérer plusieurs clients, pour la sécurité (limitation du taux de requêtes,gère les certificats ssl), pour la production


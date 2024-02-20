# Étape de construction
FROM node:lts  

# Définition du répertoire de travail
WORKDIR / .

# Installation des dépendances
COPY /package*.json ./
RUN npm install

# Copie des fichiers sources de l'application dans l'image
COPY / .

# Construction de l'application
RUN npm run build

# Exposition du port 3000
EXPOSE 3000

CMD ["node", "dist/main"]

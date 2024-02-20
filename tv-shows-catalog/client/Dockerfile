# Étape de construction
FROM node:lts

# Définition du répertoire de travail dans le conteneur
WORKDIR / .

# Copie des fichiers de dépendances et installation
COPY package*.json ./
RUN npm install

# Copie du reste des fichiers sources de l'application
COPY / .

# Construction de l'application
RUN npm run build

EXPOSE 3000

CMD ["node", "build"]



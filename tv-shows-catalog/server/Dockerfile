# Étape de construction
FROM node:lts  

# Définition du répertoire de travail
WORKDIR / .

# Copie de tous les fichiers dont les dépendances  
COPY / .
RUN npm install

# Construction de l'application
RUN npm run build
EXPOSE 3000
CMD ["node", "dist/main"]

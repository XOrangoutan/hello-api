# 1. Image de base légère
FROM node:20-slim

# 2. Répertoire de travail dans le conteneur
WORKDIR /app

# 3. Copie des fichiers de dépendances (optimisation du cache Docker)
COPY package*.json ./

# 4. Installation des dépendances (uniquement prod pour être léger)
RUN npm install --production

# 5. Copie du reste du code source
COPY . .

# 6. Exposition du port utilisé par l'API
EXPOSE 3000

# 7. Commande de lancement
CMD ["node", "index.js"]
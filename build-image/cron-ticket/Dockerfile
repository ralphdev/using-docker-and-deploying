FROM node:current-alpine3.18

#cd app
WORKDIR /app

# Destino a /app
COPY app.js package.json ./

# Instalar Dependencias
RUN npm install

# Comando Run de la Imagen
CMD ["node", "app.js"]
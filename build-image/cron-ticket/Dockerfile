FROM node:current-alpine3.18

#cd app
WORKDIR /app

# Destino a /app
COPY app.js package.json ./

# Instalar Dependencias
RUN npm install

COPY . .

# Realizar Test
RUN npm run test

# Eliminar archivos y directorios no necesarios en Prod
RUN rm -rf tests/ && rm -rf node_modules/

# Instalar unicamente dependencias de prod
RUN npm install --prod

# Comando Run de la Imagen
CMD ["node", "app.js"]
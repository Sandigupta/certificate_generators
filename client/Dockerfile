FROM node:22

WORKDIR /app

# Install ping (iputils-ping)
RUN apt-get update && apt-get install -y iputils-ping && rm -rf /var/lib/apt/lists/*

COPY package*.json .

RUN npm install 

COPY . . 
EXPOSE 5173

CMD ["npm", "dev"]
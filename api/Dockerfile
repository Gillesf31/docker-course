FROM node:22-alpine

RUN npm install -g nodemon

WORKDIR /app

COPY package*.json .

RUN npm install

COPY . .

# EXPOSE sets metadata only; it declares that the container listens on port 4000 but does not publish it at runtime.
# Use `docker run -p 4000:4000` to actually map the port.
EXPOSE 4000

CMD ["npm", "run", "dev"]
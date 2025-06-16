FROM node:22-alpine

WORKDIR /app

COPY package*.json .

RUN npm install

COPY . .

# EXPOSE sets metadata only; it declares that the container listens on port 4000 but does not publish it at runtime.
# Use `docker run -p 4000:4000` to actually map the port.
EXPOSE 4000

CMD ["node", "app.js"]
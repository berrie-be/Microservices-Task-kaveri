FROM node:24-alpine3.22
WORKDIR /app
COPY package* .
RUN npm install
COPY . .
ENV PORT=3001
EXPOSE 3001
CMD ["node","app.js"]
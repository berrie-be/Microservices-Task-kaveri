FROM node:24-alpine3.22
WORKDIR /app
COPY package* .
RUN npm install
COPY . .
ENV PORT=3000
EXPOSE 3000
CMD ["node","app.js"]
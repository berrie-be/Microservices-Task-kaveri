FROM node:24-alpine3.22
WORKDIR /app
COPY package* .
RUN npm install
COPY . .
ENV PORT=3003
EXPOSE 3003
CMD ["node","app.js"]
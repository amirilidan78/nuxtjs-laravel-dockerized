# ------------------ Production image ------------------ #

FROM node:14 as prod

WORKDIR /app/nuxtjs

COPY package.json .

RUN npm install --only=production && npm cache clean --force

COPY . .

ENV HOST=0.0.0.0

ENV PORT=3000

RUN npm run build

ENV APP_ENV = "production"

CMD [ "npm" ,"run" , "start" ]

# ------------------ Development image ------------------ #

FROM prod as dev

RUN npm install --only=development && npm cache clean --force

ENV APP_ENV = "development"

CMD [ "npm" ,"run" ,"dev" ]

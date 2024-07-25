FROM node:20.5.0-alpine3.18
RUN addgroup nodeapp && adduser -S -G nodeapp nodeapp
WORKDIR /app/
RUN chown -R nodeapp:nodeapp /app
USER nodeapp
COPY --chown=nodeapp package*.json ./
RUN npm install
COPY --chown=nodeapp . .
EXPOSE 3000
CMD ["npm", "start"]
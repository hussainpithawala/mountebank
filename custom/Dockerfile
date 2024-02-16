FROM node:18-alpine

WORKDIR /mountebank

COPY . /mountebank

RUN npm install

# Run as a non-root user
RUN adduser -D mountebank
RUN chown -R mountebank /mountebank
USER mountebank
RUN cd /mountebank

EXPOSE 2525

ENTRYPOINT ["npx","mb"]


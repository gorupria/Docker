FROM node:latest 

WORKDIR /mydir
COPY / .
RUN npm install

EXPOSE 8000 
CMD FRONT_URL=http://localhost:5000 npm start 

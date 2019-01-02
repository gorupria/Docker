FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl
COPY script.sh .
RUN ["chmod", "+x", "./script.sh"]
CMD ["/bin/sh", "./script.sh"] 

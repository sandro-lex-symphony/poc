FROM ubuntu:18.04
RUN apt-get update
RUN apt-get install -y nginx vim curl wget 
RUN unlink /etc/nginx/sites-enabled/default
COPY rproxy.conf /etc/nginx/sites-available/rproxy.conf
RUN ln -s /etc/nginx/sites-available/rproxy.conf /etc/nginx/sites-enabled/rproxy.conf
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]

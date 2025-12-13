FROM nginx
RUN rm -rf /usr/share/nginx/html/index.html
RUN rm -rf /etc/ngnix/nginx.conf
COPY nginx.conf /etc/ngnix/nginx.conf
COPY code /usr/share/nginx/html/

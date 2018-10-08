FROM nginx:1.13.3

ENV X_PROXY_NAME  dev.slyak.com

COPY index.html /opt/data/nginx/
COPY nginx.conf.tmpl /etc/nginx/
COPY altassian.conf.tmpl /etc/nginx/conf.d/
COPY "docker-entrypoint.sh" "/"

#RUN printf "ttlsa:$(openssl passwd -crypt 123456)\n" >>conf/htpasswd

VOLUME ["/usr/share/nginx/html","/etc/nginx/conf.d","/opt/data/nginx"]
ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["nginx", "-g", "daemon off;"]
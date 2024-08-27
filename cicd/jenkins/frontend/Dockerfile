FROM  nginx:latest
EXPOSE 80
COPY /var/lib/jenkins/workspace/test/frontend/dist /usr/share/nginx/html
CMD nginx -g "daemon off;"
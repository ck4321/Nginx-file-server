# Nginx-file-server
nginx docker container to serve a folder with password

# create password 
sudo htpasswd .htpasswd username

# Run nginx
docker run -d --name=nginx -p 7777:80 -v /absoulte path/foldertoserve:/var/www/html -v /absolutepath/nginx.conf:/etc/nginx/conf.d/default.conf -v /absolutepath/.htpasswd:/etc/nginx/.htpasswd nginx

#access the server
ip.add.rr.ss:7777

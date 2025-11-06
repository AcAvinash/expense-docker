FROM nginx:mainline-alpine3.20-slim

# RUN rm -rf /etc/nginx/nginx.conf && \
#     rm -rf /etc/nginx/conf.d/default.conf && \
#     mkdir -p /var/cache/nginx/client_temp && \
#     mkdir -p /var/cache/nginx/proxy_temp && \
#     mkdir -p /var/cache/nginx/fastcgi_temp && \
#     mkdir -p /var/cache/nginx/uwsgi_temp && \
#     mkdir -p /var/cache/nginx/scgi_temp && \
#     chown -R nginx:nginx /var/cache/nginx && \
#     chown -R nginx:nginx /etc/nginx/ && \
#     chmod -R 755 /etc/nginx/ && \
#     chown -R nginx:nginx /var/log/nginx && \
#     touch /var/run/nginx.pid && \
#     chown -R nginx:nginx /var/run/nginx.pid /run/nginx.pid
# COPY nginx.conf /etc/nginx/nginx.conf
# COPY code /usr/share/nginx/html
# USER nginx




# 2️⃣ Remove default HTML and configs
RUN rm -rf /usr/share/nginx/html/* \
    && rm -rf /etc/nginx/nginx.conf \
    && rm -rf /etc/nginx/conf.d/default.conf

# 3️⃣ Copy custom Nginx config
COPY nginx.conf /etc/nginx/nginx.conf

# 4️⃣ Copy frontend static files
COPY code /usr/share/nginx/html/

# 5️⃣ Expose port 80
EXPOSE 80

# 6️⃣ Start Nginx server
CMD ["nginx", "-g", "daemon off;"]



FROM nginx
RUN rm -rf /usr/share/nginx/html/* 
# COPY index.html /usr/share/nginx/html/
COPY code /usr/share/nginx/html/
# COPY nginx.conf /etc/nginx/nginx.conf
COPY expense.conf /etc/nginx/default.d/expense.conf
# Expose port 80
EXPOSE 80
# Run nginx
# CMD ["nginx", "-g", "daemon off;"]
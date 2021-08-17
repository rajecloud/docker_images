# Build a small nginx image with static website
FROM nginx:alpine

## Remove default nginx website
RUN rm -rf /usr/share/nginx/html/*

## From 'builder' copy website to default nginx public folder
COPY --from=builder /app/dist /usr/share/nginx/html

## Copy Nginx config file
COPY default.conf /etc/nginx/conf.d/

# Expose container on Port 80
EXPOSE 80

# Start Nginx command 
CMD ["nginx", "-g", "daemon off;"]

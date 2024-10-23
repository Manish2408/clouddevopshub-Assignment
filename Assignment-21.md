## Create a Dockerfile. 📝 - Build your own custom Nginx application image. 🛠️ - Tag and push the image to Docker Hub. 

## Dockerfile
~~~
# Use the official Nginx image from Docker Hub
FROM nginx:latest

# Author information (optional)
LABEL maintainer="manish_test@gmail.com"

# Copy your custom HTML file to the default Nginx html directory
COPY ./oxer/ /usr/share/nginx/html/

# Declare a volume to persist changes to /usr/share/nginx/html (where Nginx serves files from)
VOLUME ["/usr/share/nginx/html"]

# Expose port 80 (Nginx default port)
EXPOSE 80

# Start Nginx when the container launches
CMD ["nginx", "-g", "daemon off;"]
~~~

## Screenshots

![image](https://github.com/user-attachments/assets/9a6f6ca3-b801-49c7-a8e5-86d254a93293)


![image](https://github.com/user-attachments/assets/73a1bdf0-418b-4271-b2f2-4445ed9be624)


![image](https://github.com/user-attachments/assets/450e2074-9abf-4ba0-a84c-90218104baa4)


![image](https://github.com/user-attachments/assets/8d31d885-1df6-4f47-8891-644c8b3a8ad6)

![image](https://github.com/user-attachments/assets/0d1caf31-8fb3-4c5e-a0ed-4774643a0d88)




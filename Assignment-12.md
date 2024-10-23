# Push Code from Local to GitHub 📤 Follow the best workflow to push Code as a Developer.
##Commands Used:
~~~
git init
git config --global user.name "Manish"
git config --global user.email "manish_test@gmail.com"
git add . #after editing the use this command
git commit -m "<Comment>"
git remote add origin https://github.com/Manish2408/spring-petclinic.git
git push -u origin main
~~~
## GitHub credentials (username and password or personal access token) during the push.
### Push Code Using a Personal Access Token (PAT)
Generate a Personal Access Token (PAT):

1. Go to GitHub and log in.
Navigate to Settings → Developer settings → Personal access tokens → Tokens (classic).
Click on Generate new token.
Select the scopes/permissions you want (at least repo for full control of private repositories).
Click Generate token and copy the token (you won’t see it again after you leave the page).
2. Update Git to Use the Token:
When you push your code, instead of using your password, you’ll use the Personal Access Token as the password.
### Screenshots
![image](https://github.com/user-attachments/assets/19dd062d-6b56-4e2e-a650-3c07eec4f07f)

![image](https://github.com/user-attachments/assets/c03250e0-238e-49eb-b0fa-2d2189a97486)


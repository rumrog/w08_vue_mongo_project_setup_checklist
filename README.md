# Project Setup Checklist

1. Create `project_name` folder. 
```
mkdir project_name
```
2. Git init
```
git init
```
3. Create .gitignore
```
touch .gitignore
```
4. Add the following to .gitignore
```
client/node_modules/
server/node_modules/
```

## Front-End `/client`

5. Create `client` folder with Vue [`-n` flag to avoid git init]
```
cd project_name
vue create -n client
```

6. Create services folder and ProjectService.js

```
cd client
mkdir src/components/services
touch src/components/services/ProjectService.js
```

## Back-End `/server`

7. On `/project_name`,
create `server` folder. 

```
mkdir server
```
8. Initiate `server`

```
cd server
npm init -y
```

9. Create `db` and `helpers` folders within `server` plus `server.js`
```
mkdir db helpers
touch server.js
```

10. Create `seeds.js` and `create_routers.js` inside `db` and `helpers`

```
touch db/seeds.js helpers/create_routers.js
```

11. Install nodemon
```
npm install -D nodemon
```

12. Install express, mongodb and cors
```
npm install express mongodb cors
```

13. Add the following to /server/package.json

```
"scripts": {
    "start": "node server.js",
    "test": "echo \"Error: no test specified\" && exit 1",
    "server:dev": "nodemon server.js",
    "seeds": "mongo < ./db/seeds.js"
  },
```


## Start Servers

### Server

14. Run express:

```
npm run server:dev
```

### Client

15. Run client server
    
```
npm run serve
```
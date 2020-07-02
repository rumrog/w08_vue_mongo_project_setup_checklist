# Project Setup Checklist

1. Initialize project with Vue
```bash
vue create project_name
```

## Front-End `/client`

2. Create `client` folder
```
cd project_name
mkdir client
```
3. Move the following files to `client`
```
..
mv README.md babel.config.js node_modules package-lock.json package.json public .gitignore src client
```

4. Create services folder and ProjectService.js

```
cd client
mkdir src/components/services
touch src/components/services/ProjectService.js
```

## Back-End `/server`

5. On `/project_name`,
create `server` folder. 

```
mkdir server
```
6. Initiate `server`

```
cd server
npm init -y
```

7. Create `db` and `helpers` folders within `server` plus `server.js`
```
mkdir db helpers
touch server.js
```

8. Create `seeds.js` and `create_routers.js` inside `db` and `helpers`

```
touch db/seeds.js helpers/create_routers.js
```

9. Install nodemon
```
npm install -D nodemon
```

10. Install express, mongodb and cors
```
npm install express mongodb cors
```

11. Add the following to /server/package.json

```
"scripts": {
    "start": "node server.js",
    "test": "echo \"Error: no test specified\" && exit 1",
    "server:dev": "nodemon server.js",
    "seeds": "mongo < ./db/seeds.js"
  },
```

12. Copy .gitignore from `client`

```
cp ../client/.gitignore .
```

## Start Servers

### Server

13. Run express:

```
npm run server:dev
```

### Client

14. Run client server
    
```
npm run serve
```
# Node.js & Passport Login

A secure user login and registration system built with Node.js, Express, Passport.js, and MongoDB. This application features:
- User registration with password hashing (using bcrypt)
- Login/logout functionality with session management
- Protected routes for authenticated users
- MongoDB database integration (via Mongoose)
- Dockerized MongoDB for easy setup
- EJS templating for server-side rendering

### Preview
![home](https://github.com/user-attachments/assets/d221db76-b3af-42eb-94da-20566ad371b1)
![login](https://github.com/user-attachments/assets/95b3f6d9-b68b-4ea1-a036-d970be9e0221)
![register](https://github.com/user-attachments/assets/0bfbba50-3818-4c87-8290-8386278b9617)

### Usage

```sh
$ npm install
```

```sh
$ npm start
# Or run with Nodemon
$ npm run dev

# Visit http://localhost:5000
```

### MongoDB

Open "config/keys.js" and add your MongoDB URI. (I used Docker, but you can use Atlas or others..)

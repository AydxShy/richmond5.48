mkdir backend
cd backend
npm init -y


yarn add express mongoose dotenv cors jsonwebtoken bcryptjs

config/db.js, models/User.js, models/Request.js, server.js

yarn add sqlite3 sequelize sequelize-cli


config.json

npx sequelize-cli init

models/index.js

npx sequelize-cli model:generate --name User --attributes name:string,email:string,password:string,role:string
npx sequelize-cli model:generate --name Request --attributes userId:integer,requestDetail:string,status:string
npx sequelize-cli db:migrate
npx sequelize-cli migration:generate --name add-dates-to-request
npx sequelize-cli db:migrate
npx sequelize-cli migration:generate --name add-leave-days-to-user
npx sequelize-cli db:migrate
npx sequelize-cli migration:generate --name add-phone-and-personnel-number-to-users
npx sequelize-cli db:migrate



mkdir controllers routes middleware
authController.js, requestController.js

routes/  authRoutes.js, requestRoutes.js

middleware/authMiddleware.js

yarn add express dotenv mongoose cors
yarn add bcryptjs
yarn add jsonwebtoken

cd ..
npx create-react-app frontend
cd frontend

yarn add axios react-router-dom bootstrap bootstrap-react react-datepicker


package.json dosyasına proxy atama:
  "proxy": "http://localhost:5000"




cd backend
node server.js

cd frontend
yarn start





















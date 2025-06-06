# This is my Ecommerce Website

Welcome to my React and Node Website fully-functional e-commerce website. 



## To Building this Project I use :-

- HTML5 and CSS3: Semantic Elements, CSS Grid, Flexbox
- React: Components, Props, Events, Hooks, Router, Axios
- Redux: Store, Reducers, Actions
- Node & Express: Web API, Body Parser, File Upload, JWT
- MongoDB: Mongoose, Aggregation
- Development: ESLint, Babel, Git, Github,
- Deployment: Heroku
- Watch React & Node Tutorial

## Run Locally

### 1. Clone repo

```
$ git clone git@github.com:basir/node-react-ecommerce.git
$ cd node-react-ecommerce
```

### 2. Install MongoDB

Download it from here: https://docs.mongodb.com/manual/administration/install-community/

### 3. Run Backend

```
$ npm install
$ npm start
```

### 4. Run Frontend

```
# open new terminal
$ cd frontend
$ npm install
$ npm start
```

### 5. Create Admin User

- Run this on chrome: http://localhost:5000/api/users/createadmin
- It returns admin email and password

### 6. Login

- Run http://localhost:3000/signin
- Enter admin email and password and click signin

### 7. Create Products

- Run http://localhost:3000/products
- Click create product and enter product info

## Support

- Q/A: https://webacademy.pro/oldamazona
- Contact Instructor: [Basir](mailto:basir.jafarzadeh@gmail.com)




### Rate and Review Products

This part shows list of reviews by users for each products. also it provides a form to enter rating and review for every single product. also it update the avg rating of each product by user ratings.

1. index.html
2. link fontawesome
3. Rating.js
4. create stars based on props.value
5. show text based on props.text
6. index.css
7. style rating, span color gold and last span to gray, link text to blue
8. HomeScreen.js
9. use Rating component
10. ProductScreen.js
11. use Rating component, wrap it in anchor#reviews
12. list reviews after product details
13. create new review form to get rating and reviews
14. index.css
15. style reviews
16. ProductScreen.js
17. implement submitHandler
18. productActions.js
19. create saveProductReview(productId, review)
20. productConstants.js
21. create product review constants
22. productReducers.js
23. create productReviewSaveReducer
24. store.js
25. add productReviewSaveReducer
26. backend
27. productRoute.js
28. router.post('/:id/reviews')
29. save review in product.reviews
30. update avg rating

### Upload Product Images On Local Server

Admin shoud be able to uploads photos from their computer. This section is about uploading images on local server ans aws s3 cloud server.

1. npm install multer
2. routes/uploadRoute.js
3. import express and multer
4. create disk storage with Date.now().jpg as filename
5. set upload as multer({ storage })
6. router.post('/', upload.single('image'))
7. return req.file.path
8. server.js
9. app.use('/api/uploads',uploadRoute)
10. ProductsScreen.js
11. create state hook for uploading
12. create input image file and onChange handler
13. define handleUploadImage function
14. prepare file for upload
15. axios post file as multipart/form-data
16. set image and set uploading
17. check result

### Upload Product Images On AWS S3

Section to uploading images amazon aws s3 cloud server.

1. create aws account
2. open https://s3.console.aws.amazon.com
3. create public bucket as amazona
4. create api key and secret
5. past it into .env as accessKeyId and secretAccessKey
6. move dotenv to config.js
7. add accessKeyId and secretAccessKey to config.js
8. npm install aws-sdk multer-s3
9. routes/uploadRoute.js
10. set aws.config.update to config values
11. create s3 from new aws.S3()
12. create storageS3 from multerS3 by setting s3, bucket and acl
13. set uploadS3 as multer({ storage: storageS3 })
14. router.post('/s3', uploadS3.single('image'))
15. return req.file.location
16. ProductsScreen.js
17. on handleUploadImage set axios.post('api/uploads/s3')
18. check result on website and s3

## Summary

In this tutorial, we have made an eCommerce website like Amazon. Feel free to change this project based on your needs and add it to your portfolio.
Also, I will love to hear your comment about this React and Node tutorial. Please share your thoughts here.

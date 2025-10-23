# Express.js Interview Questions & Answers

## 1. What is Express.js?
**Answer:** Express.js is a minimal and flexible Node.js web application framework that provides features for building web and mobile applications.

## 2. Why use Express.js?
**Answer:** Simplifies routing, middleware handling, request and response management, and supports REST API development.

## 3. How to install Express.js?
**Answer:**
```bash
npm install express
```

## 4. How to create a basic Express server?
**Answer:**
```javascript
const express = require('express');
const app = express();

app.get('/', (req, res) => res.send('Hello World'));

app.listen(3000, () => console.log('Server running on port 3000'));
```

## 5. What is middleware in Express?
**Answer:** Functions that execute during the request-response cycle to handle operations like authentication, logging, or body parsing.

## 6. How to use middleware?
**Answer:**
```javascript
app.use(express.json()); // parse JSON body
```

## 7. What are the types of middleware?
**Answer:**
- Application-level
- Router-level
- Built-in
- Error-handling

## 8. How to create routes in Express?
**Answer:**
```javascript
app.get('/users', (req, res) => res.send('Users'));
app.post('/users', (req, res) => res.send('Create User'));
```

## 9. What is router in Express?
**Answer:** Modular, mountable route handler for handling route paths separately.

## 10. How to use Router?
**Answer:**
```javascript
const router = express.Router();
router.get('/', (req, res) => res.send('Home'));
app.use('/home', router);
```

## 11. What is app.use()?
**Answer:** Mounts middleware functions or routers at specified paths.

## 12. What is app.listen()?
**Answer:** Binds and listens for connections on the specified host and port.

## 13. How to handle 404 errors?
**Answer:**
```javascript
app.use((req, res) => {
  res.status(404).send('Not Found');
});
```

## 14. How to handle errors in Express?
**Answer:**
```javascript
app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).send('Something broke!');
});
```

## 15. How to parse request body?
**Answer:** Using built-in middleware:
```javascript
app.use(express.json());
app.use(express.urlencoded({ extended: true }));
```

## 16. What is CORS and how to enable it in Express?
**Answer:** Cross-Origin Resource Sharing allows cross-domain requests. Use `cors` middleware:
```javascript
const cors = require('cors');
app.use(cors());
```

## 17. How to serve static files?
**Answer:**
```javascript
app.use(express.static('public'));
```

## 18. How to handle query parameters?
**Answer:**
```javascript
app.get('/search', (req, res) => {
  const query = req.query.q;
  res.send(`Search for ${query}`);
});
```

## 19. How to handle route parameters?
**Answer:**
```javascript
app.get('/users/:id', (req, res) => {
  res.send(`User ID: ${req.params.id}`);
});
```

## 20. How to redirect in Express?
**Answer:**
```javascript
res.redirect('/new-path');
```

## 21. How to set headers in Express?
**Answer:**
```javascript
res.set('Content-Type', 'application/json');
```

## 22. How to send JSON response?
**Answer:**
```javascript
res.json({ name: 'John', age: 30 });
```

## 23. What is the difference between res.send() and res.json()?
**Answer:**
- `res.send()`: Sends string, buffer, or object
- `res.json()`: Sends JSON response with proper headers

## 24. How to chain middleware?
**Answer:**
```javascript
app.get('/example', mw1, mw2, (req, res) => res.send('Done'));
```

## 25. How to use template engines with Express?
**Answer:**
```javascript
app.set('view engine', 'ejs');
res.render('index', { title: 'My Page' });
```

## 26. How to enable URL encoding?
**Answer:**
```javascript
app.use(express.urlencoded({ extended: true }));
```

## 27. What is app.param()?
**Answer:** Used to handle route parameters and pre-processing before route handler.

## 28. How to handle file uploads?
**Answer:** Using `multer` middleware.

## 29. How to implement REST API?
**Answer:** Using Express routes, request handlers, and middleware to manage CRUD operations.

## 30. How to mount a router on a path?
**Answer:**
```javascript
app.use('/api', apiRouter);
```

## 31. What is next() function in middleware?
**Answer:** Passes control to the next middleware function in the stack.

## 32. How to disable 'X-Powered-By' header?
**Answer:**
```javascript
app.disable('x-powered-by');
```

## 33. How to enable HTTPS in Express?
**Answer:**
```javascript
const https = require('https');
const fs = require('fs');
https.createServer({ key: fs.readFileSync('key.pem'), cert: fs.readFileSync('cert.pem') }, app).listen(443);
```

## 34. How to use cookies?
**Answer:** Using `cookie-parser` middleware.

## 35. How to implement sessions?
**Answer:** Using `express-session` middleware.

## 36. What is res.locals?
**Answer:** Object passed to the views for local variables.

## 37. How to enable compression?
**Answer:** Using `compression` middleware.

## 38. How to use Helmet for security?
**Answer:**
```javascript
const helmet = require('helmet');
app.use(helmet());
```

## 39. How to handle JSON Web Tokens (JWT)?
**Answer:** Using `jsonwebtoken` package for authentication and authorization.

## 40. How to log requests?
**Answer:** Using `morgan` middleware.

## 41. How to limit request size?
**Answer:**
```javascript
app.use(express.json({ limit: '10kb' }));
```

## 42. How to implement rate limiting?
**Answer:** Using `express-rate-limit` package.

## 43. How to handle asynchronous errors?
**Answer:** Using try-catch inside async functions or packages like `express-async-errors`.

## 44. How to render HTML pages?
**Answer:** Using template engines like EJS, Pug, or Handlebars.

## 45. How to handle WebSockets?
**Answer:** Using `socket.io` with Express.

## 46. How to create API versioning?
**Answer:** Mount different routers for different versions:
```javascript
app.use('/api/v1', v1Router);
app.use('/api/v2', v2Router);
```

## 47. How to implement rate-limited APIs?
**Answer:** Using `express-rate-limit` and applying middleware to specific routes.

## 48. How to enable static file caching?
**Answer:**
```javascript
app.use(express.static('public', { maxAge: '1d' }));
```

## 49. How to handle errors globally?
**Answer:** Using an error-handling middleware at the end of all routes.

## 50. How to structure large Express apps?
**Answer:** Split routes, controllers, middleware, and models into separate folders for modular architecture.



### 1. **Http**
This is an older way to make HTTP requests. It allows you to send requests and handle responses asynchronously.

```javascript
const xhr = new XMLHttpRequest();
xhr.open('GET', 'https://api.example.com/data', true);
xhr.onload = function () {
  if (xhr.status >= 200 && xhr.status < 300) {
    console.log(JSON.parse(xhr.responseText));
  } else {
    console.error('Request failed:', xhr.statusText);
  }
};
xhr.onerror = function () {
  console.error('Request error');
};
xhr.send();
```

### 2. **Fetch API**
The Fetch API is a modern alternative to `XMLHttpRequest` and provides a more powerful and flexible feature set. It uses Promises, making it easier to handle asynchronous requests.



### 3. **Axios**
Axios is a popular library for making HTTP requests. It is built on top of the Fetch API and provides a simpler API and some additional features, like interceptors.






### 1. **What is an API?**
APIs define a set of rules and protocols for how different software components should interact. In web development, APIs often refer to RESTful APIs or GraphQL APIs that allow you to fetch or manipulate data from a server.

### 2. **Types of APIs**
- **REST APIs**: Use standard HTTP methods (GET, POST, PUT, DELETE) and are typically based on resources (e.g., users, posts).
- **GraphQL APIs**: Allow clients to request only the data they need, providing more flexibility than traditional REST APIs.
- **Web APIs**: Browser APIs that allow interaction with web browser features (e.g., Geolocation API, Fetch API).

### 3. **Making API Calls in JavaScript**
You can interact with APIs using various methods, primarily through the `Fetch API`, `XMLHttpRequest`, or libraries like `Axios`.

#### **Using Fetch API**
```javascript
fetch('https://api.example.com/data')
  .then(response => {
    if (!response.ok) {
      throw new Error('Network response was not ok');
    }
    return response.json();
  })
  .then(data => console.log(data))
  .catch(error => console.error('Fetch error:', error));
```

#### **Using Axios**
```javascript
import axios from 'axios';

axios.get('https://api.example.com/data')
  .then(response => console.log(response.data))
  .catch(error => console.error('Axios error:', error));
```






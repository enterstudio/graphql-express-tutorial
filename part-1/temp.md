`npm init`

`npm install --save express`

`touch index.js`

add the following code in index.js
```
const express = require('express')
const app = express()

app.get('/', _ => res.send("Hello world !"))

// run server on port 3000
app.listen('3000', _ => console.log('Server is listening on port 3000...'))
```

in package.json add script `"start": "node index.js"`

`npm install --save graphql express-graphql`

create Todo fake model in /models

create schema with query in graphql/Schema/Schema.js
with a fakedatabase

import graphqlHTTP and schema in index.js and create graphql middleware

add mutations in schema.js

test mutation with :
```
mutation {
  createTodo(id: 4, content: "test") {
    id
  }
}
```

query all with :
```
query {
  todo {
    id,
    content
  }
}
```

now we can :
- get all / one todo
- create a todo
- check a todo when it's done
- delete a todo
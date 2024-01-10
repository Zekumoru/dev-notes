# Sessions

## Setup a session

### Install packages

```bash
yarn add express-session
yarn add -D @types/express-session
```
### Setting up

Import the session:

```typescript
import session from 'express-session';
```

Then use it:

```typescript
app.use(session({
    secret: 'some secret',
    resave: false,
    saveUninitialized: true,
    cookie: {
        maxAge: 1000 * 60 * 60, // 1 hour
    }
}));
```

##  Setup a session with mongoose

### Install packages

```bash
yarn add express-session mongoose connect-mongo
yarn add -D @types/express-session @types/mongoose
```

### Setting up

Import the following packages:

```typescript
import session from 'express-session';
import MongoStore from 'connect-mongo';
import mongoose from 'mongoose';
```

Connect to mongodb:

```typescript
mongoose.connect(db_connection_string);
```

And finally use it:

```typescript
app.use(session({
    secret: 'some secret',
    resave: false,
    saveUninitialized: true,
    store: MongoStore.create({
        mongoUrl: db_connection_string,
        collectionName: 'sessions',
    }),
    cookie: {
        maxAge: 1000 * 60 * 60, // 1 hour
    }
}));
```


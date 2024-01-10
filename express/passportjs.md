# PassportJS

## Setting up PassportJS with LocalStrategy

### Install packages

```bash
yarn add passport passport-local
yarn add -D @types/passport @types/passport-local
```
### Setting up

Import the following packages:

```typescript
import passport from 'passport';
import { Strategy as LocalStrategy } from 'passport-local';
```

Setup local strategy:

```typescript
passport.use(
    new LocalStrategy(async (username, password, done) => {
        // find user from db
        const user = await getUserByUsername(username);

        // handle user does not exist
        if (!user) {
            return done(null, false, { message: 'User does not exist!' });
        }

        // handle password authentication
        const matched = await comparePasswords(password, user.password);
        if (!matched) {
            return done(null, false, { message: 'Incorrect password!' });
        }

        return done(null, user);
    });
);

passport.serializeUser((user, done) => {
    done(null, user._id);
});

passport.deserializeUser(async (id, done) => {
    const user = await getUserById(id);
    done(null, user);
});
```

> Don't forget to handle errors by using a try-catch block.

Use passport in express app:

```typescript
app.use(passport.initialize());
app.use(passport.session());
```
And finally authenticate a user:

```typescript
app.post('/login', passport.authenticate('local', {
    successRedirect: '/',
    failureRedirect: '/login',
}));
```
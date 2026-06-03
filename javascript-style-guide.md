# JavaScript Style Guide

> This style guide reflects the project's ESLint conventions

## Naming Conventions

### Variables and Functions

The Village uses camelCase for variables and functions. The first word is lowercase, additional words start with an uppercase letter, and there are no spaces between words.

### DO

```js
const firstName = "Brando";
```

### DON'T

```js
const firstname = "Brando";
const FirstName = "Brando";
```

### File Names

Files other than README and LICENSE use lowercase names at all times.

## Naming Variables and Functions

Use descriptive names that explain the purpose of the variable or function.

### DO

```js
function getUserProfile(userId) {
  const user = {
    id: userId,
    name: "Brando",
    email: "brando@example.com",
  };

  return user;
}
```

### DON'T

```js
function user(userId) {
  const user = {
    id: userId,
    name: "Brando",
    email: "brando@example.com",
  };

  return user;
}
```

## Declaring Variables and Functions

Declare variables and functions locally whenever possible. Prefer `const` for values that do not change, use `let` only when reassignment is required, and never use `var`.

## Code Blocks

Use braces for multi-line control structures, loops, and function bodies.

```js
if (user) {
  return user.name;
}
```

## Indentation and Spacing

### Spacing

Use spaces around operators such as `+`, `-`, `*`, `/`, and `=`.

```js
const numbers = 1 + 3 - 5;
```

### Indentation

Use two spaces for indentation. Keep formatting consistent with ESLint and Prettier.

```js
const getUserName = () => {
  if (user) {
    return user.name;
  }

  return "Unknown";
};
```

## Semicolons

Use semicolons at the end of statements to keep the code consistent and ESLint-friendly.

```js
const events = ["break-up", "job-promotion", "holiday"];
const moods = ["happy", "sad", "frustrated", "overwhelmed"];
```

## Formatting

### Line Length

Keep lines under 80 characters when practical. Break long lines into smaller, easier-to-read lines.

### Vertical Readability

Write one statement per line and separate logical blocks with blank lines when needed.

### DO

```js
const user = {
  firstName: "Wayne",
  lastName: "Campbell",
  age: 50,
  role: "Admin",
};
```

### DON'T

```js
const user = { firstName: "Wayne", lastName: "Campbell", age: 50, role: "Admin" };
```

## Comments

Write comments to explain why a decision was made, not just what the code does.

### DO

```js
const crypto = require("node:crypto");

// Store a salted hash with Node's crypto module to protect user credentials.
const hashedPassword = crypto
  .scryptSync(password, salt, 64)
  .toString("hex");
```

### DON'T

```js
const crypto = require("node:crypto");

// Hash the user's password.
const hashedPassword = crypto
  .scryptSync(password, salt, 64)
  .toString("hex");
```

## Password Hashing Example

Use Node's built-in crypto module for password hashing and salting.

```js
const crypto = require("node:crypto");

function generateSalt() {
  return crypto.randomBytes(64).toString("hex");
}

UserSchema.pre("save", function (next) {
  if (!this.salt) {
    this.salt = generateSalt();
  }

  if (!this.isModified("password")) return next();

  this.password = crypto
    .scryptSync(this.password, this.salt, 64)
    .toString("hex");

  next();
});
```

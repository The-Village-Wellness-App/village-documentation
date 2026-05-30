# JaveScript Style Guide

> This Style Guide includes coding conventions for programming with JavaScript.

## Name Case

### Variables and Functions

The village uses camelCase for variables and functions, meaning that the first word is lower case, additional words are title case, and there is no space between words.

When the variable name is a singular word this can remain all lowercase.

### **DO**

```js
const firstName = "Brando";
```

#### DON'T

```js
const firstname = "Brando";
```

```js
const FirstName = "Brando";
```

### File Names

Files other than README and LICENSE will use lower case at all times.

## Naming Variable & Functions

Variable and function names are un-obscured, ensuring that the name describes exactly what the variable/function does.

### **DO**

```js
function getUserProfile(userId) {
  const user = {
    id: userId,
    name: "Brando",
    email: "brando@example.com"
  };

  return user;
}
```

#### DON't

```js
function user(userId) {
  const user = {
    id: userId,
    name: "Brando",
    email: "brando@example.com"
  };

  return user;
}
```

## Declaring Variables & Functions

Variables and functions will be declared locally at all times. Variables and functions will be declared with 'const' wherever possible, occasionally they may be declared with 'let', but never 'var'.

## Code Blocks

Multiple lines of code will be contained within curly braces { }.

```js
const = pain {
    location: "knee",
    rating: 5,
    day: Monday,
};
```

## Indentations and Spacing

### Spacing

The Village allows for a space on either side of operators such as +-*/=.

```js
const numbers = 1 + 3 - 5
```

### Indentation

Each new indentation is one 'tab' which equates to 4 spaces in most environments or editors, though it might equate to 2 when using extensions such as 'prettier' to format code.

```js
const getUsersName = () => {
    if (user) {
        return user.name
    }
};
```

## Semicolons

Semicolons are used to end each statement.

```js
const events = [break-up, job-promotion, holiday];

const moods = [happy, sad, frustrated, overwhelmed];
```

## Formatting

### Line Length

The project aims to keep the length of lines <80 characters where possible.

Long lines are structured more closely to the left of the IDE.

### Vertical Readability

The Village ensures vertical readability - seperating seperate lines of codes.

### **DO**

```js
const = user {
    firstName: "Wayne",
    lastName: "Campbell",
    age: 50,
    role: "Admin"
};
```

#### DON'T

```js
const = user {firstName: "Wayne", lastName: "Campbell", age: 50, role: "Admin"
};
```

### Comments

Comments are 'why-centric' - explaining why code choices have been made, rather than just explaining what the code does.

### **DO**

```js
// Store a hash instead of the plaintext password to protect user credentials if the database is compromised
const hashedPassword = await bcrypt.hash(password, 10);
```

#### DON'T

```js
// Hash the user's password
const hashedPassword = await bcrypt.hash(password, 10);
```

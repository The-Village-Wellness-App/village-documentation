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

#### DON'T 

```js
const FirstName = "Brando";
```

### Objects

### File Names

Files other than README and LICENSE files will use lower case.

## Indentations and Spacing

### Spacing

Allow for a space on either side of operators such as +-*/=.

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

## Line Length

The project aims to keep the length of lines <80 characters where possible.
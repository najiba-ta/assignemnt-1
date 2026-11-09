# union and intersection types in typescript

union and intersection types are useful features in typescript. they help developers work with different types of data. both make code more flexible and reusable, but they work in different ways.

a union type allows a variable to accept more than one type. we use the `|` symbol to create a union type. for example:

```ts
type Id = string | number;

let userId: Id = 101;
userId = "user101";
```

here userId can accept either a string or a number. this is useful when a value can have different types.

on the other hand, an intersection type combines multiple types into one. we use the `&` symbol to create an intersection type. for example:

```ts
type User = {
  name: string;
};

type Account = {
  email: string;
};

type UserAccount = User & Account;

const account: UserAccount = {
  name: "asha",
  email: "asha@example.com"
};
```

here UserAccount must contain both name and email properties because it combines User and Account.

union and intersection types are both important in typescript. union allows different possible types, while intersection combines multiple types. understanding these concepts helps developers write better and more flexible code.
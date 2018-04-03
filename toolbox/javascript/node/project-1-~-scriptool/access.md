```bash
package name: (access)
version: (1.0.0)
description: Holds an item in a text file.
```

#### access has been created.

I have installed the **Chai **testing framework, hopefully that will help me out a bit. I'm going to be using the `expect` style, it seems similar to Ruby's rspec.

Here we have the repo:

[https://github.com/dewinterjack/access](https://github.com/dewinterjack/access)

---

Let's imagine I'm using the package access, that hasn't been written yet.

The 2 features defined were:

1. Can recieve a single piece of data

2. Can return the same data

A text file would be used for storage.

Someone using the package may use it like this:

```js
var acc = require('access')

acc.("Jack Dewinter");
```

That's one way of doing it. However, it could also be done in the CLI.

Running:

```bash
access -w
```

Could produce the message:

```bash
What is your input?

==>  Jack Dewinter

|=====================:

The String, "Jack Dewinter" has been successfully saved to access.txt
```

Maybe I'm already jumping ahead, I think one of these functionalities is good to start with.

Completing it the `require` way will be fine to release 1.0.0 package. Then maybe the other functionality could be 1.5.0, I need to find a good way to version properly.


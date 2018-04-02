### Node

I know that I'm going to have a fun time with Node quite soon... TBC

---

**Project**

Private, markdown-like app for to-dos/thoughts. CLI view and input.

* I need something that can run on mobile as well. 
* Organiser features

* Calender

---

Tracking tool for other applications. Stats/Health etc

---

Modules should expose an error-first callback interface. **What does this mean??**

I should always check for errors with callbacks.

It has something to do with the asynchronous flow of an app.

A standard for Node developers. You can't write everything yourself, we **depend **on other developer's dependencies.

If developers aren't playing their part implementing this pattern then the communication breaks.

[Helpful article.](http://fredkschott.com/post/2014/03/understanding-error-first-callbacks-in-node-js/)

### Error-First Callback

1. First argument is reserved for an error.
2. The second argument is for a successful response of data.

This will be a useful concept to implement into [scriptool](/toolbox/javascript/node/project-1-~-scriptool.md)

If there isn't an error, that error argument is set to null. Successful data is returned to the second argument.

```
fs.readFile('/scrip.txt, function(err, data){
    console.log(data);
});
```

This is the filesystem, reading scrip.txt, when the reading task has completed, the function \(callback\) is called, this is whether it was a success or not.


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

If there isn't an error, that error argument is set to null. Successful data is returned to the second argument.fs.readFile\('/scrip.txt,

```javascript
function(err, data){
    console.log(data);
});
```

This is the filesystem, reading scrip.txt, when the reading task has completed, the function \(callback\) is called, this is whether it was a success or not.

If all is well, data will contain the contents of scrip.txt, however, what if there was an issue?

The file may not be there, or there could be other complications, say with fs or readFile \(imagining it was a less predicable piece of code, such as a dependency from npm\).

If it does go wrong, error will hold an error object. It will contain information on what went wrong, this can be handy.

As the callback creator, it is my responsibility to deal with the potential and treat the error, whether I think it will happen or not.

I can deal with it in multiple ways, such as crashing the program or using another callback.

```javascript
fs.readFile('/scrip.txt, function(err, data){
    if(err){
        console.log('Unknown error');
        return;
    }
    console.log(data);
});
```

Ta da!

Next time... Promises. But seriously.. what does that mean? TBC...


The first challenge when dealing with javascript/node.js is to understand how asynchronous is working. 

How many times have I launched a program, expected that a function will have a value but another process was not done yet so I got *null* or an error.
All pictures showed below belongs to [Jack Siu](https://jack-siu.medium.com/?source=post_page-----bb5e8d4ffd2e--------------------------------), blogger from Medium.

Let's go through examples to understand this main concept.

In a synchronous world, each step is executed one after the other, so a sleep will pause the flow of process (python example) :

```python
import time

print('Start')
time.sleep(2)
print('Timeout')
print('End')
```
![Asynchronous Example 1](/images/asynchronous_example_1.gif)

Not in an asynchronous world, where two timelines coexist : 

```js
console.log('Start')
setTimeout(() => console.log('Timeout'), 2000)
console.log('End')
```

![Asynchronous Example 1](/images/asynchronous_example_2.gif)

So, in a more concrete example, if you want to read a file and show the content
```js
var content;
fs.readFile('./Index.html', function read(err, data) {
    if (err) {
        throw err;
    }
    content = data;
    console.log(content) // log in second timeline
});
console.log(content);
```

 ![Asynchronous Example 1](/images/asynchronous_example_3.gif)

*Game over*. You got a **undefined** as a result of your console log. 

## References

[Two dimensional timeline — A way to think about asynchronous JavaScript](https://medium.com/javascript-in-plain-english/two-dimensional-timeline-a-way-to-think-about-asynchronous-javascript-bb5e8d4ffd2e)
[Beginner's guide to Javascript's Async/Await](https://saiteja0413.hashnode.dev/beginners-guide-to-javascripts-asyncawait)
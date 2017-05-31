# Introduction
There are often cases where you need to program access to dom events.
For a example of using dom events we will look at assigning click events.

## Assigning Events
There are two things you need to do to assign click events.
1. Create a event handler.
1. Assign the event.

```
export class DomExample {
    doClickHandler;

    constructor() {
        // 1. Define the event handler
        this.doClickHandler = this.doClick.bind(this);

        // 2. Assign the handler as callback
        document.addEventHandler("click", this.doClickHandler);
    }

    dispose() {
        // 1. Remove the event using the handler
        document.removeEventHandler("click", this.doClickHandler);

        // 2. Set the handler to null
        this.doClickHandler = null;
    }

    doClick() {
        console.log("you clicked something");
    }
}
```

### The handler
To add and remove events you need to provide a event callback.  
When events fire the "this" keyword will be different to the class.  
To ensure that the keyword "this" means the class we use the bind method to define what "this" should mean in the event.
If you want the keyword "this" to mean anything else when the event fires you can define it during the bind call.

Now that you have defined the pointer you can assign it as callback to the events.

Note: The name of the handler is that of the method + Handler e.g. doSomething function has a handler of doSomethingHandler

### Dom evens on lists and list items
As a rule do not add event listeners for list items but rather on the list itself.  
e.g. do not add events on each li in a ul, instead put one event listener on the ul and check target property of the event to see if the the target is the item you are interested in.

### Passive events by default
Ensure that youre events for input is defined as passive by default.  
https://developers.google.com/web/tools/lighthouse/audits/passive-event-listeners


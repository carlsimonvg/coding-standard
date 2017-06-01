# Memory management and event monitoring
It is critical to monitor that all the events you have attached to the dom is removed when the element is no longer in use.
A easy way to do this is to use the chrome console at the appropriate breakpoint to check what events are still registered on the dom element.

For more details on how to use this please see the following page:  
https://developers.google.com/web/tools/chrome-devtools/console/events

A easy way is to just query the element to see what events are currently attached.

```
getEventListeners(element);
```

You can also use this on document to see all events.

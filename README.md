# express-basic
basic conc

After the basic requires, we say "every request goes through this function" with app.all. And that function looks an awful lot like middleware, don't it?

The three calls to app.get are Express's routing system. They could also be app.post, which respond to POST requests, or PUT, or any of the HTTP verbs. The first argument is a path, like /about or /. The second argument is a request handler similar to what we've seen before. To quote the Express documentation:

[These request handlers] behave just like middleware, with the one exception that these callbacks may invoke next('route') to bypass the remaining route callback(s). This mechanism can be used to perform pre-conditions on a route then pass control to subsequent routes when there is no reason to proceed with the route matched.

In short: they're basically middleware like we've seen before. They're just functions, just like before.
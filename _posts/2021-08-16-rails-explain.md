---
layout: post
title: "Explaining explaining in Rails"
---

### What is EXPLAIN?

SQL variants like MySQL include ways to inspect how a particular query would be executed, including what indices will be used. This can give you an idea of how the query can be expected to perform. 

For instance, if there's more than one index on a table that the query could make use of, it can be handy to know which one it actually will make use of, for the particular database instance. That's not something that's always easy to reason out abstractly, and what route the database picks can be dependent on the scale/shape of the data actually present.

The actual database query would go something like this:
```
EXPLAIN ANALYZE SELECT *** FROM *** ...;
```
But in the context of a Rails application, you may want to get this output from the Rails console, or add a statement somewhere in your application code that runs the query and writes the result to a log file.

I recently learned about this while troubleshooting a long-running query, where the tables involved in the query were temporary and not available after the fact, and the query itself was dynamically constructed in application code.

There are a couple ways to perform an `EXPLAIN` query, depending what you're starting with...

### Adding to a scope/relation

If you're chaining together a scope or relation, something like `Person.where(first_name: 'Nick')`, then you can tack `.explain` on the end of the method chain, to return the explain output.

### Bespoke SQL

Let's say your code has constructed a SQL query directly. Maybe you have the query (as a SQL-encoded string) in a variable called `sql`. 

In a model context, where `self.class.connection` is the database connection, you might run the actual query using `self.class.connection.execute(sql)`. There are other methods that might be more convenient depending what you expect to get back from your query.

In order to get the `EXPLAIN` output, you do need to consult the database itself, and the syntax could be `self.class.connection.explain(sql)`.

Hope this helps!

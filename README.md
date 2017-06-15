# Rest Architecture Cheatsheet

## Definitions

REST stands for _**RE**presentational **S**tate **T**ransfer_. The term was introduced in 2000, in Roy Thomas Fielding's dissertation [Architectural Styles and the Design of Network-based Software Architectures](http://www.ics.uci.edu/~fielding/pubs/dissertation/top.htm).

## Hey server, can I tell you something _please?_

The following table the expected meaning of requests in a restful API for typical use-cases:

| Method | Path to a specific id, like `/printers/{id}` | Path to a collection, like `/printers` |
| :---------: | :------------------------------: | :-----------------------------: |
| GET | "Please _get_ me the data for this printer" | "Please get me the data for the entire collection of printers" |
| PUT | "Please _(over)write_ this printer with the object I have in body" | "Please _(over)write_ this collection of printers with the object I have in body" |
| POST | _Don't do it. You post specific items at the collection level_ | "My body contains a printer object. Please add it to the collection. It'd nice if you get back to me with the resulting ID" |
| DELETE | "Please delete this printer" | "Please delete the entire collection of printers" |
| PATCH | "Please patch this printer object with the properties I'm sending you in body" | _Not typically allowed_ |


## References

- **[RFC 7230](https://tools.ietf.org/html/rfc7230)** HTTP/1.1 Message Syntax and Routing
- **[RFC 7231](https://tools.ietf.org/html/rfc7231)** HTTP/1.1 Semantics and Content

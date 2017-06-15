# Rest Architecture Cheatsheet

## Definitions

REST stands for _**RE**presentational **S**tate **T**ransfer_. The term was introduced in 2000, in Roy Thomas Fielding's dissertation [Architectural Styles and the Design of Network-based Software Architectures](http://www.ics.uci.edu/~fielding/pubs/dissertation/top.htm).

## Hey server, can I tell you something _please?_

The following table the expected meaning of requests in a restful API:

| Method | Operation | Path to a specific id, like `/printers/{id}` | Path to a collection, like `/printers` |
| :---------: | :---------: | :------------------------------: | :-----------------------------: |
| GET | Read | "Please get me the data for this printer" | "Please get me the data for the entire collection of printers" |
| PUT | Add / Replace | "Please add or replace this printer, all infos are in my body" | "Please write or replace this collection of printers, all infos are in my body" |
| POST | Add | _Don't do it. You post specific items at the collection level_ | "Please add this subset of printers to your collection. It'd nice if you give me the resulting IDs in return" |
| DELETE | Delete | "Please delete this printer" | "Please delete the entire collection of printers" |


## References

- **[RFC 7230](https://tools.ietf.org/html/rfc7230)** HTTP/1.1 Message Syntax and Routing
- **[RFC 7231](https://tools.ietf.org/html/rfc7231)** HTTP/1.1 Semantics and Content

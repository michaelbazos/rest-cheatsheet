# Rest Architecture Cheatsheet

## Definitions

REST stands for _**RE**presentational **S**tate **T**ransfer_. The term was introduced in 2000, in Roy Thomas Fielding's dissertation [Architectural Styles and the Design of Network-based Software Architectures](http://www.ics.uci.edu/~fielding/pubs/dissertation/top.htm).

## Summary

The following describe typical use cases of HTTP methods in a restful API:

| Method | Path to a specific id, like `/printers/{id}` | Path to a collection, like `/printers` |
| :---------: | :------------------------------: | :-----------------------------: |
| GET | Get data for the item `{id}` | Get data for the entire collection |
| PUT | (Over)write the item `{id}` with the provided body content | (Over)write the entire collection with the provided body content |
| POST | _Don't do it_ | Post a new item to the collection |
| DELETE | Delete the item `{id}` | Delete the entire collection |


## References

- **[RFC 7230](https://tools.ietf.org/html/rfc7230)** HTTP/1.1 Message Syntax and Routing
- **[RFC 7231](https://tools.ietf.org/html/rfc7231)** HTTP/1.1 Semantics and Content

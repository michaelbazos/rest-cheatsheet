# Rest Architecture Cheatsheet

## Definitions

REST stands for _**RE**presentational **S**tate **T**ransfer_. The term was introduced in 2000, in Roy Thomas Fielding's dissertation [Architectural Styles and the Design of Network-based Software Architectures](http://www.ics.uci.edu/~fielding/pubs/dissertation/top.htm).

## Summary

The following describe typical use cases of HTTP methods in a restful API:

| HTTP method | Specific item `/printers/{{id}}` | Collection of items `/printers` |
| :---------: | :------------------------------: | :-----------------------------: |
| GET | Get a representation for the requested id | Get collection details |

## References

- **[RFC 7230](https://tools.ietf.org/html/rfc7230)** HTTP/1.1 Message Syntax and Routing
- **[RFC 7231](https://tools.ietf.org/html/rfc7231)** HTTP/1.1 Semantics and Content

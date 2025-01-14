
# Hexagon Benchmarking Test

This is the Hexagon portion of a [benchmarking test suite](../../../README.md) comparing a variety
of web development platforms. The test utilizes Hexagon routes, serialization and database access.

## Tests

You can verify the benchmarks with the following command (from the project root):
`./tfb --mode verify --test hexagon hexagon-jetty hexagon-tomcat hexagon-netty hexagon-nettyepoll`

To run the full benchmarks locally, on the project root (not this directory) execute:
`./tfb --mode benchmark --test hexagon hexagon-jetty hexagon-tomcat hexagon-netty hexagon-nettyepoll`

## Infrastructure Software Versions

* [Hexagon stable version](http://hexagonkt.com)

## Test URLs

In URLs replace `${DB_ENGINE}` with: `postgresql`

and `${TEMPLATE_ENGINE}` with: `pebble`

### Jetty

* JSON Encoding Test: http://localhost:9090/json
* Plain Text Test: http://localhost:9090/plaintext
* Data-Store/Database Mapping Test: http://localhost:9090/${DB_ENGINE}/db?queries=5
* Fortunes: http://localhost:9090/${DB_ENGINE}/${TEMPLATE_ENGINE}/fortunes
* Database updates: http://localhost:9090/${DB_ENGINE}/update
* Database queries: http://localhost:9090/${DB_ENGINE}/query

### Netty

* JSON Encoding Test: http://localhost:9090/json
* Plain Text Test: http://localhost:9090/plaintext
* Data-Store/Database Mapping Test: http://localhost:9090/${DB_ENGINE}/db?queries=5
* Fortunes: http://localhost:9090/${DB_ENGINE}/${TEMPLATE_ENGINE}/fortunes
* Database updates: http://localhost:9090/${DB_ENGINE}/update
* Database queries: http://localhost:9090/${DB_ENGINE}/query

### Netty Epoll

* JSON Encoding Test: http://localhost:9090/json
* Plain Text Test: http://localhost:9090/plaintext
* Data-Store/Database Mapping Test: http://localhost:9090/${DB_ENGINE}/db?queries=5
* Fortunes: http://localhost:9090/${DB_ENGINE}/${TEMPLATE_ENGINE}/fortunes
* Database updates: http://localhost:9090/${DB_ENGINE}/update
* Database queries: http://localhost:9090/${DB_ENGINE}/query

### Tomcat

* JSON Encoding Test: http://localhost:8080/json
* Plain Text Test: http://localhost:8080/plaintext
* Data-Store/Database Mapping Test: http://localhost:8080/${DB_ENGINE}/db?queries=5
* Fortunes: http://localhost:8080/${DB_ENGINE}/${TEMPLATE_ENGINE}/fortunes
* Database updates: http://localhost:8080/${DB_ENGINE}/update
* Database queries: http://localhost:8080/${DB_ENGINE}/query

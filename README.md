 Tagline
sql_heretic will provide a full-fledged framework to expose arbitrary data sources, 
without requiring the application developer to write a single line of application code.

* Why make sql_heretic?
Many applications are more-or-less simple interfaces to the underlying data-source.
There is no "completely ready" web-framework to wrap around a data-source, and many 
applications suffer from code-bloat, re-inventing the wheel, and incomplete adherence
to standards. On the other hand, most data-sources are hard to version and test for 
integrity vis-a-vis the application code. sql_heretic is aiming to solve these by exposing 
hooks to the underlying data-source, making it inherently testable, versionable, and 
wrapping it in best-in-class tooling and network-interface standards.

* In-Depth
sql_heretic will act as a passthrough of predefined parametrized data-source queries 
through a network interface. The core server itself will be written entirely in a 
streaming, reactive, non-blocking way, only acting as glue-code for the network calls. 
Each data-source will be manually added using custom drivers to conform to a regular 
interface. This regularization will allow integrating many web-framework and 
application-server best-practices as cross-cutting concerns. The notions of data 
migration and API versioning will be merged, to allow easy upgrades and rollbacks. 
Developers will be defining the business domain in the native data-source language, 
as well as turning configuration knobs to best suite their needs.

* Developer Experience
Developers will be maintaining YAML files where schema migrations, endpoints and tests 
will reside in close proximity. A rich CLI interface will be developed to facilitate 
quick actions and control the code-base. A [popular-code-editor] plugin will be developed
to streamline developer exprience.

* Features
	- [ ] High-performance
		- [ ] streaming, non-blocking architecture
		- [ ] constant memory utilization
		- [ ] stability in production
		- [ ] high-throughput
	- [ ] Built-in DB migrations
		- [ ] testing of stored functions/procs, and indices directly in migrations
	- [ ] API endpoints
		- [ ] very small code footprint
		- [ ] advanced parameter validation
		- [ ] built-in pagination
		- [ ] automatic multiple response formats
		- [ ] auto-GZIP compression
		- [ ] direct mapping between API and DB queries
		- [ ] API test framework
		- [ ] Create/Update/Delete endpoints wrapped in a transaction
		- [ ] automatically discoverable API
			- [ ] Swagger/RAML
			- [ ] HATEOAS
	- [ ] Extensibility
		- [ ] custom webhook integration
			- [ ] for filtering, transformations, and reporting
		- [ ] custom code plugins
			- [ ] request filters
			- [ ] request transformation
			- [ ] result transformation
			- [ ] result folding/aggregation
			- [ ] integrated testing
	- [ ] Security
		- [ ] HTTPS termination
		- [ ] support for role-based access-controls
	- [ ] Automatic Logging
		- [ ] JSON format for indexing in Lucene/Kibana/Splunk/Mongo/etc.
		- [ ] access logs
		- [ ] application logs
		- [ ] telemetry logs for performance analysis


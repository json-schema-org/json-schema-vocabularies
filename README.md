# json-schema-vocabularies

This repository is for discussing possible extension vocabularies to be designed and documented outside of the formal JSON Schema organization's effort.  Starting with JSON Schema draft 2019-09, it is possible to create identifiable, re-usable 3rd-party vocabularies, which will be essential for JSON Schema's long-term success.  It is simply not possible to incorporate every idea and use case into the initial standard.  Not if we ever want it to be a standard and not just a draft!

## Active vocabularies _(out of date)_

_**NOTE:** This repository was originally set up with the intent to develop the vocabularies here.  That is no longer the case.  Instead, we are useing this as a holding area for ideas, and encouraging 3rd-parties interested in designing and writing plugins to look for and discuss ideas here.  The rest of this README has not yet been updated for this shift._

The following vocabularies are currently considered in-scope.  Please open an issue to discuss adding another vocabulary to the active set.  These vocabularies may share some keywords and structure.  All of the current active vocabularies share two characteristics:

* They are _generating_ some presentation or description of a schema or hyper-schema, rather then describing data or operations on that data
* They may need to put limits on the set of possible schemas or hyper-schemas that can produce _well-defined, interoperable results_

For instance, not all programming languages have constructs that map well to every validation keyword, nor are there clear UX intuitions for how to present complex validation schemas.  Similarly, a statically generated set of documenation cannot capture every aspect of a fully dynamic hypermedia system.  Vocabularies may not forbid the presence of any particular valdation or hyper-schema feature, but may declare certain schemas to produce undefined results in order to keep the resulting implementation requirements to a manageable level. 

### JSON UI Schema

Goal:  To allow building UIs from a schema, mapping validation keywords to UI widgets, and hyper-schema links to form submission attributes and/or multi-form workflows.  The [json-schema-form](https://github.com/json-schema-form/json-schema-form) project is the princpal starting point for this work.

Editor: @Anthropic

### JSON API Documentation Schema

Goal:   A minimal set of keywords to describe the usage of hyper-schemas within a defined API.  Authentication, authorization, and HTTP headers are areas that may be addressed by this vocabulary.  Unlike OpenAPI, RAML, etc., this format will be strictly complementarly to JSON Hyper-Schema, and assume its use as the primary hypermedia approach for the API being described.

Editors: @Relequestual, @handrews

### JSON Code Generation Schema

Goal: Automatically generating libraries in a variety of languages.

Editor(s): [open]

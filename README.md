# json-schema-vocabularies
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](https://github.com/json-schema-org/.github/blob/main/CODE_OF_CONDUCT.md)
[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
[![Financial Contributors on Open Collective](https://opencollective.com/json-schema/all/badge.svg?label=financial+contributors)](https://opencollective.com/json-schema)

Starting with JSON Schema draft 2019-09, it is possible to create identifiable, re-usable, third-party vocabularies, which will be essential for JSON Schema's long-term success.  It is simply not possible to incorporate every idea and use case into the initial standard, not if we ever want JSON Schema to be a standard and not just a draft!

This repository is for discussing possible extension vocabularies to be designed and documented outside of the formal JSON Schema organization's effort.

Please feel free to peruse the issues and add your thoughts or even create new issues for new ideas that could be supported by JSON Schema.

## What is a vocabulary?

While the requirements of vocabularies and how JSON Schema interacts with them is [in the spec](https://json-schema.org/draft/2019-09/json-schema-core.html#rfc.section.4.3.3), the concept may be easier to understand by reading the documentation in a plain-language format.  Below are some additional resources written by third parties.

<!-- The idea is to have as many here as possible. -->
<!-- - [Understanding JSON Schema]()  I thought we had updated this for 2019-09. -->
- [How Vocabularies Work](https://docs.json-everything.net/schema/vocabs) by [@gregsdennis](https://github.com/gregsdennis)
<!-- anyone else? kinda lonely here -->

## Tips for writing vocabularies

As a minimum set of requirements, it is suggested that vocabularies:

- are defined by some human-readable document that gives semantic meaning to the keywords it defines.  This can be a formal RFC, similar to the JSON Schema specification, or something as simple as a README or a blog post.
- provide a meta-schema so that the keyword(s) can be syntactically validated within a schema.  It may be necessary to create meta-schemas for each draft to be supported by the new keyword(s).
- are accompanied by at least one implementation, ideally manifested as a plugin to an existing validator.

JSON Schema strives to be language-agnostic in order to foster as much adoption as possible.  This means that it should be implementable in any language, or at least as far as a language can support the features.  It is suggested that vocabularies are written in a way to allow for these limitations.

## Active vocabularies

The following attempts to be a curated collection of vocabularies that have been defined by third parties.  Often, they are submitted by developers who maintain JSON Schema validators and/or work on the specification directly.

### OpenAPI 3.1

<!-- Headerless tables have been requested https://github.com/github/cmark-gfm/issues/91 -->
|||
|-|-|
|**Goal**||
|**Documentation**|https://github.com/OAI/OpenAPI-Specification/blob/main/versions/3.1.0.md<br>(no separate vocab, mixed into the overall spec)|
|**Vocabulary ID**|`https://spec.openapis.org/oas/3.1/vocab/base`|
|**Meta-schema ID**|`https://spec.openapis.org/oas/3.1/meta/base`|
|**Edited by**| The OpenAPI [Team](https://github.com/OAI)|
|**Project site**|https://openapis.org/|
|**Known implementations**|[JsonSchema.Net.OpenApi](https://www.nuget.org/packages/JsonSchema.Net.OpenApi/)|

### Accessing Instance and External Data

|||
|-|-|
|**Goal**|To allow schemas to validate known keywords against data located within the instance being validated or in external sources.  Attempts to provide a solution for the highly-debated `$data` keyword.|
|**Documentation**|https://docs.json-everything.net/schema/vocabs/data-2023|
|**Vocabulary ID**|`https://docs.json-everything.net/schema/vocabs/data-2023`|
|**Meta-schema ID**|`https://json-everything.net/meta/vocab/data-2023`|
|**Edited by**|[@gregsdennis](https://github.com/gregsdennis)|
|**Project site**|https://github.com/gregsdennis/json-everything|
|**Known implementations**|[JsonSchema.Net.Data](https://www.nuget.org/packages/JsonSchema.Net.Data/)|

### Extended Array Validation

|||
|-|-|
|**Goal**|To provide extended validation of items within arrays.|
|**Documentation**|https://docs.json-everything.net/schema/vocabs/array-ext|
|**Vocabulary ID**|`https://docs.json-everything.net/schema/vocabs/array-ext`|
|**Meta-schema ID**|`https://json-everything.net/meta/vocab/array-ext`|
|**Edited by**|[@gregsdennis](https://github.com/gregsdennis)|
|**Project site**|https://github.com/gregsdennis/json-everything|
|**Known implementations**|[JsonSchema.Net.ArrayExt](https://www.nuget.org/packages/JsonSchema.Net.ArrayExt/)|

_**NOTE** This was initially published as the UniqueItems vocabulary.  The ArrayExt extension supersedes that one._
# json-schema-vocabularies

Starting with JSON Schema draft 2019-09, it is possible to create identifiable, re-usable, third-party vocabularies, which will be essential for JSON Schema's long-term success.  It is simply not possible to incorporate every idea and use case into the initial standard, not if we ever want JSON Schema to be a standard and not just a draft!

This repository is for discussing possible extension vocabularies to be designed and documented outside of the formal JSON Schema organization's effort.

Please feel free to peruse the issues and add your thoughts or even create new issues for new ideas that could be supported by JSON Schema.

## What is a vocabulary?

While the requirements of vocabularies and how JSON Schema interacts with them is [in the spec](https://json-schema.org/draft/2019-09/json-schema-core.html#rfc.section.4.3.3), the concept may be easier to understand by reading the documentation in a plain-language format.  Below are some additional resources written by third parties.

<!-- The idea is to have as many here as possible. -->
<!-- - [Understanding JSON Schema]()  I thought we had updated this for 2019-09. -->
- [How Vocabularies Work](https://gregsdennis.github.io/json-everything/usage/schema-vocabs.html) by [@gregsdennis](https://github.com/gregsdennis)
<!-- anyone else? kinda lonely here -->

## Tips for writing vocabularies

As a minimum set of requirements, it is suggested that vocabularies:

- are defined by some human-readable document that gives semantic meaning to the keywords it defines.  This can be a formal RFC, similar to the JSON Schema specfication, or something as simple as a README or a blog post.
- provide a meta-schema so that the keyword(s) can be syntactically validated within a schema.  It may be necessary to create meta-schemas for each draft to be supported by the new keyword(s).
- are accompanied by at least one implementation, ideally manifested as a plugin to an existing validator.

JSON Schema strives to be language-agnostic in order to foster as much adoption as possible.  This means that it should be implementable in any language, or at least as far as a language can support the features.  It is suggested that vocabularies are written in a way to allow for these limitations.

## Active vocabularies

The following attempts to be a curated collection of vocabularies that have been defined by third parties.  Often, they are submitted by developers who maintain JSON Schema validators and/or work on the specification directly.

### Accessing Instance and External Data

<!-- Headerless tables have been requested https://github.com/github/cmark-gfm/issues/91 -->
|||
|-|-|
|**Goal**|To allow schemas to validate known keywords against data located within the instance being validated or in external sources.  Attempts to provide a solution for the highly-debated `$data` keyword.|
|**Documentation**|https://gregsdennis.github.io/json-everything/usage/vocabs-data.html|
|**Vocabulary ID**|`https://gregsdennis.github.io/json-everything/vocabs-data`|
|**Meta-schema ID**|`https://gregsdennis.github.io/json-everything/meta/data`|
|**Edited by**|[@gregsdennis](https://github.com/gregsdennis)|
|**Project site**|https://github.com/gregsdennis/json-everything|
|**Known implementations**|[JsonSchema.Net.Data](https://www.nuget.org/packages/JsonSchema.Net.Data/)|

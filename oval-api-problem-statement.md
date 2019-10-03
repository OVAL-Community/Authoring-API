
# What is needed (in priority order)

1. A code generator for the model library: A complete language specific data model (e.g., JAXB) that can be generated from the OVAL schema.
  - Code must be able to read in OVAL from a file into an internal data structure and serialize it back to a file.
  - The code must be able to create a complete OVAL definition using language APIs from scratch and then serialize it to XML.
  - Tracking and ensuring internal identifier references are consistant
  - A sufficant language needs to be selected.
    - The language must have a mature package management infrastructure (e.g., NodeJS, PiP)
    - Must have a significant user community, with access to integrated development environments (IDEs)
    - Must be capable of running on all popular end-user operating systems.
    - Should strongly consider Python
    - Source and distribution license selected should allow for commercial and international use, without encumbrances (e.g. MIT, Apache)
1. Application Library: Additonal API code to make constructing data model instances easier.
  - features:
    - builder pattern
    - validation
    - version translation
    - identifier creation/tracking
    - canonicalization for de-duplicating OVAL constructs - i.e., collapsing or reusing similar OVAL objects within the same workspace)
    - Behavior-driven development approach for expressing logic in an easier to read and develop API vs OVAL XML.
  - It might be useful to distribute generated code as a library
  - Can be versioned and shared.
  - Dependencies on the library can be managed using package management capabilities.
  - Work towards a stable library interface in the long-run
  - Source and distribution license selected should allow for commercial and international use, without encumbrances (e.g. MIT, Apache)
1. Templating or macro support for common OVAL data patterns. These can be versioned and released using the language's package management features.
1. Support other SCAP formats: Add support for XCCDF and other SCAP formats.

# Initial starting point

- Start with the OVAL core and a single platform schema to keep the scope as small as possible, while providing a solid proof-of-concept.

# Next Steps

- Find an individual or organization to contribute 2-3 weeks to complete #1 and parts of #2 above.

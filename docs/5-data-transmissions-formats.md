[![index.md](assets/back_main_page_icon_124174_32.png)](index.md) [Go to Contents](index.md)

### XML Transformation

* Tree-based processors
  * Represent entire XML document as object tree
  * Can traverse tree forward or backward
  * Pros: easy to search with XPath or API-specific tools
  * Cons: more memory needed , slower than streaming
* Streaming processors
  * Build or parse XML one node at a time
  * Devided into  ""pull""  and ""push"" processors
  * Cons: 	
    * Complete data set not stored in memory;
    * XPath searches not supported;
    * SAX coding is complex
  * Examples: SAX, StAX, XMLPullParser
  * Benefits:
    * As XML is read, the processor emits events
    * After event is handled, the data can be discarded
* Binding Processors
  * Works like DOM-style in the background
  * Developer annotates Java classes, runs, simple code
  * Pros: efficient programming model, easy to maintain
  * Cons: JAXB dosn't work in Android
* JAXP
  * JAva API for XML Processing
  * Sets standards for APIs included in Java SE
* API that works in Android
  * SAX, DOM, XMLPullparser, JDOM 2.0.1 or later
* We need to use namespaces if we want idntifite the concrete tag, if we have several diferent tag types with the same namespaces
* SAX: Event base streaming parser
  * Faster and uses less memory than tree-based processors
  * A push parser: pushes data into callback methods
  * works on Android
  * **Data Events**
    * Common Events
      * startDocument
      * endDocument
      * startElement
      * endElement
      * characters
    * Error-handling events
      * warning
      * error
      * fatalError
    * Other Events
      * notationDecl
      * processionInstruction
      * ignorableWhitespace
      * resolveEntity
      * unparsedEntity
      * skippedEntity
  * Handle Class 
    * extends DefaultHandler
  * Track all data manually
* DOM: Document Object Model
  * Tree-style xml parser
  * Read and Write API
  * We can search Nodes with XPath
  * Keep the document in the memory, this can lead to exceed memory
    - Node, NodeList, Element
* JDOM: Is improvement of DOM
  * Dom features
  * Parsing depends on underlying SAX parser
  * JDOM vs DOM
    * Uses superclasses instead of interfaces
    * less code for similar tasks
* StAX: Streaming API for XML
  * Event base, reading and writing XML(SAX can only read XML)
  * Low-level streaming parser wit XMLStreamReader, XMLStreamWriter
    * Faster
  * Higher level event-based parsing with XMLEventReader, XMLEventWriter
    * Less code, easier to maintain
* JAXB: Java Architecture for XML Binding
  * Reading and Writing API
  * XML structure is based on annotations in Java classes
  * Memory intensive API, so it is not appropriate to Android(can be used Simple instead)
  * Generate annotated classes from XML schemas (@XmlRootElement, @XmlAccessorType, @XmlElement)
  * Stores the entire document in memmory
  * Large documents can cause Java to run out of heap space
* Simple: Simple XML serialization
  * Similar to JAXB but lightweight
  * Large documents can cause Java to run out of heap space

### JSON Transformation

* JSON: JavaScript Object Notation
  * Lightweight and Easy to read/write
  * Supported Data Types: Strings, Numbers, Booleans, null, Arrays, Objects
  * In JAvaScript you don't need double-quotes(around keys), but in JSON you need it
* JSON-B: Java API for JSON Binding
  * Uses Annotations
* JSON-P: Java API for JSON processing
  * Streaming based API, based on Event model
  * Events: START_ARRAY, START_OBJECT, KEY_NAME, VALUE_STRING, VALUE_NUMBER, 
            VALUE_TRUE, VALUE_FALSE, VALUE_NULL, END_OBJECT, END_ARRAY
  * JSONPointer
    * Provides access to JSON properties via an expressions
    * Similar to XPath for XML (Example: /name, /brands/0/name)
  * JSONPatch:
    * Allow modifications via path-based expressions
    * Allow properties to be added, modified or removed

### Questions

* Comparison of XML and json data formats
  * Structure: XML is a tree, while json can compose higher structures using array or object
  * XML can be validated, can contain text between any elements.
* Analysis of XML processing libraries in terms of memory consumption, developer convenience, performance.
  * DOM: all content in memory. Good for heterogenous structure, not well defined structure.
  * StaX: high performance, minimal footprint.
  * JAXB: useful when structure is well defined, XML is small.
* Use cases
  * E.g. JAXB is good for remote procedure call, for example in web services.
  * Etc

The Ultimate JSON Library: JSON.simple vs. GSON vs. Jackson vs. JSONP:
https://dzone.com/articles/the-ultimate-json-library-jsonsimple-vs-gson-vs-ja
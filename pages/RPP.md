- [[Propositional Logic]]
- [[Relational Logic]]
- [[Non-Monotonic Logic]]
- Rule-based system
- Probabilistic Reasoning
-
- # Semantic Network
	- What
		- A semantic network is a graphic notation for representing knowledge in patterns of interconnected nodes
		- it represents knowledge or supports reasoning
		- a form of knowledge representation
		- The structural idea is that knowledge can be stored in the form of graphs, with nodes representing objects in the world, and arcs representing relationships between those objects
	- How
		- Semantic nets consist of nodes, links and link labels. In these network diagrams, nodes appear in the form of circles or ellipses or even rectangles which represent objects such as physical objects, concepts or situations.
		- Links appear as arrows to express the relationships between objects, and link labels specify relations.
	- Why good
		- Semantic Networks Are Majorly Used For
			- They are simple and can be easily implemented and understood.
			- The semantic network is more natural than the logical representation;
			- The semantic network has a greater expressiveness compared to logic.
	- Why not good
		- There is no standard definition for link names
		- Semantic Nets are not intelligent, dependent on the creator
		- Links on object represent only binary relations
		- sparsed in knowledge -> makanya ada OOR
	- What type
		- Definitional Networks
			- These networks emphasize and deal with only the subtype or is a relation between a concept type and a newly defined subtype.
			- A producing network is referred to as a generalization hierarchy.
			- It supports the inheritance rule for duplicating attributes.
		- Assertion Networks
			- Assertion Networks – Designed to assert propositions is intended to state recommendations. Most data in an assertion network is genuine unless it is marked with a modal administrator. Some assertion systems are even considered as the model of the reasonable structures underlying the characteristic semantic natural languages.
		- Implicational Networks
			- – Uses Implication as the primary connection for connecting nodes. These networks are also used to explain patterns of convictions, causality and even deductions.
		- Executable Network-
			- Contains mechanisms that can cause some changes to the network itself by incorporating some techniques, for example, such as attached procedures or marker passing which can perform path messages, or associations  and searches for patterns
		- Learning Networks
			- These are the networks that build and extend their representations by acquiring knowledge through examples. Contain mechanisms in such networks brings changes within the network itself through representation by securing information. A classic example could be like, the changing of new information from the old system by including and excluding nodes and arcs, or by changing numerical qualities called weights, and connected with the arcs and nodes.
		- Hybrid Networks
			- Networks that combine two or more of previous techniques, either in a single network or in a separate, but closely interacting network Hybrid network has been clearly created to implement ideas regarding human cognitive mechanisms, while some are created generally for computer performance.
	-
-
- # Object Oriented Representation
	- What
		- As KB grows, it becomes critical to organize them in some
		  way.
		- cara organize knowledge base
	- Why
		- General knowledge representation is flat. Knowledge about a
		  given object or type of object could be scattered around the
		  knowledge base.
	- When
		- stereotypical knowledge
			- Frame is proposed by Minsky (1975) to define stereotype
			  situations. Example:
			  ○ birds as prototypical objects with a general property
			  that most birds can fly though there are exceptions.
	-
-
- # Description Logic
	- Why
		- OOR: Objects naturally fall into categories, but are
		  very often thought of as being members of
		  multiple categories (e.g. I am a person, a
		  parent, and a mother)
		- It is also natural for categories with more
		  complex descriptions (e.g. a family with three
		  children is a family that is not childless) →
		  need more relations than is-a & instance-of
		- Description Logics has ability to represent other
		  kinds of relationships between concepts, beyond
		  IS-A and INSTANCE-OF relationships.
		- Represent Complex Concept
	- What
		- a logical system working mainly with descriptions.
		- Concept (category, basic classes of objects) and role
		  (relation that describe objects that are parts or attributes
		  or properties of other objects). Analogy: frame and slot.
		- Concepts are being organized into a generalization
		  hierarchy.
		- A KB in a description logic is considered to be any
		  collection of sentences
		- Reasoning in a description logic means calculating
		  entailments.
		- are a family of knowledge representation lan-guages that can be used to represent the knowledge of an application domain in a structured and formally well-understood way.
		- DLs differ from their predecessors, such as semantic networks and frames,
		  in that they are equipped with a formal, logic-based semantics.
	- Why DL in ontology?
		- As already mentioned above, high quality ontologies are crucial for the Semantic
		  Web, and their construction, integration, and evolution greatly depends on the
		  availability of a well-defined semantics and powerful reasoning tools. Since DLs
		  provide for both, they should be ideal candidates for ontology languages.
	-
		-
-
- # Ontology
-
- # Semantic Web
	- url vs uri vs iri
	- While surfing the internet or checking any website, you may have encountered the words "URI" and "URL" multiple times. These are the two important concepts of web and are mostly used interchangeably. But they are not the same as each other; the main difference between URI and URL is that URI can represent both URL and URN of a resource simultaneously, whereas URL can only specify the address of the resource on the internet. In this topic, we will see URI and URL individually and how both can be differentiated from each other.
	- A URI or Uniform Resource Identifier is a string identifier that refers to a resource on the internet. It is a string of characters that is used to identify any resource on the internet using location, name, or both.
	- A URI has two subsets; URL (Uniform Resource Locator) and URN (Uniform Resource Number). If it contains only a name, it means it is not a URL. Instead of directly URI, we mostly see the URL and URN in the real world.
	- A URI contains scheme, authority, path, query, and a fragment. Some most common URI schemes are HTTP, HTTPs, ftp, Idap, telnet, etc.
	-
	- Syntax of URI
	  The Syntax of URI is given below:
	- scheme:[//authority]path[?query][#fragment]  
	  Scheme: The first component of URI is scheme that contain a sequence of characters that can be any combination of letter, digit, plus sign, or hyphen (_), which is followed by a colon (:). The popular schemes are http, file, ftp, data, and irc. The schemes should be registered with IANA.
	  Authority: The authority component is optional and preceded by two slashes (//). It contains three sub-components:
	  userinfo: It may contain a username and an optional password separated by a colon. The sub-component is followed by the @ symbol.
	  host: It contains either a registered name or an IP address. The IP address must be enclosed within [] brackets.
	  Port: Optional
	  Path: It consists of a sequence of path segments separated by a slash(/). The URI always specifies it; however, the specified path may be empty or of 0 lengths.
	  Query: It is an optional component, which is preceded by a question mark(?). It contains a query string of non-hierarchical data.
	  Fragment: It is also an optional component, preceded by a hash(#) symbol. It consists of a fragment identifier that provides direction to a secondary resource.
	-
	- Some examples of URI
	  mailto:hey.Doe@example.com
	  news:comp.infosystems.www.servers.unix
	  urn:oasis:names:specification:docbook:dtd:xml:4.1.2
	-
	- ![image.png](../assets/image_1652889930772_0.png)
	-
-
- # Knowledge Graph
	- 7
	- Semantic Web is a set of technologies that want to make the data on the web readable and understood by machines. The domain that semantic web is the web. Therefore the URI is in the bottom of the technologies stack.
	- Semantic Network is a graph model to store the information. If you can model your data as a graph with node and edge, you can think it as a semantic network.
	- Knowledge graph is also a kind of graph model. However, it emphasis the store of all data on the level of both schema and individual. Therefore, it has no essential difference with Semantic network.
	- Knowledge base is an instantiated storage of a domain knowledge. You can think it as a database. It has not to be a graph model, if you can store the knowledge in some way, you can call it as knowledge base.
	-
	- W3C semantic web or linked data standards are widely used in the development of knowledge graphs. JSON-LD, in fact, is one of those standards: See JSON for Linking Data.
	- “Semantic web” is a term that originated with web pioneer and World Wide Web Consortium founder Tim Berners-Lee (TBL) in an article in Scientific American in 1999, one that described a vision of a relationship-rich, scalable, contextual data web, a web of graph-oriented and well-described data that could live side by side with existing web content. The W3C led the development over decades of standard semantic graph technologies, including Resource Description Framework (RDF), a triplified data interchange standard. Each RDF triple can be considered a small graph. Each triple consists of a subject, verb (relationship or edge) and object, plus any associated attributes.
	- ![image.png](../assets/image_1652891471449_0.png)
	-
	- Simple semantic graphs can scale by adding other standard edges and nodes, Tinker Toy style. To make sure the graph nodes and edges are reusable, each element of the graph is labeled with an IRI, or International Resource Identifier, a globally unique ID and web address.
	  A term associated with publishing quality structured data on the web is “Linked Data”, which originated in 2006. LinkedData - W3C Wiki The W3C is also behind that term.
	  Linked Data technologies such as RDF, RDFS, SPARQL, OWL, SKOS and JSON-LD are also core to the semantic web stack. See Semantic Web - W3C. Sometimes the terms “linked data” and “semantic web” are used synonymously.
	-
	- A knowledge graph (a term coined by Google in 2012, after they bought Metaweb, which had created a graph knowledge base called Freebase) ideally consists of a meaningful standard graph data model or ontology of your domain (=a description map of people, places, things and ideas and how they’re connected, composed or generated in OWL (web ontology language) and/or RDFS (Resource Description Framework Schema), plus the content and other data that’s informed by and can be integrated with the help of that model. All sorts of data can be integrated via a semantic knowledge graph, and all of that data can be stored and lives side by side with the data model(s), with everything, including data models or schemas and instance data, in RDF. For that reason, all declarations and rules in the full standard knowledge graph can be harnessed by applications, making it possible to simplify, avoid duplication and scale application development beyond organizational boundaries.
	- Semantic web/linked data technologies are how knowledge graphs can scale and allow global data and scalable graph data model reuse. For that reason, they’re fundamental to open big data that’s shared at scale. Thus the reason and rationale behind the Linked Data Cloud, which expands by leaps and bounds every year.
-
- # Case Based Reasoning
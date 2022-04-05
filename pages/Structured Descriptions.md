- the frame representation seen there focused more on the organization
  and invocation of procedures than on inferences about the objects and
  categories themselves.
-
- Reasoning about objects in everyday thinking
  goes well beyond the simple cascaded computations seen in that chapter,
  and is based on considerations like the following:
	- objects are very often thought of as being members of
	  multiple categories (e.g., I am an author, an employee, and a father);
	- objects have parts, sometimes in multiples (e.g., books have titles,
	  tables have legs, automobiles have wheels);
-
- compound predicate
	- Hunter&Gatherer(x),
		- both Hunter(x) and Gatherer(x) would also be true
	- In a description logic, we refer to the frame type of
	  description as a concept and to the slot as a role.
-
- Description Logic
	- representasi more complex logic, dibandingkan dengan frame yang cuma bisa is a dan slot
	- constant: variable (instantiation)
	- role: slot, atribut
	- concept: class
-
- concept forming operator:
	- menggabungkan 2 concept menjadi concept
		- ALL manager canadian
			- manager: role
			- canadian: class
-
- connective equivalent:
	- menyatakan kesamaan antar sentence
	-
- Reasoning:
	- satisfaction
	- subsumption
-
- Entailment:
	- normal form
	- structure matching
		- untuk menentukan apakah d berarti kita menyocokkan dari yang general (e) ke yang specific (d)
-
- Description languange bisa direpresentasikan dengan DAG.
	- taxonomy arise naturally out of a DL KB
	- nodes: atomic concept
	- edge: a_i connect a_j  if a_i subsume a_j
	- constant c linked only to the most specific atomic concepts a in the taxonomy such that 
	  KB |= (c -> a)
-
-
- Next: [[Ontology]]
-
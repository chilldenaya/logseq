- Cara menentukan suatu sentence valid, satisfiable, not satisfiable:
	- ![image.png](../assets/image_1644993642130_0.png)
-
- Reverse evaluation:
	- diberikan beberapa sentence, kita mencari interpretasi mana yang memenuhi sentence terebut
	- caranya adalah dengan membuat truth table
	- proses:
		- cari row mana saja yang memenuhi sentencenya
		- row - row ini adalah possible interpretation
		- kalau ada sentence lain, coba lagi masukin
		- cari row mana yang memenuhi semua sentence
		-
		-
- Logical entailment:
	- semantic Reasoning
		- truth table
collapsed:: true
			- ![image.png](../assets/image_1644994208337_0.png)
			- ![image.png](../assets/image_1644994216630_0.png)
			- jeleknya: harus buat dua table
		- validity checking
collapsed:: true
			- ![image.png](../assets/image_1644994250857_0.png)
			- ![image.png](../assets/image_1644994290165_0.png)
		- unsatisfiability checking
collapsed:: true
			- ![image.png](../assets/image_1644994260618_0.png){:height 103, :width 430}
			- ![image.png](../assets/image_1644994305703_0.png){:height 341, :width 413}
	- proof method
		- rule of inference
			- ![image.png](../assets/image_1644994870067_0.png)
collapsed:: true
				-
			- ![image.png](../assets/image_1644994877846_0.png)
			-
			- ![image.png](../assets/image_1644994824864_0.png)
			-
		- axiom schemata
			- bisa digunakan untuk proving sentences yang ga ada premis nya, contoh
collapsed:: true
				- p-> (q->p)
			- ![image.png](../assets/image_1644999733271_0.png)
			- ![image.png](../assets/image_1644999740361_0.png)
			- cara ngeprove:
				- ![image.png](../assets/image_1644999788244_0.png)
				- ![image.png](../assets/image_1644999794941_0.png)
				- ![image.png](../assets/image_1644999948576_0.png)
				- conclusion dikatakan sebagai provable ketika cuma pake axion schemata dan modus ponens
			-
		- propositional resolution
collapsed:: true
			- ![image.png](../assets/image_1645000130616_0.png)
collapsed:: true
				- cara mengubah ke clausal form:
collapsed:: true
					- ![image.png](../assets/image_1645000195234_0.png)
					- ![image.png](../assets/image_1645000202159_0.png)
					- contoh:
collapsed:: true
						- ![image.png](../assets/image_1645000237035_0.png)
						-
				- resolution method:
collapsed:: true
					- ![image.png](../assets/image_1645000376844_0.png)
				- contoh:
collapsed:: true
					- ![image.png](../assets/image_1645000476583_0.png)
					-
				-
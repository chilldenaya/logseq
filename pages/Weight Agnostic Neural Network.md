- Weight agnostic neural network menggunakan pendekatan yang berbeda dalam pencarian arsitektur terbaik.
- Hal mendasar yang membedakan wann dan nas/enas adalah wann tidak melakukan proses pelatihan bobot sama sekali. wann murni menilai kinerja suatu model hanya dari arsitektur nya saja. WANN tidak melakukan weight training secara eksplisit. Selain itu, search space dari wann tidaklah didefinisikan dari awal. Dalam keberjalanan iterasinya, arsitektur yang dibentuk akan semakin membesar, tanpa adanya batas atas (upper bound). Kita dapat memandang bahwa bobot adalah 'solusi' dari NAS/ENAS sedangkan arsitektur adalah 'solusi' dari WANN
	- The
	  weights are the solution; the found architectures merely a better substrate for the weights to inhabit. (WANN)
- WANN dibangun dengan tujuan arsitektur yang didapatkan dapat mengerjakan task sederhana tanpa perlu adanya kebergantungan dengan weight dalam arsitektur yang digunakan. Hal ini dilakukan dengan cara tidak memberikan weight peran apapun dalam perhitungan kinerja; memberikan seluruh bobot dalam arsitektur dengan nilai yang sama.
- Perhatikan bahwa ketika kita menggunakan satu nilai untuk keseluruhan nilai bobot dalam arsitektur, dimensi dari matriks bobot akan menjadi satu, sangat jauh menghemat memory.
- Proses iterasi pencarian arsitektur oleh WANN adalah sebagai berikut:
	- An initial population of minimal neural network topologies is created,
	- each network is evaluated over multiple rollouts, with a different shared weight value assigned
	  at each rollout,
	- networks are ranked according to their performance and complexity, and
	- new population is created by varying the highest ranked network topologies, chosen probabilistically
	  through tournament selection <referensi tournament selection here>
- we are not interested in searching merely for
  any weight agnostic neural networks, but networks that can be described with a minimal description
  length [35, 97, 98].
- Networks topologies are judged based on three criteria: mean performance
  over all weight values, max performance of the single best weight value, and the number of connections in the network.
- TODO hal menarik dalam wann adalah kita bisa liat perjalanan informasi dalam network, contoh ketika bipedal
- WANN menggunakan operator [[NEAT]] untuk pencarian arsitekturnya
	- The operators used to search for neural network topologies are inspired by the wellestablished neuroevolution algorithm NEAT [110]. While in NEAT the topology and weight values
	  are optimized simultaneously, we ignore the weights and apply only topological search operators.
-
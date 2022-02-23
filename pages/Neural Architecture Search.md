- Apa itu NAS https://arxiv.org/abs/1611.01578
	- NAS merupakan metode pencarian arsitektur yang diformulasikan oleh ... .
	- Secara konsep, NAS  terdiri atas tiga komponen utama, search space, search strategy, dan performance estimation strategy.
		- Search space
			- merupakan himpunan arsitektur yang memenuhi kriteria atau aturan bentuk arsitektur yang diinginkan. Dalam pembuatan search space, penggunaan prior knowledge terhadap domain permasalahan tertentu mampu meringkas kardinalitas search space sehingga mampu mempermudah proses pencarian arsitektur (Survery NAS https://arxiv.org/abs/1808.05377)
		- Search strategy
			- merupakan tata cara pencarian atau pembuatan arsitektur yang termasuk ke dalam search space. Search space seringkali unbounded. Ketika search space tidak dibatasi, search strategy harus mampu mengatasi permasalahan klasik exploration-exploitation trade-off.
		- Performance estimation strategy
			- Dalam deep learning, penggunaan training-validation dataset untuk mengukur kinerja model sangat lazim digunakan. Namun, penggunaan strategi pengukuran kinerja ini memerlukan banyak waktu dan sumber daya. Beberapa riset berfokus dalam mengembangkan metode pengukuran kinerja yang lebih hemat sumber daya. <tambahkan penjelasan riset terkait>
			-
- NAS bekerja dengan cara ...
	- NAS bekerja dengan cara merepresentasikan suatu neural network menjadi suatu variable-length string.  Suatu recurrent network yang disebut sebagai controller bekerja untuk menghasilkan string ini. String yang dihasilkan dalam controller lantar ditranslasi kembali menjadi suatu neural network yang disebut sebagai 'child network', dan digunakan untuk menyelesaikan task yang bersangkutan. Akurasi dari child network ini akan menhadi reward signal untuk controller. Di iterasi berikutnya, controller akan menghasilkan child network dengan akurasi lebih tinggi dengan peluang yang lebih besar. Dalam kata lain, controller akan 'belajar' untuk mencari child network yang lebih baik.
	- Gambar ... menunjukkan controller yang bekerja secara recurrent akan menghasilkan konfigurasi convolutional neural network.
	- Dalam iterasinya, controller akan berhenti melakukan proses pelatihan ketika banyaknya layer mencapai batas tertentu atau mencapai iterasi tertentu.
- bagaimana hasil kerja nas
	- NAS methods have outperformed manually designed archi... (NAS Survey)
	- Despite its impressive empirical performance, NAS is computationally expensive and time consuming (ENAS)
- ternyata NAS sangat lambat karena (yang dibilang [[ENAS]] )
	- _We observe that the computational
	  bottleneck of NAS is the training of each child model to
	  convergence, only to measure its accuracy whilst throwing
	  away all the trained weights._
-
-
	-
	-
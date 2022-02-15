- Apa itu NAS
- NAS bekerja dengan cara ...
	- In NAS, an
	  RNN controller is trained in a loop: the controller first
	  samples a candidate architecture, i.e. a child model, and
	  then trains it to convergence to measure its performance
	  on the task of desire. The controller then uses the performance as a guiding signal to find more promising architectures. This process is repeated for many iterations
- bagaimana hasil kerja nas
	- Despite its impressive empirical performance, NAS is computationally expensive and time consuming
- ternyata NAS sangat lambat karena (yang dibilang [[ENAS]] )
	- _We observe that the computational
	  bottleneck of NAS is the training of each child model to
	  convergence, only to measure its accuracy whilst throwing
	  away all the trained weights._
-
-
	-
	-
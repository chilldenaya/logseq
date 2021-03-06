-
- What
	- Reinforcement Learning adalah bagian dari machine learning
		- Usually we categorize machine learning as supervised, unsupervised, and reinforcement learning
	- Supervised and unsupervised learning are usually one-shot,
	  myopic, considering instant rewards; while reinforcement learning is sequential, far-sighted, considering long-term accumulative rewards. (https://arxiv.org/pdf/1810.06339.pdf)
	- **Reinforcement learning is usually about sequential decision making**
	  id:: 622f5252-5a41-4373-95f7-9d9818e09ed0
	- ![image.png](../assets/image_1647267881989_0.png)
		- An RL agent interacts with an environment over time. At each time step t, the agent receives a state st in a state space S, and selects an action at from an action space A, following a policy π(at|st), which is the agent’s behavior, i.e., a mapping from state st to actions at. The agent receives a scalar reward rt, and transitions to the next state st+1, according to the environment dynamics, or model, for reward function R(s, a), and, state transition probability P(st+1|st, at), respectively
-
- EXPLORATION VS. EXPLOITATION
	- The exploration vs exploitation dilemma is about the agent needs to exploit the currently best action to maximize rewards greedily, yet it has to explore the environment to find better actions, when the policy is not optimal yet, or the system is non-stationary.
	- An RL agent needs to trade off between exploration of uncertain policies and exploitation of the
	  current best policy, a fundamental dilemma in RL
-
- Deep Reinforcement Learning
	- We obtain deep reinforcement learning (deep RL) methods when we use deep neural networks to
	  represent the state or observation, and/or to approximate any of the following components of reinforcement learning: value function, vˆ(s; θ) or qˆ(s, a; θ), policy π(a|s; θ), and model (state transition function and reward function).
	- Deep RL algorithms are able to take in very large inputs (e.g. every pixel rendered to the screen in a video game) and decide what actions to perform to optimize an objective (eg. maximizing the game score) (https://en.wikipedia.org/wiki/Deep_reinforcement_learning#cite_note-francoislavet2018-1)
	- Deep reinforcement learning has been used for a diverse set of applications including but not limited to robotics, video games, natural language processing, computer vision, education, transportation, finance and healthcare. [1]
-
-
- # Sutton - Reinforcement Learning
- ## 1.1 Reinforcement Learning
- ### Introduction
- Reinforcement learning problems involve learning what to do—how to map situations to actions—so as to maximize a numerical reward signal
- These three characteristics
	- 1. being closed-loop in an essential way,
		- they are closed-loop problems because the learning system’s actions influence its later inputs
	- 2. not having direct instructions as to what actions to take,
		- must discover which actions yield the most reward by trying them out
	- 3. and where the consequences of actions, including reward signals,
		- actions may affect not only the immediate reward but also the next situation and, through that, all subsequent rewards
	- play out over extended time periods—are the three most important distinguishing features of reinforcement learning problems.
- Agent
	- Clearly, such an agent must be able to sense the state of the environment to some extent
	  and must be able to take actions that affect the state
- Reinforcement learning is different from unsupervised learning
	- unsupervised learning is typically about finding structure hidden in collections of unlabeled data.
	- Although one might be tempted to think of reinforcement learning as a kind of unsupervised learning because it does not rely on examples of correct behavior, reinforcement learning is trying to maximize a reward signal instead of trying to find hidden structure
-
- ### Exploration vs Exploitation
- One of the challenges that arise in reinforcement learning, and not in other kinds of learning, is the trade-off between exploration and exploitation
- Exploitation:
	- To obtain a lot of reward, a reinforcement learning agent must prefer actions that it has tried in the past and found to be effective in producing reward
- Exploration:
	- But to discover such actions, it has to try actions that it has not selected before
-
- ## 1.2 Examples
- A master chess player makes a move. The choice is informed both by planning—anticipating possible replies and counterreplies—and by immediate, intuitive judgments of the desirability of particular positions and moves.
- All involve interaction between an active decision-making agent and its environment, within which the agent seeks to achieve a goal despite uncertainty about its environment
- The agent’s actions are permitted to affect the future state of the environment thereby affecting the options and opportunities available to the agent at later times
- In all of these examples the agent can use its experience to improve its performance over time. The chess player refines the intuition he uses to evaluate positions, thereby improving his play
-
- ## 1.3 Element of Reinforcement Learning
- Beyond the agent and the environment, one can identify four main subelements of a reinforcement learning system:
	- a policy,
	- a reward signal,
	- a value function, and, optionally,
	- a model of the environment
-
- ## Policy
- A policy defines the learning agent’s way of behaving at a given time
- a policy is a mapping from perceived states of the environment to actions to be taken when in those states
	- states + policy -> action
- The policy is the core of a reinforcement learning agent in the sense that it alone is sufficient to determine behavior. In general, policies may be stochastic.
-
- ## Reward
- A reward signal defines the goal in a reinforcement learning problem
- On each time step, the environment sends to the reinforcement learning agent a single number, a reward
- The reward signal thus defines what are the good and bad events for the agent
- The agent’s sole objective is to maximize the total reward it receives over the long run
- The reward signal is the primary basis for altering the policy. If an action selected by the
  policy is followed by low reward, then the policy may be changed to select some other action in that situation in the future
-
- ## Value Function
- a value function specifies what is good in the long run
- value of a state is the total amount of reward an agent can expect to accumulate over the future, starting from that state.
- values indicate the long-term desirability of states after taking into account the states that are
  likely to follow, and the rewards available in those states. For example, a state might always yield a low immediate reward but still have a high value because it is regularly followed by other states that yield high rewards
- Rewards are basically given directly by the environment, but values must be estimated and re-estimated from the sequences of observations an agent makes over its entire lifetime
- There is a methods that do not appeal to value functions.
	- called **policy gradient methods**
	- These methods search in spaces of policies defined by a collection of numerical parameters
	- They estimate the directions the parameters should be adjusted in order to most rapidly improve a policy’s performance
	- they produce these estimates while the agent is interacting with its environment and so can take
	  advantage of the details of individual behavioral interactions
-
- ## Environment Model
- This is something that mimics the behavior of the environment, or more generally, that allows inferences to be made about how the environment will behave
- given a state and action, the model might predict the resultant next state and next reward
- Methods for solving reinforcement learning problems that use models and planning are called model-based methods, as opposed to simpler model free methods that are explicitly trial-and-error learners
-
- # Temporal-Difference Learning
- Combination of monte-carlo ideas and dynamic programming
- TD methods can learn directly from raw experience wdithout a model of the environment’s dynamics (monte carlo approach)
- TD methods update estimates based in part on other learned estimates, without waiting for a final outcome (dynamic programming)
- ![image.png](../assets/image_1650435800227_0.png){:height 247, :width 414}
- For any fixed policy π, the TD algorithm described above has been proved to converge to Vπ, in the mean for a constant step-size parameter if it is sufficiently small, and with probability 1 if the step-size parameter decreases according to the usual stochastic approximation conditions (2.7).
- One of the most important breakthroughs in reinforcement learning was the development of an off-policy TD control algorithm known as Q-learning
- In  this  case,  the  learned  action-value  function, Q, directly approximates q∗,the optimal action-value function,  independent of the policy being followed
- ![image.png](../assets/image_1650437119921_0.png){:height 242, :width 556}
- Pertanyaan: apa itu episode??
	- Recall that an episode consists of an alternating sequence of states and state–action pairs:
	- dataset:
		- indosum
		- liputan6
		- xlsum indonesia
-
- # Q Learning
- Must read: https://theaisummer.com/Deep_Q_Learning/
-
- Deep Q-learning:
	- in Q-learning (and in general value based reinforcement learning) we are typically interested in learning a Q-function, 𝑄(𝑠,𝑎). This is defined as
	  𝑄(𝑠,𝑎)=𝔼𝜋[𝐺𝑡|𝑆𝑡=𝑠,𝐴𝑡=𝑎].
	- For tabular Q-learning, where you have a finite state and action space you can maintain a table lookup that maintains your current estimate of the Q-value. Note that in practice even the spaces being finite might not be enough to not use DQN, if e.g. your state space contains a large number, say 1010000, of states, then it might not be manageable to maintain a separate Q-function for each state-action pair
	- n Q-learning (and in general value based reinforcement learning) we are typically interested in learning a Q-function, 𝑄(𝑠,𝑎). This is defined as
	  𝑄(𝑠,𝑎)=𝔼𝜋[𝐺𝑡|𝑆𝑡=𝑠,𝐴𝑡=𝑎].
	- For tabular Q-learning, where you have a finite state and action space you can maintain a table lookup that maintains your current estimate of the Q-value. Note that in practice even the spaces being finite might not be enough to not use DQN, if e.g. your state space contains a large number, say 10^10000, of states, then it might not be manageable to maintain a separate Q-function for each state-action pair
-
- # Deep Q Network
- Here we use recent advances in training deep neural networks to
  develop a novel artificial agent, termed a deep Q-network, that can
  learn successful policies directly from high-dimensional sensory inputs
  using end-to-end reinforcement learning
	- their applicability has previously
	  been limited to domains in which useful features can be handcrafted,
	  or to domains with fully observed, low-dimensional state spaces
- We set out to create a single algorithm that would be able to develop
  a wide range of competencies on a varied range of challenging tasks—a
  central goal of general artificial intelligence
- a deep Q-network
  (DQN), which is able to combine reinforcement learning with a class
  of artificial neural network known as deep neural networks
- the goal of the agent is to select actions in a fashion that maximizes cumulative future
  reward. More formally, we use a deep convolutional neural network to
  approximate the optimal action-value function
- Reinforcement learning is known to be unstable or even to diverge
  when a nonlinear function approximator such as a neural network is
  used to represent the action-value (also known as Q) function <DQN>
	- First, in online gradient-based temporal-difference reinforcement learning algorithms, approximating the action-value function often leads to instability <DQN survey>
- The key technique to achieve stability in DQN is
  experience replay
	- In specific, a replay memory is used to store the trajectory of the Markov decision process (MDP).
	- At each iteration of DQN, a mini-batch of states,
	  actions, rewards, and next states are sampled from the replay memory as observations to train the
	  Q-network, which approximates the action-value function.
	- The intuition behind experience replay
	  is to achieve stability by breaking the temporal dependency among the observations used in training
	  the deep neural network
-
- # DQN for Text Summarization
- <> (20xx) memanfaatkan Deep Q-Network untuk menyelesaikan masalah peringkasan teks otomatis bertipe ekstraktif. Tujuannya adalah membentuk Deep Q-Network yang mampu membuat ringkasan terbaik dengan cara memilih action (kalimat yang dimasukkan ke dalam sum di iterasi tersebut) sesuai dengan state summary dan reward di tiap iterasinya. Proses learning dilakukan berdasarkan pasangan dokumen dan gold summary terkait.
- Dalam tiap iterasi learningnya, proses teks summarization dapat dibagi menjadi tiga bagian besar, sentence encoding, document encoding, dan reinforcement learning.
- Gambar II.x menunjukkan arsitektur DQN-text summarization.
- ## Sentence Encoder
- Di tahap pertama, CNN/RNN model digunakan untuk melakukan proses information extraction melalui sentence encoding, yaitu menerima vektor representasi kata dari suatu kalimat, lalu merepresentasikan  tiap-tiap kalimat tersebut sebagai suatu vektor.
- RNN structure:
	- ...
- CNN structure:
	- ...
- ## Document Encoder
- Setelah itu, output dari CNN/RNN pada tahapan pertama akan menjadi masukan untuk RNN tahap dua yang akan digunakan untuk membangun hidden state representation dari masing-masing kalimat. Hasil representasi tiap kalimat ini lalu digunakan untuk membangun representasi dokumen secara utuh dengan cara melakukan transformasi non-linier.
- Formula II.x menunjukkan proses pembentukan document representation.Oleh karena itu, tahap kedua ini dapat juga kita pandang sebagai proses document encoding.
- hidden state representation = local sentential information, document representation= global sentential information
- The hierarchical network consisting of sentence en-coder and document encoder not only learns the representations of the internal states for the DQN, but also generates a set of ac-tion representations for sentences in document
- ## DQN Training
- Algoritma II.x menunjukkan proses iterasi DQN training. Proses learning dilakukan secara iteratif, dengan tiap iterasinya menghasilkan suatu state, action, reward, dan q-value function.
- hidden state representation dari masing-masing kalimat bersama dengan document representationnya akan digunakan untuk mengaproksimasi q-value masing-masing kalimat.
- berikut merupakan rumusan aproksimasi Q value
- i menunjukkan, j menunjukkan, Wc, Ws, Wr, Wp menunjukkan, Sum_i menunjukkan vektor representation dari summary (state) di iterasi tersebut, dengan formula II.x
- Dengan Q-value ini, action dapat dipilih dengan menggunakan proses epsilon-greedy policy.
- reward dihitung dengan cara menghitung nilai ROUGE dari summary yang terbangun di iterasi tersebut dengan gold summary yang ada.
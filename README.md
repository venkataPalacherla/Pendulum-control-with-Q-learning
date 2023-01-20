# Pendulum-control-with-Q-learning
Implemented Q-learning on a pendulum to invert the position state of pendulum.
 <p align = 'center'><img src = "Assets/inversePendulum.gif"></p>  

$$
\begin{algorithm}[htb]
\caption{Q-learning}\label{alg:q_learning}
\begin{algorithmic}[1]
\State Set $\gamma \in [0, 1]$, $\epsilon$ and $\alpha$.
\State Initialize $Q(x, u)$ for all states and controls .
\For{$episode$ in $episodes$}
\State Initialize state $x_0$
\For{$step$ in $episode$}
\State Choose a control using $\epsilon$-greedy policy from $Q$ 
\State calculate $x_{t+1}$
\State Compute $g(x_{t}, \mu(x_t))$ 
\State Compute delta error using $\alpha$  
\State Update $Q(x_t, u_t)$
\EndFor
\EndFor
\end{algorithmic}
\end{algorithm}


$$

# Markov Property
"The future is independent of the past given the present"
미래는 현재가 주어지면 과거로부터 독립이다.

## Markov Property

--------------------------------------------------------------------
**Definition**
A state $S_t$ is Markov if and only if 
$$
\mathbb{P}[S_{t+1}|S_t] = \mathbb{P}[S_{t+1}|S_1, \cdots, S_t].
$$
--------------------------------------------------------------------
The state captures all relevant information from the history.
state는 history에서 모든 관련 정보를 수집한다.
Once the state is known, the history may be thrown away.
state가 알려지면, history는 버려질 수 있다. (?)
The state is a sufficient statistic of the future.
state는 미래에 대한 충분 통계량이다.
# State Transition Matrix
For a Markov state $s$ and successor state $s'$, the state transition probability is defined by
$$
\mathcal{P}_{ss'} = \mathbb{P}[S_{t+1}=s'|S_t=s].
$$
State transition matrix $\mathcal{P}$ defines transition probabilities from all states $s$ to all successor states $s'$,
$$
\mathcal{P} = from 
\begin{bmatrix}
\mathcal{P}_{11} & \cdots & \mathcal{P}_{1n} \\
\vdots & \ddots & \vdots \\
\mathcal{P}_{n1} & \cdots & \mathcal{P}_{nn}
\end{bmatrix},
$$
where each row for the matrix sums to 1.
행렬의 행의 합이 1이어야 한다.
# Markov Process
A Markov Process is a memoryless random process, i.e. a sequence of random states $S_1, S_2, \cdots$ with the Markov property.

--------------------------------------------------------------------
**Definition**
A Markov Process (or Markov Chain) is a tuple $\langle\mathcal{S}, \mathcal{P}\rangle$ 
- $\mathcal{S}$ is a (finite) set of states
- $\mathcal{P}$ is a state transition probability matrix,
	$\mathcal{P}_{ss'} = \mathbb{P}[S_{t+1}=s'|S_t=s]$
--------------------------------------------------------------------

> in Graph Neural Networks, 
> 	adjacency matrix가 state transition matrix와 개념이 동일하므로, 
> 	adaptive adjacency matrix에 활용할 수 있을 것으로 예상


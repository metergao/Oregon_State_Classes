################################################################################
Tue 03/28
################################################################################
Turing test - Can a human determine if they are talking to a computer or a human.
    * Problems
        - Not reproducible
        - Can't be analyzed mathematically
        - Tends to focus on homanslike errors
        - Does not produce useful competer programs

Cognitive Modeling (Thinking Humanly)
    * Models of the internal workings of the human mind.

################################################################################
Thu 03/30
################################################################################
*Rational Agents*
    Agent: Something that acts.
    Rational: means more than just logically justified. It also means "doing the right thing"
    Rational Agent: An agent that acts to acheve the best outcome given its resources.

*Vocab*
Agent:              Anything that perceives its environment through sensors and acts on the environment through actuators.
Percept sequence:   A complete history of everything the agent has ever perceived. 
Agent function:     Maps precept sequence to action.
Agent program:      Implements the agent function.
Rationality:        Do the actions that cause the agent to be most successful.
    1) Performance measure of success
    2) Agents's prior knowledge of environment
    3) Actions agent can perform
    4) Agents's percept sequence to date

*Learning*
1) Initially, designers compute some prior knowledge to include in policy.
2) When deciding its next action, agent does some computation

Performance, Environment, Actuators, Sensors (PEAS Descriptions of Task environments)


*Properties of Onvironmonts*
Fully Observable: Can access complete state of environment at each point in time.
    - Partially observable: Could be due to noisy, inaccurate sensor data
Deterministic: If next state of the environment completely determined by current state and agent's action
    - Stochastic: A partially observable environment can appear to be stochastic. 
    - Strategic:  Environment is deterministic except for actions of other agents.
Episodic: Agent's experience divided into independent' atomic episodes in which agents perceives and performs a single action in each episode.
    - Sequential: Current decision affects all future decisions.
Static: Agent doesn't need to keep sensing while decides what action to take, doesn't need to worry about time.
    - Dynamic: Environment changes while agent is thinking.
    - Semidynamic: environment doesn't change with time but agent's performance does
Discrete: The states, the actions, the environment.
    - Continuous 


################################################################################
Thu 04/01
################################################################################

*Search*
    1) A finite set of statets S
    2) A notn-empty set of initial states I (subset) S
    3) A notn-empty set of goal states I (subset) S
    4) Sucsessors where to go next
    5) Cost what is the cost of each state.

Search Tree:
    Start with the Inital state.
    Order in which you expand nodes.
    Avoid repeated states.

Uninformed Search Strategies
    No Information

    * Completeness      - Guaranteed the find a solution
    * Optimality        - Does it find the optimal solution?
    * Time Complexity   - How long does it take?
    * Space complexity  - How much memory does it take?

Complexity
    1) Branching factor - maximum number of successors from the node.
    2) Depth            - Shollowest goal node
    3) Maximum length   - Lenght of the path to the goal


################################################################################
Tue 04/04
################################################################################
**Uniformed Search**

Depth-first Search
* Complete?     No - can go infininte depth
* Optimal?      No - Can have shallower goals
* Time complex  O(b^m)
* space complex O(bm)

Depth-simitde Search
- Solves infinite path problem by using predetermined depth limit l
- Nodes depth l are threated as if they have no successors

* Complete?     No - Goal can be past limit
* Optimal?      No - Can have shallower goals
* Time complex  O(b^l)
* space complex O(bl)

Bidircetional search
- Run on search forward and one backwards

* Complete?     yes - provided branching factor is finite
* Optimal?      yes - If the setp costs are identical in both directions
* Time complex  O(b^(d/2))
* space complex O(b^(d/2))



## Proof 1
Turing answers the halting problem, that is, the question of if a computing program can determine if any program is finite or continues in a circular loop.

- Establish the existence of two algorithms, machine *H* and machine *D*. 
- Every number that exists represents a different algorithm.
- Every algorithm is either circular (when computed, the computing machine enters an infinite loop), or circle-free (when computed, the computing machine eventually stops).
- Each algorithm is represented as a string of symbols, that presumably produces an output. These strings are represented as $S.D.$
	- By extension, Machines D and H each possess their own respective $S.D.$ 

The ultimate responsibility of machine H is to evaluate the integrity of the algorithm that exists under every number, whether it is circular or circle-free. When it is done, machine H should produce a diagonal number of 0s and 1s which ultimately defines the set which represents all algorithms that are circle-free. 

**By this definition, Machine H is a circle-free algorithm, as it should stop when it has evaluated every circle-free algorithm.**


Machine H evaluates algorithms by taking number $N$ and parsing it into string $S.D$, which is then passed to Machine D. Machine D works under machine H and uses a number of arbitrary heuristics to determine whether string $S.D.$ is circle-free, or if it continues forever (Turing). 
- If Machine D returns an unsatisfactory answer, Machine H continues to the next number.
- If Machine D returns a "satisfactory" answer, in other words, it determines that an algorithm is circle-free, machine H verifies it as such by emulating or running the algorithm itself and determining that the computing machine does not enter an infinite loop.
#### Scenario
- Machine H has tested an arbitrary number of algorithms (e.g., $N=6501$), of which 3 numbers have been satisfactory (circle-free).
- Machine H reaches it's own algorithm, $N=6502$. $N$ is converted by Machine H into algorithm $K$, which is identical to the algorithm of Machine H.
- As algorithm $K$ is identical to that of Machine H, Machine D must by definition determine it to be circle-free. It returns this to Machine D. Provided with a satisfactory algorithm, Machine D begins to verify the satisfiability of algorithm $K$.
- Algorithm $K$ is run until the algorithm is tasked with evaluating the satisfiability of $N=6502$, which has the same $S.D.$ or algorithm as algorithm $K$. Being that this $S.D.$ being verified within algorithm $K$ is identical to that of algorithm $K$, it is verified as circle-free. Within algorithm $K$, this $S.D.$ is verified once more.
- Because of this, Machine H will never reach $N=6503$; it is forced to verify that Machine H's $S.D.$ is circle-free *ad infinitum.* With this, the premise that Machine H is circle-free is contradicted, as in verifying that Machine H is circle-free, it enters the same circular nature that a circular algorithm does.

With this, the hypothetical Machine H will never evaluate every circle-free algorithm. 
## Proof 2
- Establish the existence of two machines, Machine E and Machine M.
- Machine E's responsibility is to determine whether Machine M ever prints a given symbol, given the $S.D.$ of Machine M.

1. $\exists{x}E(x)\rightarrow \exists(x)G(x)$, where the responsibility of Machine G is to determine if Machine M prints the symbol '0' infinitely often.
2. $\exists(x)E(x)\rightarrow \exists(x)G'(x)$, where the responsibility of Machine G' is to determine if Machine M prints the symbol '1' infinitely often.
3. Subsequently, the existence of Machine E entails that there exists a process that can determine whether M can print an infinity of figures. 
4. If this process can determine if M can print an infinity of figures, Machine E can determine that Machine M is circle-free.
5. Proof 1 states that no machine or algorithm can validate that a machine is circle free.

With this, Machine E is impossible. 

### Proof 3/Conclusion
No general algorithm can solve all mathematical problems. There exists a limit to the scope of questions that computation can answer. 


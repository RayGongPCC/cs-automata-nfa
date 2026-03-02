# cs-automata-nfa

At first I mixed up problems where the accept condition depends on only one symbol (e.g., counting 1’s) with problems that require tracking constraints for both inputs (0 and 1).
If only one symbol matters, the DFA/NFA only needs to track one “dimension” (like mod counting or parity). But if both 0 and 1 constraints exist, I must track two dimensions at once (e.g., #1 mod 3 + #0 parity) using a product-style construction. The accepting state must satisfy both constraints simultaneously.

I was also unsure when ε-transitions were appropriate. I learned that ε is useful when the NFA needs to move or branch without consuming input, such as:

branching into multiple possible paths from the start,

connecting sub-automata for union/concatenation/star without reading a symbol,

representing “choice” or “glue,” not replacing required 0/1 reads.
For pure counting constraints in a DFA, ε is usually unnecessary.

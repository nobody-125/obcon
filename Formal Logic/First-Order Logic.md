First-order logic is a language that builds upon the syntax used by TRUTH FUNCTIONAL LOGIC, the most important additions being quantified variables, which allow the use of sentences that contain their own variables.
* **Name:** A referrer expressed as a lowercase letter
* **Predicate:** A property which can be bound to names, expressed as an uppercase letter.
* **Quantifier:** Permits claims about objects in a **domain.** The universal quantifier ($\forall$) applies to everything in the domain, the existential quantifier ($\exists$) permits specific claims about objects in a domain.
* **Domain:** Classifies the range of "objects" under discussion, influences the interpretation of quantifiers.
##### Deriving Double Negation Elimination
There does not exist a rule for "double negation elimination", in other words, $¬(¬P)\rightarrow P$, however, this may be obtained using derived rules.
### Quantifier Scope
- Original statement: Every dog owner is the friend of a dog owner.
- Half translation: For any *x* that is a dog owner, there is a dog owner who *x* is a friend of.
- Initial translation: $\forall x[x \text{ is a dog owner} \rightarrow \exists y(y \text{ is a dog owner who } x \text{ is a friend of.}$ 
- Complete translation: $\forall x [\exists x (Dz \land O(x,z))\rightarrow \exists y(\exists z (Dz \land O(y,z) \land F(x,y))]$ 
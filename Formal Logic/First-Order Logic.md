### Quantifier Scope
- Original statement: Every dog owner is the friend of a dog owner.
- Half translation: For any *x* that is a dog owner, there is a dog owner who *x* is a friend of.
- Initial translation: $\forall x[x \text{ is a dog owner} \rightarrow \exists y(y \text{ is a dog owner who } x \text{ is a friend of.}$ 
- Complete translation: $\forall x [\exists x (Dz \land O(x,z))\rightarrow \exists y(\exists z (Dz \land O(y,z) \land F(x,y))]$ 
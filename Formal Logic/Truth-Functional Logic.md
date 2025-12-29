- Conjunction introduction:
	- $A:R1$
	- $B:R2$
	- $A\rightarrow B:\,\rightarrow I\,3-4$
- Conjunction elimination:
	- $A\land B:R1$
	- $A:\land\,\exists\, 2$
- Conditional elimination:
	- $A\rightarrow B:R1$
	- $A:R2$
	- $B:\,\rightarrow \exists\,4,3$
##### Examples
$P\rightarrow R\vdash (P\lor Q)\rightarrow((Q\rightarrow R)\rightarrow R)$ 
1. $P\rightarrow R$
	2. $P\lor Q$
		3. $Q\rightarrow R$
			4. $P:\text{AS}$
			5. $R:\,\rightarrow \exists\, 4,1$ 
			6. $Q:\,\text{AS}$
			7. $R:\,\rightarrow\exists\,6,3$
		(8.) $R:\lor\exists\,2,4-5,6-7$
	(9.) $(Q\rightarrow R)\rightarrow R:\rightarrow \text{I}\, 3-8$
(10.) $(P\lor Q)\rightarrow ((Q\rightarrow R)\rightarrow R):\text{I}\,2-9$
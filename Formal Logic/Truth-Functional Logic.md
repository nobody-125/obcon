- Conditional introduction:
	- $P:\text{R}1$
	- $Q:\text{R}2$
	- $P\rightarrow Q:\,\rightarrow \text{I}\,3-4$
-  Conditional elimination:
	- $P\rightarrow Q:\text{R}1$
	- $P:\text{R}2$
	- $Q:\,\rightarrow \exists\,4,3$
- Conjunction introduction:
	- $P:\text{R}1$
	- $Q:\text{R}2$
	- $P\land Q:\land\,\text{I}\,3-4$
- Conjunction elimination:
	- $P\land Q:\text{R}1$
	- $P:\land\,\exists\, 2$
- Disjunction introduction:
	-  $P:\text{R}1$
	- $Q:\text{R}2$
	- $P\lor Q:\lor\,\text{I}\,3-4$
- Disjunction elimination:
	- $P\lor Q:\text{R}\,1$
		- $P:\text{AS}$
		- ...
		- $C$
		- $Q:\text{AS}$
		- ...
		- $C$
	- $C:\lor\,\exists\,2,3-5,6-7$
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

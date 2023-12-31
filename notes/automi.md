Automi finiti
------
Gli automi finiti sono spesso chiamati anche *automi a stati finiti*, e sono strumenti *modellistici*

Un *automa finito deterministico (AFD)*, può essere visto come un calcolatore elementare dotato di stato intero e supporto unidirezionale di input. 

- il **funzionamento** consiste di trasizioni di stato dopo che è stato letto un simbolo in input. 
	- ad ogni stato _q_ sono associate azioni che l'automa esegue quando transita in _q_

Un automa AFD M è una quintupla M=(Σ, Q, $q_k$ , $Q_f$, δ)
dove:
	- Σ è l'alfabeto
	- Q è un insieme finito chiamato *insieme di stati dell'automa*
	- $q_0$ è un elemento speciale di Q detto *stato iniziale*
	- $Q_f \subseteq Q$ è l'insieme di stati finali detti anche *stati di accettazione dell'input*
	- δ è la funzione che determina le transizioni di stato, mappando coppie *<stato,simbolo>* 


#### Computazione di un automa
---
Ad ogni passo, l'automa si trova in uno stato *q*, legge un simbolo *x* dall'input e transita nello stato determinato da $\delta(q,x)$.

Finisce di computare in uno dei due casi:
1. **ho finito di leggere tutta la sequenza di input**
2. **la funzione di transizione è indefinita per lo stato attuale e il simbolo in lettura**
Tipicamente, le computazioni hanno un costo di *O(n)*. 



> Gli automi sono rappresentati tramite i *diagrammi di transizione*. 
> 	- sono dei grafi i cui nodi sono gli stati e archi le transizioni.
> 	- ogni arco è etichettato da un simbolo in input
> 	- gli statati finali sono accerchiati doppiamente
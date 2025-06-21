100 prisoner problem implemented in the notebook.

Too lazy to write some more so I'll add Wikipedia Copy/Paste to the README :

The 100 prisoners problem has different renditions in the literature. The following version is by Philippe Flajolet and Robert Sedgewick:[1]

_The director of a prison offers 100 death row prisoners, who are numbered from 1 to 100, a last chance. A room contains a cupboard with 100 drawers. The director randomly puts one prisoner's number in each closed drawer. The prisoners enter the room, one after another. Each prisoner may open and look into 50 drawers in any order. The drawers are closed again afterwards. If, during this search, every prisoner finds their number in one of the drawers, all prisoners are pardoned. If even one prisoner does not find their number, all prisoners die. Before the first prisoner enters the room, the prisoners may discuss strategy — but may not communicate once the first prisoner enters to look in the drawers. What is the prisoners' best strategy?_

If every prisoner selects 50 drawers independently and randomly, the probability that a single prisoner finds their number is 50%. The probability that all prisoners find their numbers is the product of the single probabilities, which is (⁠1/2⁠)100 ≈ 0.0000000000000000000000000000008, a vanishingly small number. The situation appears hopeless. 

Surprisingly, there is a strategy that provides for the survival of all the prisoners with probability more than 30%. The key to success is that the prisoners do not have to decide beforehand which drawers to open. Each prisoner can use the information gained from the contents of every drawer they already opened to decide which one to open next. Another important observation is that this way the success of one prisoner is not independent of the success of the other prisoners, because they all depend on the way the numbers are distributed.[2]

To describe the strategy, not only the prisoners, but also the drawers, are numbered from 1 to 100; for example, row by row starting with the top left drawer. The strategy is now as follows:[3]

_Each prisoner first opens the drawer labeled with their own number.
If this drawer contains their number, they are done and were successful.
Otherwise, the drawer contains the number of another prisoner, and they next open the drawer labeled with this number.
The prisoner repeats steps 2 and 3 until they find their own number, or fail because the number is not found in the first fifty opened drawers._

If the prisoner could continue indefinitely this way, they would inevitably loop back to the drawer they started with, forming a permutation cycle (see below). By starting with their own number, the prisoner guarantees they are on the specific cycle of drawers containing their number. The only question is whether any cycle is longer than fifty drawers - and only one cycle can possibly be too long, since at most one can comprise more than half of the total drawers. 
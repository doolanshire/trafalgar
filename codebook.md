# Trafalgar
A small database in CSV format holding information on the ships that fought at the battle of Trafalgar.

The file is comma-separated and each row corresponds to a single ship.

Ships are first sorted thus:

1. British fleet (four sub-groups)
 * Attacking the head of the Franco-Spanish fleet (*HMS Africa* only)
 * Weather Column
 * Lee Column
 * Attached (frigates and smaller vessels)

2. Franco-Spanish fleet (two sub-groups)
 * Line of battle
 * Attached (frigates and smaller vessels)

Within each group, ships are sorted by sailing order.

## Variables

* **ship**: the name of the ship.
* **type**: the ship type, from the following factors:
	* 4-decker
	* 3-decker
	* 2-decker
	* Frigate
	* Brig
	* Cutter
	* Schooner
* **guns**: the number of guns mounted on the ship at the moment of the battle. Carronades are included.
* **fleet**: the fleet the ship belongs to, from one of the three factors:
	* British
	* French
	* Spanish
* **construction**: nation which built the ship, to account for captured vessels. Four possible factors:
	* British
	* French
	* Spanish
	* Cuban
* **commander**: the officer commanding the ship.Two names (separated by a comma) are listed for flagships, and for ships that had their commander killed in action or as a direct consequence of it. In the latter case, the symbol '†' (killed in action) or '(DOW)' (Died Of Wounds) is appended to the deceased officer's name. Uniquely, Capt. Don Antonio Pareja of *Argonauta* is listed '(WIA)' (Wounded In Action).
* **group**: the group the ship operated in. One of the following factors:
	* Attacking the head of the Franco-Spanish fleet (*HMS Africa* only)
	* Weather Column (British fleet only)
	* Lee Column (British fleet only)
	* Line of Battle (Franco-Spanish fleet only)
	* Attached (British and Franco-Spanish fleets)
* **order**: sailing order of the ship *within its group*. Bear in mind this variable is **not** unique.
* **complement**: the crew complement of the ship.
* **killed**: number of men killed in the course of the action.
* **wounded**: number of men wounded in the course of the action.
* **total**: total number of casualties suffered by the ship's complement in the course of the action. The sum of killed and wounded.
* **percentage**: the percentage of the ship's complement having become a casualty (killed or wounded) in the course of the action. The value of this column is an *integer*. If more precision is desired, simply calculate the percentage from the appropriate columns.

## Sources

* ADKIN, Mark – *The Trafalgar Companion* (2005)
* GOODWIN, Peter – *The Ships of Trafalgar: the British, French, and Spanish fleets, 21 October 1805* (2005)

## License

The database is offered under the [ODC-By](https://opendatacommons.org/licenses/by/1-0/) license. Unless otherwise stated, any other bits of code and scripting are available under the [MIT License](https://opensource.org/licenses/MIT).

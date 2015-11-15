# timemachine
## Functional Requirements From User Perspective
1. Enter all the events they want a schedule to be made from to create a 'shopping' list
	* User can choose a blacklisted/whitelisted timeslot for an event. Eg. Breakfast is only between 8am and 11am.
2. Enter blacklisted times
3. Pinned and unpin times for events so that timeblock is temporarily blacklisted.
4. Click and drag events to other times
	* Hovering over an event shows all other possible times for it
	* If moved into a timeslot already occupied, the incumbent event's timeslot is automatically recalculated.
## Development Requirements 
### Backend	
* Compute all permutations on backend once and serve it when they click generate
* Permutation algorithm
* Output JSON/XML, etc. of final schedule choice to be used by Google Calendar, etc.
### Frontend
* Session storage to temporarily cache the user's events
* Hovering over an event highlights all other possible slots on calendar 
* Draggable events on a calendar
	* When element is hovering over an occupied timeslot, imcumbent event moves to some other possible spot
		* If there's no other available slot for incumbent, it gives some sort of notification.
		* Algorithm that chooses the other possible slot from the set based on perhaps preference parameters
	

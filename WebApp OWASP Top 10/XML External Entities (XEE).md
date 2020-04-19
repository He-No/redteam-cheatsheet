Attacking systems that parse XML input

<?xml version="1.0" encoding="ISO-8859-1"?>
<!DOCTYPE gift {
	<!ENTITY from "<payload>">
]>

<gift>
	<To>Frank</To>
	<From>&from;</From>
	<Item>Pokemon Cards</Items>
</gift>


### payload @git of PayloadAllThings
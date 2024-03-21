```kotlin

val data = mapOf(Name to "Greta", Nickname to "Eco warrior", AKA to "Captain Planet", Occupation: "Unemployed")
val matchingResult = data.filter { it.value.split(" ").size == 2 }
val newObjModified = data.mapValues { it.value.toUpperCase() }
```

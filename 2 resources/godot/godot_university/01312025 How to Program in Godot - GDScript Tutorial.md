---
Date: 2025-01-31T11:00:00
tags:
  - game-making
  - godot
  - youtube
---
# labels
How to edit labels in script:
```
# Called when the node enters the scene tree for the first time.
func _ready() -> void:

	# sets label to say Hello World!
	$Label.text = "Hello World!"

	# turn label sea green
	$Label.modulate = Color.SEA_GREEN

# Create function that sets color based on "my_action" trigger (bound to spacebar)
func _input(event: InputEvent) -> void:

	# turns label red when spacebar pressed
	if event.is_action_pressed("my_action"):
		$Label.modulate = Color.RED
	
	# turns label green	when spacebar released
	if event.is_action_released("my_action"):
		$Label.modulate = Color.GREEN
```

# input
Health system:
```
extends Node

var health = 100 # create health variable and assign a value to it

func _ready() -> void:
	
	health = 40 # assign to value
	health = 20 + 30 # assign to calculation
	health += 20 # add
	health -= 10 # subtract
	health *= 4 # multiply
	health /= 2 # divide
	
	print(health) #print the current value of the health variable
```

Remove health when spacebar is pressed:
```
extends Node

var health = 100 # create health variable and assign a value to it

func _input(event: InputEvent) -> void:
	if event.is_action_pressed("my_action"): # if action is pressed (spacebar), do:
		health -= 20 # subtract 20 from health value
		print(health) # print health
```

# if-statements
if = condition that needs to be met

example:
```
	if health <= 0: # if health value is <= 0
		health = 0
		print("YOU DIED")
```
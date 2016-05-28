# Storage

## YAML
YAML is a encoding format that makes data more readable by human beings, it was inspired in languages suchs as XML, Python, Perl, and Internet Message Protocol. It was created by Clark Evans, Brian Ingerson and Oren Ben-Kiki, by the year of 2000.

YAML (pronounced as "yammel"), was designed with a very proper idea, that every data could be represented by a set of list, hashes, and simple values.
YAML only uses unicode characters (UTF-8 and UTF-16)

Examples:
```
	Blocks:
 		- Grass
 		- Sand
 		- Stone

	Users:
 		- Pedro
 		- Marco
 		- João
 		- Andreia
```


In the context of the project that we have been reviewing during this semester, YAML is used to store (Data of course! :D) some configurations related to multiple aspects, such as User data, world data, blocks data, command restrictions, zone restrictions, among others.
An more particular example can be found at [config.yml](https://github.com/sk89q/WorldEdit/blob/master/worldedit-bukkit/src/main/resources/defaults/config.yml)

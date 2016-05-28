# Storage

## YAML
YAML is a encoding format that makes data more readable by human beings, it was inspired in languages suchs as XML, Python, Perl, and Internet Message Protocol. It was created by Clark Evans, Brian Ingerson and Oren Ben-Kiki, by the year of 2000.

YAML (pronounced as "yammel"), was designed with a very proper idea, that every data could be represented by a set of list, hashes, and simple values.
YAML only uses unicode characters (UTF-8 and UTF-16)

YAML is relatively simple to use. The respective file holds the information in a indented format like the example below:

```
	Blocks:
 	- Grass
 	- Sand
 	- Stone

	Users:
 	  Pedro: '- Developer'
 	  Marco: '* Second Developer'
 	  João: '# Developer'
 	  Andreia: '\ Developer'
```

Within the domain of the Java language, YAML fields can be easily accessed using:

```java
	yamlFile.getStringList("Blocks");
	// Will return a list ['Grass', 'Sand', 'Stone']
```

```java
	yamlFile.getConfigurationSection('Users').getKeys(false)
	// Will return ['Pedro', 'Marco', 'Joao', 'Andreia']
	// We can now do:
	
	yamlFile.getString("Users.Pedro");
	// Will return '- Developer'
	
```

In the context of the project that we have been reviewing during this semester, YAML is used to store some configurations related to multiple aspects such as:
* User data
* World data 
* Blocks data 
* Command restrictions
* Zone restrictions, among others.

An more particular example can be found at [config.yml](https://github.com/sk89q/WorldEdit/blob/master/worldedit-bukkit/src/main/resources/defaults/config.yml)

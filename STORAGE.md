# Storage

## YAML
YAML é uma formato de codificação de dados para facilitar a sua leitura por humanos, foi inspirado em linguagens como XML, Python, Perl, assim como no Internet Message Protocol.
Foi proposto em 2000 por Clark Evans, juntamente com Brian Ingerson e Oren Ben-Kiki.

YAML foi desenvolvido na base de que todos os dados, podem ser representados por listas, mapas (hashes), e valores simples.
Utiliza apenas caracteres UTF (unicode).

Exemplos:
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


No contexto do projecto que estivemos a analisar durante este semestre, YAML usa-se para gravar configurações relativas a varios aspectos, tais como dados de utilizadores, blocos do mundo, restrições a comandos, entre outros.
Um exemplo  destes ficheiros pode ser encontrado no ficheiro [config.yml](https://github.com/sk89q/WorldEdit/blob/master/worldedit-bukkit/src/main/resources/defaults/config.yml)

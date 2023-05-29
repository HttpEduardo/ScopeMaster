# Scope Master


## Conteúdo:

- [Instalação](#--instalação--requerimentos)
- [Uso](#--usage--explication)
   - [Uso com metas dentro do escopo](#printing-only-in-scope-targets)
   - [Uso com destinos fora do escopo](#printing-only-in-scope-targets-by-setting-out-of-scope-urls)
   - [Lendo do arquivo de configuração](#reading-from-config-file)
   - [Usando com outras ferramentas](#encadeamento-com-outras-ferramentas)

##  Requerimentos de instalação:

Instalando a ferramenta ->

Usando ir
```bash
▶ instale github.com/HttpEduardo/ScopeMaster
```

Usando git clone
```bash
▶ git clone https://github.com/HttpEduardo/ScopeMaster.git
▶ cd escopo em
▶ chmod +x escopoin
▶ ./scopein -h
```
<br>


##  Uso e Explicação:

Em seu processo de reconhecimento, ao fazer reconhecimento de subdomínio e reconhecimento de URL, você pode obter URLs que não estão no escopo, como: "bit.ly", "twitter.com", urls aleatórios ou subdomínios. Aí vem o scopein, ele só aparece no terminal nas urls do escopo

<br>
  
### Imprimindo apenas em alvos de escopo

Preste atenção na sintaxe!
```bash
URLs de gatos | scopein -s "targetscope.com"
subdomínios cat | scopein -s "targetscope.com|targetscope2.com"
```
 

## Este projeto é apenas para fins educacionais e de recompensa por bugs!

# Scope Master


## Conteúdo:

- [Instalação](#--instalação--requerimentos)
- [Uso](#--usage--explication)
   - [Uso com metas dentro do escopo](#printing-only-in-scope-targets)
   - [Uso com destinos fora do escopo](#printing-only-in-scope-targets-by-setting-out-of-scope-urls)
   - [Lendo do arquivo de configuração](#reading-from-config-file)
   - [Usando com outras ferramentas](#encadeamento-com-outras-ferramentas)

## - Requerimentos de instalação:

Instalando a ferramenta ->

Usando ir
```bash
▶ instale github.com/ferreiraklet/scopein@latest
```

Usando git clone
```bash
▶ git clone https://github.com/ferreiraklet/scopein.git
▶ cd escopo em
▶ vá construir scopein.go
▶ chmod +x escopoin
▶ ./scopein -h
```
<br>


## - Uso e Explicação:

Em seu processo de reconhecimento, ao fazer reconhecimento de subdomínio e reconhecimento de URL, você pode obter URLs que não estão no escopo, como: "bit.ly", "twitter.com", urls aleatórios ou subdomínios. Aí vem o scopein, ele só aparece no terminal nas urls do escopo

<br>
  
### Imprimindo apenas em alvos de escopo

Preste atenção na sintaxe!
```bash
URLs de gatos | scopein -s "targetscope.com"
subdomínios cat | scopein -s "targetscope.com|targetscope2.com"
```

### Imprimindo apenas destinos dentro do escopo, definindo urls fora do escopo
 
```bash
alvos de gato | scopein -b "outscope.com"
alvos de gato | scopein -b "outscope.com|outscope2.com"
```

### Lendo do arquivo de configuração

```bash
alvos de gato
---saída---
https://google.com
https://redacted.com
https://example.com
https://twitter.com

escopo do gato
---saída---
google.com
twitter.com


URLs de impressão do arquivo de configuração do escopo ->
alvos de gato | escopo em -f escopo

Imprimir URLs permitidos de arquivo fora do escopo
alvos de gato | escopo em -bf escopo
```


### Encadeamento com outras ferramentas

```bash
echo "http://testphp.vulnweb.com" | waybackurls | scopein -s "testphp.vulnweb.com"

echo "http://testphp.vulnweb.com" | waybackurls | scopein -b "twitter.com"

echo "http://testphp.vulnweb.com" | hakrawler | scopein -s "testphp.vulnweb.com"

echo "http://testphp.vulnweb.com" | gauplus -b svg,jpg,png,gif,pdf,js,css | escopo em -f escopos

echo "http://testphp.vulnweb.com" | gau | escopo em -bf escopos
```  


## Este projeto é apenas para fins educacionais e de recompensa por bugs!

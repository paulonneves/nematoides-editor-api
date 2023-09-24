# nematoide-filtros-api

## Projeto edição filtros nematoide
Interface que ajuda o usuário a aplicar filtros na imagens afim facilitar a visualização 
de amostras por parte do técnico para analise de nematoides.

OBS: Como trabalhar com imagens em memória:
https://cloudbytes.dev/snippets/received-return-a-file-from-in-memory-buffer-using-fastapi

## Instalação
### Docker containers
Abra o primeiro terminal na pasta Api e construa a imagem do Backend:
```
cd .\Api\ && docker build -t nemabackendfast .
```
Depois execute o container:
```
docker run --name containernema -p 80:80 nemabackendfast  
```
Em outro terminal na raiz do projeto acesse a pasta *frontend* e construa a imagem do frontend vuejs:
```
docker build -t nemafrontendfast .  
```
Por fim execute o container do frontend:
```
docker run -it -p 8030:8030 --rm --name frontendnema nemafrontendfast  
```
### Passos futuros
- [ ] Configurar o Docker Container para facilitar o processo de instalação.
- [ ] Refatorar o Backend para incluir intensidade como atributo de filtro efetivo na operação.

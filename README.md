# trello-import-apps-script
Google Apps Script para importar cartões do Trellopara uma Planilha do Google


## Pré-requisitos
Para o script funcionar é necessário:
* Obter a chave e o token de API (https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/)
* Obter o id do quadro do Trello (https://community.atlassian.com/t5/Trello-questions/How-to-get-Trello-Board-ID/qaq-p/1347525)

## Instalando
1. Abra o arquivo trello-import.gs
2. Copie o conteúdo do script
3. Abra a planilha do Google
4. Acesse o menu Ferramentas > Editor de Script
5. Cole o código do script dentro do novo arquivo de script criado
6. Substitua o conteúdo das variáveis de autenticação:
```sh
// trello variables
var api_key = "your_api_key";
var api_token = "your_api_token";
var board_id = "your_board_id";
```
7. Salve o arquivo (Ctrl+S)
8. Informe um nome para o novo projeto, por exemplo: "Trello import"
9. Feche a planilha e abra novamente. a função onOpen() será executada e o menu Trello aparecerá como última opção do menu principal

## Executando
1. Acesse o menu Trello > Update from Trello
2. Um diálogo aparecerá informando as listas disponíveis. Escolha uma das listas preenchendo seu nome, ou deixe em branco para importar todas as listas
3. O script adicionará linhas ao final da planilha com o conteúdo: 
```sh
[Nome_da_pessoa, Nome_do_cartão, Data_de_criação, Data_limite, null, Descrição, Nome_da_lista]
```

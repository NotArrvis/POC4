# POC4
# API de Fatos sobre Gatos - Documentação

## Descrição
Este projeto é uma página web simples que exibe fatos aleatórios sobre gatos, obtidos através de uma API externa. A página usa HTML, CSS e JavaScript para criar uma interface minimalista com um fundo preto e texto centralizado em cor clara.

## Funcionalidades
- Exibe um fato aleatório sobre gatos obtido da API meowfacts
- Interface responsiva e esteticamente agradável
- Atualização assíncrona do conteúdo

## Tecnologias Utilizadas
- HTML5
- CSS3
- JavaScript (ES6+)
- Fetch API

## Como Funciona

### HTML e CSS
A estrutura HTML é simples, consistindo em:
- Uma seção vazia com ID 'js' onde o conteúdo será inserido dinamicamente
- Estilos CSS para criar um layout centralizado com fundo preto e texto em cor clara

### JavaScript e a Função Fetch

O código utiliza a função `fetch`, que é uma API moderna do JavaScript para fazer requisições HTTP. No contexto deste código:

```javascript
async function fatoGato() {
    let response = await fetch(`https://meowfacts.herokuapp.com/`);
    let data = await response.json();
    return data.data;
}
```

#### Explicação da Função Fetch:
1. `fetch()` é uma função que faz uma requisição HTTP para um URL especificado
2. Ela retorna uma Promise que resolve para um objeto Response
3. No código, usamos `await` para esperar a resposta da requisição
4. Depois, usamos `response.json()` para extrair o JSON da resposta
5. O resultado final é o dado obtido da API

### Fluxo de Execução
1. A função `fatoGato()` é chamada
2. Ela faz uma requisição à API meowfacts
3. Aguarda a resposta e converte para JSON
4. O fato sobre gato é extraído e retornado
5. O HTML é atualizado com o novo fato usando `innerHTML`

## Como Usar
1. Abra o arquivo HTML em um navegador moderno
2. A página automaticamente carregará e exibirá um fato aleatório sobre gatos

## Observações
- É necessário uma conexão com a internet para funcionar
- A API pode ocasionalmente estar indisponível
- O conteúdo é atualizado apenas ao recarregar a página

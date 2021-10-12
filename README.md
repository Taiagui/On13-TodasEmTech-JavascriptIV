# **JavaScript - IV - Requisições**
## Instruções Iniciais:

1. Instalem o Node.js na máquina de vocês, na ultima versão disponível do programa: https://nodejs.org/en/
2. Instalem também o Postman na máquina de vocês: https://www.postman.com/downloads/
3. Forkem o repositório para a conta pessoal de vocês.
4. Clonem no computador de vocês o repositório forkado em suas contas particulares.

**_ATENÇÃO_: Não modifiquem o conteúdo do projeto original forkado, apenas a que você copiou e renomeou!**

### Façam suas perguntas através do DontPad

[http://dontpad.com/On13-JSIV](http://dontpad.com/On13-JSIV)

----

## **1. Requisição a APIs**

Bom, para começar, precisamos primeiro definir o que são APIs. Porque se fala tanto sobre APIs e endpoints dentro do mundo da programação?

Nós, humanos, desenvolvemos formas intermediárias para nos comunicarmos - através da fala, da escrita ou de gestos. Da mesma forma, também foi desenvolvida uma forma para que uma aplicação consiga se comunicar com os seus servidores e com outras aplicações.

![api-diagram](assets/api-diagram.png)

**APIs** - ou Application Programming Interface - **são uma série de métodos e funções que permitem que aplicações acessem dados e interajam com componentes de softwares externos, sistemas operacionais ou microsserviços**. Uma API disponibiliza uma interface de comunicação e de integração entre aplicações.

**Simplificando: uma API entrega uma requisição de um usuário (user request) para um sistema e retorna ao usuário a resposta do sistema (response)**.

APIs são muito utilizadas porque elas são práticas e facilitam o desenvolvimento de uma aplicação. Exemplo: você está criando uma página de formulário de cadastro ao seu sistema. No campo de endereço, você precisa que ele seja automaticamente encontrado e preenchido a depender do CEP inserido pelo usuário na tela.

Ao invés de criar do zero uma aplicação que faça essa busca e preenchimento, você pode utilizar uma API já pronta que realiza essa função que você precisa - no caso, a [ViaCEP](https://viacep.com.br/), [ApiCEP](https://apicep.com/api-de-consulta/), dentre outras.

É possível classificar APIs de diversas formas, mas para fins do nosso estudo, cabe trazer as SOAP APIs e as REST APIs.

**1. SOAP APIs:** SOAP - ou Simple Object Access Protocol - APIs são protocolos de comunicação web e são usados para transmitir informações e dados via HTTP/HTTPS. Aqui, os dados são retornados no formato xml (uma estrutura semelhante a do HTML, mas que não possui as tags pré-definidas).

**2. REST APIs:** A arquitetura REST - ou Representational State Transfer - é amplamente utilizada dentro do desenvolvimento de APIs. Isso porque, ao contrário da arquitetura SOAP, as REST APIs tem um modelo mais simples de requisição. O nosso estudo será concentrado nelas.

O processo de requisição de uma REST API envolve quatro passos específicos:

### **1) Requisição:**

Cada REST API possui uma documentação, dispondo sobre o modo que deve ser feita essa requisição, e quais os tipos de requisições que são aceitas pela API.

Mas, de modo geral, a requisição de uma REST API é feita se utilizando de dois requisitos: **a URL disponibilizada para utilização da API (HTTP protocol) e o método HTTP que você precisa**.  

Existem muitos métodos HTTP, mas os mais usados são os seguintes:

| Método   |      Função      |  Status de Retorno |
|----------|:-------------:|------:|
| GET |  Traz informações | 200 |
| POST |    Cria um novo item   |   201 |
| PUT | Atualiza um item |    200 |
| DELETE | Remove um item |    200 |

**IMPORTANTE:** É preciso saber quais métodos são aceitos pela API. A descrição dos métodos que são aceitos normalmente é feita na documentação da API em específico.

### **2) Input (opcional):**

A API pode pedir que informações específicas constem dentro do *header* e do *body* da requisição e, de forma geral, essas especificidades estão dispostas dentro da documentação de uma API.

Essas informações específicas podem ser um parâmetro de pesquisa, ou um token de autenticação, dentre outras informações.

### **3) Processamento no back-end:**

Com o envio da requisição, ela é processada dentro da API. A depender da requisição pedida, cabe ao sistema do back-end encontrar informações, atualizar dados, criar um dado novo, ou até mesmo deleta-lo.

### **4) Resposta:**

Com o processamento da requisição, a API retorna uma resposta ao usuário. Essa resposta é composta por um **código de status do retorno** e do **próprio dado retornado no formato JSON**.

Relação dos códigos de status de retorno: https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status.

---

## **2. JSON**

JSON é a abreviação de *JavaScript Object Notation* ou Notação de Objeto Javascript. É uma sintaxe para armazenar e transferir dados. Trata-se de uma string que se parece bastante com um objeto JavaScript.

```Javascript
[
  {
    "nome": "Iza",
    "idade": 1,
    "castrado": true,
    "cor": ["branco", "preto"],
    "caracteristicas": ["fofinha", "sociável"]
  },
  {
    "nome": "Beyoncé",
    "idade": 1,
    "castrado": true,
    "cor": ["amarelo", "branco", "marrom", "dourado"],
    "caracteristicas": ["brincalhão", "dengoso"]
  },
]
```

O formato JSON é amplamente utilizado na resposta de requisições por ele ser leve e fácil de ler e escrever. Nota-se que as propriedades necessariamente tem que estar entre aspas duplas.

Na sua forma original, o JSON tem esse formato:

```Javascript
{["\"id"\:"\"10001"\"\"name"\:"\"ABC"\]}
```

Para que possamos utiliza-lo dentro do JavaScript, nos servimos do método JSON.parse(data), que transforma a data string do JSON em um objeto JavaScript para ser manipulado e o retorna.

---

## **3. XMLHttpRequest (ou Protocolo HTTP)**

XMLHttpRequest (XHR) é um objeto que são usados para interagir com servidores. São usados para receber dados de uma URL sem ter que atualizar de novo a página - é criado uma requisição assíncrona.

Apesar de ter "XML" no seu nome, a requisição de XMLHttpRequest pode receber qualquer tipo de dado.

---

## **Links Úteis:**

### **Requisição a APIs**

https://developer.mozilla.org/pt-BR/docs/Glossary/API

https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status

https://pt.wikipedia.org/wiki/Interface_de_programa%C3%A7%C3%A3o_de_aplica%C3%A7%C3%B5es

https://developer.mozilla.org/en-US/docs/Web/API

https://rockcontent.com/br/blog/rest-api/

https://www.webscrapingapi.com/beginners-guide-apis/

https://searchapparchitecture.techtarget.com/definition/RESTful-API

### **JSON**
https://www.json.org/json-en.html

https://www.devmedia.com.br/o-que-e-json/23166

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse

### **XMLHttpRequest**



### **Promises**


### **Async/Await**





<h1>
    <a href="https://cursos.alura.com.br/course/chatgpt-otimizando-qualidade-resultados">
     <img align="center" width="40px" src="https://www.alura.com.br/assets/api/cursos/chatgpt-otimizando-qualidade-resultados.svg"></a>
    <span>
        Curso de ChatGPT: Otimizando a qualidade dos resultados
    </span>
</h1>

## 🔨 Objetivos

- Aprender como criar prompts no ChatGPT utilizando diferentes estratégias;
- Utilizar boas práticas para obter resultados mais confiáveis;
- Entender como maximizar os resultados obtidos;
- Criar prompts para diferentes aplicações;
- Saber como trabalhar com textos longos no ChatGPT;
- Conhecer a OpenAI Playground.

## 📚 Aulas

**A01** Criando os primeiros prompts

**A02** Melhorando a confiabilidade dos resultados

**A03** Explorando aplicações

**A04** Estratégias para textos longos

## 📜 Sumário

- [O que são Prompts?](#o-que-são-prompts)
- [Compreendendo as limitações do ChatGPT - Por que nem sempre as respostas são precisas?](#compreendendo-as-limitações-do-chatgpt---por-que-nem-sempre-as-respostas-são-precisas)
- [Utilizando diferentes estratégias para criar prompts](#utilizando-diferentes-estratégias-para-criar-prompts)
  - [Prompts de Demonstração](#prompts-de-demonstração) 
  - [Prompts de Conclusão](#prompts-de-conclusão)
- [Entendendo o que são tokens](#entendendo-o-que-são-tokens)
- [Boas práticas na escrita de prompts](#boas-práticas-na-escrita-de-prompts)
  - [Uso de delimitadores para estruturar o prompt](#uso-de-delimitadores-para-estruturar-o-prompt)
  - [Uso de caracteres especiais e acentos](#uso-de-caracteres-especiais-e-acentos)
  - [Uso de sinais de pontuação](#uso-de-sinais-de-pontuação)
  - [Uso de citações](#uso-de-citações)
  - [Clareza e especificidade](#clareza-e-especificidade)
  - [Fornecer contexto](#fornecer-contexto)
  - [Evitar perguntas complexas](#evitar-perguntas-complexas)
- [Estratégias avançadas para maximizar resultados com o ChatGPT](#estratégias-avançadas-para-maximizar-resultados-com-o-chatgpt)
  - [Consultando instâncias múltiplas do modelo](#consultando-instâncias-múltiplas-do-modelo)
  - [Análise de pontos em comum e diferenças](#análise-de-pontos-em-comum-e-diferenças)
  - [Evitando pular etapas na análise](#evitando-pular-etapas-na-análise)
  - [Atribuindo pontuações aos aspectos relevantes](#atribuindo-pontuações-aos-aspectos-relevantes)
  - [Geração de novas ideias com base nas pontuações](#geração-de-novas-ideias-com-base-nas-pontuações)

## O que são Prompts?

**`Prompts`** são instruções ou entradas fornecidas ao ChatGPT para orientar a geração de texto. Eles são essenciais
para obter respostas relevantes do modelo.

## Compreendendo as limitações do ChatGPT - Por que nem sempre as respostas são precisas?

- O modelo pode produzir **respostas plausíveis, mas incorretas**, devido a imprecisões nos dados de treinamento. Ele também 
é sensível a pequenas variações nos prompts e pode ter problemas de prolixidade, usando frases comuns em excesso.

- Tem limitações em sua **capacidade de memória e contexto**. Ele pode não acessar adequadamente informações ou referências 
anteriores na conversa, levando a respostas inconsistentes.

- O modelo pode gerar **respostas imprecisas e tendenciosas** devido aos dados de treinamento e à forma como foram coletados,
  destacando a importância de avaliar criticamente as respostas geradas.

## Utilizando diferentes estratégias para criar prompts

Exploraremos aqui estratégias que aprimoram a eficácia dos prompts, impulsionando o desempenho do modelo ChatGPT para 
produzir respostas mais precisas e confiáveis. Duas abordagens principais se destacam:

###  Prompts de Demonstração
Esses prompts apresentam exemplos ao modelo para indicar o que se espera dele. Esse método, também conhecido como aprendizado
de poucos disparos (Few-Shot learning), permite que o modelo aprenda com apenas alguns exemplos fornecidos no prompt.

Exemplo:

```
Preciso do título para um curso.

Exemplo: Python básico implementando um tradutor de texto
Resposta: Traduzindo qualquer linguagem com Python

Exemplo: Excel para organizar a semana
Resposta: "Resposta do modelo..."
```

### Prompts de Conclusão
Esses prompts orientam o modelo a completar uma frase ou padrão fornecido. 

Exemplo:

```
"Eu quero/Eu preciso/Me dê um curso de Python..."
```

## Entendendo o que são tokens

Os modelos entendem e processam o texto dividindo-o em tokens. Um **`token`** pode ser uma palavra individual, um caractere, 
ou até mesmo uma parte de uma palavra. Por exemplo, a frase “Hello World!” teria os seguintes tokens:

![](https://caelum-online-public.s3.amazonaws.com/3146-chatgpt/hello.png)

Temos 3 tokens:
- Hello;
- world;
- Um token para o sinal de exclamação.

Enquanto isso, essa mesma frase em português, seria dividida da seguinte forma:

![](https://caelum-online-public.s3.amazonaws.com/3146-chatgpt/ola.png)

Nesse caso temos 5 tokens:
- Ol;
- á;
- mund;
- o;
- Um token para o sinal de exclamação.

Com isso, é possível verificar que dependendo do idioma o processo de tokenização divide as palavras de forma diferente.

> [**Tokenizer**](https://platform.openai.com/tokenizer): Ferramenta da **OpenAI** para checar como um texto se traduz em 
tokens.

O modelo do ChatGPT atribui um valor de representação a cada token, capturando informações contextuais e semânticas. Essas 
informações semânticas referem-se ao significado e à interpretação das palavras, frases ou sentenças em um contexto específico.

> A semântica está relacionada ao estudo do significado das palavras e como elas se combinam para formar ideias e expressões 
mais complexas.

No contexto do processamento de linguagem natural, as informações semânticas são usadas para capturar o significado e a 
intenção subjacentes a uma sequência de palavras. Ao entender as informações semânticas, um modelo de linguagem como o 
ChatGPT pode inferir o contexto e responder de maneira mais precisa.

Então, os tokens de entrada são passados sequencialmente pelo modelo, permitindo que ele analise o contexto anterior para 
gerar previsões sobre o próximo token.

> **Observanção**: O número de tokens de entrada é limitado para garantir o bom desempenho do modelo e controlar 
os custos computacionais. Se um prompt exceder o limite de tokens permitido, será necessário reduzi-lo ou dividir em partes 
para se adequar ao limite.

## Boas práticas na escrita de prompts

### Uso de delimitadores para estruturar o prompt

#### Três aspas duplas (`"""`) indicam um texto que não deve ser processado, facilitando a compreensão do modelo.

Exemplo:

```
Dê um título para o texto abaixo:

Texto:

“””Python é uma linguagem de propósito geral de alto nível, multiparadigma, suporta o paradigma orientado a objetos, 
imperativo, funcional e procedural. Possui tipagem dinâmica e uma de suas principais características é permitir a fácil 
leitura do código e exigir poucas linhas de código se comparado ao mesmo programa em outras linguagens. “””

Título:
```

#### Três crases (` ``` `) são usadas para marcar blocos de código.

Exemplo:

~~~
Explique o código abaixo:

```
for i in range(5):
   print(i)
```
~~~

#### Sublinhados (`_____`) delimitam áreas para preenchimento, úteis para formatos de formulário.

Exemplo:

```
Sugestão #k

Título: _____
Descrição: _____
Ideia de thumbnail: _____
Texto de thumbnail: _____
Duração: _____
Canais: _____, _____, _____
Pontos fortes: _____, _____, _____

Retorne 3 desses, cada um em seu bloco.
```

### Uso de caracteres especiais e acentos

Utilizar acentos e caracteres especiais ao escrever em português ajuda o modelo a entender melhor o contexto da solicitação.

Exemplo:

```
"Sobre o que é o livro 'Storytelling com Dados' da autora Cole Nussbaumer Knaflic?"
```

### Uso de sinais de pontuação

Sinais de pontuação, como vírgulas, interrogações e pontos finais, ajudam a separar cláusulas e tornar o prompt mais
legível e compreensível.

Exemplo:

```
"Qual é a diferença entre as linguagens Python e R?"
```

### Uso de citações

Aspas podem ser usadas para citar trechos relevantes de texto, especialmente em perguntas baseadas em citações.

Exemplo:

```
"Qual é a mensagem principal transmitida por Machado de Assis em 'Dom Casmurro'?"
```

### Clareza e especificidade

Ser claro e específico ao escrever o prompt ajuda o modelo a entender exatamente o que é solicitado e a gerar uma resposta
precisa.

Exemplo:

```
"Como é a sintaxe da linguagem de programação Python?"
```

### Fornecer contexto

Informações adicionais ou contexto relevante ajudam o modelo a compreender melhor a pergunta e a gerar uma resposta mais
precisa.

Exemplo:

```
"Considere o seguinte trecho de código em Python. Qual é a saída esperada quando este código é executado?" (seguido pelo 
código Python relevante)
```

### Evitar perguntas complexas

Evitar perguntas complexas ou que exigem respostas detalhadas, dividindo-as em perguntas menores e mais simples.

Exemplo:

```
"Explique brevemente o funcionamento do algoritmo de ordenação bubble sort."
```

## Estratégias avançadas para maximizar resultados com o ChatGPT

### Consultando instâncias múltiplas do modelo

Obter respostas de diferentes instâncias do ChatGPT amplia as opções disponíveis e oferece variedade de abordagens para 
resolver problemas ou gerar ideias.

Exemplo:

```
Solicitar três respostas de diferentes instâncias do ChatGPT para uma mesma pergunta, e comparar as abordagens sugeridas 
por cada instância para identificar insights úteis e perspectivas diversas.
```

### Análise de pontos em comum e diferenças

Analisar os pontos em comum e as diferenças entre as respostas do ChatGPT fornece insights valiosos e ajuda a compreender
melhor o contexto do problema.

Exemplo:

```
Comparar as respostas geradas pelo ChatGPT para identificar padrões, tendências ou variações na abordagem do problema.
```

### Evitando pular etapas na análise

Revisar cuidadosamente as sugestões do ChatGPT é essencial para evitar erros simples e garantir a qualidade e precisão 
dos resultados.

Exemplo:

```
Verificar se o ChatGPT seguiu todas as etapas necessárias ao fornecer uma resposta, evitando assim conclusões precipitadas 
ou incorretas.
```

### Atribuindo pontuações aos aspectos relevantes

Atribuir pontuações aos aspectos relevantes das respostas do ChatGPT permite quantificar a eficácia de cada elemento e 
identificar áreas de melhoria.

Exemplo:

```
Avaliar a clareza, relevância e originalidade de cada resposta do ChatGPT, e atribuir uma pontuação de 0 a 100 para cada 
resposta com base na sua viabilidade, inovação e potencial impacto, ajudando a priorizar e selecionar a abordagem mais 
promissora.
```

### Geração de novas ideias com base nas pontuações

Gerar novas ideias com base nas pontuações atribuídas aos aspectos relevantes das respostas do ChatGPT permite otimizar 
a criatividade e maximizar a qualidade das soluções.

Exemplo:

```
Criar uma nova proposta ou solução que aproveite os pontos fortes identificados nas respostas do ChatGPT, enquanto aborda 
ou corrige eventuais pontos fracos.
```
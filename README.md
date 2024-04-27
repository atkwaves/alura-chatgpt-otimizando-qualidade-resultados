<h1>
    <a href="https://cursos.alura.com.br/course/chatgpt-otimizando-qualidade-resultados">
     <img align="center" width="64px" src="https://www.alura.com.br/assets/api/cursos/chatgpt-otimizando-qualidade-resultados.svg">
    </a>
    <span>
        Curso de ChatGPT: Otimizando a qualidade dos resultados
    </span>
</h1>

## 🎯 Objetivos

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
- [Explorando aplicações](#explorando-aplicações)
  - [Resumos multilíngues](#resumos-multilíngues)
  - [Analisando sentimentos](#analisando-sentimentos)
  - [Transformando o tom de voz](#transformando-o-tom-de-voz)
  - [Convertendo formatos](#convertendo-formatos)
  - [Verificação ortográfica/verificação gramatical](#verificação-ortográficaverificação-gramatical)
  - [Criando respostas automáticas para e-mails](#criando-respostas-automáticas-para-e-mails)
- [Estratégias para textos longos](#estratégias-para-textos-longos)
- [Playground](#playground)
  - [System e Message](#system-e-message)
  - [Ajustando as configurações](#ajustando-as-configurações)

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

## Explorando aplicações

### Resumos multilíngues

Resumir textos multilíngues envolve identificar o idioma original, solicitar um resumo nesse idioma e usar marcadores
específicos para garantir a precisão da tradução automática.

Exemplo:

```
Resuma o texto. O resumo deve ter uma frase:

Texto: """Texto..."""

Idioma:XXXXX 
Resumo em XXXXX: ____
```

### Analisando sentimentos

Analisar sentimentos envolve contextualizar o modelo, fornecer um exemplo de texto a ser analisado e solicitar uma
resposta específica, como a classificação do sentimento em uma única palavra.

Exemplo:

```
"Qual o sentimento da seguinte resenha de produto, que está delimitada por aspas?

Dê a resposta com uma única palavra: "positivo", "misto", "neutro" ou "negativo".

Texto: """Texto..."""

Sentimento:
```

### Transformando o tom de voz

Ajustar o tom de um texto, transformando-o de uma abordagem inicialmente crítica ou dura para uma mais amigável e equilibrada,
por exemplo, permite transmitir uma opinião de forma mais respeitosa e acessível aos leitores ou seguidores, adaptando-se
às necessidades de comunicação da situação.

Exemplo:

```
Reescreva o texto abaixo delimitado por """, deixando seu tom de voz mais simpático e amigável:

Texto: """Texto..."""
```

### Convertendo formatos

Para converter dados de um tipo para outro, é crucial fornecer uma descrição precisa do problema e dos dados envolvidos.
Isso inclui especificar o formato dos dados de entrada e o formato desejado de saída.

Exemplo:

```
Temos alguns dados armazenados em um dicionário na linguagem X chamado “funcionários” . Escreva esses dados no formato CSV. 
Retorne apenas o CSV.

Entrada: Dados de entrada
Saída:
```

### Verificação ortográfica/verificação gramatical

É possível orientar o modelo a identificar e corrigir erros ortográficos, gramaticais e de pontuação, além de sugerir
melhorias na estrutura e coesão das frases.

Exemplo:

```
Revise e corrija o texto abaixo delimitado por """. Reescreva a versão corrigida.

Texto: """Texto..."""
```

### Criando respostas automáticas para e-mails

A criação de respostas automáticas para e-mails é solução eficiente para lidar com grandes volumes de correspondência
eletrônica. Ao desenvolver prompts específicos para esse fim, é possível orientar o modelo a gerar respostas adequadas e
personalizadas com base no conteúdo e no contexto de cada mensagem recebida.

Exemplo:

```
Você é um assistente de IA de atendimento ao cliente. Sua tarefa é enviar uma resposta por e-mail a um(a) cliente. Dado 
o e-mail do(a) cliente delimitado por """", gere uma resposta para agradecer ao cliente por sua avaliação. Se o sentimento 
for positivo ou neutro, agradeça por sua revisão. Se o sentimento for negativo, peça desculpas e sugira que eles entrem 
em contato com o atendimento ao cliente. Certifique-se de usar detalhes específicos da resenha. Escreva em um tom conciso 
e profissional. Assine o e-mail como Atendimento ao cliente.

Resenha: """Resenha..."""

Sentimento da resenha:
```

## Estratégias para textos longos

Quando trabalhamos com textos grandes no GPT, precisamos **`dividir o conteúdo em partes menores`** para obter os melhores resultados. 
Isso porque o GPT tem uma memória limitada (limite de caracteres para processamento). Podemos fazer isso manualmente, **`copiando 
e colando em diferentes conversas (trabalho em paralelo)`** , ou automatizar o processo com ferramentas como o **LangChain**.

> [**LangChain**](https://github.com/langchain-ai/langchain): Ferramenta que permite fazer cadeias longas de conversa com a 
> I.A, o que é útil quando se atinge o limite e precisa manter a memória. Ela oferece estratégias, como manter um resumo 
> na memória ou descartar os trechos mais antigos e manter os mais recentes. Essa escolha de estratégia permite manter uma 
> conversa mais fluída com a IA.

## Playground

Ferramenta interativa dentro da [OpenAI Platform](https://platform.openai.com/), permitindo que os usuários experimentem 
e explorem os modelos de linguagem da OpenAI de forma prática e direta. É um ambiente onde é possível interagir com o modelo 
de linguagem, enviando perguntas ou prompts e recebendo respostas geradas pelo modelo em tempo real.

### System e Message

Quando alguém envia sua primeira mensagem para o GPT, o código envia uma mensagem oculta informando ao GPT que ele é um 
assistente solícito. Isso acontece toda vez que uma conversa é iniciada. Essa mensagem, chamada de mensagem de sistema, 
não é visível para o usuário, mas é crucial para definir o comportamento do GPT.

Para acessá-la, é necessário ir para a seção **"Playground"**. Lá, a mensagem padrão do sistema pode ser encontrada na 
área **"System"** à esquerda, onde está escrito: `"Você é uma assistente solícita"`.

Na interação tradicional de chat, o usuário envia o texto e a instrução. No entanto, se houver muitas regras, o assistente 
pode confundi-las com o texto e ignorá-las. Uma solução é enviar apenas as **`instruções`** no campo **"System"** e o 
**`texto`** no campo **"User"**. Isso evita confusão entre as instruções e o texto, pois são mensagens distintas: uma vinda 
do sistema e outra do usuário.

Exemplo:

Ao criar uma instrução no campo "system", solicitando um resumo do texto em 60 palavras, todas as mensagens do usuário 
serão automaticamente resumidas para esse limite.

~~~
Primeiro, identifique o idioma.

Resuma o texto em 60 palavras na língua original.

A saída deve ser na forma:

```
Idioma: ""

Resumo no idioma: ""
```
~~~

### Ajustando as configurações

A interface do ChatGPT é baseada na interação entre usuário e assistente, e permite configurar diversas características, 
como:

**`Modelo` 3.5 ou 4 do GPT;**

**`Temperatura` da resposta, que determina o quão aleatória ou previsível será a resposta;**
- Quando a temperatura é ajustada para zero, o modelo retorna conclusões idênticas ou muito semelhantes para o mesmo prompt, 
aumentando a confiança do modelo e tornando as respostas mais precisas e determinísticas.
- Aumentar a temperatura resulta em respostas menos previsíveis e mais diversas, pois diminui a confiança do modelo, permitindo 
uma gama mais ampla de respostas, embora com menor certeza sobre sua precisão.

**`Maximum Length` define o comprimento máximo que uma resposta pode ter;**
- Quando um número limite é definido, o modelo interrompe a geração de texto assim que atinge esse limite de caracteres. 
Essa funcionalidade é útil para controlar a extensão das respostas geradas e evitar resultados muito longos.

**`Top P/Nucleus Sampling` técnica que controla a diversidade das respostas, levando em conta apenas as probabilidades das 
palavras mais prováveis;**
- Ao definir um valor para o Top P, como 1, por exemplo, o modelo seleciona as palavras mais prováveis até alcançar uma 
probabilidade acumulada de 100%. Isso impede que o modelo gere respostas muito raras ou improváveis.

**`Frequency Penalty` controla a repetição de tokens em uma resposta;**
- Ao definir um valor mais alto para essa penalidade, o modelo é incentivado a evitar repetições excessivas, resultando 
em respostas mais variadas e dinâmicas.

**`Presence Penalty` controla a preferência do modelo por incluir ou evitar informações específicas nas respostas.**
- Ao aumentar o valor do Presence Penalty, o modelo tende a evitar mencionar as palavras ou frases fornecidas como instrução 
(prompt), gerando respostas que não incluem explicitamente essas informações.
- Ao diminuir o valor do Presence Penalty ou defini-lo como zero, o modelo tem mais liberdade para incluir as informações 
fornecidas nas respostas, o que pode resultar em respostas mais diretas e que mencionam explicitamente o solicitado.
- Essa configuração pode ser útil para gerar respostas mais criativas, evitando depender excessivamente das informações 
fornecidas. No entanto, é importante observar que um valor alto de Presence Penalty pode fazer com que o modelo ignore 
completamente as informações fornecidas, especialmente em casos de instruções mais longas ou complexas.

## 🔧 Ferramentas

[![ChatGPT](https://img.shields.io/badge/chatGPT-74aa9c?style=for-the-badge&logo=openai&logoColor=white)](https://platform.openai.com/docs/introduction)

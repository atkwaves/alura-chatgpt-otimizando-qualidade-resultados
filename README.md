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

## Sumário

- [O que são Prompts?](#o-que-são-prompts)
- [Compreendendo as limitações do ChatGPT - Por que nem sempre as respostas são precisas?](#compreendendo-as-limitações-do-chatgpt---por-que-nem-sempre-as-respostas-são-precisas)
- [Utilizando diferentes estratégias para criar prompts](#utilizando-diferentes-estratégias-para-criar-prompts)
  - [Prompts de Demonstração](#prompts-de-demonstração) 
  - [Prompts de Conclusão](#prompts-de-conclusão)
- [Entendendo o que são tokens](#entendendo-o-que-são-tokens)

  

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

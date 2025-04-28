# Explorando evolução de código

Neste exercício, iremos explorar a evolução de código em sistemas reais.

Iremos utilizar a ferramenta [GitEvo](https://github.com/andrehora/gitevo).
Essa ferramenta analisa a evolução de código em repositórios Git nas seguintes linguagens: Python, JavaScript, TypeScript e Java.

Você deve submeter via Moodle apenas o link do seu `fork`, conforme descrito abaixo.

# Passo 1: Selecionar repositório a ser analisado

Selecione um repositório relevante na linguagem de sua preferência (Python, JavaScript, TypeScript ou Java).
Você pode encontrar projetos interessantes nos links abaixo:

- Python: https://github.com/topics/python?l=python
- JavaScript: https://github.com/topics/javascript?l=javascript
- TypeScript: https://github.com/topics/typescript?l=typescript
- Java: https://github.com/topics/java?l=java

# Passo 2: Instalar e rodar a ferramenta GitEvo

Instale a ferramenta [GitEvo](https://github.com/andrehora/gitevo) com o comando:

```
pip install gitevo
```

Rode a ferramenta no repositório selecionado através do seguinte comando (dependendo da linguagem do projeto que escolheu):

```shell
# Python
$ gitevo -r python <git_url>

# JavaScript
$ gitevo -r js <git_url>

# TypeScript
$ gitevo -r ts <git_url>

# Java
$ gitevo -r java <git_url>
```

Onde `<git_url>` é URL do repositório a ser analisado.
Por exemplo, para analisar o projeto Flask escrito em Python:

```
$ gitevo -r python https://github.com/pallets/flask
```

# Passo 3: Explorar os gráficos de evolução de código (`index.html`)

Ao rodar a ferramenta [GitEvo](https://github.com/andrehora/gitevo), o arquivo `index.html` é gerado com diversos gráficos de evolução de código.

Abra o arquivo `index.html` e observe com atenção os gráficos gerados.

# Passo 4: Explicar um gráfico de evolução de código

Selecione um dos gráficos de evolução e explique-o com suas palavras.
Por exemplo, você pode:

- Detalhar a evolução ao longo do tempo, 
- Detalhar se as curvas estão de acordo com boas práticas,
- Explicar grandes alterações nas curvas,
- Explorar a documentação do repositório em busca de explicações para grandes alterações
- Etc.

Seja criativo!

# Exercício

Para responder este exercício, primeiramente, você deve fazer um `fork` deste repositório.
No Moodle, você deve submeter apenas a URL do seu `fork`.

Em seguida, adicione o arquivo gerado `index.html` no seu fork.

Por fim, responda as questões abaixo no seu `fork`: 

1. Repositório selecionado: https://github.com/yt-dlp/yt-dlp

2. Gráfico selecionado: Control Flows
  
3. Explicação: 
O gráfico "Control flows" mostra a evolução da quantidade de estruturas de controle no código do projeto yt-dlp entre 2020 e 2025, analisando especificamente o uso de if, for, try, with e while statements. Observando a linha azul, que representa o número de if_statement, vemos uma tendência clara de crescimento ao longo dos anos, saindo de cerca de 5.700 em 2020 para aproximadamente 8.800 em 2025. Esse crescimento consistente indica que o projeto foi se tornando progressivamente mais complexo em suas decisões lógicas, o que é esperado conforme novas funcionalidades e suportes a diferentes tipos de fluxos de download foram adicionados. A curva do if_statement não apresenta picos bruscos, mas sim um crescimento gradual, o que é um sinal de que as alterações no projeto foram feitas de forma incremental e controlada, respeitando boas práticas de desenvolvimento.

No caso dos for_statement, a linha rosa também mostra uma tendência de crescimento, mas em uma escala bem menor. O número de for passou de cerca de 1.400 em 2020 para aproximadamente 2.340 em 2025. Esse aumento reflete uma expansão no processamento de listas e coleções, o que é natural num projeto como yt-dlp que manipula múltiplos links, formatos e recursos de mídia. Semelhantemente aos if, o crescimento é constante e sem quebras abruptas, indicando boas práticas no sentido de modularizar a complexidade crescente com iterações bem distribuídas ao invés de criar grandes estruturas monolíticas.

As curvas dos try_statement, with_statement e while_statement apresentam valores absolutos muito menores, e seu crescimento também é moderado. O try_statement, que representa o tratamento de exceções, subiu de pouco mais de 300 em 2020 para cerca de 500 em 2025. Isso sugere que, ao longo do tempo, houve uma preocupação crescente em capturar e tratar erros de forma apropriada, especialmente importante em um projeto que depende da comunicação com fontes externas (e.g., sites que mudam constantemente suas APIs ou bloqueiam acessos). O with_statement, relacionado ao gerenciamento de contexto (como abrir e fechar arquivos automaticamente), quase quadruplicou seu uso de 76 em 2020 para mais de 400 em 2025, o que indica uma adoção maior de práticas modernas de manipulação de recursos, melhorando a segurança e a legibilidade do código. O while_statement teve um aumento muito pequeno e se manteve estável, o que é normal, já que loops while são geralmente usados de forma muito controlada para evitar riscos de loops infinitos.

A análise dos principais marcos do repositório mostra que parte desse crescimento está associada à introdução de novos módulos e melhorias contínuas no suporte a diferentes websites e formatos de mídia, principalmente a partir de 2021, quando o yt-dlp se consolidou como o principal fork moderno do youtube-dl. As grandes melhorias de 2021 para 2022, incluindo integração com o SponsorBlock e melhorias na extração de listas de reprodução, explicam o aumento mais pronunciado nas curvas de if e for. Além disso, a preocupação cada vez maior com a robustez, segurança de exceções e manuseio de múltiplos formatos justifica o crescimento dos try e with.

Portanto, de forma geral, o gráfico "Control flows" revela um projeto que cresce de maneira saudável e responsável, acompanhando as boas práticas de engenharia de software à medida que sua base de usuários e a complexidade de suas funcionalidades aumentam. Não há indícios de crescimento desordenado ou de más práticas associadas a grandes reescritas ou adição súbita de estruturas de controle mal planejadas.



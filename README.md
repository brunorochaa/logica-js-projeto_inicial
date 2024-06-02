# [Lógica de programação: mergulhe em programação com JavaScript](https://cursos.alura.com.br/course/logica-programacao-mergulhe-programacao-javascript)
Faça esse curso de Lógica de programação e:
- Exiba mensagens na tela de forma interativa
- Utilize variáveis no desenvolvimento de software
- Ingresse no mundo de desenvolvimento seguindo boas práticas de programação
- Desenvolva uma aplicação do início ao fim, inspirada no mundo real
- Aprenda a adaptar soluções desenvolvidas pela linguagem em seus programas de software

---

# 1. Iniciando com JavaScript: O que aprendemos?
- Preparamos o ambiente de desenvolvimento com a instalação do Visual Studio Code para criar programas utilizando a linguagem JavaScript;
- Entendemos o conceito de variável para guardar informações, como números ou palavras, para usar mais tarde no nosso programa;
- Usamos o `alert` para exibir uma mensagem passando algumas instruções sobre o programa e usamos o `prompt` para interagir com a pessoa permitindo inserir um valor e armazenando em uma variável;
- Criamos um `if`, que é uma instrução em programação que permite ao computador tomar decisões ao executar um bloco de código apenas se uma condição específica for verdadeira.

## Código
```js 
alert('Boas vindas ao jogo do número secreto');
let numeroSecreto = 29;
let chute = prompt('Escolha um número de 1 em 30:')

if (chute == numeroSecreto) {
    console.log('Isso ai! Você descobriu o número secreto! (29)');
}
```

## Para saber mais: documentação
A leitura da documentação oficial de uma linguagem de programação é crucial para que uma pessoa desenvolvedora de software possa utilizá-la de forma eficaz.

No caso do JavaScript, essa documentação fornece uma ampla gama de informações, incluindo conceitos sobre sintaxe, as bibliotecas e as funcionalidades disponíveis na linguagem.

Alguns links úteis para a documentação oficial do JavaScript incluem:
- [A documentação da linguagem de programação JavaScript](https://developer.mozilla.org/pt-BR/docs/Learn/JavaScript/First_steps/What_is_JavaScript)
- [Guia de JavaScript: o que é e como aprender a linguagem mais popular do mundo?](https://www.alura.com.br/artigos/javascript)

Ao ler a documentação oficial, temos uma compreensão mais profunda da linguagem e de suas funcionalidades. Isso facilita a escrita de códigos mais limpos, claros e seguros. A documentação também pode ajudar o desenvolvedor ou desenvolvedora a economizar tempo, além de evitar a necessidade de pesquisar em fóruns ou outras fontes de informação não confiáveis. 

---

# 2. Condicionais e concatenação: O que aprendemos?
- Utilizamos o console para testar e depurar nosso código, exibindo mensagens e valores durante a execução do programa;
- Aprendemos a utilizar estruturas condicionais (if/else) para criar lógicas que permitem ao programa tomar decisões com base em condições específicas;
- Implementamos um bloco de código para exibir uma mensagem caso o chute do usuário não seja igual ao número secreto;
- Usamos template strings para concatenar o número secreto com o valor armazenado em uma variável e exibir uma mensagem personalizada.

## Código
```js
alert('Boas vindas ao jogo do número secreto');
let numeroSecreto = 29;
console.log(numeroSecreto);
let chute = prompt('Escolha um número de 1 em 30:')

// Se chute for igual ao número secreto.
if (chute == numeroSecreto) {
    alert(`Isso ai! Você descobriu o número secreto! ${numeroSecreto}`);
} else {
    alert('Você errou!');
}
```

## Para saber mais: ponto e vírgula no JavaScript
No JavaScript, o uso do ponto e vírgula (`;`) é uma prática recomendada. A linguagem possui um mecanismo chamado "inserção automática de ponto e vírgula" (automatic semicolon insertion - ASI), que tenta adicionar ponto e vírgulas automaticamente em certos pontos do código onde eles são ausentes.

Isso significa que, em alguns casos, o JavaScript tentará "corrigir" a falta de ponto e vírgula inserindo-o automaticamente. No entanto, a interpretação do ASI pode levar a comportamentos inesperados e erros sutis, especialmente quando as regras não são claras.

Portanto, para evitar possíveis problemas e garantir a clareza do código, muitos desenvolvedores preferem adicionar explicitamente ponto e vírgula em seus programas.

Apesar da inserção automática de ponto e vírgula poder ajudar a mitigar erros de sintaxe, é uma boa prática adicionar ponto e vírgula manualmente para evitar ambiguidades e problemas de interpretação. Isso é particularmente importante em situações como quando várias instruções estão em uma mesma linha, ao usar declarações de retorno de valor ou ao minificar o código.

Em projetos colaborativos ou de grande escala, a consistência no estilo de codificação e a clareza do código são cruciais, e o uso explícito de ponto e vírgula contribui para um código mais legível e menos sujeito a erros de interpretação por parte dos programadores e do próprio mecanismo de ASI.

- [Leitura complementar da documentação sobre o JavaScript.](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Lexical_grammar#automatic_semicolon_insertion)
Quer saber o que a comunidade recomenda? 
- [Leia mais neste link do Stack Overflow.](https://pt.stackoverflow.com/questions/3341/utilizar-ou-n%C3%A3o-ponto-e-v%C3%ADrgula-no-fim-das-linhas-em-javascript)

---

# 3. Loops e Tentativas: O que aprendemos?
- Aprendemos a verificar se um número é maior ou menor do que outro utilizando estruturas condicionais (if/else) em nosso programa;
- Utilizamos o loop "while" para repetir um bloco de código enquanto uma determinada condição for verdadeira, e permitir assim que o programa execute uma ação várias vezes;
- Implementamos um contador de tentativas para acompanhar e exibir a quantidade de vezes que o usuário tentou adivinhar um número secreto. Podemos fazer isso, por exemplo, em um jogo de adivinhação.

## Código
```js
alert('Boas vindas ao jogo do número secreto');
let numeroSecreto = 29;
console.log(numeroSecreto);
let chute;
let tentativas = 1;

// Enquanto chute não for igual ao numéro secreto.
while (chute != numeroSecreto) {
    chute = prompt('Escolha um número de 1 em 30:')

    // Se chute for igual ao número secreto.
    if (chute == numeroSecreto) {
        alert(`Isso ai! Você descobriu o número secreto! ${numeroSecreto} com ${tentativas} tentativas!`);
    } else {
        if ( chute > numeroSecreto) {
            alert(`O número secreto é menor que ${chute}`);
        } else {
            alert(`O número secreto é maior que ${chute}`);
        }

        // tentativas = tentivas + 1;
        tentativas ++;
    }
}
```

## Para saber mais: Para saber mais: operadores lógicos
Quando escrevemos programas em JavaScript, frequentemente nos deparamos com a necessidade de tomar decisões com base em condições. É aqui que os operadores lógicos entram em cena e nos ajudam a criar uma lógica robusta e eficaz.

A seguir, vamos explorar os operadores lógicos de uma forma simples e fácil de entender. Teremos exemplos claros para ilustrar seu funcionamento.

### AND (&&)
O operador AND, representado pelos símbolos "&&", é utilizado para combinar duas condições e avaliar se ambas são verdadeiras. Se ambas as condições forem verdadeiras, o resultado será… verdadeiro. Caso contrário, logicamente será falso. Por exemplo:
```js
let idade = 25;
let possuiCarteira = true;

// se idade é maior que 18 e possui carteira…
if (idade > 18 && possuiCarteira) {
  console.log("Pode dirigir!");
} else {
  console.log("Não pode dirigir.");
}
```

### OR (||)
O operador OR, representado pelos símbolos "||", é usado para verificar se pelo menos uma das condições é verdadeira. Se uma das condições for verdadeira, o resultado será verdadeiro. Se ambas forem falsas, o resultado será falso. Veja um exemplo:
```js
let temMaça = false;
let temBanana = true;

// se tem maça ou tem banana…
if (temMaça || temBanana) {
  console.log("Você tem frutas!");
} else {
  console.log("Não tem frutas.");
}
```

### **Outros tipos de operadores lógicos**
<table><thead><tr><th>Operador</th><th>Nome</th><th>Exemplo</th><th>Resultado</th></tr></thead><tbody><tr><td>==</td><td>Igual</td><td><strong>A == B</strong></td><td>Verdadeiro se A <strong>for igual</strong> a B</td></tr><tr><td>!=</td><td>Diferente</td><td><strong>A != B</strong></td><td>Verdadeiro se A <strong>não for igual</strong> a B</td></tr><tr><td>&lt;</td><td>Menor que</td><td><strong>A &lt; B</strong></td><td>Verdadeiro se A <strong>for menor que</strong> B</td></tr><tr><td>&gt;</td><td>Maior que</td><td><strong>A &gt; B</strong></td><td>Verdadeiro se A <strong>for maior que</strong> B</td></tr><tr><td>&lt;=</td><td>Menor ou igual</td><td><strong>A &lt;= B</strong></td><td>Verdadeiro se A <strong>for menor ou igual</strong> a B.</td></tr><tr><td>&gt;=</td><td>Maior ou igual</td><td><strong>A &gt;= B</strong></td><td>Verdadeiro se A <strong>for maior ou igual</strong> a B.</td></tr></tbody></table>

### *Operadores Lógicos*
<table><thead><tr><th>Operador</th><th>Nome</th><th>Exemplo</th><th>Resultado</th></tr></thead><tbody><tr><td>&amp;&amp;</td><td>E / AND</td><td>(A &gt; B) <strong>&amp;&amp;</strong> (B == C)</td><td>Verdadeiro se A fo maior que B <em><strong>E</strong></em> B for igual a C</td></tr><tr><td><strong>ǀǀ</strong></td><td>OU / OR</td><td>(A &gt; B) <strong>ǀǀ</strong> (B == C)</td><td>Verdadeiro se A for maior que B <em><strong>OU</strong></em> B for igual a C</td></tr><tr><td>!</td><td>NEGAÇÃO</td><td>!(A == B)</td><td>Verdadeiro se  A <em><strong>NÃO</strong></em> for igual a B</td></tr></tbody></table>

Gostou desse conhecimento e quer mais? A [Rafa Ballerini tem um artigo incrível](https://www.alura.com.br/artigos/operadores-matematicos-em-javascript) falando sobre ```Como utilizar operadores de comparação em Javascript``` que vale a pena a leitura.

---

# 4. Boas práticas de programação: O que aprendemos?
- Aprendemos a evitar código duplicado utilizando estratégias para exibir a palavra "tentativas" no singular ou plural, dependendo do número de tentativas realizadas;
- Analisamos a documentação e encontrar informações relevantes para o desenvolvimento do nosso programa;
- Descobrimos como utilizar a função Math.random() para gerar um número aleatório, permitindo a criação de desafios e jogos mais dinâmicos e variados.

## Código
```js
alert('Boas vindas ao jogo do número secreto');
let numeroSecreto = parseInt(Math.random() * 100 + 1);
let chute;
let tentativas = 1;

// Enquanto chute não for igual ao numéro secreto.
while (chute != numeroSecreto) {
    chute = prompt('Escolha um número de 1 em 100:')

    // Se chute for igual ao número secreto.
    if (chute == numeroSecreto) {
        break;
    } else {
        if ( chute > numeroSecreto) {
            alert(`O número secreto é menor que ${chute}`);
        } else {
            alert(`O número secreto é maior que ${chute}`);
        }

        tentativas ++;
    }
}

let palavraTentativa = tentativas > 1 ? 'tentativas' : 'tentativa'
alert(`Isso ai! Você descobriu o número secreto! ${numeroSecreto} com ${tentativas} ${palavraTentativa}.`);
```

## Para saber mais: preciso decorar cada linha de código ou comando?
Compreender cada linha de código ou comando em detalhes é certamente uma aspiração louvável, mas não é necessário decorar. O desenvolvimento de software moderno é uma tarefa complexa, e as linguagens de programação oferecem uma ampla gama de recursos e bibliotecas.

Em vez de memorizar cada linha, é mais valioso entender os conceitos fundamentais por trás das estruturas de programação e saber como usar a documentação efetivamente.
A documentação de uma linguagem de programação é uma ferramenta essencial para todos os desenvolvedores. Ela não apenas fornece uma referência rápida para a sintaxe e os comandos, mas também explica os conceitos subjacentes, oferece exemplos práticos e ajuda a compreender os diferentes recursos disponíveis.

Através da documentação você pode aprender a utilizar bibliotecas, explorar casos de uso avançados e entender as melhores práticas recomendadas pela comunidade. Isso economiza tempo, evita erros e permite que você se mantenha atualizado com as últimas atualizações da linguagem.

Em vez de se preocupar em memorizar cada detalhe, concentre-se em desenvolver habilidades de resolução de problemas, compreender os princípios de design de software e aprender a pesquisar eficientemente na documentação. A capacidade de ler e interpretar a documentação é uma habilidade valiosa, pois permite que você aprenda novas linguagens e tecnologias de maneira eficaz, adaptando-se rapidamente às mudanças do cenário de desenvolvimento. Portanto, em sua jornada como pessoa desenvolvedora, lembre-se de que a habilidade de compreender e usar a documentação é tão importante quanto saber escrever código.

Nesta aula, [vimos como usar a documentação para gerar um número aleatório através da documentação do Mozilla.](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Math/random) Porém, existe também o [W3Schools (W3S)](https://www.w3schools.com/js/default.asp) que é um recurso online amplamente conhecido e utilizado para aprender diversas tecnologias de desenvolvimento web, incluindo JavaScript (JS).

O site oferece tutoriais interativos, exemplos de código, referências de sintaxe e conceitos fundamentais relacionados ao JavaScript e outras linguagens web.
Ao explorar o W3Schools, você pode adquirir uma compreensão sólida dos princípios do JS, desde o básico até tópicos mais avançados, como manipulação do DOM, interações do usuário e requisições assíncronas.

O W3Schools é uma ferramenta valiosa para aprimorar suas habilidades em JavaScript, oferecendo um ambiente prático para experimentar o código, compreender os conceitos-chave e aplicar o conhecimento adquirido em seus próprios projetos de desenvolvimento web.

---

# Refêrencias
### 1. [Lógica de Programação Crie seus primeiros programas usando Javascript e HTML](https://www.casadocodigo.com.br/products/livro-programacao?_pos=1&_sid=4661f8240&_ss=r)
`Este livro apresenta uma abordagem totalmente prática. Uma didática pensada no iniciante, com a qual os conceitos são apresentados com motivações práticas, através do surgimento da necessidade para depois mostrar a solução.`

### 2. [Lógica de programação com Portugol](https://www.casadocodigo.com.br/products/livro-portugol?_pos=2&_sid=4661f8240&_ss=r)
`Neste livro, Joice Mendes e Rafael Muniz apresentam todos os conceitos necessários para a criação da lógica de programação e dos algoritmos. Você vai aprimorar sua percepção lógica e aprender a aplicá-la na programação, cobrindo tópicos desde a sintaxe do Portugol, variáveis, comandos, estruturas condicionais, operadores relacionais e lógicos, estruturas de repetição, até vetores, matrizes e funções. O material é recheado com 85 exemplos de código, 55 exercícios de fixação com gabarito e um projeto prático ao longo do aprendizado. Todos os capítulos contam com um vídeo complementar disponibilizado na internet.`

### 3. [Livro: "Estruturas de Dados e Algoritmos com JavaScript"](https://www.google.com.br/books/edition/Estruturas_de_dados_e_algoritmos_com_Jav/0nWKDwAAQBAJ?hl=pt-BR&gbpv=1&dq=estrutura+de+dados+javascript&printsec=frontcover)
`Este livro aborda de forma detalhada as estruturas de dados e algoritmos mais comuns, fornecendo exemplos práticos em JavaScript.`

### 4. [Site: MDN Web Docs](https://developer.mozilla.org/pt-BR/)
`A documentação oficial da Mozilla Developer Network (MDN) é uma excelente fonte de informações sobre JavaScript. Lá você encontrará explicações detalhadas sobre a sintaxe, recursos da linguagem e exemplos de código.`

### 5. [Eloquent JavaScript 3rd edition (2018)](https://eloquentjavascript.net/)
`Este é um livro sobre JavaScript, programação e as maravilhas do mundo digital. Um guia essencial para toda a pessoa desenvolvedora web. Em inglês.`

### 6. [Algoritmos - Teoria e Prática, Thomas H. Cormen](https://books.google.com.br/books/about/Algoritmos_Teoria_e_Pr%C3%A1tica.html?id=6iA4LgEACAAJ&source=kp_book_description&redir_esc=y)
`Este livro apresenta um texto abrangente sobre o moderno estudo de algoritmos para computadores. É uma obra clássica, cuja primeira edição tornou-se amplamente adotada nas melhores universidades em todo o mundo, bem como padrão de referência para profissionais da área.`

### 7. [JavaScript: O Guia Definitivo](https://www.amazon.com.br/JavaScript-Guia-Definitivo-David-Flanagan/dp/856583719X/ref=sr_1_1?keywords=javascript&qid=1701835643&sr=8-1&ufe=app_do%3Aamzn1.fos.6121c6c4-c969-43ae-92f7-cc248fc6181d)
`Referência completa para programadores, JavaScript: O guia definitivo fornece uma ampla descrição da linguagem JavaScript básica e das APIs JavaScript do lado do cliente definidas pelos navegadores Web. Recomendado para programadores experientes que desejam aprender a linguagem de programação da Web e para programadores JavaScript que desejam ampliar seus conhecimentos e dominar a linguagem, este é o guia do programador e manual de referência de JavaScript completo e definitivo.`

### 8. [HTML5 e CSS3 Domine a web do futuro](https://www.casadocodigo.com.br/products/livro-html-css?_pos=2&_sid=ee24eb627&_ss=r)
`Neste livro você irá aprender a criar páginas elegantes de forma simples! HTML e CSS, quando bem utilizados, podem ser o sucesso de um projeto e, com os novos recursos, muito do que antes era trabalhoso agora não é mais. Aprenda as melhores técnicas para escrever seu site por meio de exemplos práticos de funcionalidades úteis do cotidiano. Construa menus, aplique efeitos, estilize elementos visuais, melhore a semântica da sua página e muito mais!`

### 9. [Guia Front-End: O caminho das pedras para ser um dev Front-End](https://www.casadocodigo.com.br/products/livro-guia-frontend?_pos=5&_sid=ee24eb627&_ss=r)
`Neste livro, Diego Eis nos guia sobre o mundo de desenvolvimento web por meio de uma análise franca e objetiva de diversas tecnologias adotadas, necessidades do mercado e postura profissional. Você não vai aprender diretamente sobre essas tecnologias aqui, mas certamente vai desenvolver um senso mais apurado e uma nova forma de olhar para elas, o que é fundamental nesse mundo de aprendizado não linear.`

### 10. [Como utilizar operadores de comparação em Javascript](https://www.alura.com.br/artigos/operadores-matematicos-em-javascript)
`Neste artigo de Rafa Ballerini você aprenderá as diferenças entre operadores de comparação em JavaScript e como utilizá-los`

### 11. [Documentação MDN: O que é JavaScript?](https://developer.mozilla.org/pt-BR/docs/Learn/JavaScript/First_steps/What_is_JavaScript)
`Neste primeiro artigo há uma análise profunda da linguagem, respondendo questões como "O que é JavaScript?", e "O que ele faz?", para você se sentir confortável com a proposta da linguagem.`

### 12. [JavaScript Tutorial - Documentação W3Schools](https://www.w3schools.com/js/default.asp)
`Este tutorial ensina JavaScript do básico ao avançado. Em Inglês`

### 13. [Guia de JavaScript: o que é e como aprender a linguagem mais popular do mundo?](https://www.alura.com.br/artigos/javascript)
`Neste artigo, você vai conhecer o que é JavaScript, para que serve e como utilizá-lo.`

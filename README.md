## O que é TypeScript?
TypeScript é um superset do JavaScript que adiciona tipagem estática opcional e outras funcionalidades, ajudando a melhorar a qualidade do código e a facilitar a manutenção.

## Tipos Básicos
TypeScript tem tipos primitivos que ajudam a definir a natureza dos dados:
- string: texto
- number: números
- boolean: verdadeiro ou falso
- any: qualquer tipo (evitar quando possível)
- void: sem retorno (geralmente usado em funções)
- null e undefined: representando a ausência de valor

## Inferência de Tipos
TypeScript pode inferir tipos automaticamente, com base na atribuição de valores. Por exemplo:
```bash
let nome = "Camilla"; // Tipo inferido como string
```

## Anotações de Tipos
Você pode especificar explicitamente os tipos de variáveis, parâmetros de função e retornos:
```bash
let idade: number = 30;

function soma(a: number, b: number): number {
  return a + b;
}
```

## Interfaces
As interfaces permitem definir a forma de um objeto, ajudando na organização e reutilização de tipos:
```bash
interface Pessoa {
  nome: string;
  idade: number;
}

const pessoa: Pessoa = {
  nome: "Camilla",
  idade: 30,
};
```

## Configuração do TypeScript
O `tsconfig.json` é um arquivo de configuração fundamental em projetos TypeScript, que define as opções do compilador e determina como o TypeScript deve se comportar durante a compilação. Aqui estão os aspectos mais importantes do tsconfig.json e suas opções:
```bash
{
  "compilerOptions": {
    // Opções do compilador
  },
  "include": [
    // Arquivos ou diretórios a serem incluídos
  ],
  "exclude": [
    // Arquivos ou diretórios a serem excluídos
  ],
  "files": [
    // Arquivos específicos a serem incluídos
  ]
}
```

## Compilador TypeScript (tsc)
O compilador TypeScript, conhecido como `tsc`, é a ferramenta que converte código TypeScript em JavaScript. Essa conversão é necessária porque navegadores e ambientes de execução JavaScript (como Node.js) não entendem TypeScript diretamente. O tsc analisa o código TypeScript, verifica a tipagem e produz o código JavaScript correspondente, que pode ser executado em qualquer ambiente compatível.

## Pasta `dist`
A pasta dist (abreviação de "distribution") é uma convenção comum em projetos para armazenar os arquivos compilados. Quando você compila seu código TypeScript, é uma boa prática configurar o outDir no tsconfig.json para direcionar a saída da compilação para a pasta dist. Isso ajuda a manter o código-fonte TypeScript separado do código JavaScript gerado.

## npm run build
O comando npm run build é uma convenção comum em projetos JavaScript, incluindo aqueles que utilizam TypeScript. Esse comando geralmente é usado para compilar o código TypeScript e gerar a versão pronta para produção da aplicação. Para usar o comando npm run build, você deve definir um script no seu arquivo package.json. Normalmente, isso envolve usar o comando tsc para compilar o código TypeScript.

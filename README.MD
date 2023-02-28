# Aprendendo Sass

Este repositório foi criado para ensinar os fundamentos do Sass, um pré-processador CSS que permite escrever código CSS mais rápido e eficiente. O Sass é um dos pré-processadores CSS mais populares e é amplamente utilizado em projetos web.

## O que é Sass?

Sass é um pré-processador CSS que estende a sintaxe do CSS e adiciona recursos avançados, como variáveis, nesting, mixins, funções e muito mais. O Sass permite escrever código CSS de forma mais eficiente e organizada, economizando tempo e esforço.

## Variáveis do Sass

As variáveis do Sass permitem definir valores que podem ser reutilizados em todo o código. Elas são definidas com o símbolo `$` seguido do nome da variável e do valor a ser atribuído. Por exemplo:

```scss
$cor-primaria: #007bff;
$cor-secundaria: #6c757d;

.botao {
  background-color: $cor-primaria;
  color: $cor-secundaria;
}
```

## Nesting do Sass

O nesting é um recurso do Sass que permite aninhar seletores de CSS dentro de outros seletores, criando uma hierarquia visual do código. Isso ajuda a organizar e simplificar o código. Por exemplo:

```scss
.container {
  width: 100%;

  .item {
    display: inline-block;
    margin-right: 10px;
  }
}
```

## Referenciando ao seletor atual "&"

O símbolo & é usado para referenciar o seletor atual dentro do código Sass. Isso é especialmente útil para criar seletores mais específicos e manter a hierarquia do código. Por exemplo:

```scss
.botao {
  background-color: #007bff;

  &:hover {
    background-color: #0069d9;
  }

  &--grande {
    font-size: 1.5rem;
  }
}
```

## Imports

O Sass permite importar arquivos CSS e Sass em outros arquivos Sass, permitindo uma organização mais modular do código. Por exemplo:
    
```scss
// estilo.scss
@import 'botao';
@import 'menu';

// botao.scss
.botao {
  background-color: #007bff;
}

// menu.scss
.menu {
  display: flex;
}
```

## Mixins

Os mixins são um recurso do Sass que permite definir um conjunto de regras CSS que podem ser reutilizadas em todo o código. Eles são definidos com o símbolo @mixin seguido do nome do mixin e do conjunto de regras CSS. Por exemplo:

```scss
@mixin flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

.botao {
  @include flex-center;
}
```


## Funções

As funções do Sass permitem realizar cálculos e manipular valores em tempo de compilação. Elas são definidas com o símbolo @function seguido do nome da função e do conjunto de regras CSS. Por exemplo:

```scss
@function calcula-rem($tamanho-pixel) {
  $base-fonte: 16px;
  @return ($tamanho-pixel / $base-fonte) * 1rem;
}

.botao {
  font-size: calcula-rem(24px);
}
```

## Conclusão

O Sass é uma ferramenta poderosa que pode tornar o processo de desenvolvimento web mais rápido, organizado e eficiente. Ao utilizar os recursos apresentados neste repositório, é possível escrever código CSS de forma mais limpa, modular e fácil de manter. Esperamos que este tutorial tenha sido útil para você começar a trabalhar com Sass em seus projetos.

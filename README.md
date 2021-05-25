# Material de Apoio - Bootcamp Santander

## Aula 1: Configurando Ambiente - Frontend

### Links

- Node.js - [https://nodejs.org/en/](https://nodejs.org/en/)
- Visual Studio Code - [https://code.visualstudio.com/](https://code.visualstudio.com/)
- Angular CLI - [https://angular.io/cli](https://angular.io/cli)

## Aula 3: Configurando o Projeto

### Trecho de código para adicionar o [normalize](https://necolas.github.io/normalize.css/):

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css" integrity="sha512-NhSC1YmyruXifcj/KFRWoC561YpHpc5Jtzgvbuzx5VozKpWvQ+4nXhPdFgmx8xqexRcpAglTj9sIBWINXa8x5w==" crossorigin="anonymous" />
```

Mais informações sobre o **box-sizing**:  [https://tableless.github.io/iniciantes/manual/css/box-model.html](https://tableless.github.io/iniciantes/manual/css/box-model.html)

Mais informações sobre o **height: 100%**: [https://imasters.com.br/css/por-que-height-100-nao-funciona](https://imasters.com.br/css/por-que-height-100-nao-funciona) 

### Código do CSS Global da aplicação

```css
:root {
  --background-color: #EAEAEA;
  --primary-color: #EA1D25;
  --secondary-color: #FFFFFF;
  --text-color: #5C6369;
  --text-color-light: rgba(92, 99, 105, 0.45);
  --positive-variation-color: #87D883;
  --negative-variation-color: #F55A5F;
}

* {
  box-sizing: border-box;
}

html, body {
  height: 100%;
  width: 100%;
  margin: 0;
  background-color: var(--background-color);
  font-family: 'Segoe UI', sans-serif;
}
```

## Aula 4: Criação dos componentes da aplicação

### Links com mais informações sobre CSS

- Guia completo do Flexbox - [https://css-tricks.com/snippets/css/a-guide-to-flexbox/](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- Flexbox Froggy - [https://flexboxfroggy.com/](https://flexboxfroggy.com/)
- Conceitos básicos de Flexbox - [https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)
- Conceitos básicos do CSS Grid - [https://tableless.com.br/um-pouco-sobre-css-grid-layout/](https://tableless.com.br/um-pouco-sobre-css-grid-layout/)
- Guia completo do CSS Grid - [https://css-tricks.com/snippets/css/complete-guide-grid/](https://css-tricks.com/snippets/css/complete-guide-grid/)
- Unidades de medidas relativas - [https://desenvolvimentoparaweb.com/css/unidades-css-rem-vh-vw-vmin-vmax-ex-ch/](https://desenvolvimentoparaweb.com/css/unidades-css-rem-vh-vw-vmin-vmax-ex-ch/)

## Aula 5: Integração com a API

### Entendo um pouco melhor sobre Javascript/Typescript

- Entendendo o Hoisting do javascript - [https://medium.com/opensanca/hoisting-em-javascript-9f22b1f78448](https://medium.com/opensanca/hoisting-em-javascript-9f22b1f78448)
- Um pouco sobre Promises e assincronismo - [https://medium.com/trainingcenter/entendendo-promises-de-uma-vez-por-todas-32442ec725c2](https://medium.com/trainingcenter/entendendo-promises-de-uma-vez-por-todas-32442ec725c2)
- Template Strings / Interpolação de Strings - [https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Template_literals](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Template_literals)
- Tipos do Typescript - [https://bognarjunior.wordpress.com/2018/09/16/typescript-tipos-de-dados/](https://bognarjunior.wordpress.com/2018/09/16/typescript-tipos-de-dados/)

### Bindings e diretivas do Angular

- Property Binding - [https://angular.io/guide/property-binding](https://angular.io/guide/property-binding)
- Binding de atributos - [https://angular.io/guide/attribute-binding](https://angular.io/guide/attribute-binding)
- Inputs e Outputs - [https://angular.io/guide/inputs-outputs](https://angular.io/guide/inputs-outputs)
- Diretivas Básicas - [https://angular.io/guide/built-in-directives](https://angular.io/guide/built-in-directives)

### Códigos das sombras e transições CSS

header.component.css:

```css
.header {
  width: 100%;
  padding: 1rem 1.5rem;
	...

  box-shadow: 0 3px 6px rgba(0,0,0,0.16), 0 3px 6px rgba(0,0,0,0.23);
}
```

stock-card.component:

```css
.stock-card-container {
  width: 21.375rem;
  height: 13.8125rem;
  background-color: var(--secondary-color);
	...

  box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
  transition: all 0.3s cubic-bezier(.25,.8,.25,1);
}

.stock-card-container:hover {
  box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
}
```

## Aula 6: Publicando o Projeto no GitHub Pages

### Links

- GitHub - [https://github.com/](https://github.com/)
- angular-cli-ghpages - [https://github.com/angular-schule/angular-cli-ghpages/#readme](https://github.com/angular-schule/angular-cli-ghpages/#readme)

### Comando do Angular CLI para realizar o Deploy

```json
"scripts": {
	....
	"deploy":  "ng deploy --base-href=https://<seu-usuario>.github.io/<repositorio>/",
	...
}
```

Será necessário substituir o `<seu-usuário>` pelo seu nome de usuário do Github e o `<repositorio>` pelo nome do repositório criado anteriormente.

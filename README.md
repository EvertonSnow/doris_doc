# Doris (Provador Virtual)

<!-- DOCS-IGNORE:start -->
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->

[![All Contributors](https://img.shields.io/badge/all_contributors-0-orange.svg?style=flat-square)](#contributors-)

<!-- ALL-CONTRIBUTORS-BADGE:END -->
<!-- DOCS-IGNORE:end -->

Um provador virtual que te dá o poder de experimentar roupas sem precisar ir à loja ou ficar colocando e tirando peças.

A IA da Doris, dá a possibilidade do seu cliente poder experimentar peças diretamente no seu corpo, fazer combinações e descobrir qual é o tamanho ideal para o seu tipo de corpo sem sair da sua casa.

<img src="https://assets.website-files.com/645000b409645991ca395152/645023fae36dc9af099227e3_01-Widget.png" width="560"/>

Com uma foto frontal e uma de perfil, seus clientes podem experimentar virtualmente todas as peças que estarão disponibilizadas na Doris e saber qual o tamanho ideal!

<img src="https://assets.website-files.com/645000b409645991ca395152/6453fc9cbef8e5315e84627d_w-04.png" width="560"/>

A Doris traz a tecnologia de Try-On, Mix&Match, Sizing e Recomendações para o seu e-commerce de moda, melhorando ainda mais a experiência de compra.

<img src="https://assets.website-files.com/645000b409645991ca395152/6452aac3f96b4a1afb8058bd_T2.png" width="560"/>

Transformando a experiência em eficiência: com mais conversões, aumento no engajamento e menos reversa!

## Informações Adicionais

Para a instalação do widget Doris, é necessário: Possuir conta e credenciais Doris; permitir a instalação do Módulo VTEX/Doris de maneira adequada para atender:

- Instalação do Widget;
- Integração do catálogo de produtos;
- Manutenção do catálogo (atualização);
- E, a integração com o carrinho de compra.

Para eventuais dúvidas, consulte a documentação para obter mais informações sobre como ter acesso a Doris ou entre em contato através de nosso site.

## Instalação

1. Instale o App de Provador da Doris Mobi no seu ambiente VTEX, você pode utilizar o VTEX IO Toolbelt (CLI), usando 0 seguinte comando:

```sh
vtex install codeby.dorismobi@0.3.9
```

2. Configure via admin, na seção Doris Settings no app store as seguintes informações abaixo:

- Public Api Key;
- Private Api Key;
- Capa da abertura: imagem a ser utilizada na abertura do app ao clicar no botão;
- Imagem de background do botão: campo opcional, ao qual o usuário pode inserir uma imagem no botão;
- Cor primária: caso opte por não utilizar uma imagem, pode ser inserido somente uma cor no botão em hexadecimal;
- Qual é o parâmetro de identificação única dos seus produtos: forma como os produtos podem ser identificados, como EAN e Vtex_id;
- Qual é atributo que identifica o código único da cor?
- Informe o parâmetro que identifica o tamanho (size specification);
- Informe o atributo que identifica a marca do produto;
- Informe o atributo que identifica o código único dos produtos;
- Chave da Vtex e Token da Vtex: poderá ser verificado como cadastrar no seguinte link: <https://help.vtex.com/pt/tutorial/chaves-de-aplicacao--2iffYzlvvz4BDMr6WGUtet>
  - Vtex App Key;
  - Vtex App Token;

- **Busque diretamente o app em:** <https://mystore.myvtex.com/admin/apps/>

3. Adicione o `codeby.dorismobi` como uma peerDependencies no seu `manifest.json`:

```json
  peerDependencies: {
    "codeby.dorismobi": "0.x"
  }
```

4. Adicione o bloco `"doris-button"` no seu tema, dentro de um context de produto, por exmplo:
   em baixo do botão de comprar/adicionar ao carrinho.

```json
{
  "flex-layout.col#right-col": {
    "props": {
      "preventVerticalStretch": true,
      "rowGap": 0
    },
    "children": [
      "flex-layout.row#product-name",
      "product-rating-summary",
      "flex-layout.row#list-price-savings",
      "flex-layout.row#selling-price",
      "product-installments",
      "product-separator",
      "product-identifier.product",
      "sku-selector",
      "product-quantity",
      "product-assembly-options",
      "product-gifts",
      "flex-layout.row#buy-button",
    + "doris-button",
      "availability-subscriber",
      "shipping-simulator",
      "share#default"
    ]
  }
}
```

## Resultado

<img src="https://codeby.vteximg.com.br/arquivos/doris-mobi-screen-1.png" width="560"/>
<br/>
<img src="https://codeby.vteximg.com.br/arquivos/doris-mobi-screen-2.png" width="560"/>

<!-- DOCS-IGNORE:start -->

## Contribuidores

Desenvolvido por:

<a href="https://codeby.global/" target="_blank" alt="Codeby"><img src="https://codeby.global/cdn/shop/files/logo-default-v2.png?v=1684868339&width=120"></a>

Contribuição:

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

<!-- DOCS-IGNORE:end -->

## Termos e Condições

[Termos de Uso e Política de Privacidade](https://www.doris.mobi/termos-e-condicoes-e-politica-de-privacidade)

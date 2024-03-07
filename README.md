# Doris (Virtual Try-On) 🛒

<!-- DOCS-IGNORE:start -->
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->

[![All Contributors](https://img.shields.io/badge/all_contributors-0-orange.svg?style=flat-square)](#contributors-)

<!-- ALL-CONTRIBUTORS-BADGE:END -->
<!-- DOCS-IGNORE:end -->

Introducing Virtual Fitting Room Doris, a revolutionary tool that empowers you to try on clothes in the comfort of your home, without the need to travel to the store or the hassle of constantly putting on and taking off pieces.

With artificial intelligence integrated into the platform, the customer has the unique opportunity to see the pieces directly on their body, explore different combinations, and find the perfect size for their body type, all without having to leave home.

<img src="https://assets.website-files.com/645000b409645991ca395152/645023fae36dc9af099227e3_01-Widget.png" width="560"/>

Using only a front and profile photo, customers have access to the unique experience of virtually trying on all available pieces on the Doris platform, ensuring the discovery of the ideal size for each individual.

<img src="https://assets.website-files.com/645000b409645991ca395152/6453fc9cbef8e5315e84627d_w-04.png" width="560"/>

Doris brings Try-On, Mix&Match, and Sizing technology, along with recommendations to enhance the shopping experience on its fashion e-commerce.

<img src="https://assets.website-files.com/645000b409645991ca395152/6452aac3f96b4a1afb8058bd_T2.png" width="560"/>

Transforming experience into efficiency: with more conversions, increased engagement, and fewer returns!

## Important Information ⚠️

For the installation of the Doris widget, it is necessary to have a Doris account and credentials to allow the proper installation of the VTEX/Doris Module, including:

- Widget installation; ✅
- Integration of the product catalog; ✅
- Catalog maintenance (updates); ✅
- Integration with the shopping cart. ✅

## Compatibility 🧩

This app is only compatible with VTEX IO stores.

## Installation 💻

Before installing the Doris Mobi Fitting Room app in your VTEX environment, you'll need to use the [VTEX IO Toolbelt (CLI)](https://developers.vtex.com/docs/guides/vtex-io-documentation-vtex-io-cli-install), and after its installation, proceed with the following steps:


1. To install the app, simply run the following command in your VTEX account:

```sh
vtex install codeby.dorismobi@0.3.18
```

Access the /apps route in the store's admin. In the list of installed apps, look for our app, which should be displayed as follows:

<img src="https://github.com/codeby-global/codeby.doris-mobi/assets/19894638/2e3dba67-65ef-484e-a5ec-930ad34c65c1" width="460"/>


2. Go to the app's "Settings" and configure the following information according to your integration and store data:

- Public Api Key Doris;
- Private Api Key Doris;
- Opening cover: image to be used in the app's opening when clicking the button, for example:
  <img src="https://github.com/codeby-global/codeby.doris-mobi/assets/14927925/7905b030-29b5-41b8-b2ff-4f1313bea0d7" width="460"/>
- Button background image: optional field, where the user can insert an image on the button, for example:
  <img src="https://github.com/codeby-global/codeby.doris-mobi/assets/14927925/7bfd5a71-2345-43c3-8059-3546644a02a3" width="460"/>
- Primary color: if you choose not to use an image, you can enter only a color on the button in hexadecimal;
- What is the unique identification parameter for your products: how products can be identified, such as:
  - Product reference code (Ref_id)
  - EAN
  - Vtex product ID (Vtex_id);
- What attribute identifies the unique color code?
- Provide the parameter that identifies the size (size specification);
- Provide the attribute that identifies the product brand;
- Provide the attribute that identifies the unique product codes;
- Vtex Key and Vtex Token: can be checked on how to register at the following link: <https://help.vtex.com/pt/tutorial/chaves-de-aplicacao--2iffYzlvvz4BDMr6WGUtet>
  - Vtex App Key;
  - Vtex App Token;
  - Catalog, Vtex IO, Logistics, Master data, Vtable ⚠️

  The access key needs to have at minimum the following permissions:

## Catalog:

* Product Management
* Product Form
* SKU Images Management
* Product and SKU Management
* Fields List
* Attributes Management
* Value Fields List
* Attribute Values Management
* Category
* Similar Category
* Price Range
* Providers
* Supplier Management
* Groups
* Brands
* SKUs
* Field Validation
* Value Field Validation


## Vtex IO - Infrastructure:

* Read Workspace Apps
* Link App
* Install App
* Vbase Read Only
* Vbase Read Write
* Read Workspace Services
* Install Service
* Log Access - Read-only
* Read Published Service
* Debug App
* Import Redirects
* Workspace Manipulation
* Read Edition
* Allow APP Configuration
* Change Sponsored Tenant Edition

## Logistics - Logistics Viewer:

* Logistics Inventory Read Only
* Logistics Shipping Read Only
* Transportation Read Only

## Master Data - Generic Resources:

* Access to Insert and Edit but Not to Delete

## Vtable 
* Main Access
##

Example:

<img src="https://github.com/codeby-global/codeby.doris-mobi/assets/19894638/1b939b25-289d-4d66-bbbc-f723bf0db811" width="560"/>

3. Add `codeby.dorismobi` as a peerDependencies in your theme's `manifest.json`:

```json
  peerDependencies: {
    "codeby.dorismobi": "0.x"
  }
```

4. Add the `"doris-button"` block to your theme. It needs to be within the structure of the [Vtex product page](https://developers.vtex.com/docs/guides/vtex-io-documentation-building-a-product-details-page), for example, below the buy/add to cart button.

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

## Result 🎯

<img src="https://codeby.vteximg.com.br/arquivos/doris-mobi-screen-1.png" width="560"/>
<br/>
<img src="https://codeby.vteximg.com.br/arquivos/doris-mobi-screen-2.png" width="560"/>

<!-- DOCS-IGNORE:start -->

## Contributors 🧑‍💻

Developed by:

<a href="https://codeby.global/" target="_blank" alt="Codeby"><img src="https://codeby.global/cdn/shop/files/logo-default-v2.png?v=1684868339&width=120"></a>

<!-- ALL-CONTRIBUTORS-LIST:END -->

<!-- DOCS-IGNORE:end -->

## Terms and Conditions 📃

[Termos de Uso e Política de Privacidade](https://www.doris.mobi/termos-e-condicoes-e-politica-de-privacidade)

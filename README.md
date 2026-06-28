# Quickstart for Bitasmbl project (Angular)

## 1) Install Bitasmbl-CLI package

```bash
npm i bitasmbl-cli
```

## 2) Run bitasmbl command to set up the project

```bash
bitasmbl pull --repoUrl https://github.com/he1snber8/Bitasmbl_unique-name-for-angular_5bb_419 --appId 419 --repoId 246
```

## 3) Enter into the main directory and start coding!

```bash
cd Bitasmbl_unique-name-for-angular_5bb_419
```

## Customize requirements in a way you like

Bitasmbl organizes development into requirements. Each requirement describes a feature or implementation goal and can define suggested file locations through a `paths` array.

The `paths` property acts as a mapping guideline, helping contributors understand where related code should live.

You can customize `paths` mappings through the `bitasmbl.json` file.

{"Requirement":"Build learning frontend","Paths":["**/src/app/modules/**","**/src/app/components/**","**/src/app/pages/**","**/src/app/routes/**"]}

## Requirement Evaluation

Bitasmbl includes a requirement evaluation workflow that lets contributors select a task and submit work for validation.

Run:

```bash
bitasmbl evaluate
```

Example output:

<pre>
? Available Requirements:

❯ [<span style="color:#9333ea">1</span>] <span style="color:#9333ea"> Define portfolio layout </span>            [3]
  [2] Build showcase components            [3]
  [3] Implement navigation routing         [3]
</pre>

`[x]` on the right represents the number of submission attempts remaining for a requirement.

## Example evaluation result

```ts
/*
|--------------------------------------------------------------------------
| BITASMBL EVALUATION
|--------------------------------------------------------------------------
| REQUIREMENT:
| Implement product catalog UI
|
| SCORE: 22/100
| STATUS: FAIL ✕
|
| INSIGHT:
| The component renders static product data and does not use a service,
| typed models, loading state, error handling, or reusable UI structure.
|--------------------------------------------------------------------------
*/

import { Component } from '@angular/core';

@Component({
  selector: 'app-product-catalog',
  template: `
    <main class="catalog">
      <h1>Products</h1>

      <section class="grid">
        <article *ngFor="let product of products">
          <h2>{{ product.name }}</h2>
          <p>{{ product.price }}</p>
        </article>
      </section>
    </main>
  `,
})
export class ProductCatalogComponent {
  products = [
    { id: 1, name: 'Keyboard', price: 89.99 },
    { id: 2, name: 'Mouse', price: 49.99 },
  ];
}
```

## Learn More

For complete command references, workflow explanations, and additional documentation, visit:

👉 [Bitasmbl Documentation](https://bitasmbl.com/docs)

## CSS Combinators Overview

- **Adjacent Sibling Combinator (`+`)**: Selects the element that directly follows a specified element.
    - **Example:**
      ```html
      <div></div>
      <p>I will be red</p>
      <p>I will not be affected</p>
  
      <style>
      div + p {
          color: red;
      }
      </style>
      ```
    - **Explanation:** Only the first `<p>` after the `<div>` will be red.

- **General Sibling Combinator (`~`)**: Selects all sibling elements that follow a specified element.
    - **Example:**
      ```html
      <div></div>
      <p>I will be red</p>
      <p>I will also be red</p>
  
      <style>
      div ~ p {
          color: red;
      }
      </style>
      ```
    - **Explanation:** All `<p>` elements that follow the `<div>` at the same level will be red.

- **Child Combinator (`>`)**: Selects all elements that are direct children of a specified element.
    - **Example:**
      ```html
      <div>
        <p>I will be red</p>
        <span>
          <p>I will not be affected</p>
        </span>
      </div>
  
      <style>
      div > p {
          color: red;
      }
      </style>
      ```
    - **Explanation:** Only the `<p>` that is a direct child of the `<div>` will be red, not the one inside the `<span>`.

- **Descendant Combinator (Space)**: Selects all elements that are descendants of a specified element.
    - **Example:**
      ```html
      <div>
        <p>I will be red</p>
        <span>
          <p>I will also be red</p>
        </span>
      </div>
  
      <style>
      div p {
          color: red;
      }
      </style>
      ```
    - **Explanation:** Both `<p>` elements inside the `<div>` will be red, regardless of their nesting level.

By ZvSimon
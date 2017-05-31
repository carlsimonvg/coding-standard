# CSS Rules

## Naming
1. css names are all lowercase and new words are seprated by "-" e.g. "some-class"

## Variables
1. Variables are used when css properties are modified by the application.
1. They are not to be used as a distribution of constants, that is what scss is for.

Animations initiated from js should pass on changed data via variables.

```js
element.style.setProperty("--duration", 300);
element.style.setProperty("--top", 100);
```

## Namespaces
1. Global classes do not require namespaces
1. Components must be name spaced in scss using the component element as the root element.

Namespace example:
```scss
my-component {
  .part1 {
    background: $primary-background;
  }
  
  .part2 {
    background: $secondary-background;
  }
}
```

## Location
SCSS markup must be placed in a file appropriately named.
Markup must follow a mobile first where possible.

Mobile spesific changes must be located in a mobile folder   
Desktop spesific changes must be located in a desktop folder
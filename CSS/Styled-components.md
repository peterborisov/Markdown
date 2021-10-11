# Styled Components

## Basics

### Props
```
const Button = styled.button`
  background: ${props => props.primary ? "black" : "white"};
`;

render(
  <div>
    <Button primary>Primary</Button>
  </div>
);
```
### Extending Styles
```
const Button = styled.button`
  color: palevioletred;
`;

const TomatoButton = styled(Button)`
  color: tomato;
  border-color: tomato;
`;
render(
  <div>
    <Button>Normal Button</Button>
    <TomatoButton>Tomato Button</TomatoButton>
  </div>
);
```
### Pseudoelements, pseudoselectors, and nesting
- The ampersand (&) can be used to refer back to the main component. 
- If you put selectors in without the ampersand, they will refer to children of the component.
```
const Thing = styled.div.attrs((/* props */) => ({ tabIndex: 0 }))`
  color: blue;

  &:hover {
    color: red; // when hovered
  }

  & ~ & {
    background: tomato; // as a sibling
  }

  & + & {
    background: lime; // next to
  }

  &.something {
    background: orange; // tagged with an additional CSS class ".something"
  }

  .something-else & {
    border: 1px solid; // inside another element labeled ".something-else"
  }
`
```
### Attaching additional props
- To avoid unnecessary wrappers that just pass on some props to the rendered component, or element, you can use the .attrs constructor. It allows you to attach additional props (or "attributes") to a component.
```
const Input = styled.input.attrs(props => ({
  type: "text",
  size: props.size,
}))`
`;
render(
  <div>
    <Input placeholder="A small text input" />
    <br />
    <Input placeholder="A bigger text input" size="2em" />
  </div>
);
```

## Advanced Usage

### Theming
- styled-components has full theming support by exporting a ThemeProvider wrapper component. This component provides a theme to all React components underneath itself via the context API.

### Getting the theme without styled components
- via withTheme higher-order component
- via useContext React hook

### Referring to other components
```
const Link = styled.a`
  color: palevioletred;
`;

const Icon = styled.svg`
  ${Link}:hover & {
    fill: rebeccapurple;
  }
`;
`;

render(
  <Link>
    <Icon />
  </Link>
);
```

## API Reference

# Dev Server

Feel free to import TypeScript files in the script tag!

## Usage
```
Dev Server

INSTALL:
  deno install --allow-net --allow-read --allow-write --unstable https://deno.land/x/dev_server/mod.ts

USAGE:
  dev_server [path] [options]

OPTIONS:
  -h, --help          Prints help information
  -p, --port <port>   Set port
  --tsconfig <path>   Path to tsconfig.json
  --template <name>   Create app with template
```

## Getting Started

```
dev_server my_app --template react_app --port 8000
```

```html
<!-- index.html -->
<div id="root"></div>
<script crossorigin src="https://unpkg.com/react@16/umd/react.production.min.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@16/umd/react-dom.production.min.js"></script>
<script type="module" src="./index.tsx"></script>
```

```tsx
// index.tsx
const { useState } = React;

function Index(): JSX.Element {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}

ReactDOM.render(<Index />, document.getElementById("root"));
```

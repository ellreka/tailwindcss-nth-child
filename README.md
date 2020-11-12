# tailwind-nth-child

## Install

```bash
yarn add -D tailwind-nth-child
```

```javascript
plugins: [require('tailwindcss-nth-child')(['3n', 'n+3'])]
```

## Usage

```javascript
variants: {
  textColor: ({ after }) => after(['nth-child-3n', 'nth-child-n+3'])
}
```

```jsx
<ul>
  {[1, 2, 3, 4, 5, 6].map((v) => (
    <li key={v} className="nth-child-3n:text-red-500">
      foo_{v}
    </li>
  ))}
</ul>
```

```js
・foo_1
・foo_2
・foo_3 // textColor is red
・foo_4
・foo_5
・foo_6 // textColor is red
```

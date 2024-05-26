[![npm](https://img.shields.io/npm/v/@zitterorg/delectus-est.svg)](https://www.npmjs.com/package/@zitterorg/delectus-est) ![downloads](https://img.shields.io/npm/dt/@zitterorg/delectus-est.svg) [![CI](https://github.com/zitterorg/delectus-est/actions/workflows/ci.yml/badge.svg)](https://github.com/zitterorg/delectus-est/actions)

# Merge-Refs

A function that merges React refs into one. Filters out invalid (eg. falsy) refs as well and returns original ref if only one valid ref was given.

## tl;dr

- Install by executing `npm install @zitterorg/delectus-est` or `yarn add @zitterorg/delectus-est`.
- Import by adding `import mergeRefs from '@zitterorg/delectus-est'`.
- Use it in `ref` like so: `<div ref={mergeRefs(ref, someOtherRef)} />`

## Accepted refs

- Refs created using `createRef()`
- Refs created using `useRef()`
- Functional refs

## Example

```tsx
function Hello() {
  const ref1 = useRef<HTMLDivElement>(); // I'm going to be updated!
  const ref2 = (element: HTMLDivElement) => {
    // I'm going to be called!
  };

  return <div ref={mergeRefs(ref1, ref2)} />;
}
```

## License

The MIT License.

## Author

<table>
  <tr>
    <td >
      <img src="https://avatars.githubusercontent.com/u/5426427?v=4&s=128" width="64" height="64" alt="Wojciech Maj">
    </td>
    <td>
      <a href="https://github.com/wojtekmaj">Wojciech Maj</a>
    </td>
  </tr>
</table>

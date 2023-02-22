# useIntersectionObserver-React-Hook
This is a custom React hook that simplifies the process of using the Intersection Observer API to detect when an element is visible within the viewport. It is useful for lazy-loading images or other resources, as well as for implementing "infinite scroll" pagination.

## Installation

Install using [npm](https://www.npmjs.com/):

`npm i useintersectionobserver-react-hook`

## Usage

Import the `useIntersectionObserver` hook and use it in your component:

```jsx
import { useIntersectionObserver } from 'use-intersection-observer';

function MyComponent() {
const [targetRef, isIntersecting] = useIntersectionObserver();

return (
<div ref={targetRef}>
{isIntersecting ? 'Element is visible' : 'Element is not visible'}
</div>
);
}
```

You can also pass options to the hook, such as the root element, root margin, and threshold:

```jsx
const options = {
  root: null,
  rootMargin: '0px',
  threshold: 1.0
};

const [targetRef, isIntersecting] = useIntersectionObserver(options);
```

If you don't pass the options to the hook, the ones above will be applied by default.

## License

This project is licensed under the [MIT License](https://opensource.org/license/mit/).

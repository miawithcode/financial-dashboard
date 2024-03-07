# Simplified Financial Dashboard

> This is a Next.js project-based learning from [Next.js Website](https://nextjs.org/learn/dashboard-app).


## CSS Styling

> Take a look at the [CSS documentation](https://nextjs.org/docs/app/building-your-application/styling) for more information.

1. Global styles - import `global.css` in `/app/layout.tsx`
2. How to apply CSS styles in Next.js
   - [Tailwind CSS](https://tailwindcss.com/)
   - [CSS Modules](https://nextjs.org/docs/basic-features/built-in-css-support)
   - Sass
   - CSS-in-JS libraries such as [styled-components](https://github.com/vercel/next.js/tree/canary/examples/with-styled-components)

### `clsx` Library - conditionally apply class names

> [clsx](https://www.npmjs.com/package/clsx) is a library that lets you toggle class names easily. View [documentation](https://github.com/lukeed/clsx) for more details.

Basic usage: 
```tsx
import clsx from 'clsx';
 
export default function InvoiceStatus({ status }: { status: string }) {
  return (
    <span
      className={clsx(
        'inline-flex items-center rounded-full px-2 py-1 text-sm',
        {
          'bg-gray-100 text-gray-500': status === 'pending',
          'bg-green-500 text-white': status === 'paid',
        },
      )}
    >
    // ...
)}
```

## Fonts

> See the documentation for [adding multiple fonts](https://nextjs.org/docs/app/building-your-application/optimizing/fonts#using-multiple-fonts) and the [full list of options](https://nextjs.org/docs/app/api-reference/components/font#font-function-arguments).

Next.js automatically optimizes fonts in the application when you use the next/font module. 

It downloads font files at build time and hosts them with your other static assets. 

This means when a user visits your application, there are no additional network requests for fonts which would impact performance.
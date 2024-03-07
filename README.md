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
# Simplified Financial Dashboard

> This is a Next.js 14 project-based learning from [Next.js Website](https://nextjs.org/learn/dashboard-app).


## `clsx` Library - conditionally apply class names

[clsx](https://www.npmjs.com/package/clsx) is a library that lets you toggle class names easily. View [documentation](https://github.com/lukeed/clsx) for more details.

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
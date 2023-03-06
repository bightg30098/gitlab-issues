Create Shared Component - Select

1. Create a folder named `select` under `packages/ui/src/components` folder.
2. Create a file named `Select.tsx` under `packages/ui/src/components/select` folder.
3. Create a file named `Select.stories.tsx` under `packages/ui/src/components/select` folder.

(There is a existing `Select` in `apps/eco-ssot/components/select/Select.jsx`, you can take a look at it.)

---

In `Select.tsx` file,you'll need to write a component with `theme` prop support.:

- wistron: for wistron theme
- dt: for dt theme

You can find the theme color defined in `packages/tailwind-config/{dt,wistron}.preset.js`.

Basic:

- [ ] Implement a listbox component using [Headless UI](https://headlessui.com/).

Advanced:

- [ ] Position the listbox component using [Floating UI](https://floating-ui.com/).

`placement` prop support:
| 'top'
| 'top-start'
| 'top-end'
| 'right'
| 'right-start'
| 'right-end'
| 'bottom'
| 'bottom-start'
| 'bottom-end'
| 'left'
| 'left-start'
| 'left-end';

`strategy` prop support: 'absolute' | 'fixed'

---

In `Select.stories.tsx` file,you'll need to write a story for the component.

Example Usage:

```tsx
<Select
  options={options}
  onChange={() => {}}
  placement="top"
  strategy="fixed"
/>
```

- [ ] Add a story for the component.

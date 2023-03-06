I wrote some feedbacks to your EditableTable. So far so good!

Please checkout to `51-editable-table-feedbacks` for details.

There are some improvements need to be done:

- [ ] Reuse BaseTable. Either `return <BaseTable />` or pass prop to it `<BaseTable editable />`
- [ ] No `theme === 'wistron'` checking everywhere

And most important thing for better UX:

- [ ] **NO LAYOUT SHIFT WHEN TOGGLING EDITING**

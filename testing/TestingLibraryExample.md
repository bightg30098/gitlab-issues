We use [vitest](https://vitest.dev/) as our unit test framework.

Following tools are used to test our UI:

- [React Testing Library](https://testing-library.com/docs/react-testing-library/intro)
- [Mock Service Worker](https://mswjs.io/)

### React Testing Library

- Read the quick start [guide](https://testing-library.com/docs/react-testing-library/example-intro) to understand the basic usage.
- Before writing unit tests, read the [best practice](https://kentcdodds.com/blog/common-mistakes-with-react-testing-library) of React Testing Library

### Mock service worker

- Update the mock of API responses under `__mocks__` folder if your tests need that API.

### Writing tests

1. Create testing file under `src/__tests__/`
2. `Describe` the test suite.
3. Expect the correct behavior `it` will happen.
4. You may need to use `renderWithProviders` if your component is wrapped in `Router` or whatever `providers`.
5. Run `pnpm test:eco-ssot` or `cd apps/eco-ssot && pnpm test` start testing.

examples:

`src/__tests__/components/Button.test.jsx`

```tsx
describe("Button", () => {
  it("renders primary button", () => {
    const { container } = render(<Button variant="primary" />);

    /**
     * The `container` object contains the rendered component.
     * You can use the `toHaveClass` matcher to check if the component has the correct class.
     * The `bg-primary-600` class is applied to the primary button.
     */
    expect(container.firstChild).toHaveClass("bg-primary-600");
  });
});
```

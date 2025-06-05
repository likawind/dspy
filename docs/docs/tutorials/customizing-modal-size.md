# Customizing Modal Size with Style API

Mantine provides several ways to customize the size of a Modal component. This guide will help you understand how to adjust the modal size using the available props and clarify the limitations regarding custom CSS variables.

## Using the `size` Prop

The simplest way to set the size of a Mantine Modal is by using the `size` prop. This prop accepts predefined size values like `"xs"`, `"sm"`, `"md"`, `"lg"`, `"xl"`, or a specific number representing the width in pixels.

```jsx
<Modal
  opened={settingsOpened}
  onClose={closeSettings}
  size="lg" // or a number like 500 for pixels
  centered
  padding="xl"
  radius="16px"
>
  {/* Modal content */}
</Modal>
```

## Customizing with CSS Classes

If you need more control over the modal's size, you can use custom CSS classes. Define your styles in a CSS file and apply them using the `className` prop.

```css
/* styles.css */
.customModalSize {
  width: 600px;
  max-width: 90%;
}
```

```jsx
import './styles.css';

<Modal
  opened={settingsOpened}
  onClose={closeSettings}
  className="customModalSize"
  centered
  padding="xl"
  radius="16px"
>
  {/* Modal content */}
</Modal>
```

## Limitations of Custom CSS Variables

Currently, Mantine does not support directly setting a custom CSS variable like `--modal-size` through the style API. If you attempt to use a CSS variable in this way, it will not affect the modal size. Instead, use the `size` prop or custom CSS classes as described above.

## Conclusion

While Mantine does not support setting a custom CSS variable for modal size directly through the style API, you can effectively manage modal dimensions using the `size` prop or by applying custom CSS classes. These methods provide flexibility and control over the appearance of your modals.
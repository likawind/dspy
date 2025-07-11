# Setting `--modal-size` Using the Style API in Mantine Modal

The Mantine Modal component allows you to customize its appearance using the `styles` prop. One of the powerful features of this prop is the ability to set CSS custom properties, such as `--modal-size`, directly on the Modal's root element. This can be particularly useful when you want to define a consistent size for your modal that can be referenced by child components or other CSS rules.

## How to Set `--modal-size`

To set the `--modal-size` property, you need to pass it within the `styles` prop of the Modal component. Here's a step-by-step example:

```tsx
import { Modal } from '@mantine/core';

const MyModal = ({ opened, onClose }) => {
  return (
    <Modal
      opened={opened}
      onClose={onClose}
      withCloseButton={false}
      zIndex={9999}
      withinPortal={false}
      styles={{
        root: { 
          overflowY: "auto", 
          maxHeight: "90vh", 
          "--modal-size": "800px" // <-- Set the CSS variable here
        },
        body: { padding: 0 },
      }}
    >
      {/* Modal content */}
    </Modal>
  );
};
```

### Explanation
- **`styles` Prop**: This prop allows you to define custom styles for different parts of the Modal. In this example, we are targeting the `root` element of the Modal.
- **`--modal-size`**: By setting this CSS custom property, you can define a size that can be reused within the Modal or by any child components that reference `var(--modal-size)`.
- **Custom Value**: Replace `"800px"` with any size value you need for your application.

## Practical Reference
For a practical implementation, you can refer to the [SearchWidgetModal.tsx](https://github.com/runllm/RunLLM/blob/main/src/search-widget/src/layout/SearchWidgetModal.tsx) file in the RunLLM codebase. This file demonstrates how the `styles` prop is used to set `--modal-size` and other styles for the Modal component.

By following this approach, you can ensure that your modals have a consistent and customizable size across your application.
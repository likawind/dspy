# RunLLM Codebase File Structure Overview

The RunLLM codebase is organized into several top-level directories, each serving a specific purpose. Below is a comprehensive overview of these directories and their subdirectories, along with brief descriptions of their contents and functionality.

## Top-Level Directories

- **`data`**
  - Contains all API data used for training built-in models.

- **`migrations`**
  - Holds database schema versions and migration codes for managing database changes.

- **`src`**
  - This is the core implementation directory containing various submodules for different functionalities.

- **`testing`**
  - Contains testing code, although some may be outdated.

## `src` Subdirectories

- **`deployment`**
  - Contains Kubernetes deployment configurations.

- **`dockerfiles`**
  - Includes Docker files for all containerized components, with each component's file in its own subdirectory.

- **`finetune`**
  - Contains implementations for finetuning jobs that run inside containers.

- **`ingestion`**
  - Contains implementations for ingestion jobs that run inside containers.

- **`server`**
  - Main REST API server implementations. For more details, refer to the [server CONTRIBUTION guide](https://github.com/runllm/ApiOverflow/blob/main/src/server/CONTRIBUTE.md).

- **`shared`**
  - Contains shared Python code used by multiple modules. For more details, refer to the [shared CONTRIBUTION guide](https://github.com/runllm/ApiOverflow/blob/main/src/shared/CONTRIBUTE.md).

- **`ui`**
  - Main web application UI implementations. For more details, refer to the [UI CONTRIBUTION guide](https://github.com/runllm/ApiOverflow/blob/main/src/ui/CONTRIBUTE.md).

- **`vscode-extension`**
  - UI code for the VSCode extension, sharing some code with the `ui` directory. For more details, refer to the [VSCode extension structure guide](https://github.com/runllm/ApiOverflow/blob/main/src/vscode-extension/docs/extension-structure.md).

## Additional Resources

For more detailed information on contributing to specific modules, please refer to the following documentation files:

- [CONTRIBUTE.md](https://github.com/runllm/ApiOverflow/blob/main/CONTRIBUTE.md)
- [src/shared/CONTRIBUTE.md](https://github.com/runllm/ApiOverflow/blob/main/src/shared/CONTRIBUTE.md)
- [src/server/CONTRIBUTE.md](https://github.com/runllm/ApiOverflow/blob/main/src/server/CONTRIBUTE.md)
- [src/ui/CONTRIBUTE.md](https://github.com/runllm/ApiOverflow/blob/main/src/ui/CONTRIBUTE.md)
- [src/vscode-extension/docs/extension-structure.md](https://github.com/runllm/ApiOverflow/blob/main/src/vscode-extension/docs/extension-structure.md)

This overview should help you navigate and understand the structure of the RunLLM codebase more effectively.
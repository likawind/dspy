# RunLLM Project Folder Structure

Understanding the folder structure of the RunLLM project is crucial for navigating the codebase efficiently. Below is a detailed explanation of each main directory, including their purposes and typical contents.

- **`/data`**
  - **Purpose**: This directory contains all API data used for training built-in models.
  - **Contents**: You will typically find datasets and configuration files related to model training.

- **`/migrations`**
  - **Purpose**: This directory holds the database schema versions and migration codes, specifically for the Planetscale database.
  - **Contents**: Expect to find SQL files and scripts that manage database schema changes over time.

- **`/src`**
  - **Purpose**: This is the core of the project, containing all main implementations.
  - **Subdirectories**:
    - **`/deployment`**: Contains Kubernetes deployment configurations.
    - **`/dockerfiles`**: Houses Docker files for all containerized components, with each component's file in its own subdirectory.
    - **`/finetune`**: Contains code for finetuning jobs that run inside containers.
    - **`/ingestion`**: Includes code for data ingestion jobs.
    - **`/server`**: Main REST API server implementations. More details can be found in `src/server/CONTRIBUTE.md`.
    - **`/shared`**: Shared Python code used by multiple modules. Refer to `src/shared/CONTRIBUTE.md` for more information.
    - **`/ui`**: Main web application UI implementations. Additional details are available in `src/ui/CONTRIBUTE.md`.
    - **`/vscode-extension`**: UI code for the VSCode extension, sharing some code with `/ui` by copy-pasting.

- **`/testings`**
  - **Purpose**: Contains testing code for the project.
  - **Contents**: Includes various test scripts, though some may be outdated.

This structured approach helps in maintaining a clean and organized codebase, making it easier for developers to locate specific files or functionalities.
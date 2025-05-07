# RunLLM Codebase File Structure Overview

The RunLLM codebase is organized into several top-level directories, each serving a specific purpose. Below is a comprehensive overview of the file structure, detailing the purpose of each directory and subdirectory. For more detailed information, please refer to the linked documentation files.

## Top-Level Directories

- `/data`
  - Contains all API data used for training built-in models.

- `/migrations`
  - Holds database schema versions and migration codes for PlanetScale.

- `/src`
  - Core implementations of the RunLLM codebase.

- `/testings`
  - Contains testing code, though some may be outdated.

## `/src` Directory Structure

- `/src/deployment`
  - Kubernetes deployment configurations.

- `/src/dockerfiles`
  - Docker files for all containerized components, with each component's file in its own subdirectory.

- `/src/finetune`
  - Implementations for finetuning jobs that run inside containers.

- `/src/ingestion`
  - Implementations for ingestion jobs that run inside containers.

- `/src/server`
  - Main REST API server implementations.
  - **Subdirectories and Files:**
    - `/app/api`
      - Definitions of all REST endpoints.
      - Contains subdirectories for requests, responses, and middlewares.
    - `/core`
      - Main logic implementations.
    - `config.py`
      - Main configuration file parsing `configmap.yml`.
    - `server.py`
      - Top-level server code.
  - Refer to [src/server/CONTRIBUTE.md](https://github.com/runllm/ApiOverflow/blob/main/src/server/CONTRIBUTE.md) for more details.

- `/src/shared`
  - Shared Python code used by multiple modules.
  - **Subdirectories and Files:**
    - `data_loaders/`
      - Interfaces and implementations for data loaders.
    - `indexers/`
      - Interfaces and implementations for indexers.
    - `job/`
      - Interface definitions for jobs, job specs, and job runners.
    - `models/`
      - Database models implemented with SQLAlchemy ORM.
    - `state/`
      - Definitions for internal data structures passed across system components.
    - `vault/`
      - Vault component interfaces and implementations.
    - `constants.py`
      - All constants.
    - `enums.py`
      - All enum definitions.
  - Refer to [src/shared/CONTRIBUTE.md](https://github.com/runllm/ApiOverflow/blob/main/src/shared/CONTRIBUTE.md) for more details.

- `/src/ui`
  - Main web application UI implementations.
  - Refer to the `ui` section in [CONTRIBUTE.md](https://github.com/runllm/ApiOverflow/blob/main/CONTRIBUTE.md) for more details.

- `/src/vscode-extension`
  - UI code for the VSCode extension, sharing some code with `/src/ui` by copy-pasting.

For further insights and contributions, please refer to the [CONTRIBUTE.md](https://github.com/runllm/ApiOverflow/blob/main/CONTRIBUTE.md) file.
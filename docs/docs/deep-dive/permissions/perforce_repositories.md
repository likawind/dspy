# Setting Up Explicit Permissions for Perforce Repositories

This guide provides a comprehensive walkthrough for setting up explicit permissions for Perforce repositories using the centralized Role-Based Access Control (RBAC) microservice. This service allows you to manage permissions effectively, ensuring secure access control.

## Defining Resources

To manage permissions for a Perforce repository, you must first define it as a resource in the permission system. This involves specifying a table name and a unique resource ID.

- **Table Name**: Use a descriptive name like `"perforce_repo"` to identify the resource type.
- **Resource ID**: Assign a unique identifier to each Perforce repository.

## Granting Permissions

Permissions can be granted using the `GrantAccess` API. This API allows you to assign specific actions (e.g., READ, UPDATE, DELETE) to users or roles.

### Example: Granting Permissions via HTTP API

To grant a user full access to a Perforce repository with ID `1234`, use the following HTTP request:

```bash
curl -X POST https://api.runllm.com/api/permission/grant \
  -H "x-api-key: <your prod api key>" \
  -H "Content-Type: application/json" \
  -d '{
    "table_name": "perforce_repo",
    "id": 1234,
    "owner": "user:<user_id>",
    "actions": ["READ", "UPDATE", "DELETE"]
  }'
```

## Enforcing Permissions

Before allowing access or operations on a Perforce repository, use the `EnforceResource` API to validate user permissions.

### Example: Enforcing Permissions in Code

```python
can_access = auth_manager.enforce_resource(
    owner=str(user_id),
    table_name="perforce_repo",
    id=1234,
    action=CRUDAction.READ
)
if not can_access:
    raise HTTPException(status_code=403, detail="Permission denied.")
```

This code checks if the user has the necessary permissions to access the repository.

## Role-Based Access Control

For group-based access control, assign users to roles and grant permissions to these roles.

### Example: Assigning a User to a Role

To add a user to an organization admin role:

```bash
curl -X POST https://api.runllm.com/api/permission/add-to-role \
  -H "x-api-key: <your prod api key>" \
  -H "Content-Type: application/json" \
  -d '{"sub": "<user_id>", "role": "organization:<org_id>:admin"}'
```

Then, grant the role access to the Perforce repository using the `GrantAccess` API with `"owner": "organization:<org_id>:admin"`.

## API Examples

### Granting Permissions

- **Endpoint**: `/api/permission/grant`
- **Method**: POST
- **Headers**: `x-api-key`, `Content-Type: application/json`
- **Payload**:
  ```json
  {
    "table_name": "perforce_repo",
    "id": <repo_id>,
    "owner": "user:<user_id>",
    "actions": ["READ", "UPDATE", "DELETE"]
  }
  ```

### Enforcing Permissions

- **Endpoint**: `/api/permission/enforce`
- **Method**: POST
- **Headers**: `x-api-key`, `Content-Type: application/json`
- **Payload**:
  ```json
  {
    "owner": "user:<user_id>",
    "table_name": "perforce_repo",
    "id": <repo_id>,
    "action": "READ"
  }
  ```

By following this guide, you can effectively manage permissions for Perforce repositories, ensuring secure and controlled access within your organization.
# SQL Assistant Usage Restrictions and Optimization

## Usage Restrictions for Free-Tier Users

The SQL assistant has specific usage restrictions for users on the free tier. Understanding these restrictions can help you manage your usage effectively and avoid unexpected service interruptions.

### Conditions Triggering Restrictions

1. **Creation Date**: If your assistant (pipeline) was created after February 24, 2025, it is subject to free-tier limits.
2. **User Role**: Users with the `ROOT_ADMIN_ROLE` may be exempt from certain restrictions.
3. **Billing Tier**: Assistants on a paid tier are not subject to free-tier restrictions.
4. **Usage Count**: Free-tier users are limited to 50 billable chats. Exceeding this limit will trigger usage restrictions.

### Specific Limits for Free-Tier Users

- **Billable Chat Limit**: 50 billable chats.

### Steps to Regain Access

- **Upgrade to a Paid Plan**: Upgrading your assistant to a paid plan will remove the free-tier limitations and allow continued usage.

### Tips for Optimizing Usage

- **Monitor Usage**: Regularly check your usage to ensure you do not exceed the free-tier limits.
- **Understand Role-Based Exemptions**: If you are an admin, verify if you have higher or unrestricted limits.

### Example Restriction Messages

If you exceed the free-tier limit, you may encounter the following message:

> "Assistant usage is blocked as it has exceeded the free tier limit. Please upgrade to a paid plan to continue using the assistant."

### Technical Enforcement Mechanisms

The system checks various conditions to determine if assistant usage should be blocked. These include the creation date of the pipeline, user role, billing tier status, and the number of billable chats used. If any of these conditions indicate that the free-tier limits have been exceeded, usage will be blocked until the conditions are resolved, typically by upgrading to a paid plan.

By understanding these restrictions and optimizing your usage, you can ensure uninterrupted access to the SQL assistant.
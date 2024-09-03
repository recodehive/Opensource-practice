## Authentication

> Product owner
> Users wish to use their existing authentication

Login with GitHub OAuth with NextAuth library.

```mermaid
sequenceDiagram
    Guest->>User: Login?
    User-->>Guest: Yes!
    Guest-)User: Authenticated
```

### Prerequisites 

These are the subtasks required:
- [x] install library
- [ ] look into https://github.com/eddiejaoude/eddiejaoude/issues/99
- [ ] setup OAuth app
...

We must also include the login hook:

```js
// create the new user a Stripe account
const user = getUser();
const stripe = createNewStripeUser(user);
```

### After

Use feature flags to hide login button until fully tested

> [!CAUTION]
> Do not run in production until after migration


```mermaid


gitGraph:
    commit "Ashish"
    branch newbranch
    checkout newbranch
    commit id:"1111"
    commit tag:"test"
    checkout main
    commit type: HIGHLIGHT
    commit
    merge newbranch
    commit
    branch b2
    commit
```

```mermaid
flowchart TD
    Start["Start"] --> Enter_Credentials["Enter Username and Password"]
    Enter_Credentials --> Validate_Credentials["Validate Credentials"]
    Validate_Credentials -->|Valid| Success["Login Successful"]
    Validate_Credentials -->|Invalid| Failure["Login Failed"]
    Success --> End["End"]
    Failure --> Enter_Credentials

```

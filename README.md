C4Context
    title Automated User Access Review System - System Context Diagram

    Person(admin, "Security Administrator", "Manages user access reviews, generates reports, and configures the system.")
    Person(manager, "Line Manager", "Reviews and approves/revokes user access for their team members.")
    System(accessReviewSystem, "Automated User Access Review System", "Automates the process of user access review and certification.")
    System_Ext(identityProvider, "Identity Provider (IdP)", "Manages user identities and authentication (e.g., Azure AD, Okta).")
    System_Ext(resourceSystem, "Resource System", "Systems containing resources with user access (e.g., File Servers, Databases, Applications).")
    System_Ext(auditLog, "Audit Log System", "Stores audit logs of user access and review activities.")

    Rel(admin, accessReviewSystem, "Configures, Manages, and Generates Reports")
    Rel(manager, accessReviewSystem, "Reviews and Approves/Revokes Access")
    Rel(accessReviewSystem, identityProvider, "Retrieves User Information")
    Rel(accessReviewSystem, resourceSystem, "Retrieves Access Permissions")
    Rel(accessReviewSystem, auditLog, "Stores Audit Logs")

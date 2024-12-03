# Identity Management (EE vs CE)

It is essential to guarantee that only the right individuals have appropriate access to your workspace and every conversation there. With Rocket.Chat, you can connect to your Active Directory application or Identity Management System through [Lightweight Directory Access Protocol](../../use-rocket.chat/workspace-administration/settings/ldap/) (LDAP), [Open Authorization](../../use-rocket.chat/workspace-administration/settings/oauth/) (OAuth), and [Security Assertion Markup Language](../../use-rocket.chat/workspace-administration/settings/saml/) (SAML).

## **LDAP / AD** <a href="#ldap3" id="ldap3"></a>

Leverage advanced settings such as background sync, roles mapping from groups, auto-logout, and advanced user data sync with [LDAP ](../../use-rocket.chat/workspace-administration/settings/ldap/)in your workspace. Here are some differences between the community and enterprise editions when using LDAP.

| Community                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Enterprise                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><strong>Login</strong></p><p><strong>Login Fallback:</strong> This option allows regular password users to log in on Rocket.Chat. It will let LDAP users continue using Rocket.Chat if the LDAP server is down.</p><p><strong>Merge with existing Rocket.Chat users:</strong> Detect if the LDAP user is already registered on Rocket.Chat and use the same user for both authentication types.</p><p><strong>Filter what LDAP users can log in:</strong> There are two settings to manage this: Search Filter and Group Filter.</p> | <p><strong>Advanced User Data Sync</strong></p><p>Load information from the LDAP user to Rocket.Chat</p><p><strong>Load Custom User Data from LDAP:</strong> Load any LDAP attribute to a custom field on Rocket.Chat</p><p><strong>Advanced-Data Sync:</strong> Perform additional operations based on data from LDAP</p><p><strong>Roles Mapping from Groups:</strong> You can map any LDAP group to a Rocket.Chat role</p><p><strong>Auto-Subscribe to Channels:</strong> You can map any LDAP group to a Rocket.Chat channel</p><p><strong>Auto-Unsubscribe from Channels:</strong> You can also remove users from Rocket.Chat channels on LDAP</p><p><strong>Auto-Join Teams:</strong> You can map any LDAP group to a Rocket.Chat team</p><p><strong>Auto-Leave Teams:</strong> You can also remove users from Rocket.Chat teams on LDAP</p> |
| <p><strong>Basic User Data Sync</strong></p><p>Load information from the LDAP user to Rocket.Chat</p><p><strong>Load Basic User Data from LDAP:</strong> Email, name, and username.</p><p><strong>Load Avatars:</strong> Load the user's avatar from an LDAP attribute</p>                                                                                                                                                                                                                                                              | <p><strong>Background Sync</strong></p><p>Periodic background sync</p><p><strong>Incremental Sync:</strong> Give the option to use Incremental Sync (will be implemented in a future release)</p><p><strong>Sync User Active State:</strong> Determine if users should be enabled or disabled on Rocket.Chat based on the LDAP status</p><p><strong>Auto logout:</strong> Auto logout user on the next sync when it's removed/disabled on the LDAP group</p>                                                                                                                                                                                                                                                                                                                                                                                       |
| <p><strong>Encryptions</strong></p><p>The encryption method used to secure communications to the LDAP server</p>                                                                                                                                                                                                                                                                                                                                                                                                                        | \*\*\*\*                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |

## **SAML** <a href="#saml3" id="saml3"></a>

Create role mapping from user groups by selecting any field you want to sync with Rocket.Chat.

| Community                                                                                                                                                                                                                 | Enterprise                                                                                                                                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><strong>Basic Synchronization:</strong> Keep user data in sync with the server on login (email, name, and username)</p><p><strong>Customizable User Interface:</strong> Ability to customize button color and text</p> | <p><strong>Roles mapping:</strong> Role mapping from user groups</p><p><strong>Fields mapping:</strong> Select any field you want to sync with RC</p><p><strong>Advanced:</strong> Advanced settings (eg. login with username and password x win user)</p> |

{% content-ref url="../../use-rocket.chat/workspace-administration/settings/saml/" %}
[saml](../../use-rocket.chat/workspace-administration/settings/saml/)
{% endcontent-ref %}

## **OAuth / Custom OAuth** <a href="#oauth3" id="oauth3"></a>

Let your users log in via Facebook, Google, LinkedIn, GitHub, and others.

| Community                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Enterprise                                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><strong>Basic Social logins / pre-defined OAuth options</strong></p><p>Keep user data in sync with the server on login (Unique identifier and username)</p><p><strong>Avatar import</strong></p><p><strong>Login methods:</strong> Apple, Dolphin, Drupal, Facebook, GitHub, GitHub Enterprise, GitLab, Google, Linkedin, Meteor, Nextcloud, Tokenpass, Twitter, WordPress</p><p><strong>Basic Custom OAuth:</strong></p><p>Basic login settings</p><p>Login via Custom OAuth protocol using a unique identifier</p><p>Load Name, Username, and Email from</p><p>OAuth</p><p>Import Avatar from OAuth</p> | <p><strong>Advanced Custom OAuth:</strong></p><p>Assign Rocket.Chat roles based on OAuth roles</p><p>Join channels automatically based on OAuth roles</p> |

{% content-ref url="../../resources/frequently-asked-questions/ldap-faq.md" %}
[ldap-faq.md](../../resources/frequently-asked-questions/ldap-faq.md)
{% endcontent-ref %}
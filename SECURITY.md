# Security & Backup Guidelines

## What SHOULD Be Backed Up to GitHub

✅ **Safe to include:**
- WordPress Content Export (XML files)
- - Plugin & Theme information/lists
  - - Custom code (non-sensitive)
    - - Configuration documentation
      - - Backup procedures and instructions
        - - Database schema (structure only, no data)
         
          - ## What SHOULD NOT Be Backed Up to GitHub
         
          - ❌ **NEVER include:**
          - - `wp-config.php` (contains database credentials)
            - - `.env` files (environment variables)
              - - API keys or secrets
                - - Database backups with user data
                  - - Passwords or authentication tokens
                    - - Private keys or certificates
                      - - Customer/user personal information
                        - - Sensitive configuration files
                         
                          - ## Security Best Practices
                         
                          - ### 1. WordPress Configuration
                          - ```
                            // DO NOT COMMIT:
                            - wp-config.php with DB credentials
                            - Salts and authentication keys
                            - Admin usernames and passwords

                            // DO commit documentation:
                            - Required configuration steps
                            - Sample wp-config (with values replaced)
                            - Instructions for setup
                            ```

                            ### 2. Database Backups
                            ```
                            // DO NOT include in public repo:
                            - Database export files (.sql, .sql.gz)
                            - Sensitive user data
                            - Customer information
                            - Email addresses

                            // Alternative:
                            - Use DreamHost server backups (encrypted, private)
                            - Use cloud storage for full backups
                            - Only commit XML export (no user data)
                            ```

                            ### 3. API & Third-Party Keys
                            ```
                            // DO NOT commit:
                            - WPForms API keys
                            - Jetpack tokens
                            - Payment gateway credentials
                            - Cloud service API keys
                            - CDN access tokens

                            // Store these:
                            - In .env files (not in repo)
                            - In wp-config.php (not in repo)
                            - In DreamHost control panel
                            - In secure password manager
                            ```

                            ### 4. User Data Protection
                            ```
                            // DO NOT commit:
                            - User tables from database
                            - Email lists
                            - Customer information
                            - Form submissions
                            - Comments with user emails

                            // Instead:
                            - Keep in database only
                            - Use DreamHost encrypted backups
                            - GDPR compliant storage
                            ```

                            ## Backup Repository Security Checklist

                            - ✅ Repository is PUBLIC (contains no sensitive data)
                            - - ✅ Only documentation and XML exports
                              - - ✅ All credentials stored elsewhere
                                - - ✅ No database backups with data
                                  - - ✅ No API keys or tokens
                                    - - ✅ Gitignore properly configured
                                     
                                      - ## Recommended Secure Backup Strategy
                                     
                                      - ### For GitHub (Public)
                                      - - WordPress XML exports only
                                        - - Configuration documentation
                                          - - Restore instructions
                                            - - Backup inventory
                                             
                                              - ### For DreamHost (Private)
                                              - - Full automated daily backups
                                                - - Encrypted storage
                                                  - - One-click restoration
                                                    - - 14-day backup history
                                                     
                                                      - ### For Personal Storage (Private)
                                                      - - Local backup copies (encrypted)
                                                        - - External hard drive backup
                                                          - - Cloud encrypted storage (Backblaze, etc.)
                                                            - - Never share publicly
                                                             
                                                              - ## If You Accidentally Commit Sensitive Data
                                                             
                                                              - ⚠️ **IMMEDIATE ACTIONS:**
                                                             
                                                              - 1. **Revoke all compromised credentials:**
                                                                2.    - Change database password
                                                                      -    - Regenerate API keys
                                                                           -    - Update authentication tokens
                                                                            
                                                                                - 2. **Remove from GitHub history:**
                                                                                  3.    ```bash
                                                                                           # BFG Repo-Cleaner (recommended)
                                                                                           bfg --delete-files wp-config.php

                                                                                           # Or git-filter-branch
                                                                                           git filter-branch --tree-filter 'rm -f wp-config.php'
                                                                                           ```

                                                                                        3. **Force push to remove history:**
                                                                                        4.    ```bash
                                                                                                 git push --force-with-lease
                                                                                                 ```

                                                                                              4. **Alert users** (if personal data exposed)
                                                                                          
                                                                                              5. ## Compliance & Privacy
                                                                                          
                                                                                              6. - ✅ GDPR compliant (no PII in public repo)
                                                                                                 - - ✅ CCPA compliant (no personal data exposed)
                                                                                                   - - ✅ No customer information publicly available
                                                                                                     - - ✅ Security through separation (sensitive data elsewhere)
                                                                                                      
                                                                                                       - ## Links & Resources
                                                                                                      
                                                                                                       - - [GitHub Secret Scanning](https://github.com/features/security)
                                                                                                         - - [OWASP Secrets Management](https://cheatsheetseries.owasp.org/cheatsheets/Secrets_Management_Cheat_Sheet.html)
                                                                                                           - - [WordPress Security](https://wordpress.org/support/article/hardening-wordpress/)
                                                                                                             - - [DreamHost Security](https://www.dreamhost.com/security/)
                                                                                                               - 

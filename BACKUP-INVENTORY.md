# WordPress Portfolio Backup Inventory

## Last Updated: June 3, 2026

## Current Backups

### 1. WordPress Content Export (XML)
- **Filename**: ashleypimenta-2026-06-03.xml
- - **Type**: WordPress eXtended RSS (WXR) Export
  - - **Size**: ~5-10 MB (compressed)
    - - **Contents**: All posts, pages, portfolio items, comments, categories, tags, custom fields
      - - **Location**: Downloaded to local computer (2026-06-03)
        - - **Status**: ✅ Complete
          - - **Import Method**: WordPress Tools > Import > WordPress Importer
            - - **Notes**: This is the primary backup for content recovery
             
              - ### 2. Duplicator Full Site Backup
              - - **Status**: ⚠️ Incomplete (Server Build Interrupt at 59.8%)
                - - **Reason**: Server hosting constraints on 6.42GB site
                  - - **Attempted Date**: June 3, 2026
                    - - **Size**: 6.42 GB (files) + 23 MB (database)
                      - - **Location**: DreamHost Server
                        - - **Resolution**: Use DreamHost native backups instead
                         
                          - ### 3. DreamHost Server Backups
                          - - **Status**: ✅ Available
                            - - **Location**: DreamHost Control Panel
                              - - **Access**: panel.dreamhost.com > Backups
                                - - **Frequency**: Automatic daily backups (last 14 days available)
                                  - - **Includes**: Full file system + database
                                    - - **Recovery**: Contact DreamHost support for one-click restoration
                                     
                                      - ### 4. UpdraftPlus Backup
                                      - - **Status**: Available for setup
                                        - - **Type**: Incremental backup plugin
                                          - - **Features**: Scheduled automatic backups, cloud storage integration
                                            - - **Cloud Options**: Google Drive, Dropbox, Amazon S3, OneDrive
                                             
                                              - ## Backup Strategy Recommendations
                                             
                                              - ### For Content-Only Recovery (Recommended for GitHub)
                                              - ✅ Use WordPress XML Export files
                                              - - Small size (perfect for GitHub)
                                                - - Contains all posts, pages, portfolio items
                                                  - - Easy to import to any WordPress installation
                                                    - - Recommended frequency: Monthly
                                                     
                                                      - ### For Full Site Recovery
                                                      - ✅ Use DreamHost Server Backups
                                                      - - Includes all files, themes, plugins, database
                                                        - - Automatic daily backups
                                                          - - One-click restore via DreamHost
                                                            - - No manual management needed
                                                             
                                                              - ### For Scheduled Automated Backups
                                                              - ✅ Configure UpdraftPlus
                                                              - - Set to weekly or daily schedule
                                                                - - Store to Google Drive or cloud service
                                                                  - - Includes incremental backups
                                                                    - - Email notifications for backup completion
                                                                     
                                                                      - ## File Size Considerations for GitHub
                                                                     
                                                                      - ```
                                                                        GitHub File Limits:
                                                                        - Max single file: 100 MB
                                                                        - Recommended repo size: < 1 GB
                                                                        - Your XML export: ~5-10 MB ✅ Compatible
                                                                        - Full site backup: ~6.4 GB ❌ Not recommended for GitHub
                                                                        ```

                                                                        ## Backup Schedule

                                                                        | Backup Type | Frequency | Method | Status |
                                                                        |-------------|-----------|--------|--------|
                                                                        | XML Export | Monthly | Manual Export | Scheduled |
                                                                        | Database | Daily | DreamHost Auto | Active |
                                                                        | Full Site | Daily | DreamHost Auto | Active |
                                                                        | Incremental | Weekly | UpdraftPlus | To Setup |

                                                                        ## Recovery Procedures

                                                                        ### Quick Content Restore (15 min)
                                                                        1. Download XML from GitHub
                                                                        2. 2. WordPress Admin > Tools > Import
                                                                           3. 3. Run WordPress Importer
                                                                              4. 4. Upload XML file
                                                                                 5. 5. Done!
                                                                                   
                                                                                    6. ### Full Site Restore (24-48 hrs)
                                                                                    7. 1. Contact DreamHost support
                                                                                       2. 2. Request restoration from available backup date
                                                                                          3. 3. DreamHost restores via SFTP or file manager
                                                                                             4. 4. Site returns to selected point-in-time
                                                                                               
                                                                                                5. ## Encryption & Security
                                                                                               
                                                                                                6. - ✅ XML exports do NOT contain passwords or API keys
                                                                                                   - - ✅ GitHub repository is public (no sensitive data)
                                                                                                     - - ✅ DreamHost backups are server-side encrypted
                                                                                                       - - ⚠️ Never commit credentials, API keys, or wp-config.php to GitHub
                                                                                                        
                                                                                                         - ## Storage Locations Summary
                                                                                                        
                                                                                                         - | Location | Backup Type | Access | Reliability |
                                                                                                         - |----------|------------|--------|-------------|
                                                                                                         - | GitHub | XML Export | Public | Permanent |
                                                                                                         - | DreamHost | Full Site | Control Panel | 99.9% |
                                                                                                         - | Local Machine | XML Export | Downloads folder | User dependent |
                                                                                                         - | Cloud (Optional) | UpdraftPlus | Drive/Dropbox | 99.99% |
                                                                                                         - 

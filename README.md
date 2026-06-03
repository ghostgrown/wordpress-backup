# WordPress Portfolio Backup

Backup repository for Ash M. Bettencourt-Pimenta's WordPress portfolio site (ashleypimenta.com)

## Contents

- **WordPress Content Export (XML)**: Full export of all posts, pages, portfolio items, and content structure
- **Database backup scripts**: Tools for backing up and restoring the WordPress database
- **Site configuration**: Important WordPress configuration and settings documentation

## Site Details

- **Site URL**: https://www.ashleypimenta.com
- **WordPress Version**: 7.0
- **Backup Date**: June 3, 2026
- **Total Size**: ~6.42 GB (files) + 23 MB (database)

## Using This Backup

### Importing the XML Export
1. Go to WordPress Admin > Tools > Import
2. Choose "WordPress" importer
3. Upload the `.xml` backup file
4. Map authors and import content

### Full Site Restore
For a full site restore including files and database, use the Duplicator backup files or contact hosting provider (DreamHost).

## Backup Tools Used

- **WordPress Export**: Native WordPress export tool
- **Duplicator Plugin**: Full site backup and migration plugin
- **UpdraftPlus**: Additional WordPress backup plugin

## Notes

- This repository contains backup exports only
- For large file backups (>100MB), files are excluded from GitHub
- Full site backups are stored on DreamHost servers
- Regular backups are recommended for production sites

## Restoring from Backup

### Via WordPress
1. Download the XML file from this repository
2. Go to Tools > Import in WordPress admin
3. Install and run WordPress importer
4. Select the downloaded XML file
5. Map users and import

### Full Restore
For a complete restore including themes, plugins, and database settings:
1. Contact DreamHost support for full server backup restoration
2. Or use Duplicator plugin with the full backup archive

## Important

This backup contains no sensitive data (credentials, API keys are not included). Always keep backups in secure locations.

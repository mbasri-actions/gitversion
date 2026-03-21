# Change Log

All notable changes to this project will be documented in this file.

## [v1.1.0](https://github.com/mbasri-actions/gitversion/compare/v1.0.0...v1.1.0) (2026-03-21)

- Added automated versioning workflow to streamline release processes
- Added major and minor version tagging for easier version management
- Added isTerraformModule input for Terraform versioning support
- Added githubToken input for AI inference in changelog generation
- Migrated from Claude to GitHub Models for enhanced AI capabilities
- Fixed handling of missing previous tags during initial releases
- Fixed shell parameter expansion issues for input paths
- Fixed environment variable interpolation syntax issues in changelog process
- Refactored changelog generation logic to improve maintainability
- Refactored AI changelog prompt to external template file for clarity
- Consolidated versioning and changelog updates into a single commit process
- Removed redundant token input and simplified logic for environment variables
- Automated commit and push of generated changelog updates for efficiency
- Simplified git log and comparison link generation process in changelog
- Updated versioning logic and improved AI model integration for better results

## [v1.0.0](https://github.com/mbasri-actions/gitversion/tree/v1.0.0) (2026-01-07)

- Initial commit

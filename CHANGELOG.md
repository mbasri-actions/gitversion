# Change Log

All notable changes to this project will be documented in this file.

## [v1.1.9](https://github.com/mbasri-actions/semver/compare/v1.1.8...v1.1.9) (2026-03-24)

- Refactored gitversion to semver for clarity in version management

## [v1.1.8](https://github.com/mbasri-actions/gitversion/compare/v1.1.7...v1.1.8) (2026-03-22)

- Renamed gitversion workflow and pinned action version for consistency in CI configuration

## [v1.1.7](https://github.com/mbasri-actions/gitversion/compare/v1.1.6...v1.1.7) (2026-03-21)

- Added trailing comma to Terraform version update for improved clarity in CI configuration

## [v1.1.6](https://github.com/mbasri-actions/gitversion/compare/v1.1.5...v1.1.6) (2026-03-21)

- Simplified Terraform update status presentation in CI job summary

## [v1.1.5](https://github.com/mbasri-actions/gitversion/compare/v1.1.4...v1.1.5) (2026-03-21)

- Expanded release job summary in CI workflows to include detailed metrics and commit logs

## [v1.1.4](https://github.com/mbasri-actions/gitversion/compare/v1.1.3...v1.1.4) (2026-03-21)

- Added job summaries to display release details in CI workflows

## [v1.1.3](https://github.com/mbasri-actions/gitversion/compare/v1.1.2...v1.1.3) (2026-03-21)

- Improved CI workflow by using version sorting to identify previous tags

## [v1.1.2](https://github.com/mbasri-actions/gitversion/compare/v1...v1.1.2) (2026-03-21)

- Updated AI inference action for improved performance in CI workflow
- Removed Node.js 24 override to ensure compatibility with future versions

## [v1.1.1](https://github.com/mbasri-actions/gitversion/compare/v1...v1.1.1) (2026-03-21)

- Changed JavaScript actions to consistently use Node.js version 24 in CI workflow

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

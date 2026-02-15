# Changelog

All notable changes to the Camunda n8n Bridge will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/),
and this project adheres to [Semantic Versioning](https://semver.org/).

## [0.2.0] - 2026-02-15

### Added
- Execution odometer for usage-based self-reporting: silent AtomicLong counter
  persisted to ACT_GE_PROPERTY every 1,000 executions via upsert, with restore
  on startup and formatted mileage banner logging. All errors swallowed to
  protect process execution.

## [0.1.0] - 2026-02-08

### Added
- Initial release of the Camunda n8n Bridge Java delegate
- Routes Camunda 7 service tasks to n8n webhooks via HTTP
- Apache HttpClient 5 with Jackson, shaded to avoid classpath conflicts
- Spring 5.3.31 compatibility (Java 11 target)
- GitHub Actions release workflow triggered on `v*` tags

### Fixed
- Spring 6.x incompatibility with JDK 11 (downgraded to Spring 5.3.31)

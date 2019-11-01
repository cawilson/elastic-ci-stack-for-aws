# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [v4.3.5](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.3.5) (2019-11-01)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v4.3.4...v4.3.5)

### Changed
- Prune docker builder cache periodically [#642](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/642) (@sj26)

## [v4.3.4](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.3.4) (2019-07-28)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v4.3.3...v4.3.4)

### Changed
- Bump agent to v3.13.2, docker to 19.03 and compose to 1.24.1 [#609](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/609) (@lox)
- Docker experimental needs boolean not string [#610](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/610) (@lox)

## [v4.3.3](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.3.3) (2019-06-01)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v4.3.2...v4.3.3)

### Changed
- Bump agent to 3.12.0 [#594](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/594) (@lox)

## [v4.3.2](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.3.2) (2019-04-16)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v4.3.1...v4.3.2)

### Changed
- Bump agent scaler to support newer regions [#566](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/566) (@lox)

## [v4.3.1](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.3.1) (2019-04-09)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v4.3.0...v4.3.1)

### Fixed
- Add back us-east-1 to regions [#563](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/563) (@ksindi)

## [v4.3.0](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.3.0) (2019-04-06)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v4.2.0...v4.3.0)

### Added
- Add EnableAgentGitMirrorsExperiment parameter [#555](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/555) (@lox)

### Fixed
- Remove temporary packer key [#551](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/551) (@lox)

### Changed
- Updated experimental lambda-based auto-scaler, respect ScaleDownPeriod [#559](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/559) (@lox)
- Bump agent to 3.10.3 [#558](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/558) (@lox)
- Install pigz for parallel decompression in docker pull [#560](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/560) (@lox)
- Use spawn vs multiple systemd units [#552](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/552) (@lox)
- Write cloudwatch metrics from lambda scaler [#541](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/541) (@lox)
- Bump docker-login, ecr and secrets plugins to latest [#550](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/550) (@lox)
- Bump lifecycled to v3.0.2 [#548](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/548) (@lox)
- Restart agent on SIGPIPE (journald restart) [#545](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/545) (@lox)
- Set the priority of the agent to its instance integer [#539](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/539) (@tduffield)

## [v4.2.0](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.2.0) (2019-02-25)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v4.1.0...v4.2.0)

### Added
- Add an experimental lambda scaler [#529](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/529) (@lox)
- Add helpers to Makefile for building packer image [#535](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/535) (@tduffield)
- Allow users to configure the root block device [#534](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/534) (@tduffield)

### Fixed
- Fix typo in CF setting [#537](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/537) (@tduffield)
- Make sure we reload the systemd unit files [#533](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/533) (@tduffield)

## [v4.1.0](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.1.0) (2019-02-11)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v4.0.4...v4.1.0)

### Changed
- Bump docker to 18.09.2 to fix CVE-2019-5736 [#532](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/532) (@lox)
- Fix typo in docker experimental config [#528](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/528) (@lox)
- Allow users to specify additional sudo permissions [#527](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/527) (@tduffield)
- Add new "TerminateInstanceAfterJob" configuration [#523](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/523) (@tduffield)
- Add Buildkite Org to Cloudwatch Metrics as a Dimension to support multiple orgs per AWS account [#510](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/510) (@lox)

## [v4.0.4](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.0.4) (2019-01-29)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v4.0.3...v4.0.4)

### Fixed
- Fix bug where lifecycled logs aren't flushed to cloudwatch logs [#524](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/524) (@lox)
- Prevent systemd from killing agent process group [#521](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/521) (@lox)

### Changed
- Expose AgentLifecycleTopic for programatic scaling [#522](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/522) (@tduffield)

## [v4.0.3](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.0.3) (2019-01-18)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v4.0.2...v4.0.3)

### Changed
- Bump docker to 18.09.1 [#516](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/516) (@lox)
- Bump agent to 3.8.2 [#514](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/514) (@lox)
- Tunable knob for ASG Cooldown period [#495](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/495) (@prateek)

## [v4.0.2](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.0.2) (2018-12-20)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v4.0.1...v4.0.2)

### Fixed
- Set a region for awslogsd [#508](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/508) (@dgarbus)
- Fix bug where lifecycled didn't pick up handler script [#507](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/507) (@lox)

### Changed
- Add a EnableDockerExperimental param [#506](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/506) (@lox)
- Bump docker to 18.09.0 [#505](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/505) (@lox)

## [v4.0.1](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.0.1) (2018-11-30)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v4.0.0...v4.0.1)

### Fixed
- Show correct stack version in log output [#503](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/503) (@lox)
- Remove duplicate AssociatePublicIpAddress

## [v4.0.0](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.0.0) (2018-11-28)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v4.0.0-rc3...v4.0.0)

No changes from v4.0.0-rc3.

## [v4.0.0-rc3](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.0.0-rc3) (2018-11-05)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v4.0.0-rc2...v4.0.0-rc3)

### Changed
- Use rsyslogd+awslogs for logs [#498](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/498) (@lox)
- Remove the dash in description to be consistent with v3 [#499](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/499) (@lox)
- Goss specs [#497](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/497) (@lox)
- Bump lifecycled to v3.0.0 [#496](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/496) (@lox)
- Support timestamp-lines [#494](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/494) (@raylu)
- Add docs for using the bootstrap script [#493](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/493) (@toolmantim)
- Start logging daemons as soon as possile during bootstrap [#492](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/492) (@zsims)
- Merge template files into a single file [#487](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/487) (@lox)
- Move AMI copy into a dedicated step [#486](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/486) (@lox)
- Update AMI to latest packages [#480](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/480) (@lox)

## [v4.0.0-rc2](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.0.0-rc2) (2018-09-04)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v4.0.0-rc1...v4.0.0-rc2)

### Added
- Install Git LFS [#468](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/468) (@lox)

### Changed
- Update to the very latest aws-cli [#478](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/478) (@lox)
- Bump lifecycled to 2.0.2 [#475](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/475) (@lox)
- Default BuildkiteAgentRelease to stable [#474](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/474) (@lox)
- Added InstanceCreationTimeout as parameter [#476](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/476) (@RexChenjq)
- Update README.md to reflect Amazon Linux 2[#470](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/470) (@alexjurkiewicz)
- Clean up docker login hooks [#466](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/466) (@lox)
- Rename the log group name we are using for elastic-stack.log file so we are consistent [#463](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/463) (@arturopie)
- Update to latest Amazon Linux 2 LTS [#462](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/462) (@lox)

## [v4.0.0-rc1](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v4.0.0-rc1) (2018-07-18)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v3.2.1...v4.0.0-rc1)

### Changed
- Use Amazon Linux 2 as base AMI [#363](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/363) (@lox)
- Bump docker-login and ecr plugin to latest [#454](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/454) (@lox)
- Bump docker to 18.03.1-ce and docker-compose to 1.22.0 [#455](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/455) (@lox)
- Support attaching multiple policies via the parameter [#446](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/446) (@zsims)
- Make KeyName optional [#444](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/444) (@zsims)
- Provide InstanceRoleName as Output [#438](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/438) (@lox)

## [v3.3.1](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v3.3.1) (2018-09-13)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v3.3.0...v3.3.1)

### Fixed
- Bump lifecycled to v2.1.1 [#488](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/488) (@lox)

## [v3.3.0](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v3.3.0) (2018-09-04)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v3.2.1...v3.3.0)

### Changed
- Bump Amazon Linux to 2018.03 [#471](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/471) (@lox)
- Bump docker to 18.03.1-ce and docker-compose to 1.22.0 [#455](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/455) (@lox)
- Support attaching multiple policies via the parameter [#446](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/446) (@zsims)

### Fixed
- Set correct variable to pass to upstream ecr plugin [#453](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/453) (@bshelton229)
- Use exit instead of return in bk-check-disk-space.sh script [#440](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/440) (@arturopie)
- Move cleanup cron jobs to run hourly [#429](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/429) (@arturopie)

## [v3.2.1](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v3.2.1) (2018-05-24)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v3.2.0...v3.2.1)

### Changed
- Support enabling agent experiments [#423](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/423) (@lox)
- Use the docker directory to check for disk space [#418](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/418) (@arturopie)
- Set InstanceRoleName as stack template output [#421](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/421) (@dblandin)

## [v3.2.0](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v3.2.0) (2018-05-17)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v3.1.1...v3.2.0)

### Changed
- Updated stable agent to buildkite-agent v3.1.2
- Default EnableDockerUserNamespaceRemap to true [#417](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/417) (@lox)
- Bump the minimum inodes to 250K to allow for big docker images [#416](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/416) (@lox)
- Update to the new secrets hooks repo URL [#414](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/414) (@toolmantim)

## [v3.1.1](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v3.1.1) (2018-05-02)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v3.1.0...v3.1.1)

### Changed
- Updated stable agent to buildkite-agent v3.1.1
- Bump docker to 18.03.0-ce and docker-compose to 1.21.1 [#411](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/411) (@lox)

## [v3.1.0](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v3.1.0) (2018-04-30)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v3.0.0...v3.1.0)

### Changed
- Allow userns remapping to be disabled [#410](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/410) (@lox)
- Update lifecycled to 2.0.1 [#407](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/407) (@lox)
- Fix cfn stack instance profile name [#395](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/395) (@chandanadesilva)

## [v3.0.0](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v3.0.0) (2018-04-18)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v3.0.0-rc1...v3.0.0)

## [v3.0.0-rc1](https://github.com/buildkite/elastic-ci-stack-for-aws/tree/v3.0.0-rc1) (2018-04-18)
[Full Changelog](https://github.com/buildkite/elastic-ci-stack-for-aws/compare/v2.3.5...v3.0.0-rc1)

### Changed
- Use new Metrics API, drop requirement for org-slug and api-token [#405](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/405) (@lox)
- Bump Lifecycled to v2.0.0 [#404](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/404) (@lox)
- Add support for billing tags [#398](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/398) (@tduffield)
- Drop support for buildkite-agent v2, stable is 3.0.0 [#400](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/400) (@lox)
- Don't blow up when no plugins are enabled [#394](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/394) (@haines)
- Fail install if docker hasn't started [#387](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/387) (@lox)
- Update docker to stable 17.12.1-ce [#391](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/391) (@lox)

## v2.3.5 - 2018-02-26
### Changed
- Make EnableDockerUserNamespaceRemap the new default [\#378](https://github.com/buildkite/elastic-ci-stack-for-aws/issues/378)
- Docker 17.12.1-ce-rc2 (Related to [\#377](https://github.com/buildkite/elastic-ci-stack-for-aws/issues/377))

## v2.3.4 - 2018-02-13
### Fixed
- Configure docker before it starts to avoid corruption [\#377](https://github.com/buildkite/elastic-ci-stack-for-aws/issues/377)

### Added
- Show elastic stack logs in Instance Terminal for easier debugging
- Collect cron output in elastic-stack.log
- Check (and free) diskspace before builds

## v2.3.3 - 2018-01-11
### Fixed
- Amazon Linux 2017.09.1 (to mitigate Meltdown/Spectre)
- Docker 17.12.0-ce and Compose 1.18.0

## v2.3.2 - 2018-01-07
### Fixed
- Bump metrics lambda version to v2.0.2
- Bump ECR plugin to 1.1.3

## v2.3.1 - 2017-12-23
### Fixed
- Updated to latest buildkite-metrics lambda version (v2.0.0) that respects rate limiting headers [\#357](https://github.com/buildkite/elastic-ci-stack-for-aws/issues/357)
- Added a new parameter for adding extra buildkite-agent tags/metadata [\#359](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/340)

## v2.3.0 - 2017-10-20
### Fixed
- Autoscaling is suspended when lifecycled crashes [\#344](https://github.com/buildkite/elastic-ci-stack-for-aws/issues/344)
- Optimize the permissions check script to only fix the current pipeline’s build dir [\#340](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/340) (@toolmantim)

### Changed
- CloudWatch Logs namespaced [\#342](https://github.com/buildkite/elastic-ci-stack-for-aws/issues/342)
- Docker 17.09.0-ce [\#350](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/350) (@lox)
- Buildkite Agent v2.6.6 and v3.0.0-beta34

### Added
- Optionally run docker as buildkite agent with userns-remap  [\#341](https://github.com/buildkite/elastic-ci-stack-for-aws/pull/341) (@lox)

## 2.2.0-rc3 - 2017-08-12
### Changed
- Bump buildkite-metrics to v1.5.0 (retry on error)
- Replace shudder with new lifecycled that supports spot notifications

## 2.2.0-rc2 - 2017-06-26
### Changed
- Re-added deprecated DOCKER_HUB_USER variables

## 2.2.0-rc1 - 2017-07-18
### Changed
- Move ecr, secrets and docker-login to plugins
- Add a signature llama to the environment hook
- Show stack version in the environment hook
- Move pipeline to yaml, json version is deprecated
- Use Shudder tool to handle autoscaling events and spot notifications
- Docker 17.06.0-ce

### Removed
- Remove deprecated DOCKER_HUB_USER variables

## 2.1.4 - 2017-06-28
### Changed
- Buildkite Agents v3.0.0-beta28
- Edge agent version is downloaded when instances boot rather than baked in AMI
- Added SECRETS_PLUGIN_ENABLED to allow secrets downloading to be disabled

## 2.1.3 - 2017-06-20
### Changed
- Updated to latest Amazon Linux 2017.03.1 (see security advisory AWS-2017-007)
- Updated docker-compose to 1.14.0

## 2.1.2 - 2017-06-16
### Fixed
- Using an env secrets bucket hook caused builds to fail with an undefined variable error

## 2.1.1 - 2017-06-12
### Changed
- 🐳 Docker-Compose 1.14.0-r2 (with support for cache_from directive)
- Buildkite Agents v2.6.3 and v3.0.0-beta27
- Agent version defaults to beta rather than stable

### Fixed
- Using git-credentials was broken (#290)
- Managed secrets bucket failed to create (#282)

## 2.1.0 - 2017-05-12
### Added
- A secrets bucket is created automatically if left blank
- Git over HTTPS is supported via a git-credentials file
- A customisable ScaleDownPeriod parameter is available to prevent rapid scale downs

### Changed
🐳 Docker 17.05.0-ce and Docker-Compose 1.13.0
- Buildkite Agents v2.6.3 and v3.0.0-beta23
- Latest aws-cli
- Autoscaling group is replaced on update, for smoother updates in large groups

### Fixed
- Fixed a bug where the stack would scale up faster than instances were launching

## 2.0.2 - 2017-04-11
### Fixed
- 🕷 Avoid restarting docker whilst it's initializing to try and avoid corrupting it (#236)

## 2.0.1 - 2017-04-04
### Added
- 🆙 Includes new Buildkite Agent v2.5.1 (stable) and v3.0-beta.19 (beta)

### Fixed
- ⏰ Increase the polling duration for scale down events to prevent hitting api limits (#263)

## 2.0.0 - 2017-03-28
### Added
- Docker 17.03.0-ce and Docker-Compose 1.11.2
- Metrics are collected by a Lambda function, so no more metrics sub-stack 🎉
- Secrets bucket uses KMS-backed SSE by default
- Support authenticated S3 paths for BootstrapScriptUrl and AuthorizedUsersUrl
- New regions (US Ohio)
- ECRAccessPolicy parameter for easy Amazon ECR configuration
- Fixed size stacks are possible, and don't create auto-scaling resources
- Added version number to stack description and agent metadata
- Optionally non-public agent instances

### Fixed
- Improved scale-up/scale-down logic
- Cloudwatch logs are sent to correct region
- Fixed size stacks are support
- Correct release names for beta and edge agent
- Better error handling for when fetching env or private-key fails
- Regions that require v4 signatures are better handled
- Working docker-gc script
- Autoscaling is suspended during stack updates
- Breaking changes

### Changed
- Initialization logs have moved to /var/log/elastic-stack.log

### Removed
- ManagedPolicyARNs has been removed, a singular version exists now: ManagedPolicyARN

## 1.1.1 - 2016-09-19
### Fixed
- 👭 If you run multiple agents per instance, chmod during build environment setup no longer clashes (#143)
- 🔐 The AWS_ECR_LOGIN_REGISTRY_IDS option has been fixed, so it now calls aws ecr get-login --registry-ids correctly (#141)

## 1.1.0 - 2016-09-09
- ### Added
- 📡 Buildkite Agent has been updated to the latest builds
- 🐳 Docker has been upgraded to 1.12.1
- 🐳 Docker Compose has been upgraded to 1.8.0
- 🔒 Can now add a custom managed policy ARN to apply to instances to add extra permissions to agents
- 📦 You can now specify a BootstrapScriptUrl to a bash script in an S3 bucket for performing your own setup and install tasks on agent machine boot
- 🔑 Added support for a single SSH key at the root of the secrets bucket (and SSH keys have been renamed)
- 🐳 Added support for logging into any Docker registry, and built-in support for logging into AWS ECR (N.B. the docker login environment variables have been - renamed)
- 📄 Docker, cloud-init and CloudFormation logs are sent to CloudWatch logs
- 📛 Instances now have nicer names
- ⚡ Updating stack parameters now triggers instances to update, no need for deleting and recreating the stack

### Fixed
- 🚥 The "queue" parameter is now "default" by default, to make it easier and less confusing to get started. Make sure to update it to "elastic" if you want to continue using that queue name.
- 🐳 Jobs sometimes starting before Docker had started has been fixed
- ⏰ Rolling upgrades and stack updates are now more reliable, no longer should you get stack timeouts



## 1.0.0 - 2016-07-28
### Added
- Initial release! 🎂🎉

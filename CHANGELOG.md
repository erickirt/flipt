# Changelog

This format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [v1.59.2](https://github.com/flipt-io/flipt/releases/tag/v1.59.2) - 2025-07-15

### Fixed

- `authn`: github allowed_teams keys are lowercased in configuration (#4445)

## [v1.59.1](https://github.com/flipt-io/flipt/releases/tag/v1.59.1) - 2025-06-27

### Fixed

- flag metadata parsing from snapshot (#4384)

## [v1.59.0](https://github.com/flipt-io/flipt/releases/tag/v1.59.0) - 2025-06-26

### Added

- `csrf`: allow to set trusted origins (#4347)

### Changed

- `audit`: improve delete audit events for rollout and rule (#4346)

### Fixed

- `ui`: just show segment name in segment picker (#4381)

## [v1.58.5](https://github.com/flipt-io/flipt/releases/tag/v1.58.5) - 2025-06-10

### Fixed

- `csrf`: update middleware usage to comply with gorilla/csrf changes (#4343)

## [v1.58.4](https://github.com/flipt-io/flipt/releases/tag/v1.58.4) - 2025-06-05

### Changed

- `storage`: use transaction for force namespace deletion (#4255)

### Fixed

- `audit`: add rollout ID to audit payload for create/update actions (#4294)
- allow percentage threshold zero value (#4290)

## [v1.58.3](https://github.com/flipt-io/flipt/releases/tag/v1.58.3) - 2025-05-26

### Fixed

- `storage`: allow force deletion of namespace with complex cfg (#4253)

## [v1.58.2](https://github.com/flipt-io/flipt/releases/tag/v1.58.2) - 2025-05-22

### Fixed

- `storage`: map protobuf enums to ints in sql updates for rule and (#4231)
- `audit`: keep segment data for rollout and rule (#4229)

## [v1.58.1](https://github.com/flipt-io/flipt/releases/tag/v1.58.1) - 2025-05-08

### Changed

- update Contributing section in README to link DEVELOPMENT.md  Removed broken [Architecture](ARCHITECTURE.md) link, updated to [Development](DEVELOPMENT.md) for redirection, and restructured section with subsections (What To Work On, Issues, Code) to align with CONTRIBUTING.md.  Signed-off-by: Suhas A <suhasamaresh@gmail.com> (#4151)

### Fixed

- prune remotes from cache that no longer exist (#4184)

## [v1.58.0](https://github.com/flipt-io/flipt/releases/tag/v1.58.0) - 2025-04-10

### Added

- add back ability to disable UI via config (#4060)

### Fixed

- `store`: disable modification of the store in read only mode (#4061)
- regression with setting ui to readonly (#4057)
- `ui`: display missing shadows in dark mode with tailwind v4 (#4053)

## [v1.57.0](https://github.com/flipt-io/flipt/releases/tag/v1.57.0) - 2025-04-06

### Added

- Support Redis cluster (#4035)
- `cache`: support optional prefix for redis cache keys (#4034)
- add contains constraint type (#4018)

## [v1.56.0](https://github.com/flipt-io/flipt/releases/tag/v1.56.0) - 2025-03-17

### Added

- move default boolean value to top; show in flag table view (#3983)

## [v1.55.1](https://github.com/flipt-io/flipt/releases/tag/v1.55.1) - 2025-03-11

### Changed

- Fix typo in DEVELOPMENT.md (#3973)

### Fixed

- otel interceptor panic/handling after switch to grpchan (#3975)
- `ui`: use correct default theme on first load (#3976)

## [v1.55.0](https://github.com/flipt-io/flipt/releases/tag/v1.55.0) - 2025-02-06

### Changed

- switch to in process communication between GRPC gateway and GRPC backend which should significantly improve HTTP performance.(#3856)

### Fixed

- `ui`: ui.topbar.color config setting has been broken since v1.53.0 (#3857)
- apply UI additional http headers only for requests to UI assets (#3853)
- `audit`: allow to send events with complex payload to kafka with avro (#3827)

## [v1.54.1](https://github.com/flipt-io/flipt/releases/tag/v1.54.1) - 2025-01-10

### Fixed

- update flag with no metadata (#3791)

## [v1.54.0](https://github.com/flipt-io/flipt/releases/tag/v1.54.0) - 2025-01-01

### Added

- add UI support for flag metadata (#3717)

### Changed

- `ui`: replace headlessui Switch with radix-ui (#3774)
- `cache`: use namespace.version as part of cache key (#3743)
- `ui`: make flags/segments views take up more screen space (#3726)

### Fixed

- otel http parent propogation (#3758)
- `ui`: fix the user profile icon (#3741)
- `authz`: support namespaces filtering (#3692)
- `sdk/go`: ensure empty string cannot be passed as path parameters (#3722)
- remove default namespace as a requirement to list namespaces  (#3716)
- `ui`: use useEffect for error when tokens could not be fetch (#3723)
- `ui`: use available namespace as selected before default fallback (#3719)
- remove default namespace as a requirement to list namespaces (#3711)

## [v1.53.2](https://github.com/flipt-io/flipt/releases/tag/v1.53.2) - 2024-12-12

### Fixed

- handle case where git repo already exists for local clone (#3712)

## [v1.53.1](https://github.com/flipt-io/flipt/releases/tag/v1.53.1) - 2024-12-09

### Fixed

- `analytics`: prevent panic with clickhouse setup (#3694)
- `analytics`: use rfc3339 for timestamps (#3695)

## [v1.53.0](https://github.com/flipt-io/flipt/releases/tag/v1.53.0) - 2024-12-06

### Added

- `ui`: new table view for flags and segments (#3664)

### Changed

- `ui`: stop using /meta/config endpoint (#3684)
- `ui`: use black as black, white as white (#3687)
- `github auth`: pass org and teams to metadata (#3654)

### Fixed

- `ui`: use table skeleton while flags or segments are loading (#3682)
- `ui`: use local timezone as default (#3680)
- `ui`: fix layout for user name and login (#3666)
- `analytics`: support Victoria Metrics with Prometheus storage (#3663)

## [v1.52.2](https://github.com/flipt-io/flipt/releases/tag/v1.52.2) - 2024-12-03

### Fixed

- dont return db url in meta/config response (#3681)

## [v1.52.1](https://github.com/flipt-io/flipt/releases/tag/v1.52.1) - 2024-11-27

### Added

- `analytics`: allow to set Authorization header for prometheus (#3656)

### Changed

- remove extra line in changelog to make linter happy (#3655)

### Fixed

- `ui`: tweak flag tabs to have the same layout (#3659)
- `config`: incorrect json serialization tag (#3658)

## [v1.52.0](https://github.com/flipt-io/flipt/releases/tag/v1.52.0) - 2024-11-25

### Added

- `analytics`: use Prometheus as source for analytics to display chart (#3619)

### Changed

- `ui`: rework dropdown component (#3634)
- `ui`: remove some duplication with buttons (#3615)
- `nightly`: fix goreleaser configuration for nightly (#3614)
- `ui`: remove nightwind as dependency (#3599)

### Fixed

- `import`: import flags with complex metadata (#3639)
- `config`: update schema for git storage backend property (#3617)
- `ui`: use dark scheme for browser built-in inputs/scrolls in dark mode (#3601)

## [v1.51.1](https://github.com/flipt-io/flipt/releases/tag/v1.51.1) - 2024-11-05

### Changed

- replace gofrs/uuid with google/uuid (#3576)
- `examples`: bump examples with recent changes (#3575)
- update attachment messaging and size to allow 1mb (#3595)

### Fixed

- pin goreleaser to v2.3.x to fix arm release (#3598)
- devcontainer update go version to 1.23 (#3597)
- `ui`: remove unnecessary scrolls for quick edit forms (#3592)
- `ofrep`: forward x-flipt-namespace http header from grpc-gateway to (#3591)
- `cockroachdb`: rework migrations for cockroachdb v23 and v24 (#3573)
- use user's home for sqlite db if no preferred location (#3570)

## [v1.51.0](https://github.com/flipt-io/flipt/releases/tag/v1.51.0) - 2024-10-28

### Changed

- `ofrep`: relax flags constraint for bulk evaluation (#3556)
- don't allow to delete segment which is in use (#3552)
- `export`: display a better error for missing segments and don't hide them in ui (#3527)

### Fixed

- Import issue when --address and --drop is used (#3530)

## [v1.50.1](https://github.com/flipt-io/flipt/releases/tag/v1.50.1) - 2024-10-01

### Added

- `ext`: determinism in exporting and declarative formats (#3509)

### Fixed

- skip authz for clickhouse (#3511)

## [v1.50.0](https://github.com/flipt-io/flipt/releases/tag/v1.50.0) - 2024-09-17

### Added

- Add configurable nonce for OIDC provider. (#3453)

### Fixed

- `audit`: include default_variant into flag audit payload (#3472)
- `storage`: map protobuf enums to ints in sql (#3454)
- support scoped namespace tokens for evaluation data api (#3452)

## [v1.49.2](https://github.com/flipt-io/flipt/releases/tag/v1.49.2) - 2024-09-09

### Fixed

- enable pgx simple protocol if prepared statements disabled (#3436)
- check authz for client-side evaluation endpoint (#3438)

## [v1.49.1](https://github.com/flipt-io/flipt/releases/tag/v1.49.1) - 2024-09-03

### Changed

- `authz`: use lock only during the variables update (#3431)

### Fixed

- `storage/fs`: threading insecure and ca bundle on fetch (#3433)

## [v1.49.0](https://github.com/flipt-io/flipt/releases/tag/v1.49.0) - 2024-09-02

### Added

- `ui`: save sort state in redux (#3415)
- `authz`: added a helper function to the policy engine to simplify (#3419)

### Changed

- `audit`: add integration testing for audit webhooks (#3384)

### Fixed

- `ui`: show boolean flags as enabled in the console dropdown (#3399)

## [v1.48.1](https://github.com/flipt-io/flipt/releases/tag/v1.48.1) - 2024-08-16

### Fixed

- `audit`: provide correct leveled_logger for retryablehttp client (#3382)

## [v1.48.0](https://github.com/flipt-io/flipt/releases/tag/v1.48.0) - 2024-08-14

### Added

- `ofrep`: implement bulk evaluation for OFREP (#3364)
- Support import export namespace data (#3356)
- support postgresql url prefix (#3354)

### Changed

- `sdk`: update go sdk examples with new change in gRPC (#3363)
- generate OpenAPI from grpc (#3357)
- add rajyan as a contributor for code (#3359)
- add radekska as a contributor for code (#3355)

### Fixed

- `cors`: add missing from default allowed CORS headers (#3378)
- `gh`: clear unused tools before dagger runs (#3362)
- use different error messages for namespace scoped token errors (#3358)

## [v1.47.1](https://github.com/flipt-io/flipt/releases/tag/v1.47.1) - 2024-08-01

### Fixed

- `storage`: support mysql 5.7 in 12 migration (#3334)
- `ui`: preserve default variant during the flag updates (#3330)

## [v1.47.0](https://github.com/flipt-io/flipt/releases/tag/v1.47.0) - 2024-07-29

### Added

- add single evaluation endpoint for OFREP (#3267)
- `import`: Add import append flag to import new flags only not existing in DB yet (#3299)
- default variants (#3271)
- support etag for declarative stores (#3287)
- support for flag metadata - api only (#3196)

### Changed

- Update default rollout (#3301)
- show default value in flag table (#3300)
- add kvnhmn as a contributor for code (#3304)
- add wtertius as a contributor for code (#3303)

## [v1.46.3](https://github.com/flipt-io/flipt/releases/tag/v1.46.3) - 2024-08-01

### Fixed

- `storage`: support mysql 5.7 in 12 migration (#3334)

## [v1.46.2](https://github.com/flipt-io/flipt/releases/tag/v1.46.2) - 2024-07-25

### Fixed

- `config`: remove experiment tag from config struct (#3305)

## [v1.46.1](https://github.com/flipt-io/flipt/releases/tag/v1.46.1) - 2024-07-17

### Fixed

- passing invalid logger to retriable http client (#3285)

## [v1.46.0](https://github.com/flipt-io/flipt/releases/tag/v1.46.0) - 2024-07-15

### Added

- Etag support for client side evaluation (#3248)
- Add provider configuration for ofrep (#3247)
- `audit`: implement sink for kafka (#3204)

### Changed

- Fix issue with missing code coverage report (#3238)

## [v1.45.2](https://github.com/flipt-io/flipt/releases/tag/v1.45.2) - 2024-07-25

### Fixed

- passing invalid logger to retriable http client
- `config`: remove experiment tag from config struct (#3305)

## [v1.45.1](https://github.com/flipt-io/flipt/releases/tag/v1.45.1) - 2024-07-09

### Fixed

- Forward x-flipt-accept-server-version to grpc (#3262)

## [v1.45.0](https://github.com/flipt-io/flipt/releases/tag/v1.45.0) - 2024-06-26

### Added

- Rbac cloud (#3203)
- `authz`: add opa bundle support (#3194)
- support environment variable substitution in config files (#3195)

### Changed

- `authz`: move out of experimental (#3203)
- `proto`: prevent panic in protoc-gen-go-flipt-sdk (#3215)
- `build`: move to new dagger v0.11.8 (#3144)

### Fixed

- `build`: configure token authentication for migration test suite (#3177)

## [v1.44.1](https://github.com/flipt-io/flipt/releases/tag/v1.45.2) - 2024-07-09

### Fixed

- forward x-flipt-accept-server-version to grpc (#3262)

## [v1.44.0](https://github.com/flipt-io/flipt/releases/tag/v1.44.0) - 2024-06-13

### Added

- allow to copy evaluate command in a CLI format (#3154)
- `build/testing`: add authz specific integration tests (#3163)
- Audit failed authz attempts (#3155)
- support writing audit events to stdout for log (#3113)
- `ui`: allow change top bar theme color (#3128)

### Changed

- dont log grpc healthcheck

### Fixed

- `ui`: prevent reload after logout (#3149)
- `auth`: allow authorization for Github and OIDC behind the reverse (#3135)

## [v1.43.0](https://github.com/flipt-io/flipt/releases/tag/v1.43.0) - 2024-05-30

### Added

- experimental: Authz (#3008)
- add support for ghe (#3136)
- `cache/redis`: support ca certificate and insecure tls options (#3107)
- `fs/git`: add support for cloning target repository to the local filesystem

### Changed

- add tvcsantos as a contributor for code (#3137)
- add vk-rv as a contributor for code (#3112)
- `config`: rename git backend filesystem to local (#3110)

### Fixed

- `ui`: await expiring auth self before redirecting (#3133)
- issues with cloud config for cloud serve (#3129)
- use cloud auth token from JWT instead of API key if present for flipt cloud serve (#3114)
- prevent redis shutdown (#3111)
- write response for cloud login before server shutdown (#3109)

## [v1.42.1](https://github.com/flipt-io/flipt/releases/tag/v1.42.1) - 2024-05-21

### Changed

- Optimized the Git backend to only fetch explicitly required references (#3100)

## [v1.42.0](https://github.com/flipt-io/flipt/releases/tag/v1.42.0) - 2024-05-15

### Added

- logout redirect to cloud issuer (#3082)
- add banner about cloud offering (#3077)
- Cloud support (#2998)

### Changed

- `integration`: add failing case for rules with no distributions (#3078)

### Fixed

- nightly and snapshot builds (mage) (#3084)
- `migrations`: change the order of queries for mysql (#3039)

## [v1.41.2](https://github.com/flipt-io/flipt/releases/tag/v1.41.2) - 2024-05-14

### Fixed

- Bug in rules evaluation with no distributions for declarative stores (#3076)
- Make OCI reauthenticate when using AWS ECR (#3044)

## [v1.41.1](https://github.com/flipt-io/flipt/releases/tag/v1.41.1) - 2024-05-01

### Fixed

- `breaking`: sampling ratio yaml config (#3034)

## [v1.41.0](https://github.com/flipt-io/flipt/releases/tag/v1.41.0) - 2024-04-30

### Added

- add semver constraint for git storage (#2977)
- OTLP metrics exporter (#3021)
- `authn`: allow validation of jwt subject claim (#2995)
- improve open telemetry tracing instrumentation (#2984)
- `config`: support remote blob storage for service configuration (#2983)

### Changed

- `storage`: move from lib/pq to pgx (#2996)

### Fixed

- `cmd/grpc`: skip eval data service when evaluation API auth excluded (#3018)

## [v1.40.2](https://github.com/flipt-io/flipt/releases/tag/v1.40.2) - 2024-04-23

### Fixed

- `cmd/grpc`: skip eval data service when evaluation API auth excluded (#3018)

## [v1.40.1](https://github.com/flipt-io/flipt/releases/tag/v1.40.1) - 2024-04-11

### Changed

- add halcyonCorsair as a contributor for code (#2970)

### Fixed

- only store auth hash in cache (#2974)
- `auth`: skip establishing a database connection when not necessary (#2973)
- `cache`: accept a username in redis configuration (#2953)

## [v1.40.0](https://github.com/flipt-io/flipt/releases/tag/v1.40.0) - 2024-04-05

### Added

- `oci`: better integration OCI storage with AWS ECR (#2941)
- `fs/git`: add support for a directory scope (#2939)
- `cmd`: allow passing a working directory for flipt validate command (#2936)

### Changed

- moved validation into its separate package (#2831)

### Fixed

- invalid trace log level schema (#2946)
- jsonschema to correctly validate key|keys in rollout segment (#2947)
- `ui`: evaluation console provides the warning for user about context values (#2937)
- dont error on parsing in evaluator (#2918)

## [v1.39.2](https://github.com/flipt-io/flipt/releases/tag/v1.39.2) - 2024-03-29

### Fixed

- isnotoneof operator using incorrect logic (#2912)
- issue with segment constraints if belonging to same segment key in different namespaces (#2920)

## [v1.39.1](https://github.com/flipt-io/flipt/releases/tag/v1.39.1) - 2024-03-27

### Added

- make oci manifest version configurable (#2908)

## [v1.39.0](https://github.com/flipt-io/flipt/releases/tag/v1.39.0) - 2024-03-25

### Added

- add team membership check to GitHub authentication method (#2891)
- clear session if authentication methods change
- add command bar (#2815)
- add JWT aware UI and revise metadata for audit events

### Changed

- `ui`: assistance for arrays data in constraints (#2889)

### Fixed

- `ui`: allow dot in the key of variant (#2887)
- missing slash in copy as curl (#2875)
- `ui`: prevent react warning (#2845)
- `ui`: show placeholder for entity id oneof* constraint (#2799)

## [v1.38.2](https://github.com/flipt-io/flipt/releases/tag/v1.38.2) - 2024-03-15

### Fixed

- shadow bug for segments in Flipt Data API (#2860)

## [v1.38.1](https://github.com/flipt-io/flipt/releases/tag/v1.38.1) - 2024-03-13

### Fixed

- Analytics page returning 501 if not enabled (#2486)

## [v1.38.0](https://github.com/flipt-io/flipt/releases/tag/v1.38.0) - 2024-02-23

### Added

- add ability to check known flipt server verison (#2791)
- add integration test case for entity id adding
- `flipt`: add entityId as a constraint type and operator
- `otlp`: account for service name in environment variable (#2775)

### Changed

- `tracing`: move tracing setup into own package and extra tests added (#2776)

### Fixed

- `ui`: stop removing upper case letters in keys (#2790)
- `analytics`: aggregate data to run queries faster (#2778)
- `ui`: prevent multiple analytics requests at once with polling (#2777)

## [v1.37.1](https://github.com/flipt-io/flipt/releases/tag/v1.37.1) - 2024-02-12

### Added

- `analytics`: add live updates with play/pause button

### Fixed

- `ui`: increase z index for Slideover and Modal (#2758)
- csp headers for formbricks (#2757)

## [v1.37.0](https://github.com/flipt-io/flipt/releases/tag/v1.37.0) - 2024-02-09

### Added

- add inapp survey (#2753)
- first time onboarding experience (#2732)
- `analytics`: analytics support with Clickhouse (#2725)
- `sdk/go`: add kubernetes authentication provider (#2703)
- `examples`: add examples section for otlp -> clickhouse

### Changed

- fix link to devenv.sh (#2731)
- `examples`: added example how to run flipt behind nginx (#2726)
- `config`: mark authentication.exclude.metadata as deprecated (#2707)
- `cmd`: dont omit 'enabled' in evaluate cli if false (#2705)

### Fixed

- running Flipt under reverse proxy with subpath (#2734)
- `ui`: fix input alignment on small screens (#2733)
- `audit`: reordering rules or rollouts is not captured by audit logs (#2721)
- `ui`: clean redux cache when namespace or flag is deleted (#2708)

## [v1.36.0](https://github.com/flipt-io/flipt/releases/tag/v1.36.0) - 2024-01-23

### Added

- `cmd`: flipt evaluate CLI subcommand (#2678)
- `validate`: add ability to further constrain schema (#2677)
- `ui`: show configured Git ref in UI (#2673)
- `storage/fs/git`: add initial support for multiple snapshots (#2609)

### Changed

- `examples`: update openfeature example to use jaeger with otlp endpoint (#2676)
- `ui`: improve index (#2669)
- `ui`: improve Yup usage (#2647)
- `ui/console`: replace monaco with codemirror (#2646)
- `ui`: drop highlight.js (#2645)
- `ui`: drop moment.js (#2644)
- `ui`: drop lodash as deps (#2640)
- deprecate Jaeger tracing (#2675)

### Fixed

- `cfg`: json schema missing storage type oci (#2674)
- `ui`: boolean constraint type asks for value when you edit it (#2671)
- Combobox not showing options upon input click (#2642)
- `fs/object`: close reader after using it (#2648)
- `validate(cue):` get correct error line position (#2701)

## [v1.35.0](https://github.com/flipt-io/flipt/releases/tag/v1.35.0) - 2024-01-09

### Added

- JWT auth (#2620)
- `grpc`: grpc keepalive configuration (#2621)
- `storage/gcs`: add support for Google Cloud Storage (#2589)
- cache evaluation rollouts at storage layer (#2610)

### Changed

- `cleanup`: parallelize cleanup method tests (#2612)

### Fixed

- `ui`: searchbox has a black text color in dark mode so it's very hard (#2619)
- config init does not work correctly (#2616)
- close oidc providers per lib recommendation (#2598)

## [v1.34.0](https://github.com/flipt-io/flipt/releases/tag/v1.34.0) - 2023-12-28

### Added

- validate common auth config settings (#2579)
- `fs/azure`: add support for Azure Blob Storage (FS Object Backend) (#2538)
- `rpc/flipt`: add Now timestamp with microsecond precision function
- `ui`: show time/date format on settings/preferences page (#2537)

### Changed

- use rpc/flipt.Now everywhere instead of timestamppb.Now
- `ui`: move listAuthMethods to Redux RTK (#2529)

### Fixed

- `config`: always use forward-slash as separator for DB URL (#2578)
- close the indexFile after reading it (#2561)
- resolved issues with go-git 5.11.0 (#2543)
- `mysql`: increase timestamp precision from seconds to microseconds
- `cfg`: default config outputs first INFO log regardless of FLIPT_LOG_LEVEL (#2536)

## [v1.33.0](https://github.com/flipt-io/flipt/releases/tag/v1.33.0) - 2023-12-11

### Added

- `auth/github`: add organization membership check to GitHub (#2508)
- `ui`: allow setting page size for tables (#2503)
- use default config even on linux if no config found (#2496)
- `ui/console`: add copy as curl button (#2474)

### Changed

- `cli`: silence usage on error (#2512)
- `ui`: cleanup header; show user name and opt login in user dropdown (#2480)
- `ui`: replace classNames with clsx library (#2482)
- `ui`: use rtk for flags (#2478)
- `ui`: move namespaces to use redux rtk (#2472)
- rework tests for TLS options for git sources with self-signed certificates

### Fixed

- `ui`: remove h-screen from default for Loading component (#2527)
- `ui`: page api call could finish earlier that Layout api calls (#2506)
- dont show name/login section if only email (#2495)

## [v1.32.0](https://github.com/flipt-io/flipt/releases/tag/v1.32.0) - 2023-11-29

### Added

- Add pre-commit hook support (#2451)
- Added TLS options for git sources with self-signed certificates (#2443)
- `ui/tokens`: delete multiple tokens (#2424)

### Changed

- `ui`: move tokens api to Redux RTK (#2468)
- `ui`: move Rollouts to use Redux storage (#2465)
- `ui`: move Rules to use Redux for storage (#2461)
- add mattiaforc as a contributor for code (#2463)
- `ui`: move Segments to use Redux storage (#2441)
- add erka as a contributor for code (#2431)
- `cue`: add failing case for attachment array support

### Fixed

- `ui/console`: rework monaco editor (#2467)
- `ui/console`: monaco web workers don't work (#2464)
- incorrect selector usage in redux (#2446)
- camelcase JSON representation in storage config (#2445)
- `ui/token`: show search input if it contains user's input (#2439)
- `ui/token`: default namespaced token does not get created without selecting 'default' (#2438)
- `cue`: allow arrays for variant attachment

## [v1.31.3](https://github.com/flipt-io/flipt/releases/tag/v1.31.1) - 2023-11-22

### Fixed

- Bad release of 1.31.2 causing the fixes in 1.31.1 to get dropped

## [v1.31.2](https://github.com/flipt-io/flipt/releases/tag/v1.31.2) - 2023-11-21

### Fixed

- Make CUE schema more permissive and accepts arrays, as well as objects under variant attachments (#2422)

## [v1.31.1](https://github.com/flipt-io/flipt/releases/tag/v1.31.1) - 2023-11-16

### Fixed

- Support Flipt running over Git repositories with submodules (#2405)

## [v1.31.0](https://github.com/flipt-io/flipt/releases/tag/v1.31.0) - 2023-11-15

### Added

- Add support for namespaced auth tokens (#2352)
- Add constraint operator `IS ONE OF`/`IS NOT ONE OF` (#2368)
- Add rollout description to rollout cards (#2366)
- Update Colorscheme (#2363)
- Add OCI backend support (#2328)

### Changed

- Add LiteFS example for Flipt in the examples directory (#2297)

### Fixed

- No value bug for boolean constraint type (#2395)
- Support fern and customizable allowed headers via CORS (#2393)

## [v1.30.1](https://github.com/flipt-io/flipt/releases/tag/v1.30.1) - 2023-11-06

### Fixed

- Exclude health check from auth (#2350)

## [v1.30.0](https://github.com/flipt-io/flipt/releases/tag/v1.30.0) - 2023-10-31

### Added

- add flag key to variant and boolean evaluation responses (#2318)
- add subject to authentication metadata for auditing (#2299)
- `git`: support SSH authentication (#2272)

### Changed

- `ui`: redux all flag and variant state management (#2301)
- dependency updates

### Fixed

- readOnly config option should be read_only (#2298)
- Audit log path will be created if doesn't exist (#2295)

## [v1.29.1](https://github.com/flipt-io/flipt/releases/tag/v1.29.1) - 2023-10-26

### Fixed

- error about invalid offset with FS backend (#2286)

### Changed

- security: GRPC dependency updates

## [v1.29.0](https://github.com/flipt-io/flipt/releases/tag/v1.29.0) - 2023-10-23

### Added

- impl grpc health check (#2257)
- `distributions`: support updating distribution variant (#2235)
- allow disabling profiling endpoints (#2195)
- LibSQL/Turso support

### Changed

- Add default namespace in the sync store layer for FS implementations

## [v1.28.2](https://github.com/flipt-io/flipt/releases/tag/v1.28.2) - 2023-10-13

### Fixed

- `service/middleware`: use separate cache keys for old and new evaluations (#2237)

## [v1.28.1](https://github.com/flipt-io/flipt/releases/tag/v1.28.1) - 2023-10-04

### Fixed

- csp header for monaco editor (#2200)
- specify region to fix s3 feature (#2193)

## [v1.28.0](https://github.com/flipt-io/flipt/releases/tag/v1.28.0) - 2023-10-02

### Added

- `ui`: Rules tab (#2176)
- Add requestID to batch response (#2177)
- `cli`: Gen docs (#2173)
- `storage/fs`: Allow FS backends to understand multi-document YAML files
- `cli`: config edit command (#2169)
- support export otel telemetry directly over http(s) (#2155)
- `cli`: cmd shell completions (#2168)
- `import/export`: add support for exporting multiple namespaces and all namespaces
- `cli`: config init (#2147)
- `import/export`: add functionality for importing YAML stream
- `tracing`: add OTLP headers config (#2148)
- `audit`: Add webhook templating for generic request to webhooks

### Changed

- Dependency Updates

### Fixed

- export over https (#2152)

## [v1.27.2](https://github.com/flipt-io/flipt/releases/tag/v1.27.2) - 2023-09-21

### Fixed

- `security`: dont marshal secrets to JSON

## [v1.27.1](https://github.com/flipt-io/flipt/releases/tag/v1.27.1) - 2023-09-18

### Added

- Add token type and actions to audit event filter (#2121)

### Fixed

- `webhook`: Rewind HTTP request body upon request failure (#2143)
- Default config allow env overrides (#2144)

## [v1.27.0](https://github.com/flipt-io/flipt/releases/tag/v1.27.0) - 2023-09-13

### Added

- Audit info to telemetry (#2116)
- Webhook configuration for sending event payloads (#2087)
- `events`: Add feature for scoping the emission of events
- Datadog as an exporter for OTLP traces (#2083)
- Default config (#2067)
- Support page instead of link to docs (#2063)
- Ability to set default theme for UI (#2062)

### Changed

- `flipt/validate`: build entire snapshot on validate (#2093)
- Dependency updates

### Fixed

- `build/generate`: add exposed port to flipt (#2060)

## [v1.26.1](https://github.com/flipt-io/flipt/releases/tag/v1.26.1) - 2023-09-09

### Fixed

- `cmd/import`: check for correct not found error on create namespace (#2082)
- `ext`: attempt to import when namespace exists on create namespace (#2089)
- `schema`: make rollout description optional in cue schema (#2091)

## [v1.26.0](https://github.com/flipt-io/flipt/releases/tag/v1.26.0) - 2023-08-28

### Added

- exp: Homebrew tap (#2044)
- Switch to monaco editor for console (#2040)
- default to ~/Library/Application\ Support/flipt for db sqlite file on mac (#2039)
- `auth`: Add parameters for pkce flow
- `auth`: OAuth for GitHub (#2016)

### Changed

- Dependency updates

### Fixed

- hover icon visibility for copy key to clipboard in lightmode (#2056)

## [v1.25.2](https://github.com/flipt-io/flipt/releases/tag/v1.25.2) - 2023-08-23

### Fixed

- `internal/ext`: add 1.1 to versions and validate explicit 1.2 (#2042)

## [v1.25.1](https://github.com/flipt-io/flipt/releases/tag/v1.25.1) - 2023-08-21

### Fixed

- cache shadow var when setting up middleware (#2017)

## [v1.25.0](https://github.com/flipt-io/flipt/releases/tag/v1.25.0) - 2023-08-16

### Added

- `ui`: copy flag/segment key to clipboard button in ui (#1987)
- `storage/cache`: add redis connection optional params (#1983)
- `ui`: Force readonly (#1973)
- `fs/s3`: Add support for prefix filtering (#1938)
- `config/flipt.schema.*`: add oidc provider scopes property (#1946)
- `segment-anding`: the ability to and or or multiple segments in rules and rollouts (#1941)

### Changed

- `fs`: Graduate filesystem storage (#1976)

### Fixed

- `ui`: make flags/segments inputs disabled in readonly mode (#1986)

## [v1.24.2](https://github.com/flipt-io/flipt/releases/tag/v1.24.2) - 2023-08-07

### Fixed

- `ui`: rule form inputs in darkmode (#1968)
- store namespace in localstorage (#1950)
- dont clear all localstorage on 401 (#1951)

## [v1.24.1](https://github.com/flipt-io/flipt/releases/tag/v1.24.1) - 2023-08-01

### Fixed

- fix(auth/middleware): only enforce email matches on OIDC method tokens (#1934)

## [v1.24.0](https://github.com/flipt-io/flipt/releases/tag/v1.24.0) - 2023-07-31

### Added

- boolean flag type, rollouts, and new evaluation routes :tada: (#1824)
- `fs/s3`: Initial support for s3 filesystem backend (#1900)
- `email`: Add email matching logic for whitelisting OIDC
- `build`: add mage dagger:run generate:screenshots (#1868)
- add cache to get evaluation rules storage method (#1910)

### Changed

- unhide validate command (#1909)
- add rudineirk as a contributor for code (#1913)
- add ahobson as a contributor for code (#1905)
- Dependency updates

### Fixed

- renable pprof (#1912)
- dagger cli test (#1899)
- `ui`: memoize selectors for namespaces (#1837)

## [v1.23.3](https://github.com/flipt-io/flipt/releases/tag/v1.23.3) - 2023-07-06

### Fixed

- potential panic in `flipt validate` (#1831)
- support variant desc in cue import schema (#1828)

### Changed

- Dependency updates

## [v1.23.2](https://github.com/flipt-io/flipt/releases/tag/v1.23.2) - 2023-07-03

### Added

- 'Share Feedback' link in app footer (#1812)

### Changed

- trim trailing slash off of http request if exists
- `config`: ensure JSON schema validates the default configuration (#1788)
- `config`: ensure default config passes CUE validation (#1758)
- return 400 for invalid page token"
- `integration`: ensure all list limits are enforced correctly
- Dependency updates

### Fixed

- Fix `flipt validate` command (#1811)
- context cancelled/deadline exceeded errors coming back internal (#1803)
- prevent overwriting URL struct (#1784) for trailing slash change

## [v1.23.1](https://github.com/flipt-io/flipt/releases/tag/v1.23.1) - 2023-06-15

### Added

- Ability to configure use of prepared statements (for enabling PGBouncer) (#1750)
- `telemetry`: track storage type and experimental features (#1745)

### Changed

- Dependency updates

### Fixed

- `storage/sql`: set binary_parameters=yes for lib/pq when prepared statements disabled (#1753)
- UI: input bg / text in darkmode (#1752)
- count rules was not taking flagKey into account (#1738)
- tag prefix for build info/release links (#1757)

## [v1.23.0](https://github.com/flipt-io/flipt/releases/tag/v1.23.0) - 2023-06-12

### Added

- UI: Darkmode (#1692)
- UI: Copy to namespace (#1731)
- UI: Support for read-only mode (#1709)
- check source file from different places for configuration if they exist (#1650)
- Experimental: support for filesystem/git backends (#1714)
- Flipt Validate (#1642)
- add namespace to export, check for match on import (#1645)
- add storage configuration to support multiple backend types (#1644)

### Changed

- `integration`: ensure public and auth self routes are reachable (#1729)
- `cli`: ensure user configuration path supported (#1727)
- `storage/sql`: handle null description on constraint during GetSegment (#1654)
- UI: switch namespaces to use Redux (#1680)
- `build`: define CLI tests using dagger pipelines (#1679)
- Dependency updates

### Fixed

- UI: disable flag toggle in read-only mode (#1719)
- cross namespaced constraints (#1721)
- `mage`: install package-changed as dev dependency (#1716)
- UI: catch errs on call to namespaces API in namespace form (#1687)
- Get the openfeature example working (#1665)
- panic if no import file name provided (#1658)

## [v1.22.1](https://github.com/flipt-io/flipt/releases/tag/v1.22.1) - 2023-05-24

### Fixed

- `storage/sql`: handle null description on constraint during GetSegment

## [v1.22.0](https://github.com/flipt-io/flipt/releases/tag/v1.22.0) - 2023-05-23

### Added

- Datetime constraint type (#1602)
- Add optional description to constraints (#1581)

### Changed

- Dependency updates

## [v1.21.1](https://github.com/flipt-io/flipt/releases/tag/v1.21.1) - 2023-05-05

### Fixed

- `storage/sql`: paginated walk for resources using joins (#1584)

## [v1.21.0](https://github.com/flipt-io/flipt/releases/tag/v1.21.0) - 2023-05-02

### Added

- OTEL implementation for audit sinks (#1458)
- Error highlighting in console (#1528)
- Additional telemetry data captured re: database, cache and authentication (#1527)

### Fixed

- `cmd/flipt`: restore console logger defaults on fatal (#1550)
- `grpc/middleware`: set timestamp on each batch evaluate response (#1545)

### Changed

- Dependency updates

## [v1.20.2](https://github.com/flipt-io/flipt/releases/tag/v1.20.2) - 2023-05-05

### Fixed

- `storage/sql`: paginated walk for resources using joins (#1584)

## [v1.20.1](https://github.com/flipt-io/flipt/releases/tag/v1.20.1) - 2023-04-27

### Fixed

- `grpc/middleware`: set timestamp on each batch evaluate response (#1545)

## [v1.20.0](https://github.com/flipt-io/flipt/releases/tag/v1.20.0) - 2023-04-11

### Added

- Support for 'namespacing' / multi-environments. All types can now belong to a namespace allowing you to seperate your flags/segments/etc.

### Changed

- `sdk/go`: add details regarding the HTTP transport (#1435)
- All existing objects have been moved to the 'default' namespace to be fully backward compatible.
- Import/Export have been updated to be 'namespace-aware'
- Dependency updates

### Fixed

- `cmd/import`: re-open migration after dropping on import
- protojson to use DiscardUnknown option for backwards compatibility (#1453)
- `rpc/flipt`: move all openapi annotations into yaml file (#1437)

## [v1.19.5](https://github.com/flipt-io/flipt/releases/tag/v1.19.5) - 2023-05-05

### Fixed

- `storage/sql`: paginated walk for resources using joins (#1584)

## [v1.19.4](https://github.com/flipt-io/flipt/releases/tag/v1.19.4) - 2023-04-27

### Fixed

- `grpc/middleware`: set timestamp on each batch evaluate response (#1545)

## [v1.19.3](https://github.com/flipt-io/flipt/releases/tag/v1.19.3) - 2023-03-22

### Changed

- Upgraded to Go 1.20
- Dependency updates

## [v1.19.2](https://github.com/flipt-io/flipt/releases/tag/v1.19.2) - 2023-03-15

### Changed

- Dependency updates
- Return better error messages for grpc-gateway errors [#1397](https://github.com/flipt-io/flipt/pull/1397)

### Fixed

- Import/Export for CockroachDB [#1399](https://github.com/flipt-io/flipt/pull/1399)

## [v1.19.1](https://github.com/flipt-io/flipt/releases/tag/v1.19.1) - 2023-02-27

### Changed

- Dependency updates
- UI: combobox shows 'No results found' if no input matches

### Fixed

- UI: issue where Edit Rule submit button was disabled [ui #108](https://github.com/flipt-io/flipt-ui/pull/108)

## [v1.19.0](https://github.com/flipt-io/flipt/releases/tag/v1.19.0) - 2023-02-22 :lock:

### Added

- UI: Settings/API Tokens management
- Enable ability to specify bootstrap token [#1350](https://github.com/flipt-io/flipt/1350)
- Kubernetes Authentication Method [#1344](https://github.com/flipt-io/flipt/1344)

### Changed

- Dependency updates
- Switch to official redis client and redis-cache/v9 [#1345](https://github.com/flipt-io/flipt/1345)

## [v1.18.2](https://github.com/flipt-io/flipt/releases/tag/v1.18.2) - 2023-02-14 :heart:

### Added

- OpenTelemetry: support for Zipkin exporter [#1323](https://github.com/flipt-io/flipt/pull/1323)
- OpenTelemetry: support for OTLP exporter [#1324](https://github.com/flipt-io/flipt/pull/1324)

### Changed

- Deprecated `tracing.jaeger.enabled` [#1316](https://github.com/flipt-io/flipt/pull/1316)
- Added `frame-ancestors` directive to `Content-Security-Policy` header [#1317](https://github.com/flipt-io/flipt/pull/1317)

### Fixed

- UI: Clear session if 401 is returned from server [ui #88](https://github.com/flipt-io/flipt-ui/pull/88)
- Ensure all authentication methods are being cleaned up [#1337](https://github.com/flipt-io/flipt/pull/1337)
- Ensure failed cookie auth attempt clears cookies [#1336](https://github.com/flipt-io/flipt/pull/1336)
- 500 error when providing invalid base64 encoded page token [#1314](https://github.com/flipt-io/flipt/pull/1314)

## [v1.18.1](https://github.com/flipt-io/flipt/releases/tag/v1.18.1) - 2023-02-02

### Added

- Set Content-Security-Policy and `X-Content-Type-Options` headers [#1293](https://github.com/flipt-io/flipt/pull/1293)
- Ability to customize log keys/format [#1295](https://github.com/flipt-io/flipt/pull/1295)
- Additional OpenTelemetry annotations for `GetFlag` and `Evaluate` calls [#1306](https://github.com/flipt-io/flipt/pull/1306)
- UI: Visual indicator on submitting + success message [ui #52](https://github.com/flipt-io/flipt-ui/pull/52)

### Changed

- Dependency updates
- UI: Clear session on logout, change session storage format [ui #64](https://github.com/flipt-io/flipt-ui/pull/64)

### Fixed

- ListX calls could potentially lock the DB if running in SQLite. Also a nice performance boost [#1297](https://github.com/flipt-io/flipt/pull/1297)
- UI: Bug where editing constraint values did not pre-populate with existing values [ui #67](https://github.com/flipt-io/flipt-ui/pull/67)
- UI: Regression where we weren't showing help text when creating rule with no variants [ui #58](https://github.com/flipt-io/flipt-ui/pull/58)

## [v1.18.0](https://github.com/flipt-io/flipt/releases/tag/v1.18.0) - 2023-01-23

### Added

- UI: Login via OIDC [ui #41](https://github.com/flipt-io/flipt-ui/pull/41)
- UI: Validate distribution percentages [ui #37](https://github.com/flipt-io/flipt-ui/pull/37)
- New `auth.ExpireAuthenticationSelf` endpoint to expire a user's own authentication [#1279](https://github.com/flipt-io/flipt/pull/1279)

### Changed

- Dev: Switched from Task to Mage [#1273](https://github.com/flipt-io/flipt/pull/1273)
- Authentication metadata structure changed to JSON object [#1275](https://github.com/flipt-io/flipt/pull/1275)
- Dev: Make developing the UI easier by proxying `:8080` to vite [#1278](https://github.com/flipt-io/flipt/pull/1278)
- Dependency updates

### Fixed

- Setting Authentication cookies on localhost [#1274](https://github.com/flipt-io/flipt/pull/1274)
- Panic in `/meta` endpoints when Authentication was required but not present [#1277](https://github.com/flipt-io/flipt/pull/1277)
- Don't set empty CSRF cookie [#1280](https://github.com/flipt-io/flipt/pull/1280)
- Bootstrapping command in mage [#1281](https://github.com/flipt-io/flipt/pull/1281)
- Removed duplicate shutdown log [#1282](https://github.com/flipt-io/flipt/pull/1282)

## [v1.17.1](https://github.com/flipt-io/flipt/releases/tag/v1.17.0) - 2023-01-13

### Fixed

- UI: Fix useEffect warnings from eslint [ui #21](https://github.com/flipt-io/flipt-ui/pull/21)
- UI: Show info about creating rule with no variants [ui #22](https://github.com/flipt-io/flipt-ui/pull/22)
- UI: Fix issue where key was changing when updating flag/segment name [ui #25](https://github.com/flipt-io/flipt-ui/pull/25)
- UI: Fixed issue where segment form would reset when changing matchType [ui #26](https://github.com/flipt-io/flipt-ui/pull/26)
- UI: Fixed auto key generation from name weirdness [ui #27](https://github.com/flipt-io/flipt-ui/pull/27)

## [v1.17.0](https://github.com/flipt-io/flipt/releases/tag/v1.17.0) - 2023-01-12

### Added

- Brand new UI / UX :tada:
- JSON/CUE schema [#1196](https://github.com/flipt-io/flipt/pull/1196)
- Support config file versioning [#1225](https://github.com/flipt-io/flipt/pull/1225)
- OIDC Auth Methods [#1197](https://github.com/flipt-io/flipt/pull/1197)
- List API for Auth Methods [#1240](https://github.com/flipt-io/flipt/pull/1240)

### Changed

- Move `/meta` API endpoints behind authentication [#1250](https://github.com/flipt-io/flipt/pull/1250)
- Dependency updates

### Deprecated

- Deprecates `ui.enabled` in favor of always enabling the UI

### Fixed

- Don't print to stdout with color when using JSON log format [#1188](https://github.com/flipt-io/flipt/pull/1188) 

### Removed

- Embedded swagger/openapiv2 API docs in favor of hosted / openapiv3 API docs [#1241](https://github.com/flipt-io/flipt/pull/1241)

## [v1.16.0](https://github.com/flipt-io/flipt/releases/tag/v1.16.0) - 2022-11-30

### Added

- Automatic authentication background cleanup process [#1161](https://github.com/flipt-io/flipt/pull/1161).

### Fixed

- Fix configuration unmarshalling from `string` to `[]string` to delimit on `" "` vs `","` [#1179](https://github.com/flipt-io/flipt/pull/1179)
- Dont log warnings when telemetry cannot report [#1156](https://github.com/flipt-io/flipt/pull/1156)

### Changed

- Switched to use otel abstractions for recording metrics [#1147](https://github.com/flipt-io/flipt/pull/1147).
- Dependency updates

## [v1.15.1](https://github.com/flipt-io/flipt/releases/tag/v1.15.1) - 2022-11-28

### Fixed

- Authentication API read operations have been appropriately mounted and no longer return 404.

## [v1.15.0](https://github.com/flipt-io/flipt/releases/tag/v1.15.0) - 2022-11-17

### Added

- Token-based authentication [#1097](https://github.com/flipt-io/flipt/pull/1097)

### Changed

- Linting for markdown
- Merge automation for dependabot updates
- Dependency updates

## [v1.14.0](https://github.com/flipt-io/flipt/releases/tag/v1.14.0) - 2022-11-02

### Added

- `reason` field in `EvaluationResponse` payload detailing why the request evaluated to the given result [#1099](https://github.com/flipt-io/flipt/pull/1099)

### Deprecated

- Deprecated both `db.migrations.path` and `db.migrations_path` [#1096](https://github.com/flipt-io/flipt/pull/1096)

### Fixed

- Propogating OpenTelemetry spans through Flipt [#1112](https://github.com/flipt-io/flipt/pull/1112)

## [v1.13.0](https://github.com/flipt-io/flipt/releases/tag/v1.13.0) - 2022-10-17

### Added

- Page token based pagination for `list` methods for forward compatibility with
  future versions of the API [#936](https://github.com/flipt-io/flipt/issues/936)
- Support for CockroachDB :tada: [#1064](https://github.com/flipt-io/flipt/pull/1064)

### Changed

- Validation for `list` methods now requires a `limit` if requesting with an `offset` or `page_token`
- Replaced OpenTracing with OpenTelemetry [#576](https://github.com/flipt-io/flipt/issues/576)
- Updated favicon to new logo
- Documentation link in app no longer uses redirects
- Dependency updates

### Deprecated

- Deprecated `offset` in `list` methods in favor of `page_token` [#936](https://github.com/flipt-io/flipt/issues/936)

### Fixed

- Correctly initialize shutdown context after interrupt [#1057](https://github.com/flipt-io/flipt/pull/1057)

### Removed

- Removed stacktrace from error logs [#1066](https://github.com/flipt-io/flipt/pull/1066)

## [v1.12.1](https://github.com/flipt-io/flipt/releases/tag/v1.12.1) - 2022-09-30

### Fixed

- Issue where parsing value with incorrect type would return 500 from the evaluation API [#1047](https://github.com/flipt-io/flipt/pull/1047)

### Changed

- Dependency updates
- Use testcontainers for MySQL/Postgres tests to run locally [#1045](https://github.com/flipt-io/flipt/pull/1045)

## [v1.12.0](https://github.com/flipt-io/flipt/releases/tag/v1.12.0) - 2022-09-22

### Added

- Ability to log as structure JSON [#1027](https://github.com/flipt-io/flipt/pull/1027)
- Ability to configure GRPC log level seperately from main service log level [#1029](https://github.com/flipt-io/flipt/pull/1029)

### Changed

- Configuration 'enums' are encoding correctly as JSON [#1030](https://github.com/flipt-io/flipt/pull/1030)
- Dependency updates

### Fixed

- Rendering of clone icon for variants/constraints [#1038](https://github.com/flipt-io/flipt/pull/1038)

## [v1.11.0](https://github.com/flipt-io/flipt/releases/tag/v1.11.0) - 2022-09-12

### Added

- Redis example [#968](https://github.com/flipt-io/flipt/pull/968)
- Support for arm64 builds [#1005](https://github.com/flipt-io/flipt/pull/1005)

### Changed

- Updated to Go 1.18 [#1016](https://github.com/flipt-io/flipt/pull/1016)
- Replaces Logrus with Zap logger [#1020](https://github.com/flipt-io/flipt/pull/1020)
- Updated Buf googleapis version [#1011](https://github.com/flipt-io/flipt/pull/1011)
- Dependency updates

## [v1.10.1](https://github.com/flipt-io/flipt/releases/tag/v1.10.1) - 2022-09-01

### Fixed

- (Ported from v1.9.1) Issue when not using `netgo` build tag during build, resulting in native dns resolution not working for some cases in k8s. See  [https://github.com/flipt-io/flipt/issues/993](https://github.com/flipt-io/flipt/issues/993).

## [v1.10.0](https://github.com/flipt-io/flipt/releases/tag/v1.10.0) - 2022-07-27

### Added

- Redis cache support :tada: [https://github.com/flipt-io/flipt/issues/633](https://github.com/flipt-io/flipt/issues/633)
- Support for pretty printing JSON responses from API (via ?pretty=true or setting `Accept: application/json+pretty` header)
- Configuration warnings/deprecations are displayed in console at startup

### Changed

- Ping database on startup to check if it's alive
- Default cache TTL is 1m. Previously there was no TTL for the in memory cache.
- Dependency updates

### Deprecated

- `cache.memory.enabled` config value is deprecated. See [Deprecations](DEPRECATIONS.md) for more info
- `cache.memory.expiration` config value is deprecated. See [Deprecations](DEPRECATIONS.md) for more info

### Fixed

- Build date was incorrect and always showed current date/time
- Button spacing issue on targeting page
- Docker compose examples run again after switch to non-root user 

## [v1.9.1](https://github.com/flipt-io/flipt/releases/tag/v1.9.1) - 2022-09-01

### Fixed

- Issue when not using `netgo` build tag during build, resulting in native dns resolution not working for some cases in k8s. See  [https://github.com/flipt-io/flipt/issues/993](https://github.com/flipt-io/flipt/issues/993).

## [v1.9.0](https://github.com/flipt-io/flipt/releases/tag/v1.9.0) - 2022-07-06

### Changed

- Module name changed to `go.flipt.io/flipt` [https://github.com/flipt-io/flipt/pull/898](https://github.com/flipt-io/flipt/pull/898)
- Upgraded NodeJS to v18 [https://github.com/flipt-io/flipt/pull/911](https://github.com/flipt-io/flipt/pull/911)
- Removed Yarn in favor of NPM [https://github.com/flipt-io/flipt/pull/916](https://github.com/flipt-io/flipt/pull/916)
- Switched to ViteJS for UI build instead of Webpack [https://github.com/flipt-io/flipt/pull/924](https://github.com/flipt-io/flipt/pull/924)
- All UI dependencies are now bundled as well, instead of pulling from external sources (e.g. FontAwesome) [https://github.com/flipt-io/flipt/pull/924](https://github.com/flipt-io/flipt/pull/924)
- Telemetry no longer outputs log messages in case of errors or in-ability to connect [https://github.com/flipt-io/flipt/pull/926](https://github.com/flipt-io/flipt/pull/926)
- Telemetry will not run in dev or snapshot mode [https://github.com/flipt-io/flipt/pull/926](https://github.com/flipt-io/flipt/pull/926)
- Dependency updates

## [v1.8.3](https://github.com/flipt-io/flipt/releases/tag/v1.8.3) - 2022-06-08

### Changed

- Re-added ability to create rules for flags without any variants [https://github.com/flipt-io/flipt/issues/874](https://github.com/flipt-io/flipt/issues/874)

## [v1.8.2](https://github.com/flipt-io/flipt/releases/tag/v1.8.2) - 2022-04-27

### Fixed

- Broken rules reordering resulting from GRPC update [https://github.com/flipt-io/flipt/pull/836](https://github.com/flipt-io/flipt/pull/836)

## [v1.8.1](https://github.com/flipt-io/flipt/releases/tag/v1.8.1) - 2022-04-18

### Changed

- Updated telemetry to not run if `CI` is set
- Updated telemtry to flush on each batch
- Dependency updates

### Fixed

- Update CORS middleware to handle Vary header properly [https://github.com/flipt-io/flipt/pull/803](https://github.com/flipt-io/flipt/pull/803)

## [v1.8.0](https://github.com/flipt-io/flipt/releases/tag/v1.8.0) - 2022-04-06

### Added

- Helm Chart [https://github.com/flipt-io/flipt/pull/777](https://github.com/flipt-io/flipt/pull/777)
- Basic anonymous telemetry [https://github.com/flipt-io/flipt/pull/790](https://github.com/flipt-io/flipt/pull/790). Can be disabled via config.

### Changed

- Updated protoc/protobuf to v1.28 [https://github.com/flipt-io/flipt/pull/768](https://github.com/flipt-io/flipt/pull/768)
- Updated CODE_OF_CONDUCT.md with my new email address
- Updated README.md with link to [Flipt Sandbox](https://try.flipt.io)
- Updated README.md with link to Discord

## [v1.7.0](https://github.com/flipt-io/flipt/releases/tag/v1.7.0) - 2022-03-22

### Added

- Ability to quickly copy constraints/variants for easier creation [https://github.com/flipt-io/flipt/pull/754](https://github.com/flipt-io/flipt/pull/754)

### Changed

- Disallow empty rule creation in UI [https://github.com/flipt-io/flipt/issues/758](https://github.com/flipt-io/flipt/issues/758)
- `trimpath` added as [`go build` flag](https://pkg.go.dev/cmd/go#hdr-Compile_packages_and_dependencies) for builds [https://github.com/flipt-io/flipt/pull/722](https://github.com/flipt-io/flipt/pull/722)
- Base alpine image updated to 3.15.1 [https://github.com/flipt-io/flipt/pull/757](https://github.com/flipt-io/flipt/pull/757)
- Dependency updates

## [v1.6.3](https://github.com/flipt-io/flipt/releases/tag/v1.6.3) - 2022-02-21

### Added

- Test for failure to increment expected migration versions [https://github.com/flipt-io/flipt/issues/706](https://github.com/flipt-io/flipt/issues/706)
- All dependency licenses [https://github.com/flipt-io/flipt/pull/714](https://github.com/flipt-io/flipt/pull/714)

### Changed

- Dependency updates

### Fixed

- Potential null pointer bugs in importer found by fuzzing [https://github.com/flipt-io/flipt/pull/713](https://github.com/flipt-io/flipt/pull/713)

## [v1.6.2](https://github.com/flipt-io/flipt/releases/tag/v1.6.2) - 2022-02-19

### Fixed

- Issue with missing Segment.MatchType in export [https://github.com/flipt-io/flipt/issues/710](https://github.com/flipt-io/flipt/issues/710)
- Issue with version not showing in UI (again)

## [v1.6.1](https://github.com/flipt-io/flipt/releases/tag/v1.6.1) - 2022-02-13

### Fixed

- Issue where migrations were not checked against latest version
- Issue where version was not showing in UI

## [v1.6.0](https://github.com/flipt-io/flipt/releases/tag/v1.6.0) - 2022-02-13

### Added

- Flipt now shows if there is an update available in the UI [https://github.com/flipt-io/flipt/pull/650](https://github.com/flipt-io/flipt/pull/650). Can be disabled via config.
- Variants now support JSON attachments :tada: ! [https://github.com/flipt-io/flipt/issues/188](https://github.com/flipt-io/flipt/issues/188)
- Import/Export of variant attachment JSON marshal as YAML for human readability [https://github.com/flipt-io/flipt/issues/697](https://github.com/flipt-io/flipt/issues/697)

### Changed

- Dependency updates
- Update JS to ES6 syntax
- Flipt now runs without root user in Docker [https://github.com/flipt-io/flipt/pull/659](https://github.com/flipt-io/flipt/pull/659)
- Changed development task runner to [Task](https://taskfile.dev/#/) from `make`
- Re-configured how Flipt is built in a [devcontainer](https://code.visualstudio.com/docs/remote/devcontainer-cli#_building-a-dev-container-image)

## [v1.5.1](https://github.com/flipt-io/flipt/releases/tag/v1.5.1) - 2022-01-26

### Fixed

- Backwards compatability issue with using `null` as a string field in the `context` map for `Evaluate`. [https://github.com/flipt-io/flipt/issues/664](https://github.com/flipt-io/flipt/issues/664)

## [v1.5.0](https://github.com/flipt-io/flipt/releases/tag/v1.5.0) - 2022-01-11

### Changed

- Dependency updates
- Upgrade UI packages and fix linter errors [https://github.com/flipt-io/flipt/pull/625](https://github.com/flipt-io/flipt/pull/625)
- Upgraded required nodeJS version to 16

## [v1.4.0](https://github.com/flipt-io/flipt/releases/tag/v1.4.0) - 2021-08-07

### Added

- Ability to exclude `NotFound` errors in `BatchEvaluate` calls [https://github.com/flipt-io/flipt/pull/518](https://github.com/flipt-io/flipt/pull/518)

### Changed

- Dependency updates
- Add commit hash to dev build [https://github.com/flipt-io/flipt/pull/517](https://github.com/flipt-io/flipt/pull/517)
- Remove `packr` in favor of using Go 1.16 `go embed` for embedding assets [https://github.com/flipt-io/flipt/pull/492](https://github.com/flipt-io/flipt/pull/492)
- Updated process to create new releases [https://github.com/flipt-io/flipt/pull/482](https://github.com/flipt-io/flipt/pull/482)

### Fixed

- Bug when trying to add two variants of a flag to the same rule in the UI [https://github.com/flipt-io/flipt/issues/515](https://github.com/flipt-io/flipt/issues/515)

## [v1.3.0](https://github.com/flipt-io/flipt/releases/tag/v1.3.0) - 2021-06-14

### Changed

- Bunch of dependencies updated.
- [Development](DEVELOPMENT.md) updated to work with VS Remote Containers / GH Codespaces.
- Development docker image changed to be Debian based.

### Fixed

- Segment search autocompletion now works correctly when defining a rule [https://github.com/flipt-io/flipt/issues/462](https://github.com/flipt-io/flipt/issues/462)

## [v1.2.1](https://github.com/flipt-io/flipt/releases/tag/v1.2.1) - 2021-03-09

### Fixed

- Downgrade Buefy dependency to fix [https://github.com/flipt-io/flipt/issues/394](https://github.com/flipt-io/flipt/issues/394) and [https://github.com/flipt-io/flipt/issues/391](https://github.com/flipt-io/flipt/issues/391)

## [v1.2.0](https://github.com/flipt-io/flipt/releases/tag/v1.2.0) - 2021-02-14 :heart:

### Changed

- Don't error on evaluating flags that are disabled, return no match instead [https://github.com/flipt-io/flipt/pull/382](https://github.com/flipt-io/flipt/pull/382)
- Dependency updates

## [v1.1.0](https://github.com/flipt-io/flipt/releases/tag/v1.1.0) - 2021-01-15

### Changed

- Bumped dependencies
- Ignore disabled flags on batch evaluate instead of erroring [https://github.com/flipt-io/flipt/pull/376](https://github.com/flipt-io/flipt/pull/376)

## [v1.0.0](https://github.com/flipt-io/flipt/releases/tag/v1.0.0) - 2020-10-31

Happy Halloween! Flipt goes 1.0.0 today! :jack_o_lantern:

### Changed

- Bumped dependencies
- Upgrade to Go 1.15

## [v0.18.1](https://github.com/flipt-io/flipt/releases/tag/v0.18.1) - 2020-09-30

### Added

- Reflection to grpc server for usage with generic clients [https://github.com/flipt-io/flipt/pull/345](https://github.com/flipt-io/flipt/pull/345)

### Changed

- Bumped dependencies
- Added colorful output for new version available instead of normal log message
- Publishing Docker images to [ghcr.io](https://docs.github.com/en/free-pro-team@latest/packages/getting-started-with-github-container-registry/about-github-container-registry)

## [v0.18.0](https://github.com/flipt-io/flipt/releases/tag/v0.18.0) - 2020-08-02

### Added

- Ability to configure database without using URL [https://github.com/flipt-io/flipt/issues/316](https://github.com/flipt-io/flipt/issues/316)

## [v0.17.1](https://github.com/flipt-io/flipt/releases/tag/v0.17.1) - 2020-07-16

### Fixed

- Don't log database url/credentials on startup [https://github.com/flipt-io/flipt/issues/319](https://github.com/flipt-io/flipt/issues/319)

## [v0.17.0](https://github.com/flipt-io/flipt/releases/tag/v0.17.0) - 2020-07-10

### Added

- Check for newer versions of Flipt on startup. Can be disabled by setting `meta.check_for_updates=false` in config. [https://github.com/flipt-io/flipt/pull/311](https://github.com/flipt-io/flipt/pull/311)
- Ability to configure database connections [https://github.com/flipt-io/flipt/pull/313](https://github.com/flipt-io/flipt/pull/313)
- Prometheus metrics around database connections [https://github.com/flipt-io/flipt/pull/314](https://github.com/flipt-io/flipt/pull/314)
- OpenTracing/Jaeger support [https://github.com/flipt-io/flipt/pull/315](https://github.com/flipt-io/flipt/pull/315)

### Changed

- Update FQDN for cache metrics

## [v0.16.1](https://github.com/flipt-io/flipt/releases/tag/v0.16.1) [Backport] - 2020-07-16

### Fixed

- Don't log database url/credentials on startup [https://github.com/flipt-io/flipt/issues/319](https://github.com/flipt-io/flipt/issues/319)

## [v0.16.0](https://github.com/flipt-io/flipt/releases/tag/v0.16.0) - 2020-06-29

### Added

- MySQL support: [https://github.com/flipt-io/flipt/issues/224](https://github.com/flipt-io/flipt/issues/224)

## [v0.15.0](https://github.com/flipt-io/flipt/releases/tag/v0.15.0) - 2020-06-03

### Added

- Batch Evaluation [https://github.com/flipt-io/flipt/issues/61](https://github.com/flipt-io/flipt/issues/61)

## [v0.14.1](https://github.com/flipt-io/flipt/releases/tag/v0.14.1) - 2020-05-27

### Changed

- Colons are no longer allowed in flag or segment keys [https://github.com/flipt-io/flipt/issues/262](https://github.com/flipt-io/flipt/issues/262)

## [v0.14.0](https://github.com/flipt-io/flipt/releases/tag/v0.14.0) - 2020-05-16

### Added

- Ability to import from STDIN [https://github.com/flipt-io/flipt/issues/278](https://github.com/flipt-io/flipt/issues/278)

### Changed

- Updated several dependencies

## [v0.13.1](https://github.com/flipt-io/flipt/releases/tag/v0.13.1) - 2020-04-05

### Added

- End to end UI tests [https://github.com/flipt-io/flipt/issues/216](https://github.com/flipt-io/flipt/issues/216)

### Changed

- Updated several dependencies

### Fixed

- Variant/Constraint columns always showing 'yes' in UI [https://github.com/flipt-io/flipt/issues/258](https://github.com/flipt-io/flipt/issues/258)

## [v0.13.0](https://github.com/flipt-io/flipt/releases/tag/v0.13.0) - 2020-03-01

### Added

- `export` and `import` commands to export and import data [https://github.com/flipt-io/flipt/issues/225](https://github.com/flipt-io/flipt/issues/225)
- Enable response time histogram metrics for Prometheus [https://github.com/flipt-io/flipt/pull/234](https://github.com/flipt-io/flipt/pull/234)

### Changed

- List calls are no longer cached because of pagination

### Fixed

- Issue where `GetRule` would not return proper error if rule did not exist

## [v0.12.1](https://github.com/flipt-io/flipt/releases/tag/v0.12.1) - 2020-02-18

### Fixed

- Issue where distributions did not always maintain order during evaluation when using Postgres [https://github.com/flipt-io/flipt/issues/229](https://github.com/flipt-io/flipt/issues/229)

## [v0.12.0](https://github.com/flipt-io/flipt/releases/tag/v0.12.0) - 2020-02-01

### Added

- Caching support for segments, rules AND evaluation! [https://github.com/flipt-io/flipt/issues/100](https://github.com/flipt-io/flipt/issues/100)
- `cache.memory.expiration` configuration option
- `cache.memory.eviction_interval` configuration option

### Changed

- Fixed documentation link in app
- Underlying caching library from golang-lru to go-cache

### Removed

- `cache.memory.items` configuration option

## [v0.11.1](https://github.com/flipt-io/flipt/releases/tag/v0.11.1) - 2020-01-28

### Changed

- Moved evaluation logic to be independent of datastore
- Updated several dependencies
- Moved documentation to [https://github.com/flipt-io/flipt.io](https://github.com/flipt-io/flipt.io)
- Updated documentation link in UI

### Fixed

- Potential index out of range issue with 0% distributions: [https://github.com/flipt-io/flipt/pull/213](https://github.com/flipt-io/flipt/pull/213)

## [v0.11.0](https://github.com/flipt-io/flipt/releases/tag/v0.11.0) - 2019-12-01

### Added

- Ability to match ANY constraints for a segment: [https://github.com/flipt-io/flipt/issues/180](https://github.com/flipt-io/flipt/issues/180)
- Pagination for Flag/Segment grids
- Required fields in API Swagger Documentation

### Changed

- All JSON fields in responses are returned, even empty ones
- Various UI Tweaks: [https://github.com/flipt-io/flipt/issues/190](https://github.com/flipt-io/flipt/issues/190)

## [v0.10.6](https://github.com/flipt-io/flipt/releases/tag/v0.10.6) - 2019-11-28

### Changed

- Require value for constraints unless operator is one of `[empty, not empty, present, not present]`

### Fixed

- Fix issue where != would evaluate to true if constraint value was not present: [https://github.com/flipt-io/flipt/pull/193](https://github.com/flipt-io/flipt/pull/193)

## [v0.10.5](https://github.com/flipt-io/flipt/releases/tag/v0.10.5) - 2019-11-25

### Added

- Evaluation benchmarks: [https://github.com/flipt-io/flipt/pull/185](https://github.com/flipt-io/flipt/pull/185)

### Changed

- Update UI dependencies: [https://github.com/flipt-io/flipt/pull/183](https://github.com/flipt-io/flipt/pull/183)
- Update go-sqlite3 version

### Fixed

- Calculate distribution percentages so they always add up to 100% in UI: [https://github.com/flipt-io/flipt/pull/189](https://github.com/flipt-io/flipt/pull/189)

## [v0.10.4](https://github.com/flipt-io/flipt/releases/tag/v0.10.4) - 2019-11-19

### Added

- Example using Prometheus for capturing metrics: [https://github.com/flipt-io/flipt/pull/178](https://github.com/flipt-io/flipt/pull/178)

### Changed

- Update Go versions to 1.13.4
- Update Makefile to only build assets on change
- Update go-sqlite3 version

### Fixed

- Remove extra dashes when auto-generating flag/segment key in UI: [https://github.com/flipt-io/flipt/pull/177](https://github.com/flipt-io/flipt/pull/177)

## [v0.10.3](https://github.com/flipt-io/flipt/releases/tag/v0.10.3) - 2019-11-15

### Changed

- Update swagger docs to be built completely from protobufs: [https://github.com/flipt-io/flipt/pull/175](https://github.com/flipt-io/flipt/pull/175)

### Fixed

- Handle flags/segments not found in UI: [https://github.com/flipt-io/flipt/pull/175](https://github.com/flipt-io/flipt/pull/175)

## [v0.10.2](https://github.com/flipt-io/flipt/releases/tag/v0.10.2) - 2019-11-11

### Changed

- Updated grpc and protobuf versions
- Updated spf13/viper version

### Fixed

- Update chi compress middleware to fix large number of memory allocations

## [v0.10.1](https://github.com/flipt-io/flipt/releases/tag/v0.10.1) - 2019-11-09

### Changed

- Use go 1.13 style errors
- Updated outdated JS dependencies
- Updated prometheus client version

### Fixed

- Inconsistent matching of rules: [https://github.com/flipt-io/flipt/issues/166](https://github.com/flipt-io/flipt/issues/166)

## [v0.10.0](https://github.com/flipt-io/flipt/releases/tag/v0.10.0) - 2019-10-20

### Added

- Ability to write logs to file instead of STDOUT: [https://github.com/flipt-io/flipt/issues/141](https://github.com/flipt-io/flipt/issues/141)

### Changed

- Automatically populate flag/segment key based on name: [https://github.com/flipt-io/flipt/pull/155](https://github.com/flipt-io/flipt/pull/155)

## [v0.9.0](https://github.com/flipt-io/flipt/releases/tag/v0.9.0) - 2019-10-02

### Added

- Support evaluating flags without variants: [https://github.com/flipt-io/flipt/issues/138](https://github.com/flipt-io/flipt/issues/138)

### Changed

- Dropped support for Go 1.12

### Fixed

- Segments not matching on all constraints: [https://github.com/flipt-io/flipt/issues/140](https://github.com/flipt-io/flipt/issues/140)
- Modal content streching to fit entire screen

## [v0.8.0](https://github.com/flipt-io/flipt/releases/tag/v0.8.0) - 2019-09-15

### Added

- HTTPS support

## [v0.7.1](https://github.com/flipt-io/flipt/releases/tag/v0.7.1) - 2019-07-25

### Added

- Exposed errors metrics via Prometheus

### Changed

- Updated JS dev dependencies
- Updated grpc and protobuf versions
- Updated pq version
- Updated go-sqlite3 version

## [v0.7.0](https://github.com/flipt-io/flipt/releases/tag/v0.7.0) - 2019-07-07

### Added

- CORS support with `cors` config options
- [Prometheus](https://prometheus.io/) metrics exposed at `/metrics`

## [v0.6.1](https://github.com/flipt-io/flipt/releases/tag/v0.6.1) - 2019-06-14

### Fixed

- Missing migrations folders in release archive: [https://github.com/flipt-io/flipt/issues/97](https://github.com/flipt-io/flipt/issues/97)

## [v0.6.0](https://github.com/flipt-io/flipt/releases/tag/v0.6.0) - 2019-06-10

### Added

- `migrate` subcommand to run database migrations
- 'Has Prefix' and 'Has Suffix' constraint operators

### Changed

- Variant keys are now only required to be unique per flag, not globally: [https://github.com/flipt-io/flipt/issues/87](https://github.com/flipt-io/flipt/issues/87)

### Removed

- `db.migrations.auto` in config. DB migrations must now be run explicitly with the `flipt migrate` command

## [v0.5.0](https://github.com/flipt-io/flipt/releases/tag/v0.5.0) - 2019-05-27

### Added

- Beta support for Postgres! :tada:
- `/meta/info` endpoint for version/build info
- `/meta/config` endpoint for running configuration info

### Changed

- `cache.enabled` config becomes `cache.memory.enabled`
- `cache.size` config becomes `cache.memory.items`
- `db.path` config becomes `db.url`

### Removed

- `db.name` in config

## [v0.4.2](https://github.com/flipt-io/flipt/releases/tag/v0.4.2) - 2019-05-12

### Fixed

- Segments with no constraints now match all requests by default: [https://github.com/flipt-io/flipt/issues/60](https://github.com/flipt-io/flipt/issues/60)
- Clear Debug Console response on error

## [v0.4.1](https://github.com/flipt-io/flipt/releases/tag/v0.4.1) - 2019-05-11

### Added

- `/debug/pprof` [pprof](https://golang.org/pkg/net/http/pprof/) endpoint for profiling

### Fixed

- Issue in evaluation: [https://github.com/flipt-io/flipt/issues/63](https://github.com/flipt-io/flipt/issues/63)

## [v0.4.0](https://github.com/flipt-io/flipt/releases/tag/v0.4.0) - 2019-04-06

### Added

- `ui` config section to allow disabling the ui:

  ```yaml
  ui:
    enabled: true
  ```

- `/health` HTTP healthcheck endpoint

### Fixed

- Issue where updating a Constraint or Variant via the UI would not show the update values until a refresh: [https://github.com/flipt-io/flipt/issues/43](https://github.com/flipt-io/flipt/issues/43)
- Potential IndexOutOfRange error if distribution percentage didn't add up to 100: [https://github.com/flipt-io/flipt/issues/42](https://github.com/flipt-io/flipt/issues/42)

## [v0.3.0](https://github.com/flipt-io/flipt/releases/tag/v0.3.0) - 2019-03-03

### Changed

- Renamed generated proto package to `flipt` for use with external GRPC clients
- Updated docs and example to reference [GRPC go client](https://github.com/flipt-io/flipt-grpc-go)

### Fixed

- Don't return error on graceful shutdown of HTTP server

## [v0.2.0](https://github.com/flipt-io/flipt/releases/tag/v0.2.0) - 2019-02-24

### Added

- `server` config section to consolidate and rename `host`, `api.port` and `backend.port`:

  ```yaml
  server:
    host: 127.0.0.1
    http_port: 8080
    grpc_port: 9000
  ```

- Implemented flag caching! Preliminary testing shows about a 10x speedup for retrieving flags with caching enabled. See the docs for more info.

  ```yaml
  cache:
    enabled: true
  ```

### Deprecated

- `host`, `api.port` and `backend.port`. These values have been moved and renamed under the `server` section and will be removed in the 1.0 release.

## [v0.1.0](https://github.com/flipt-io/flipt/releases/tag/v0.1.0) - 2019-02-19

### Added

- Moved proto/client code to proto directory and added MIT License

## [v0.0.0](https://github.com/flipt-io/flipt/releases/tag/v0.0.0) - 2019-02-16

Initial Release!

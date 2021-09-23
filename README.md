# radar-prmt-inhospital-deploy
> :warning: **Archived Repository**:

This is a submodule collection of RADAR-CNS pRMT repositories, for the purpose of aligned inhospital study setups/deployment.
It can also be used to set up a locally editable and compilable codebase of the pRMT app, for development.

## Setup
Clone this repositroy with:
- `git clone --recurse-submodules https://github.com/RADAR-base/radar-prmt-inhospital-deploy.git`

Or if you already cloned:
- `git submodule init`
- `git submodule update`

### Config and installation
- In `radar-prmt-android/settings.gradle` remove all unnecessary device plugins. For the remaining `projectDir`s change the file path to the correct one (absolute path).
- In `radar-prmt-android/app/src/main/res/xml/remote_config_defaults.xml`:
  - provide the Empatica API key if needed.
  - leave `management_portal_url` empty if the MP is bypassed.
  - provide URLs for `kafka_rest_proxy_url` and `schema_registry_url`.
  - edit `device_services_to_connect` as needed.
  - provide `ntp_server` as needed.
- Provide `google-services.json` in `radar-prmt-android/app/`.
- Change directory into `RADAR-Schemas/java-sdk/radar-schemas-commons` and execute `../gradlew build`.
- In `radar-commons-android/build.gradle:112` change the path of the generated schema sources to the correct one.
- If needed, provide external libraries (`.aar`) for the plugins, in the respective plugins' `libs/` directory, and in `radar-prmt-android/app/libs/`

## Revisions
Submodule revision info in this repository.

| DIR                                 | BRANCH                     | ORIGIN                                                  | REV     |
|-------------------------------------|----------------------------|---------------------------------------------------------|---------|
| ./RADAR-Docker                      | dev                        | github.com/RADAR-base/RADAR-Docker                      | 185438e |
| ./RADAR-Schemas                     | dev                        | github.com/RADAR-base/RADAR-Schemas                     | 63431a1 |
| ./radar-android-application-status  | deploy/dev                 | github.com/RADAR-base/radar-android-application-status  | 0deac16 |
| ./radar-android-biovotion           | deploy/dev                 | github.com/RADAR-base/radar-android-biovotion           | 10e701f |
| ./radar-android-eegsync             | deploy/dev                 | github.com/sboettcher/radar-android-eegsync             | d986b60 |
| ./radar-android-empatica            | deploy/dev                 | github.com/RADAR-base/radar-android-empatica            | 6c40f04 |
| ./radar-android-phone               | deploy/dev                 | github.com/RADAR-base/radar-android-phone               | 94a1ffe |
| ./radar-commons                     | deploy/dev                 | github.com/RADAR-base/radar-commons                     | 7f37cb3 |
| ./radar-commons-android             | deploy/dev                 | github.com/RADAR-base/radar-commons-android             | bffab85 |
| ./radar-prmt-android                | deploy/trivial_login       | github.com/RADAR-base/radar-prmt-android                | 1952673 |

## Changelog to base branches
...

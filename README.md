# radar-prmt-inhospital
This is a hardcopy collection of RADAR-CNS pRMT repositories, for the purpose of aligned inhospital study setups.
It can also be used to set up a locally editable and compilable codebase of the pRMT app, for development.

## TODO to make it work
- In `RADAR-AndroidApplication/settings.gradle` remove all unnecessary device plugins. For the remaining `projectDir`s change the file path to the correct one (absolute path).
- In `RADAR-AndroidApplication/app/src/main/res/xml/remote_config_defaults.xml`:
  - provide the Empatica API key if needed.
  - leave `management_portal_url` empty if the MP is bypassed.
  - provide URLs for `kafka_rest_proxy_url` and `schema_registry_url`.
  - edit `device_services_to_connect` as needed.
  - provide `ntp_server` as needed.
- Change directory into `RADAR-Schemas/java-sdk/radar-schemas-commons` and execute `../gradlew build`.
- In `RADAR-Commons-Android/build.gradle:112` change the path of the generated schema sources to the correct one.
- If needed, provide external libraries (`.aar`) for the plugins, in the respective plugins' `libs/` directory, and in `RADAR-AndroidApplication/app/libs/`

## Revisions
These are the base revisions of the original repositories, however there may be local changes that are not present in the origins.

| DIR                                 | BRANCH                     | ORIGIN                                                 | REV     |
|-------------------------------------|----------------------------|--------------------------------------------------------|---------|
| ./[RADAR-AndroidApplication](https://github.com/RADAR-CNS/radar-prmt-android/tree/trivial_login)          | On branch trivial_login    | github.com/RADAR-CNS/RADAR-AndroidApplication          | ff1d8a4 |
| ./[RADAR-Android-Application-Status](https://github.com/RADAR-CNS/radar-android-application-status/tree/dev)  | On branch dev              | github.com/RADAR-CNS/RADAR-Android-Application-Status  | 0343188 |
| ./[RADAR-Android-Biovotion](https://github.com/RADAR-CNS/radar-android-biovotion/tree/gap_restructure)           | On branch gap_restructure  | github.com/RADAR-CNS/RADAR-Android-Biovotion           | 86261c8 |
| ./[RADAR-Android-Empatica](https://github.com/RADAR-CNS/radar-android-empatica/tree/dev)            | On branch dev              | github.com/RADAR-CNS/RADAR-Android-Empatica            | da99d2b |
| ./[RADAR-Android-EEGsync](https://github.com/sboettcher/RADAR-Android-EEGsync/tree/dev)             | On branch dev              | github.com/sboettcher/RADAR-Android-EEGsync            | 126cf6a |
| ./[RADAR-Android-Phone](https://github.com/RADAR-CNS/radar-android-phone/tree/dev)               | On branch dev              | github.com/RADAR-CNS/RADAR-Android-Phone               | 2170faf |
| ./[RADAR-Commons](https://github.com/RADAR-CNS/radar-commons/tree/dev)                     | On branch dev              | github.com/RADAR-CNS/RADAR-Commons                     | d92c038 |
| ./[RADAR-Commons-Android](https://github.com/RADAR-CNS/radar-commons-android/tree/dev)             | On branch dev              | github.com/RADAR-CNS/RADAR-Commons-Android             | 8dd9d79 |
| ./[RADAR-Schemas](https://github.com/sboettcher/RADAR-Schemas/tree/eegsync)                     | On branch eegsync          | github.com/sboettcher/RADAR-Schemas                    | d9cba17 |

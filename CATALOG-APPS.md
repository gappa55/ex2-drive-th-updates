# APK catalog provenance and vehicle test results

Updated 21 September 2026. Vehicle: Geely EX2, IHU629G, Android 9 / API 28.
The vehicle owner reported installation and use; no independent long-duration
playback test or compatibility guarantee for other head-unit firmware is implied.

## MicroG RE 7.1.1

The vehicle owner subsequently confirmed that MicroG RE 7.1.1 works with
YouTube ReVanced on their Geely EX2. Its catalog status is now `owner_verified`.
The exact APK, version, package and signer remain unchanged. This does not
claim compatibility with every patched application or resolve the separate
Morphe freezing report.

## VIU 2.29.0

- Package: `com.viu.phone`; version code `845`; minimum API `25`.
- Original APK, with the PCCW signing certificate retained.
- Source: [APKPure 2.29.0](https://apkpure.net/viu-korean-asian-content/com.viu.phone/download/2.29.0).
- Hash/signing certificate cross-check: [APKMirror 2.29.0](https://www.apkmirror.com/apk/pccw-ott-hong-kong-limited/viu/viu-korean-asian-content-2-29-0-release/viu-korean-asian-content-2-29-0-android-apk-download/).
- Bytes: `27168483`.
- SHA-256: `b4dc5da57d77c9d7ee4f8bc97c995b7a866b2bbf42906ff56a952b3a18cdc275`.
- Signing certificate SHA-256: `d178494ab6e7900f05053d141db954af16bf46f36f3ada08a1ac08b2b1beb7a5`.
- Owner result: installs and works on the vehicle. Added as `owner_verified`.

## YouTube ReVanced 21.13.164 (vanced.to)

- Package: `app.revanced.android.youtube`; version code `1561063732`; minimum API `28`.
- Source: [vanced.to YouTube ReVanced](https://vanced.to/youtube-revanced), [exact upstream release APK](https://github.com/vancedto/vanced.to/releases/download/2026-37/vanced.to_revanced_com.google.android.youtube_arm64v8a_v21.13.164_cli6.0.0_p6.2.0_c6507b5051.apk).
- Third-party patched APK; the EX2 project has not changed or re-signed it.
- Bytes: `194073693`.
- SHA-256: `ab23bb8ff35f6fcb59c2af5910a3b96bc2f6ca53cbfe96c9054f723affa2173f`.
- Signing certificate SHA-256: `5d87c9bdc8e368dcf80971f33455db4c2e7dd754e1f288f1162c04b2a4811708`.
- Requires `app.revanced.android.gms`; install MicroG RE 7.1.1 from the catalog first.
- Owner result: works on the vehicle. Added as `owner_verified`.
- This is ReVanced, not the separate `app.morphe.android.youtube` package.

## Other reported test results

| App/build tested | Vehicle-owner result | Catalog decision |
| --- | --- | --- |
| Google Maps 26.36.05 patched for MicroG | Opens then crashes | Not included |
| Netflix, latest supplied test APK 9.84.0 | Installs but cannot be used; screen says the app cannot work with this device | Not included |
| Earlier YouTube Morphe 21.13.164 | Entire app freezes after some use | Not included |

These outcomes do not establish a specific crash, DRM, or firmware cause.
Netflix version is identified by the supplied test set; the reported screenshot
does not independently show its version. Morphe 21.16.256 remains unverified.

All catalog entries require exact file size, SHA-256, package/version, minimum
API and signing-certificate checks before installation. Refreshing this
catalog does not install apps or alter the EX2 OTA version.

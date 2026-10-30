# APK catalog provenance and vehicle test results

**Current active catalog — 30 October 2026:** the five recent entries (Google Maps 26.12.07.884026066; YouTube (Google) 21.04.223; YouTube Music (Google) 9.15.51; microG Services 0.3.13.250932; Duo Split / PiP (Android 9 test) 1.0-a9-test5) have been withdrawn at the owner's request. The owner reported Duo did not work in their test and asked to remove these entries. The active catalog contains only Spotify, MicroG RE, VIU, YouTube ReVanced, Dooseries, and CarFlix. The dated sections below retain historical provenance and emulator results; their earlier descriptions of active listings are superseded by this withdrawal.

Updated 30 October 2026. Vehicle: Geely EX2, IHU629G, Android 9 / API 28.
Historical owner-reported results apply only to their named builds. New entries
below remain unverified unless explicitly stated; no independent long-duration
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

## Dooseries 2.2.0

- Package: `com.gappa.dooseries`; version code `31`; minimum API `24`.
- Source: exact `app-release.apk` supplied by the vehicle owner for this catalog.
- Native ABIs: `arm64-v8a`, `armeabi-v7a`, `x86_64`.
- Bytes: `105638481`.
- SHA-256: `41ec1f837147ccd4090bb8602ef118f02e4367f7c67b2b925fedd6a7499c9df1`.
- Signing certificate SHA-256: `b4eef346b6658be7ba724c99810a302333e842cf71e718c7b356141e77acfa90`.
- Android API 28 signature verification passed using the original APK v2 signature.
- Vehicle owner explicitly confirmed installation and use on Geely EX2; status `owner_verified`.
- The APK bytes, signing identity, and embedded notices are preserved without patching or re-signing.

## CarFlix 1.0.1 (added 27 September 2026)

- Package: `com.gappa.carflix`; version code `2002`; minimum API `24`.
- Source: the owner's CarFlix project, [commit `20b4bb9`](https://github.com/gappa55/carflix/commit/20b4bb9) on `codex/carflix-pip-audit` (private source repository).
- Native ABI: `arm64-v8a` only.
- Bytes: `35825058`.
- SHA-256: `1f2441f7ee4863875b67a95c704324f645cc8d319ff83de23295e730bd216731`.
- Signing certificate SHA-256: `b4eef346b6658be7ba724c99810a302333e842cf71e718c7b356141e77acfa90`.
- Android API 28 signature verification passed for these exact APK bytes.
- Prepublication validation: clean Flutter analysis, 33 Flutter tests, four native PiP tests, and one FVP Android 9 integration test passed.
- Android 9 emulator checks passed fullscreen return to the same task, pause/resume, and two reopen/PiP/close cycles in one process with native AAudio resources removed after each close. The FVP integration check covered real decode, seek, native PiP, playback progression and disposal. These are emulator results, not vehicle playback or PiP verification.
- The owner reports CarFlix is installed on their Geely EX2; status `installation_only`.
- That report does not verify installation of this newly built APK, playback, or PiP on the vehicle. Those still require testing of this release on the actual head unit.
- CarFlix and Dooseries have different package names. The Dooseries entry remains unchanged.

## Requested original APK versions (30 October 2026)

The owner requested the versions visible in their reference image and explicitly selected original Google APKs for YouTube and YouTube Music. Google Maps was identified as `26.12.07.884026066` from the visible version prefix. The microG version is the standard upstream `0.3.13.250932`, not the differently numbered Vanced or MicroG RE packages.

All four new entries are `unverified`, with an empty `verifiedOn`. This records verification of the files and Android API 28 signing metadata only. No installation, Google sign-in, GPS, navigation, or playback result on the vehicle is claimed. Earlier tested catalog entries retain their identities and owner-reported statuses. In particular, the failed earlier Maps test concerns the patched **26.36.05** build, not this original **26.12.07.884026066** build.

### Google Maps 26.12.07.884026066

- Package: `com.google.android.apps.maps`; version code `1068495411`; minimum API `28`.
- Native ABIs: `arm64-v8a, armeabi-v7a, x86, x86_64`.
- Source: [download source](https://www.apkmirror.com/apk/google-inc/maps/google-maps-26-12-07-884026066-release/google-maps-26-12-07-884026066-3-android-apk-download/).
- Bytes: `235996473`.
- SHA-256: `71964631fda366a04a778fa9bfea576021535fcde6c37190160d677bca000f7c`.
- API 28 signing certificate SHA-256: `f0fd6c5b410f25cb25c3b53346c8972fae30f8ee7411df910480ad6b2d60db83`.
- Original standalone APK, with no required split modules. ZIP CRC and API 28 signature verification passed. The original bytes and embedded notices are preserved without patching or re-signing.
- Catalog asset: [google-maps-26.12.07.884026066-original.apk](https://github.com/gappa55/ex2-drive-th-updates/releases/download/catalog-v1/google-maps-26.12.07.884026066-original.apk).

### YouTube (Google) 21.04.223

- Package: `com.google.android.youtube`; version code `1561052632`; minimum API `28`.
- Native ABIs: `arm64-v8a, armeabi-v7a, x86, x86_64`.
- Source: [download source](https://apkpure.net/youtube-app/com.google.android.youtube/download/21.04.223).
- Cross-check: [release metadata and file hash](https://www.apkmirror.com/apk/google-inc/youtube/youtube-21-04-223-release/youtube-21-04-223-android-apk-download/).
- Bytes: `171814203`.
- SHA-256: `78571be679f586d11a4e56fb1ce6bf9dfd958ce6b8af786c4a3bd94792ce8c7c`.
- API 28 signing certificate SHA-256: `3d7a1223019aa39d9ea0e3436ab7c0896bfb4fb679f4de5fe7c23f326c8f994a`.
- Original standalone APK, with no required split modules. ZIP CRC and API 28 signature verification passed. The original bytes and embedded notices are preserved without patching or re-signing.
- Catalog asset: [youtube-21.04.223-google-original.apk](https://github.com/gappa55/ex2-drive-th-updates/releases/download/catalog-v1/youtube-21.04.223-google-original.apk).

### YouTube Music (Google) 9.15.51

- Package: `com.google.android.apps.youtube.music`; version code `91551240`; minimum API `26`.
- Native ABIs: `arm64-v8a`.
- Source: [download source](https://archive.org/download/jhc-apks/apks/com.google.android.apps.youtube.music/com.google.android.apps.youtube.music-9.15.51-arm64-v8a.apk).
- Cross-check: [release metadata and file hash](https://www.apkmirror.com/apk/google-inc/youtube-music/youtube-music-9-15-51-release/youtube-music-9-15-51-4-android-apk-download/).
- Bytes: `74431248`.
- SHA-256: `a003ac2e673c2979b2268e5acfbfd74f88b93c4b75af5c7d604b3c7fb92768a4`.
- API 28 signing certificate SHA-256: `a2a1ad7ba7f41dfca4514e2afeb90691719af6d0fdbed4b09bbf0ed897701ceb`.
- Original standalone APK, with no required split modules. ZIP CRC and API 28 signature verification passed. The original bytes and embedded notices are preserved without patching or re-signing.
- Catalog asset: [youtube-music-9.15.51-google-arm64-v8a.apk](https://github.com/gappa55/ex2-drive-th-updates/releases/download/catalog-v1/youtube-music-9.15.51-google-arm64-v8a.apk).

### microG Services 0.3.13.250932

- Package: `com.google.android.gms`; version code `250932026`; minimum API `19`.
- Native ABIs: `arm64-v8a, armeabi-v7a, x86, x86_64`.
- Source: [download source](https://github.com/microg/GmsCore/releases/download/v0.3.13.250932/com.google.android.gms-250932026.apk).
- Cross-check: [release metadata and file hash](https://github.com/microg/GmsCore/releases/tag/v0.3.13.250932).
- Bytes: `105575757`.
- SHA-256: `32eb051bee23caeff9dff9ea2f0c2e2de5dbc260daea7e9496a9cd1d7dd7ad77`.
- API 28 signing certificate SHA-256: `9bd06727e62796c0130eb6dab39b73157451582cbd138e86c468acc395d14165`.
- Original standalone APK, with no required split modules. ZIP CRC and API 28 signature verification passed. The original bytes and embedded notices are preserved without patching or re-signing.
- Catalog asset: [microg-0.3.13.250932-original.apk](https://github.com/gappa55/ex2-drive-th-updates/releases/download/catalog-v1/microg-0.3.13.250932-original.apk).

YouTube Music carries platform-dependent signing-key rotation. The catalog pins its API 28 signer (`a2a1ad7ba7f41dfca4514e2afeb90691719af6d0fdbed4b09bbf0ed897701ceb`) for the Android 9 target; a newer Android platform may report a different current signer. This does not justify relaxing signature checks.

Standard microG uses `com.google.android.gms`, is signed by the microG developer, and requires compatible firmware with microG/signature-spoofing support for full functionality. Its manifest also requires the `com.android.location.provider` library. The catalog does not modify firmware or enable signature spoofing. It is separate from the existing `app.revanced.android.gms` MicroG RE entry. Copyright 2013–2025 microG Project Team; Apache License 2.0. The upstream license is attached to the catalog release as `microG-0.3.13.250932-LICENSE.txt`; embedded notices remain unchanged.

## Duo Split / PiP 1.0 test APK (30 October 2026)

The vehicle owner supplied `Duo-split-pip-testkey.apk` and explicitly requested that it be listed for their own installation testing. Status is `unverified` with empty `verifiedOn`; no installation or operation on Geely EX2 is claimed.

- Package: `com.yahooeu2k.ex5.split`; version `1.0`; version code `1`.
- Minimum API: `30` (Android 11); target API: `33`. This requirement is preserved from the original manifest.
- Bytes: `115615`.
- APK SHA-256: `e204c6070f8555c9e3bad823efc01c5f9046750ad92d41d91b2da4ad66d8a49d`.
- Signing certificate SHA-256: `a40da80a59d170caa950cf15c18c454d47a39b26989d8b640ecd745ba71bf5dc` (AOSP testkey). This signing identity does not confer Geely platform privileges.
- Source: exact owner-supplied APK; no matching Android source repository is established. The separately supplied `morluto/rea` link describes an analysis toolkit, not Duo source.
- Asset: [duo-split-pip-1.0-testkey.apk](https://github.com/gappa55/ex2-drive-th-updates/releases/download/catalog-v1/duo-split-pip-1.0-testkey.apk).
- The original bytes, manifest, signing identity and embedded notices are preserved without patching or re-signing. Standalone manifest, ZIP CRC and cryptographic signature verification for API 30 passed.
- The code implements two-app split screen and up to three floating windows using virtual displays. It depends on a compatible root/bridge environment and includes Accessibility/overlay setup commands; these paths were not executed during analysis.
- On Android 9/API 28 the existing EX2 catalog displays the entry as requiring a newer Android version and disables downloading. No compatibility or installation guard is overridden. A direct release download is available for the owner's separate testing.

## Duo Android 9 experimental port 1.0-a9-test5 (30 October 2026)

The owner asked to decode their Duo APK and try an Android 9 port after requesting its inclusion in this catalog. The active `duo-split-pip` entry now points to this experimental port, replacing the original Android 11-only entry. The original `duo-split-pip-1.0-testkey.apk` asset remains available. Other app entries are unchanged.

- Package: `com.yahooeu2k.ex5.split`; version `1.0-a9-test5`; version code `6`.
- Minimum API: `28` (Android 9); target API: `33`.
- Bytes: `132133`.
- SHA-256: `f62a045e4c70ab2042d31609c94c1ff74ba1fa8fefbabf0103cc46e097ca3781`.
- API 28 signing certificate SHA-256: `a40da80a59d170caa950cf15c18c454d47a39b26989d8b640ecd745ba71bf5dc`.
- Asset: [duo-split-pip-1.0-a9-test5.apk](https://github.com/gappa55/ex2-drive-th-updates/releases/download/catalog-v1/duo-split-pip-1.0-a9-test5.apk).
- Derived from the exact owner-supplied Duo 1.0 APK, SHA-256 `e204c6070f8555c9e3bad823efc01c5f9046750ad92d41d91b2da4ad66d8a49d`. The source snapshot is preserved. This port is modified and rebuilt; it is not the original upstream binary. No matching original source repository has been established.
- Signed with the intentionally public AOSP testkey identity used by the original, allowing a same-package test update. It is not a Geely platform signing key and does not itself grant root or system UID.

### Port changes

API 28 fallbacks replace newer window-metrics/window-context/insets calls, while newer APIs remain behind version guards. Virtual-display creation uses the Android 9 API. Touch events use an Android 9 `IInputForwarder` for the exact destination display; no default-display input fallback is used.

The system-UID display daemon delivers its Binder through an app ContentProvider using a scoped external-provider publisher. The provider accepts UID 1000 only, validates the installed-APK token and a live Binder, and exposes no data query or Binder retrieval operation. The temporary publisher has a bounded lifetime, with external-provider leases released on process exit. No SELinux policy or signature check is relaxed.

On API 28, application tasks are created without bringing them to the front, selected by package and Android user, moved to the chosen display, and focused by task ID. This avoids the Android 9 shell-start behavior that could return a fresh task to the main display. Root bootstrap retains the original GMW route and adds bounded fallback to an existing `su` implementation; it does not install or grant root.

### Verification and limits

The exact published test5 APK passes ZIP CRC, standalone manifest, package/version/minSdk, SHA-256 and API 28 cryptographic signature checks. A read-only Android 9/API 28 arm64 emulator at 1920x1080 installed the APK, launched two cold tasks from the real split picker directly onto separate displays, and accepted forwarded button clicks in both apps. A cold PiP smoke test rendered an app on its virtual display and accepted a forwarded button click. Cleanup left zero virtual displays; SELinux remained enforcing.

The unchanged display/PiP backend was also tested in test3 for divider resizing, floating-window resize/drag, the three-window limit, replacement of the oldest window, close/reopen with saved dimensions, and owner-death cleanup. A shell UID 2000 attempt to publish a fake Binder was rejected before state changed; the provider guard is unchanged in test5.

**Root setup is still a real limitation.** The emulator rejects `su` execution by an ordinary app. For runtime validation, the app-generated authenticated root starter was launched from the emulator's already-authorized host ADB root route. This validates the application and display protocol with a prepared root bridge, not automatic root bootstrap on a vehicle. No vehicle was connected, and no actual vehicle installation, root startup, keyboard/IME, media/DRM, or long-duration operation is verified. Android 9 has no corresponding per-display IME switch in this port.

Catalog status remains `unverified`, with empty `verifiedOn`. Refreshing the catalog does not install the APK or update EX2 Drive TH.

## Withdrawal of recent test entries (30 October 2026)

Removed from `catalog.json` at the owner's explicit request:

- `google-maps`: Google Maps 26.12.07.884026066 (`com.google.android.apps.maps`).
- `youtube-google`: YouTube (Google) 21.04.223 (`com.google.android.youtube`).
- `youtube-music-google`: YouTube Music (Google) 9.15.51 (`com.google.android.apps.youtube.music`).
- `microg-services`: microG Services 0.3.13.250932 (`com.google.android.gms`).
- `duo-split-pip`: Duo Split / PiP (Android 9 test) 1.0-a9-test5 (`com.yahooeu2k.ex5.split`).

The owner reported Duo unusable on their vehicle and requested removal of the other four recent entries as well. No specific firmware, root, Google-services, GPS, or playback failure cause is inferred from that report. Prior emulator results do not establish compatibility on the physical vehicle. Historical APK artifacts and provenance are retained; none of these five is offered by the active catalog. This catalog change does not uninstall apps from a device.

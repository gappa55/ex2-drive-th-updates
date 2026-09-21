# Third-party assets and notices

Application code is GPLv3. Third-party assets retain their own rights; approval to publish this release does not change their licensing. These notes record the source provenance available in the project.

## Recorded provenance

- Unitext Regular: repository provenance identifies Monotype proprietary licensing;
  no redistribution grant is recorded. The font remains bundled in the APK.
- Adapted reference icons: some sources have no stated license; cppqtdev/Tesla MIT
  notice applies only to assets from that specific MIT-licensed reference.
- Geely vehicle renders: manufacturer-source downloads without a recorded
  redistribution license. The vehicle renders remain bundled in the APK.
- itim.wav / nacom.wav: user-supplied audio remains bundled; no public redistribution
  rights were supplied in the repository. Do not assume the GPL code license covers it.
- Noto Sans Thai: SIL OFL notice is bundled with the application assets.
- Hand-written android.car stubs: Apache-2.0 per their README; no extracted Geely
  framework jar is included. Main Gradle uses these as compileOnly.
- Paho 1.2.5 JAR is a tracked build dependency with upstream about.html inside it;
  MPAndroidChart v3.1.0 is fetched via JitPack. Review their source/notices obligations
  before treating this candidate as the final public distribution package.


## APK catalog: MicroG RE 7.1.1

The separate catalog includes the unmodified arm64-v8a APK from
[MorpheApp/MicroG-RE release 7.1.1](https://github.com/MorpheApp/MicroG-RE/releases/tag/7.1.1).
It retains the original signing certificate and embedded notices. The upstream
project is Apache-2.0; the [license copy](https://github.com/gappa55/ex2-drive-th-updates/releases/download/catalog-v1/MicroG-RE-7.1.1-LICENSE.txt)
is available beside the catalog APK. This project is not affiliated with MorpheApp.
Vehicle-owner verification of MicroG covers installation. YouTube ReVanced
21.13.164 has since been reported working; the earlier Morphe freezing is a
separate unresolved test result.

## APK catalog: VIU and YouTube ReVanced

VIU 2.29.0 is the original PCCW-signed APK, downloaded from APKPure with the
file hash and signing certificate cross-checked against APKMirror. YouTube
ReVanced 21.13.164 is a third-party prebuilt APK distributed by vanced.to, not
an official Google YouTube APK. Neither APK has been changed or re-signed by
EX2 Drive TH. Their embedded notices and original ownership are retained;
they are not relicensed under the EX2 application code license.

See [CATALOG-APPS.md](CATALOG-APPS.md) for exact provenance, versions, hashes,
signing certificates, and vehicle-owner test scope. This project is not
affiliated with PCCW/VIU, Google/YouTube, ReVanced, or vanced.to.

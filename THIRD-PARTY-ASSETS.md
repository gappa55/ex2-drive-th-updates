# Third-party assets and build credentials

Application code is GPLv3. Third-party assets retain their own rights; approval to publish this release does not change their licensing. These notes record the source provenance available in the project.

## Recorded provenance

- Unitext Regular: repository provenance identifies Monotype proprietary licensing;
  no redistribution grant is recorded. The unchanged font is in both APK and source.
- Adapted reference icons: some sources have no stated license; cppqtdev/Tesla MIT
  notice applies only to assets from that specific MIT-licensed reference.
- Geely vehicle renders: manufacturer-source downloads without a recorded
  redistribution license. They remain present so source matches the APK inputs.
- itim.wav / nacom.wav: user-supplied audio remains bundled; no public redistribution
  rights were supplied in the repository. Do not assume the GPL code license covers it.
- Noto Sans Thai: SIL OFL notice is included in source assets.
- Hand-written android.car stubs: Apache-2.0 per their README; no extracted Geely
  framework jar is included. Main Gradle uses these as compileOnly.
- Paho 1.2.5 JAR is a tracked build dependency with upstream about.html inside it;
  MPAndroidChart v3.1.0 is fetched via JitPack. Review their source/notices obligations
  before treating this candidate as the final public distribution package.
- Helper/Setup build scripts retain their public AOSP platform test-key fallback
  literals. No production main-app signing key is included.


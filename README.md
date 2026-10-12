# pool-aim-assistant

Android billiards practice overlay.

## Build
Every push to `main` runs the **Build APK** GitHub Actions workflow. It builds a debug APK and uploads it as the `pool-aim-assistant-debug-apk` artifact, along with source diagnostics.

Open the [Actions page](https://github.com/alihlyhel50/pool-aim-assistant/actions) to inspect the build result and download artifacts after a successful run.

## Current limitations
The overlay uses manually positioned markers. Automatic ball detection, continuous screen analysis, and validated shot-success probabilities are not implemented yet. Treat angle/difficulty hints as geometry estimates, not guarantees.

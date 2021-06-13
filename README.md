# LineageOS

### How to build ###

```bash
# Create dirs
$ mkdir lineage ; cd lineage

# Init repo
$ repo init --depth=1 -u https://github.com/LineageOS/android.git -b lineage-17.1

# Clone my local repo
$ git clone https://github.com/homay84/android_manifest_samsung_j7y17lte.git -b lineage-17.1 .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ . build/envsetup.sh && lunch lineage_j7y17lte-userdebug && mka clean && mka api-stubs-docs && mka hiddenapi-lists-docs && mka system-api-stubs-docs && mka test-api-stubs-docs && mka bacon -j`nproc`
```

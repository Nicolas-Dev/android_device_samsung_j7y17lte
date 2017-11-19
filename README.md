Device configuration for the Samsung Galaxy Tab A

Copyright (C) 2017 The LineageOS Project
Copyright (C) 2017 Valera Chigir <valera1978@tut.by>

 Licensed under the Apache License, Version 2.0 (the "License");
 you may not use this file except in compliance with the License.
 You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

------------------------------------------------------------------

* Description

  Ce référentiel est pour LineageOS sur Samsung Galaxy Tab A (gtaxllte)

* Comment construire LineageOS pour Samsung Galaxy Tab A

  - Faire un espace de travail

mkdir cm14
cd cm14

  - Do repo init & sync

repo init -u git://github.com/LineageOS/android.git -b cm-14.1

Créer  -  .repo/local_manifests/roomservice.xml with the following content:

```
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
  <project name="Valera1978/android_device_samsung_gtaxllte" path="device/samsung/gtaxllte" remote="github" />
  <project name="Valera1978/android_kernel_samsung_exynos7870" path="kernel/samsung/exynos7870" remote="github" revision="cm-14.1_perm" />
  <project name="Valera1978/android_vendor_samsung_gtaxllte" path="vendor/samsung/gtaxllte" remote="github" />
  <project name="Valera1978/android_hardware_samsung_slsi-cm_exynos" path="hardware/samsung_slsi-cm/exynos" remote="github" />
  <project name="Valera1978/android_hardware_samsung_slsi-cm_exynos7870" path="hardware/samsung_slsi-cm/exynos7870" remote="github" />
  <project name="LineageOS/android_external_stlport" path="external/stlport" remote="github" />
  <project name="LineageOS/android_hardware_samsung" path="hardware/samsung" remote="github" />
  <project name="LineageOS/android_hardware_samsung_slsi-cm_exynos5" path="hardware/samsung_slsi-cm/exynos5" remote="github" />
  <project name="LineageOS/android_hardware_samsung_slsi-cm_openmax" path="hardware/samsung_slsi-cm/openmax" remote="github" />
</manifest>
```

repo sync

  - Copier les fichiers propriétaires du fournisseur

Il y a deux options à cela. Connectez votre appareil avec adb activé et exécutez:

./extract-files.sh

Ou si vous avez décompressé l'image du système sur votre disque, lancez simplement:

    STOCK_ROM_DIR=/path/to/system ./extract-files.sh

  - Setup environment

. build/envsetup.sh

  - Build cm14

brunch gtaxllte

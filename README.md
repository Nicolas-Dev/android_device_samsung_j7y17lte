---------------------------------------------
/           ***** Status *****              /
---------------------------------------------
/         *****ROM boot: oui*****           /
---------------------------------------------
/           *****Audio: oui *****           /
---------------------------------------------
/           ***** GPS: oui *****            /
---------------------------------------------
/          *****Capteurs: oui *****         /
---------------------------------------------
/         ***** Lumières: oui *****         /
---------------------------------------------
/           ***** RIL: oui *****            /
---------------------------------------------
/      ***** données mobile: oui *****      /
---------------------------------------------
/  ***** Audio en cours d'appel: oui *****  /
---------------------------------------------
/ *****  Camera: fonctione a moitier *****  /
---------------------------------------------

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

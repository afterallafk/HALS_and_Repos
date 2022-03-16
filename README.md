# Removing and Cloning HALS

rm -rf hardware/qcom-caf/msm8996/audio && rm -rf hardware/qcom-caf/msm8996/media && rm -rf hardware/qcom-caf/msm8996/display && rm -rf hardware/qcom-caf/wlan && git clone https://github.com/afterallafk/hardware_qcom-caf_msm8996_audio.git -b 12 hardware/qcom-caf/msm8996/audio && git clone https://github.com/afterallafk/hardware_qcom-caf_msm8996_media.git -b 12 hardware/qcom-caf/msm8996/media && git clone https://github.com/afterallafk/hardware_qcom-caf_msm8996_display.git -b 12 hardware/qcom-caf/msm8996/display && git clone https://github.com/afterallafk/hardware_qcom-caf_wlan.git -b 12 hardware/qcom-caf/wlan

# Sepolicies
rm -rf device/qcom/sepolicy && rm -rf device/qcom/sepolicy-legacy-um && rm -rf device/qcom/sepolicy_vndr && rm -rf system/sepolicy && rm -rf external/selinux && git clone https://github.com/afterallafk/android_external_selinux.git -b 12 external/selinux && git clone https://github.com/afterallafk/device_qcom_sepolicy_vndr.git -b 12 device/qcom/sepolicy_vndr && git clone https://github.com/afterallafk/device_qcom_sepolicy-legacy-um.git -b 12 device/qcom/sepolicy-legacy-um && git clone https://github.com/afterallafk/device_qcom_sepolicy.git -b 12 device/qcom/sepolicy && git clone https://github.com/afterallafk/system_sepolicy.git -b 12 system/sepolicy

# Cloning Trees

git clone https://github.com/afterallafk/device_xiaomi_onclite.git -b blaze device/xiaomi/onclite && git clone https://github.com/afterallafk/vendor_xiaomi_onclite-12.git -b twelve vendor/xiaomi/onclite && git clone https://github.com/afterallafk/kernel_xiaomi_onclite.git -b twelve kernel/xiaomi/onclite

# Starting Build Commands

. build/envsetup.sh && lunch blaze_onclite-eng && make bacon

# Maxsun-B660m-i5-12400-RX6800-Hackintosh-Configuration
## 1.Mobo: Maxsun B660m terminator
## 2.CPU: Intel i5-12400
## 3.GPU: AMD RX6800
## 4.RAM: Crucial DDR4 3200MHZ
## 5.Ethernet: On-board
## 6.Wifi-Bluetooth: Intel AX210 Wireless+bluetooth
## 7.OC: 1.0.1
## 8.OS: Sonoma 14.6 (23G80)
1. This config has implemented USB, sleep & wakeup fixes inspired by https://www.bilibili.com/video/BV1ub421J7Lk?spm_id_from=333.880.my_history.page.click, for more information please watch this video.
2. Intel AX210 wireless card+bluetooth drivers appended (24.8.27).
3. GPRW patch implemented for force sleep of USB devices, shortcoming is it only can be waked up by pressing the power button (24.8.27).
![6A2BA5A8-19A0-4D79-803F-D030C31F9A17_1_201_a](https://github.com/user-attachments/assets/b23d38ac-eb85-4499-9fba-bdc14bd2924d)
![94E6ABE7-52F9-47D2-BF6C-37F748AAC57B_1_201_a](https://github.com/user-attachments/assets/13b4de39-d6e9-4303-8e64-f0b9f26395cb)

## 9. OTA：

- open EFI/OC/config.plist with OCAuxilaryTools or OpenCore Configurator
- Misc-**security-tab**-SecureBootModel->disable
- NVRAM-**7C436110-AB2A-4BBB-A880-FE41995C9F82**-**add-tab**-boot-args->append **revpatch=auto,sbvmm,cpuname（append 'cpuname' if 4D1FDA02-38C7-4A6A-9CC6-4BCCA8B30102--revcpuname value is specified explicitly）** 
- NVRAM-**7C436110-AB2A-4BBB-A880-FE41995C9F82**-**Delete-tab** ->append **boot-args** if not exists
- Refer to: https://www.bilibili.com/video/BV1k7YKehEJv/?vd_source=73bc2d585431c0a5f9873ab95d8dd80d


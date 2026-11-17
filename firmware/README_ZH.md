# 固件

[English](README.md) | [简体中文](README_ZH.md)

ESP32-C6-Touch-LCD-1.69 的出厂固件。BIN 是从 `0x0` 烧录的合并镜像，文件名中的日期即版本。

| 文件 | 用途 |
| --- | --- |
| [ESP32-C6-Touch-LCD-1.69_FactoryOnly_20250618.bin](ESP32-C6-Touch-LCD-1.69_FactoryOnly_20250618.bin) | 出厂固件，恢复开箱演示 |

在本目录运行以下命令，将 `<PORT>` 替换为开发板对应的串口。整片擦除会清除已有设置和用户数据。

```bash
python -m pip install esptool
esptool.py --chip esp32c6 --port <PORT> erase_flash
esptool.py --chip esp32c6 --port <PORT> write_flash 0x0 ESP32-C6-Touch-LCD-1.69_FactoryOnly_20250618.bin
```


---
description: SystemConfig_Video класс. Этот класс является классом типа событий для событий конфигурации видео.
ms.assetid: ddb5924b-70d9-4693-bf68-0536c3c3fa8d
title: Класс SystemConfig_Video
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Video
- SystemConfig_Video.MemorySize
- SystemConfig_Video.XResolution
- SystemConfig_Video.YResolution
- SystemConfig_Video.BitsPerPixel
- SystemConfig_Video.VRefresh
- SystemConfig_Video.ChipType
- SystemConfig_Video.DACType
- SystemConfig_Video.AdapterString
- SystemConfig_Video.BiosString
- SystemConfig_Video.DeviceId
- SystemConfig_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 09d68fcd2710e4f16b315182624ce32eaa3729f370a4a6a071c55f705dcbe6af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811704"
---
# <a name="systemconfig_video-class"></a>\_Класс видео системконфиг

Этот класс является классом типа событий для событий конфигурации видео.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_Video : SystemConfig
{
  uint32 MemorySize;
  uint32 XResolution;
  uint32 YResolution;
  uint32 BitsPerPixel;
  uint32 VRefresh;
  char16 ChipType[];
  char16 DACType[];
  char16 AdapterString[];
  char16 BiosString[];
  char16 DeviceId[];
  uint32 StateFlags;
};
```

## <a name="members"></a>Члены

Класс **\_ видео системконфиг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ Video системконфиг** имеет следующие свойства.

<dl> <dt>

**адаптерстринг**
</dt> <dd> <dl> <dt>

Тип данных: массив **Char16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (8), **Max** (256), **Format ("s")**
</dt> </dl>

Имя или описание адаптера.

</dd> <dt>

**биосстринг**
</dt> <dd> <dl> <dt>

Тип данных: массив **Char16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (9), **Max** (256), **Format ("s")**
</dt> </dl>

Имя BIOS адаптера.

</dd> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (4)
</dt> </dl>

Число битов, используемых для вывода каждого пикселя.

</dd> <dt>

**чиптипе**
</dt> <dd> <dl> <dt>

Тип данных: массив **Char16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (6), **Max** (256), **Format ("s")**
</dt> </dl>

Имя микросхемы адаптера.

</dd> <dt>

**DACType**
</dt> <dd> <dl> <dt>

Тип данных: массив **Char16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (7), **Max** (256), **Format ("s")**
</dt> </dl>

Имя микросхемы цифрового преобразователя (DAC) адаптера.

</dd> <dt>

**DeviceId**
</dt> <dd> <dl> <dt>

Тип данных: массив **Char16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (10), **Max** (256), **Format ("s")**
</dt> </dl>

Адрес или другие идентифицирующие сведения для уникального имени логического устройства.

</dd> <dt>

**MemorySize**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (1)
</dt> </dl>

Максимальный поддерживаемый объем памяти в байтах.

</dd> <dt>

**статефлагс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (11), **Format ("x")**
</dt> </dl>

Флаги состояния устройства. Это может быть любое разумное сочетание следующих параметров.



| Значение                                                                                                                                                                                                                                                                                        | Значение                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <dt>**Отображение \_ УСТРОЙСТВО \_ , подключенное \_ к \_ рабочему столу**</dt> <dt>1 (0x1)</dt> </dl> | Устройство является частью рабочего стола.<br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <dt>**Отображение \_ \_ \_ Драйвер зеркального отображения устройств**</dt> <dt>8 (0x8)</dt> </dl>           | Представляет псевдо-устройство, используемое для отражения прорисовки приложения для подключения к удаленному компьютеру или другим целям. С этим устройством связан невидимый псевдо-монитор. Например, NetMeeting использует его.<br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <dt>**Отображение \_ \_МОДЕСПРУНЕД устройства**</dt> <dt>134217728 (0x8000000)</dt> </dl>             | Устройство имеет больше режимов вывода, чем поддерживается устройствами вывода.<br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <dt>**Отображение \_ \_Основное \_ устройство**</dt> <dt>4 (0x4)</dt> </dl>                 | Основной рабочий стол находится на устройстве. Для системы с одной картой экрана всегда устанавливается значение. Для системы с несколькими экранными картами этот набор может иметь только одно устройство.<br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <dt>**Отображение \_ \_Съемное устройство**</dt> <dt>32 (0x20)</dt> </dl>                               | Устройство является съемным; Он не может быть основным дисплеем.<br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <dt>**Отображение \_ \_ \_ Совместимость устройства VGA**</dt> <dt>16 (0x10)</dt> </dl>               | Устройство совместимо с VGA.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

**врефреш**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (5)
</dt> </dl>

Текущая частота обновления в герцах.

</dd> <dt>

**ксресолутион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (2)
</dt> </dl>

Текущее число точек по горизонтали.

</dd> <dt>

**иресолутион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (3)
</dt> </dl>

Текущее число пикселей по вертикали.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**системконфиг**](systemconfig.md)
</dt> </dl>

 

 





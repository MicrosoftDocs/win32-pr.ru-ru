---
description: Этот класс является классом типа событий для событий конфигурации логического диска.
ms.assetid: a11a8245-8ace-4061-b6c7-938002d8b9fc
title: Класс SystemConfig_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_LogDisk
- SystemConfig_LogDisk.StartOffset
- SystemConfig_LogDisk.PartitionSize
- SystemConfig_LogDisk.DiskNumber
- SystemConfig_LogDisk.Size
- SystemConfig_LogDisk.DriveType
- SystemConfig_LogDisk.DriveLetterString
- SystemConfig_LogDisk.Pad1
- SystemConfig_LogDisk.PartitionNumber
- SystemConfig_LogDisk.SectorsPerCluster
- SystemConfig_LogDisk.BytesPerSector
- SystemConfig_LogDisk.Pad2
- SystemConfig_LogDisk.NumberOfFreeClusters
- SystemConfig_LogDisk.TotalNumberOfClusters
- SystemConfig_LogDisk.FileSystem
- SystemConfig_LogDisk.VolumeExt
- SystemConfig_LogDisk.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3bff1cf526dfb7bf1ddd36fcb887e8a4b837be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984453"
---
# <a name="systemconfig_logdisk-class"></a>\_Класс системконфиг логдиск

Этот класс является классом типа событий для событий конфигурации логического диска.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_LogDisk : SystemConfig
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad1;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  uint32 Pad2;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
  uint32 Pad3;
};
```

## <a name="members"></a>Участники

Класс **системконфиг \_ логдиск** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **системконфиг \_ логдиск** имеет следующие свойства.

<dl> <dt>

**битесперсектор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (10)
</dt> </dl>

Число байтов в каждом секторе для физического диска.

</dd> <dt>

**дискнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (3)
</dt> </dl>

Номер индекса диска, содержащего этот раздел.

</dd> <dt>

**дривелеттерстринг**
</dt> <dd> <dl> <dt>

Тип данных: массив **Char16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (6), **Max** (4), **Format ("s")**
</dt> </dl>

Буква диска в формате " <letter> :".

</dd> <dt>

**DriveType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (5)
</dt> </dl>

Тип диска. Возможны следующие значения:



| Значение                                                                        | Значение                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>1</dt> </dl> | Секция<br/>                            |
| <dl> <dt>2</dt> </dl> | Том<br/>                               |
| <dl> <dt>3</dt> </dl> | Дополнительный раздел на нескольких дисках<br/> |



 

</dd> <dt>

**Системой**
</dt> <dd> <dl> <dt>

Тип данных: **Char16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (14), **Max** (16), **Format ("s")**
</dt> </dl>

Файловая система на логическом диске, например NTFS.

</dd> <dt>

**нумбероффриклустерс**
</dt> <dd> <dl> <dt>

Тип данных: **sint64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (12)
</dt> </dl>

Количество свободных кластеров в указанном томе.

</dd> <dt>

**Pad1**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (7)
</dt> </dl>

Не используется.

</dd> <dt>

**Pad2**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (11)
</dt> </dl>

Не используется.

</dd> <dt>

**Pad3**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (16)
</dt> </dl>

Не используется.

</dd> <dt>

**PartitionNumber**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (8)
</dt> </dl>

Номер индекса секции.

</dd> <dt>

**PartitionSize**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (2)
</dt> </dl>

Общий размер секции в байтах.

</dd> <dt>

**секторсперклустер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (9)
</dt> </dl>

Количество секторов в томе.

</dd> <dt>

**Размер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (4)
</dt> </dl>

Размер диска в байтах.

</dd> <dt>

**стартоффсет**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (1)
</dt> </dl>

Начальное смещение (в байтах) секции от начала диска.

</dd> <dt>

**тоталнумберофклустерс**
</dt> <dd> <dl> <dt>

Тип данных: **sint64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (13)
</dt> </dl>

Количество используемых и свободных кластеров в томе.

</dd> <dt>

**волумикст**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (15)
</dt> </dl>

Зарезервировано.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**системконфиг**](systemconfig.md)
</dt> </dl>

 

 





---
description: Этот класс является классом типа событий для событий конфигурации логического диска.
ms.assetid: 3fa5f2e4-f6fa-4c10-9634-04908783cd28
title: Класс SystemConfig_V0_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_LogDisk
- SystemConfig_V0_LogDisk.StartOffset
- SystemConfig_V0_LogDisk.PartitionSize
- SystemConfig_V0_LogDisk.DiskNumber
- SystemConfig_V0_LogDisk.Size
- SystemConfig_V0_LogDisk.DriveType
- SystemConfig_V0_LogDisk.DriveLetterString
- SystemConfig_V0_LogDisk.Pad
- SystemConfig_V0_LogDisk.PartitionNumber
- SystemConfig_V0_LogDisk.SectorsPerCluster
- SystemConfig_V0_LogDisk.BytesPerSector
- SystemConfig_V0_LogDisk.NumberOfFreeClusters
- SystemConfig_V0_LogDisk.TotalNumberOfClusters
- SystemConfig_V0_LogDisk.FileSystem
- SystemConfig_V0_LogDisk.VolumeExt
api_type:
- NA
api_location: ''
ms.openlocfilehash: dbc1ee189bae1fe71f42267f38bd40763764dea2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985933"
---
# <a name="systemconfig_v0_logdisk-class"></a>\_Класс системконфиг v0 \_ логдиск

Этот класс является классом типа событий для событий конфигурации логического диска.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_V0_LogDisk : SystemConfig_V0
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
};
```

## <a name="members"></a>Участники

Класс **системконфиг \_ v0 \_ логдиск** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **системконфиг \_ v0 \_ логдиск** имеет следующие свойства.

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

Квалификаторы: **вмидатаид** (6), **Max** (4)
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

Квалификаторы: **вмидатаид** (13), **Max** (16)
</dt> </dl>

Файловая система на логическом диске, например NTFS.

</dd> <dt>

**нумбероффриклустерс**
</dt> <dd> <dl> <dt>

Тип данных: **sint64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (11)
</dt> </dl>

Количество свободных кластеров в указанном томе.

</dd> <dt>

**Коммутаци**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (7)
</dt> </dl>

Зарезервировано.

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

Квалификаторы: **вмидатаид** (12)
</dt> </dl>

Количество используемых и свободных кластеров в томе.

</dd> <dt>

**волумикст**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (14)
</dt> </dl>

Зарезервировано.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Системконфиг \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 





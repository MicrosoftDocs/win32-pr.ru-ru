---
description: Класс Хвконфиг \_ фидиск является классом типа событий для событий конфигурации физического диска. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: b134ab45-b161-452f-be84-ccbdfa3fe4af
title: Класс HWConfig_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_PhyDisk
- HWConfig_PhyDisk.DiskNumber
- HWConfig_PhyDisk.BytesPerSector
- HWConfig_PhyDisk.SectorsPerTrack
- HWConfig_PhyDisk.TracksPerCylinder
- HWConfig_PhyDisk.Cylinders
- HWConfig_PhyDisk.SCSIPort
- HWConfig_PhyDisk.SCSIPath
- HWConfig_PhyDisk.SCSITarget
- HWConfig_PhyDisk.SCSILun
- HWConfig_PhyDisk.Manufacturer
api_type:
- NA
api_location: ''
ms.openlocfilehash: ee8a578154e2acedb5d5c8ca6d5eea4f79737e5a2cfb89b0cb658526094fd09c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086404"
---
# <a name="hwconfig_phydisk-class"></a>\_Класс хвконфиг фидиск

Класс **хвконфиг \_ фидиск** является классом типа событий для событий конфигурации физического диска.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class HWConfig_PhyDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 BytesPerSector;
  uint32 SectorsPerTrack;
  uint32 TracksPerCylinder;
  uint64 Cylinders;
  uint32 SCSIPort;
  uint32 SCSIPath;
  uint32 SCSITarget;
  uint32 SCSILun;
  string Manufacturer;
};
```

## <a name="members"></a>Члены

Класс **хвконфиг \_ фидиск** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **хвконфиг \_ фидиск** имеет следующие свойства.

<dl> <dt>

битесперсектор
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2)
</dt> </dl>

Число байтов в каждом секторе для физического диска.

</dd> <dt>

Цилиндров
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (5)
</dt> </dl>

Общее число цилиндров на физическом диске. Примечание. значение этого свойства получается через расширенные функции прерывания 13h BIOS. Значение может быть неточным, если диск использует схему перевода для поддержки размера дисков с высокой емкостью. Точные спецификации дисков можно узнать у изготовителя.

</dd> <dt>

дискнумбер
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1)
</dt> </dl>

Номер индекса диска, содержащего этот раздел.

</dd> <dt>

Изготовитель
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (10), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

Имя изготовителя диска.

</dd> <dt>

сксилун
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (9)
</dt> </dl>

Логический номер устройства (LUN) SCSI адаптера SCSI.

</dd> <dt>

сксипас
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (7)
</dt> </dl>

Номер шины SCSI адаптера SCSI.

</dd> <dt>

SCSIPort
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (6)
</dt> </dl>

Номер SCSI адаптера SCSI.

</dd> <dt>

скситаржет
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (8)
</dt> </dl>

Содержит номер целевого устройства.

</dd> <dt>

секторспертракк
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3)
</dt> </dl>

Количество секторов в каждой дорожке для этого физического диска.

</dd> <dt>

TracksPerCylinder
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4)
</dt> </dl>

Количество дорожек в каждом цилиндре на физическом диске. Примечание. значение этого свойства получается через расширенные функции прерывания 13h BIOS. Значение может быть неточным, если диск использует схему перевода для поддержки размера дисков с высокой емкостью. Точные спецификации дисков можно узнать у изготовителя.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**хвконфиг**](hwconfig.md)
</dt> </dl>

 

 





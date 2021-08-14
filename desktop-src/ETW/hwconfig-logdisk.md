---
description: Класс Хвконфиг \_ логдиск является классом типа событий для событий конфигурации логического диска. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 2b7038fa-2f20-4bb5-bac1-76b272b3421c
title: Класс HWConfig_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_LogDisk
- HWConfig_LogDisk.DiskNumber
- HWConfig_LogDisk.Pad
- HWConfig_LogDisk.StartOffset
- HWConfig_LogDisk.PartitionSize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01d200fc5c34546c96f6a78fd55548e8d5a7b0dacf74d46c411174beb66f6f4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394808"
---
# <a name="hwconfig_logdisk-class"></a>\_Класс хвконфиг логдиск

Класс **хвконфиг \_ логдиск** является классом типа событий для событий конфигурации логического диска.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class HWConfig_LogDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 Pad;
  uint64 StartOffset;
  uint64 PartitionSize;
};
```

## <a name="members"></a>Члены

Класс **хвконфиг \_ логдиск** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **хвконфиг \_ логдиск** имеет следующие свойства.

<dl> <dt>

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

Pad
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2)
</dt> </dl>

Зарезервировано.

</dd> <dt>

PartitionSize
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4)
</dt> </dl>

Общий размер секции в байтах.

</dd> <dt>

стартоффсет
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3)
</dt> </dl>

Начальное смещение (в байтах) секции от начала диска.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**хвконфиг**](hwconfig.md)
</dt> </dl>

 

 





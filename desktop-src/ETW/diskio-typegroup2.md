---
description: Этот класс является классом типа события, который помечает начало событий чтения, записи и очистки диска. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 96543ef9-cc2b-4d9a-86a8-f2458439e4d8
title: Класс DiskIo_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup2
- DiskIo_TypeGroup2.Irp
- DiskIo_TypeGroup2.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: ea08f32106c935be628bcdcd22e39ab92a0566e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540375"
---
# <a name="diskio_typegroup2-class"></a>\_Класс дискио TypeGroup2

Этот класс является классом типа события, который помечает начало событий чтения, записи и очистки диска.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{12, 13, 15}, EventTypeName{"ReadInit", "WriteInit", "FlushInit"}]
class DiskIo_TypeGroup2 : DiskIo
{
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a>Участники

Класс **дискио \_ TypeGroup2** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **дискио \_ TypeGroup2** имеет следующие свойства.

<dl> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (1), [**pointer**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Пакет запроса ввода-вывода. Это свойство определяет действие ввода-вывода.

</dd> <dt>

**иссуингсреадид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Идентификатор выдающего потока.

**Windows server 2008 R2, Windows server 2008, Windows 7 и Windows Vista:** Это свойство не поддерживается.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**дискио**](diskio.md)
</dt> </dl>

 

 





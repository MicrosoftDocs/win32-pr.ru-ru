---
description: Этот класс является классом типа события для событий конца файловой операции. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: Класс FileIo_OpEnd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_OpEnd
- FileIo_OpEnd.IrpPtr
- FileIo_OpEnd.ExtraInfo
- FileIo_OpEnd.NtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3f1c495cf44b84f8d7661b40cadec6ea255c6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816264"
---
# <a name="fileio_opend-class"></a>FileIo \_ открытый класс

Этот класс является классом типа события для событий конца файловой операции.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{76}, EventTypeName{"OperationEnd"}]
class FileIo_OpEnd : FileIo
{
  uint32 IrpPtr;
  uint32 ExtraInfo;
  uint32 NtStatus;
};
```

## <a name="members"></a>Участники

**\_ Открытый класс FileIo** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

**\_ Открытый класс FileIo** имеет следующие свойства.

<dl> <dt>

**екстраинфо**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2), Pointer
</dt> </dl>

Дополнительные сведения, возвращаемые файловой системой для операции. Например, для запроса на чтение — фактическое число считанных байтов.

</dd> <dt>

**ирпптр**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Pointer
</dt> </dl>

Пакет запроса ввода-вывода. Это свойство определяет завершающее действие ввода-вывода.

</dd> <dt>

**NtStatus**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3)
</dt> </dl>

Возвращаемое значение из операции.

</dd> </dl>

## <a name="remarks"></a>Примечания

События [**FileIo**](fileio.md) регистрируются в начале операции. Открытые события можно включить отдельно, чтобы указать конец этих операций. IRP можно использовать для сопоставления событий начала и окончания.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 





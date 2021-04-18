---
description: Этот класс является классом типа событий для событий подпрограммы обработки прерываний (ISR). Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 2c7ccace-3384-43f4-905e-e7eeeee6f87b
title: Класс ISR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISR
- ISR.InitialTime
- ISR.Routine
- ISR.ReturnValue
- ISR.Vector
- ISR.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e27d5aa2712f8493b80ea11884aae1d0ef7abee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985597"
---
# <a name="isr-class"></a>Класс ISR

Этот класс является классом типа событий для событий подпрограммы обработки прерываний (ISR).

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{67}, EventTypeName{"ISR"}]
class ISR : PerfInfo
{
  object InitialTime;
  uint32 Routine;
  uint8  ReturnValue;
  uint8  Vector;
  uint16 Reserved;
};
```

## <a name="members"></a>Участники

Класс **ISR** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **ISR** имеет эти свойства.

<dl> <dt>

**инитиалтиме**
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Extension ("Вмитиме")
</dt> </dl>

Время записи ISR.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (5), Pointer
</dt> </dl>

Зарезервировано.

</dd> <dt>

**ReturnValue**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3)
</dt> </dl>

Логическое значение, указывающее, было ли прерывание запрошено (имеет значение true, если прерывание было затребовано).

</dd> <dt>

**Подпрограмма**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2), Pointer
</dt> </dl>

Адрес подпрограммы ISR. Используйте адрес с событиями Image, чтобы определить, какое изображение запущено.

</dd> <dt>

**Вектор**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4)
</dt> </dl>

Вектор из таблицы дескрипторов прерываний, которому назначается процедура ISR.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





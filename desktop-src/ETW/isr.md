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
ms.openlocfilehash: 621bf9c97aef9ea23fba6186a419f7c205d98fba608c2539702607986de0d258
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901004"
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

## <a name="members"></a>Члены

Класс **ISR** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





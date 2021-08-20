---
description: Этот класс является классом типа события для событий PnP. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 01e9a8bb-3f54-4e20-b4db-1b4bba745d4f
title: Класс SystemConfig_PnP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PnP
- SystemConfig_PnP.IDLength
- SystemConfig_PnP.DescriptionLength
- SystemConfig_PnP.FriendlyNameLength
- SystemConfig_PnP.DeviceID
- SystemConfig_PnP.DeviceDescription
- SystemConfig_PnP.FriendlyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 082d9169bbd2ad30af6b2bc17600804f43ce7bbef5e52f15f7ac4c85b21f7b8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582204"
---
# <a name="systemconfig_pnp-class"></a>\_Класс системконфиг PnP

Этот класс является классом типа события для событий PnP.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(22), EventTypeName("PnP")]
class SystemConfig_PnP : SystemConfig
{
  uint32 IDLength;
  uint32 DescriptionLength;
  uint32 FriendlyNameLength;
  string DeviceID;
  string DeviceDescription;
  string FriendlyName;
};
```

## <a name="members"></a>Члены

Класс **системконфиг \_ PnP** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **системконфиг \_ PnP** имеет следующие свойства.

<dl> <dt>

**дескриптионленгс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2)
</dt> </dl>

Длина строки DeviceDescription в символах.

</dd> <dt>

**DeviceDescription**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (5), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

Описание устройства PnP.

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

Определяет устройство PnP.

</dd> <dt>

**FriendlyName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (6), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

Имя устройства PnP, которое будет использоваться в пользовательском интерфейсе.

</dd> <dt>

**фриендлинамеленгс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3)
</dt> </dl>

Длина строки FriendlyName в символах.

</dd> <dt>

**идленгс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1)
</dt> </dl>

Длина строки DeviceID в символах.

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

 

 





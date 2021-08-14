---
description: SystemConfig_V0_Services класс. Этот класс является классом типа событий для событий конфигурации службы.
ms.assetid: 1e6c2061-f1a2-4253-a0c4-4b45b2feceda
title: Класс SystemConfig_V0_Services
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Services
- SystemConfig_V0_Services.ServiceName
- SystemConfig_V0_Services.DisplayName
- SystemConfig_V0_Services.ProcessName
- SystemConfig_V0_Services.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5cfe3bfd4509a02eeafcb014f9265f810e4cb942e87b67390dbd1cbf841f7295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393793"
---
# <a name="systemconfig_v0_services-class"></a>\_Класс системконфиг v0 \_ Services

Этот класс является классом типа событий для событий конфигурации службы.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_V0_Services : SystemConfig_V0
{
  char16 ServiceName[];
  char16 DisplayName[];
  char16 ProcessName[];
  uint32 ProcessId;
};
```

## <a name="members"></a>Члены

Класс **системконфиг \_ v0 \_ Services** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **системконфиг \_ v0 \_ Services** имеет следующие свойства.

<dl> <dt>

**Отображаемое имя**
</dt> <dd> <dl> <dt>

Тип данных: массив **Char16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (2), **Max** (256)
</dt> </dl>

Отображаемое имя службы. В диспетчере управления службами имя сохраняется с учетом регистра. Но сравнения отображаемых имен всегда выполняются без учета регистра.

</dd> <dt>

**Идентификатор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (4)
</dt> </dl>

Идентификатор процесса, в котором выполняется служба.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Тип данных: массив **Char16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (3), **Max** (34)
</dt> </dl>

Имя процесса, в котором выполняется служба.

</dd> <dt>

**Служба**
</dt> <dd> <dl> <dt>

Тип данных: массив **Char16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (1), **Max** (34)
</dt> </dl>

Уникальный идентификатор службы. Идентификатор предоставляет сведения о функциональных возможностях, предоставляемых службой.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Системконфиг \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 





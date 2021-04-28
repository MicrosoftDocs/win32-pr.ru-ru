---
description: SystemConfig_Services класс. Этот класс является классом типа событий для событий конфигурации службы.
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: Класс SystemConfig_Services
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Services
- SystemConfig_Services.ProcessId
- SystemConfig_Services.ServiceState
- SystemConfig_Services.SubProcessTag
- SystemConfig_Services.ServiceName
- SystemConfig_Services.DisplayName
- SystemConfig_Services.ProcessName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 754b0e10c3882911c6e91fc2590c11739c3f7531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106062"
---
# <a name="systemconfig_services-class"></a>\_Класс системконфиг Services

Этот класс является классом типа событий для событий конфигурации службы.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_Services : SystemConfig
{
  uint32 ProcessId;
  uint32 ServiceState;
  uint32 SubProcessTag;
  string ServiceName[];
  string DisplayName[];
  string ProcessName[];
};
```

## <a name="members"></a>Члены

Класс **системконфиг \_ Services** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **системконфиг \_ Services** имеет следующие свойства.

<dl> <dt>

**Отображаемое имя**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (5), **Стрингтерминатион ("NullTerminated")**, **Format ("w")**
</dt> </dl>

Отображаемое имя службы. В диспетчере управления службами имя сохраняется с учетом регистра. Но сравнения отображаемых имен всегда выполняются без учета регистра.

</dd> <dt>

**Идентификатор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (1), **Format ("x")**
</dt> </dl>

Идентификатор процесса, в котором выполняется служба.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (6), **Стрингтерминатион ("NullTerminated")**, **Format ("w")**
</dt> </dl>

Имя процесса, в котором выполняется служба.

</dd> <dt>

**Служба**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (4), **Стрингтерминатион ("NullTerminated")**, **Format ("w")**
</dt> </dl>

Уникальный идентификатор службы. Идентификатор предоставляет сведения о функциональных возможностях, предоставляемых службой.

</dd> <dt>

**ServiceState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (2), **Format ("x")**
</dt> </dl>

Текущее состояние службы. Возможные значения см. в разделе **двкуррентстатеing** of **Service \_ Status \_ Process**.

</dd> <dt>

**субпроцесстаг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (3), **Format ("x")**
</dt> </dl>

Идентифицирует службу.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**системконфиг**](systemconfig.md)
</dt> </dl>

 

 





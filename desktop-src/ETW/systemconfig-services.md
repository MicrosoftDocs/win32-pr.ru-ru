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
ms.openlocfilehash: 80d0bfdc324f55bd8b697dfd63f9c2cf5c847ca3e3c931842b886c00adbc6aac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383454"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**системконфиг**](systemconfig.md)
</dt> </dl>

 

 





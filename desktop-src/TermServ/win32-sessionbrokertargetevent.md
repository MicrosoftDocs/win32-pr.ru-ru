---
title: Класс Win32_SessionBrokerTargetEvent
description: Представляет изменение целевого объекта посредника сеансов.
ms.assetid: ee3ae0ed-eb8b-4777-9b9e-0e50722cf52a
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionBrokerTargetEvent службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionBrokerTargetEvent, описание
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTargetEvent
- Win32_SessionBrokerTargetEvent.SECURITY_DESCRIPTOR
- Win32_SessionBrokerTargetEvent.TIME_CREATED
- Win32_SessionBrokerTargetEvent.ChangeType
- Win32_SessionBrokerTargetEvent.PluginName
- Win32_SessionBrokerTargetEvent.TargetName
- Win32_SessionBrokerTargetEvent.FarmName
- Win32_SessionBrokerTargetEvent.Guid
- Win32_SessionBrokerTargetEvent.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92fcd6cb93e3ac7abaa5fef33e1557008eb29b46940fae6d5165809d9252fa16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769974"
---
# <a name="win32_sessionbrokertargetevent-class"></a>\_Класс Win32 сессионброкертаржетевент

Представляет изменение целевого объекта посредника сеансов.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[AMENDMENT]
class Win32_SessionBrokerTargetEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint32 ChangeType;
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ сессионброкертаржетевент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ сессионброкертаржетевент** имеет следующие свойства.

<dl> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает произошедшее изменение. Это может быть одно из следующих значений.

<dt>

1 (0x1)
</dt> <dd>

Тип изменения не указан.

</dd> <dt>

2 (0x2)
</dt> <dd>

Внешний IP-адрес изменился.

</dd> <dt>

4 (0x4)
</dt> <dd>

Внутренний IP-адрес изменился.

</dd> <dt>

8 (0x8)
</dt> <dd>

Цель была присоединена.

</dd> <dt>

16 (0x10)
</dt> <dd>

Цель удалена.

</dd> <dt>

32 (0x20)
</dt> <dd>

Состояние целевого объекта изменилось.

</dd> <dt>

64 (0x40)
</dt> <dd>

Целевой объект бездействует.

</dd> </dl>

</dd> <dt>

**Среда**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя среды. В случае целевого объекта виртуальной машины это может быть имя узла виртуальной машины.

**Windows Server 2008 R2:** Это свойство недоступно до Windows Server 2012

</dd> <dt>

**фармнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя фермы, которой принадлежит целевой объект.

**Windows Server 2008 R2:** Это свойство недоступно до Windows Server 2012

</dd> <dt>

**Устройства**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор GUID целевого объекта.

**Windows Server 2008 R2:** Это свойство недоступно до Windows Server 2012

</dd> <dt>

**PluginName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя подключаемого модуля.

**Windows Server 2008 R2:** Это свойство недоступно до Windows Server 2012

</dd> <dt>

**\_дескриптор безопасности**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие. Это свойство наследуется от [**\_ \_ события**](/windows/desktop/WmiSdk/--event). Дополнительные сведения о константах, используемых для задания этого дескриптора безопасности, см. в разделе [константы безопасности WMI](/windows/desktop/WmiSdk/wmi-security-constants).

</dd> <dt>

**TargetName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя целевого объекта.

**Windows Server 2008 R2:** Это свойство недоступно до Windows Server 2012

</dd> <dt>

**ВРЕМЯ \_ создания**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальное значение, указывающее время создания события. Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г. Эти сведения находятся в формате всеобщего скоординированного времени (UTC). Это свойство наследуется от [**\_ \_ события**](/windows/desktop/WmiSdk/--event).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                      |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                               |
| MOF<br/>                      | <dl> <dt>Тссдвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 


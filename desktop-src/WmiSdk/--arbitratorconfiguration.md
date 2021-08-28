---
description: Ограничивает внутренние ресурсы, используемые операциями, инициированными клиентами WMI.
ms.assetid: e877899d-2f5e-4468-8c47-055fd4d16f56
ms.tgt_platform: multiple
title: Класс __ArbitratorConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ArbitratorConfiguration
- Root.__ArbitratorConfiguration.OutstandingTasksTotal
- Root.__ArbitratorConfiguration.OutstandingTasksPerUser
- Root.__ArbitratorConfiguration.TaskThreadsTotal
- Root.__ArbitratorConfiguration.TaskThreadsPerUser
- Root.__ArbitratorConfiguration.QuotaRetryCount
- Root.__ArbitratorConfiguration.QuotaRetryWaitInterval
- Root.__ArbitratorConfiguration.TotalUsers
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerTask
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerUser
- Root.__ArbitratorConfiguration.TotalCacheMemory
- Root.__ArbitratorConfiguration.TotalCacheDiskPerTask
- Root.__ArbitratorConfiguration.TotalCacheDiskPerUser
- Root.__ArbitratorConfiguration.TotalCacheDisk
- Root.__ArbitratorConfiguration.TemporarySubscriptionsPerUser
- Root.__ArbitratorConfiguration.PermanentSubscriptionsPerUser
- Root.__ArbitratorConfiguration.PollingInstructionsPerUser
- Root.__ArbitratorConfiguration.PollingMemoryPerUser
- Root.__ArbitratorConfiguration.TemporarySubscriptionsTotal
- Root.__ArbitratorConfiguration.PermanentSubscriptionsTotal
- Root.__ArbitratorConfiguration.PollingInstructionsTotal
- Root.__ArbitratorConfiguration.PollingMemoryTotal
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 4344eb368a96d2d47207748cba622d07d11ef78e0a046c6ea169305d9c587957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321124"
---
# <a name="__arbitratorconfiguration-class"></a>\_\_Класс Арбитраторконфигуратион

Класс **\_ \_ арбитраторконфигуратион** — это класс конфигурации, который ограничивает внутренние ресурсы, используемые операциями, инициированными клиентами WMI. Это одноэлементный класс, находящийся в \\ корневом пространстве имен. Класс создается внутренним образом, поэтому для него не существует MOF-файла.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[singleton]
class __ArbitratorConfiguration : __SystemClass
{
  uint32 OutstandingTasksTotal;
  uint32 OutstandingTasksPerUser;
  uint32 TaskThreadsTotal;
  uint32 TaskThreadsPerUser;
  uint32 QuotaRetryCount;
  uint32 QuotaRetryWaitInterval;
  uint32 TotalUsers;
  uint32 TotalCacheMemoryPerTask;
  uint32 TotalCacheMemoryPerUser;
  uint32 TotalCacheMemory;
  uint32 TotalCacheDiskPerTask;
  uint32 TotalCacheDiskPerUser;
  uint32 TotalCacheDisk;
  uint32 TemporarySubscriptionsPerUser;
  uint32 PermanentSubscriptionsPerUser;
  uint32 PollingInstructionsPerUser;
  uint32 PollingMemoryPerUser;
  uint32 TemporarySubscriptionsTotal;
  uint32 PermanentSubscriptionsTotal;
  uint32 PollingInstructionsTotal;
  uint32 PollingMemoryTotal;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ арбитраторконфигуратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ арбитраторконфигуратион** имеет следующие свойства.

<dl> <dt>

**аутстандингтасксперусер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется. Число невыполненных задач, инициированных пользователем, в любое время.

</dd> <dt>

**аутстандингтаскстотал**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется. Общее число невыполненных задач в любое время.

</dd> <dt>

**перманентсубскриптионсперусер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество постоянных подписок, разрешенных для конкретного пользователя в любой момент времени.

</dd> <dt>

**перманентсубскриптионстотал**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общее число постоянных подписок, разрешенных для всех пользователей за один раз.

</dd> <dt>

**поллингинструктионсперусер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество запросов событий опроса, разрешенных для конкретного пользователя в любой момент времени.

</dd> <dt>

**поллингинструктионстотал**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общее количество инструкций опроса, разрешенных для всех пользователей за один раз.

</dd> <dt>

**поллингмемориперусер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество запросов событий опроса памяти, выданных определенным пользователем, может использоваться в любой момент времени.

</dd> <dt>

**поллингмеморитотал**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общий объем памяти, который опрашивает запросы событий для всех пользователей, может быть потребителем в любой момент времени.

</dd> <dt>

**куотаретрикаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется. Число нарушений квоты, разрешенных до отмены задачи.

</dd> <dt>

**куотаретриваитинтервал**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется. Задержка, появившаяся в выполнении задачи при каждом нарушении квоты.

</dd> <dt>

**тасксреадсперусер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется. Максимальное число потоков задач, связанных с определенным пользователем в один раз.

</dd> <dt>

**тасксреадстотал**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется. Максимальное число потоков задач.

</dd> <dt>

**темпорарисубскриптионсперусер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество временных подписок, разрешенных для конкретного пользователя в любой момент времени.

</dd> <dt>

**темпорарисубскриптионстотал**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общее количество временных подписок, разрешенных для всех пользователей за один раз.

</dd> <dt>

**тоталкачедиск**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется. Общий кэш диска, связанный со всеми пользователями за один раз.

</dd> <dt>

**тоталкачедискпертаск**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется. Общий кэш диска, связанный с определенной задачей в любое время.

</dd> <dt>

**тоталкачедискперусер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется. Общий кэш диска, связанный с определенным пользователем в любой момент времени.

</dd> <dt>

**тоталкачемемори**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется. Общий кэш памяти, связанный со всеми пользователями за один раз.

</dd> <dt>

**тоталкачемеморипертаск**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется. Общий кэш памяти, связанный с определенной задачей в любое время.

</dd> <dt>

**тоталкачемемориперусер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется. Общий кэш памяти, связанный с определенным пользователем в любой момент времени.

</dd> <dt>

**тоталусерс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не используется. Максимальное число подключенных пользователей.

</dd> </dl>

## <a name="remarks"></a>Remarks

**\_ \_ Арбитраторконфигуратион** наследуется от [**\_ \_ системкласс**](--systemclass.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Root<br/>                |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_\_системкласс**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> </dl>

 


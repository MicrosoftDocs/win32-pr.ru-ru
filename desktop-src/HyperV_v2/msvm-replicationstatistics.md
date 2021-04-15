---
description: Предоставляет статистику репликации для виртуальной машины.
ms.assetid: 52d944a7-9309-4b56-97b7-e050a9501c57
title: Класс Msvm_ReplicationStatistics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationStatistics
- Msvm_ReplicationStatistics.InstanceID
- Msvm_ReplicationStatistics.Caption
- Msvm_ReplicationStatistics.Description
- Msvm_ReplicationStatistics.ElementName
- Msvm_ReplicationStatistics.StartStatisticTime
- Msvm_ReplicationStatistics.EndStatisticTime
- Msvm_ReplicationStatistics.ReplicationSuccessCount
- Msvm_ReplicationStatistics.ReplicationSize
- Msvm_ReplicationStatistics.MaxReplicationSize
- Msvm_ReplicationStatistics.ReplicationLatency
- Msvm_ReplicationStatistics.ReplicationMissCount
- Msvm_ReplicationStatistics.MaxReplicationLatency
- Msvm_ReplicationStatistics.NetworkFailureCount
- Msvm_ReplicationStatistics.ReplicationFailureCount
- Msvm_ReplicationStatistics.PendingReplicationSize
- Msvm_ReplicationStatistics.ApplicationConsistentSnapshotFailureCount
- Msvm_ReplicationStatistics.ReplicationHealth
- Msvm_ReplicationStatistics.LastTestFailoverTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f18501c2da875a9c3514549271fbc91620abef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683685"
---
# <a name="msvm_replicationstatistics-class"></a>\_Класс мсвм репликатионстатистикс

Предоставляет статистику репликации для виртуальной машины. Эти статистические данные охватывают длительность, заданную свойствами **мониторингстарттиме** и **мониторингинтервал** класса [**мсвм \_ репликатионсервицесеттингдата**](msvm-replicationservicesettingdata.md) .

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationStatistics : CIM_ManagedElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime StartStatisticTime;
  datetime EndStatisticTime;
  uint32   ReplicationSuccessCount;
  uint64   ReplicationSize;
  uint64   MaxReplicationSize;
  uint32   ReplicationLatency;
  uint32   ReplicationMissCount;
  uint32   MaxReplicationLatency;
  uint32   NetworkFailureCount;
  uint32   ReplicationFailureCount;
  uint64   PendingReplicationSize;
  uint32   ApplicationConsistentSnapshotFailureCount;
  uint32   ReplicationHealth;
  datetime LastTestFailoverTime;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ репликатионстатистикс** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ репликатионстатистикс** имеет следующие свойства.

<dl> <dt>

**аппликатионконсистентснапшотфаилурекаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общее число сбоев моментальных снимков VSS.

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.

</dd> <dt>

**ендстатистиктиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время в формате UTC, когда служба реплики Hyper-V остановила сбор данных статистики репликации. В настоящее время начинается новый цикл статистики репликации.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.

</dd> <dt>

**ласттестфаиловертиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает время последнего создания системы реплики теста для виртуальной машины с поддержкой репликации на сервере восстановления.

</dd> <dt>

**максрепликатионлатенци**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное количество времени, затраченное на выполнение одного цикла репликации в секундах.

</dd> <dt>

**максрепликатионсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное количество данных репликации, передаваемых в систему узла восстановления, в байтах. Представляет максимальный размер данных репликации, отправляемых за один цикл для этого интервала.

</dd> <dt>

**нетворкфаилурекаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общее число сетевых ошибок, обнаруженных для канала репликации с системой узла восстановления.

</dd> <dt>

**пендингрепликатионсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Размер данных для ожидающей репликации в байтах.

</dd> <dt>

**репликатионфаилурекаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общее число сбоев репликации. Сюда входят ошибки для операции репликации.

</dd> <dt>

**репликатионхеалс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Работоспособность репликации для виртуальной машины. Это может быть одно из следующих значений.

<dl> <dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (0)
</dt> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>**ОК** (1)
</dt> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (2)
</dt> <dt>

<span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Критическая** (3)
</dt> </dl>

</dd> <dt>

**ReplicationLatency**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общая задержка репликации при передаче данных в систему узла восстановления (в секундах).

</dd> <dt>

**репликатионмисскаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество пропущенных циклов репликации. Это может быть вызвано высокой нагрузкой, сетевыми проблемами или ошибками репликации.

</dd> <dt>

**репликатионсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общий объем данных репликации, передаваемых в систему узла восстановления в байтах.

</dd> <dt>

**репликатионсукцесскаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общее число успешных репликаций для виртуальной машины.

</dd> <dt>

**стартстатистиктиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время в формате UTC, когда служба реплики Hyper-V приступила к сбору данных статистики репликации.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


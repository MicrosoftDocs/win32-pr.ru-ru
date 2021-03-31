---
description: Представляет коллекцию виртуальных систем.
ms.assetid: acf51beb-1103-43a4-8dc5-1a7f2a0482be
title: Класс Msvm_VirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCollection
- Msvm_VirtualSystemCollection.CollectionID
- Msvm_VirtualSystemCollection.ElementName
- Msvm_VirtualSystemCollection.LastApplyConsistencyLevel
- Msvm_VirtualSystemCollection.LastApplyVirtualMachineIds
- Msvm_VirtualSystemCollection.LastApplyTime
- Msvm_VirtualSystemCollection.FailedOverReplicationType
- Msvm_VirtualSystemCollection.ReplicationMode
- Msvm_VirtualSystemCollection.ReplicationState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a9746356744f2743a8d6656ef4c61044223be113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423690"
---
# <a name="msvm_virtualsystemcollection-class"></a>\_Класс мсвм виртуалсистемколлектион

Представляет коллекцию виртуальных систем.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCollection : CIM_CollectionOfMSEs
{
  string   CollectionID;
  string   ElementName;
  uint16   LastApplyConsistencyLevel;
  String   LastApplyVirtualMachineIds[];
  DateTime LastApplyTime;
  uint16   FailedOverReplicationType;
  uint16   ReplicationMode;
  uint16   ReplicationState;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистемколлектион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалсистемколлектион** имеет следующие свойства.

<dl> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Уникальная идентификация объекта коллекции.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Определяемое пользователем имя коллекции. Обратите внимание, что это не обязательно должно быть уникальным.

</dd> <dt>

**фаиледоверрепликатионтипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип отработки отказа, который был выполнен для коллекции виртуальных систем.

> [!Note]  
> Добавлено в Windows 10 версии 1703.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Нет** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Обычный** (1)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Запланировано** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ластаппликонсистенцилевел**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уровень согласованности последнего примененного разностного изменения.

> [!Note]  
> Добавлено в Windows 10 версии 1703.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>С **совместимостью приложений** (1)


</dt> <dd>

Последняя примененная Дельта указывает на момент времени, когда виртуальная система находилась в состоянии совместимости с приложениями.

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Отказоустойчивость (2** )


</dt> <dd>

Последняя примененная Дельта указывает на момент времени, когда виртуальная система находилась в состоянии отказоустойчивости.

</dd> <dt>

<span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>

<span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Противоречивое аварийное завершение группы** (3)


</dt> <dd>

Последняя примененная Дельта указывает на момент времени, когда группа находилась в состоянии сбоя.

</dd> </dl>

</dd> <dt>

**ластапплитиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время, когда последняя репликация применяется к восстановлению для коллекции виртуальных систем.

> [!Note]  
> Добавлено в Windows 10 версии 1703.

 

</dd> <dt>

**ластаппливиртуалмачинеидс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив идентификаторов виртуальных машин, которые были успешно применены при последнем цикле применения.

> [!Note]  
> Добавлено в Windows 10 версии 1703.

 

</dd> <dt>

**ReplicationMode**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип репликации для коллекции виртуальных систем.

> [!Note]  
> Добавлено в Windows 10 версии 1703.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Нет** (0)


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

**Основной** (1)


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

**Реплика** (2)


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

**Тестовая реплика** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Состояние репликации для коллекции виртуальных систем.

> [!Note]  
> Добавлено в Windows 10 версии 1703.

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

**Готово к репликации** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

**Ожидание завершения начальной репликации** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

**Репликация** (3)


</dt> <dd></dd> <dt>

<span id="Failover_initiated"></span><span id="failover_initiated"></span><span id="FAILOVER_INITIATED"></span>

**Инициирована отработка отказа** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

**Восстановлено** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

**Зафиксировано** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

**Приостановлено** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Критическая** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

**Ожидание запуска повторной синхронизации** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

Повторная **Синхронизация** (10)


</dt> <dd></dd> <dt>

<span id="Planned_failover_initiatedRepurpose_initiatedTest_failover_initiatedPartially_enabled"></span><span id="planned_failover_initiatedrepurpose_initiatedtest_failover_initiatedpartially_enabled"></span><span id="PLANNED_FAILOVER_INITIATEDREPURPOSE_INITIATEDTEST_FAILOVER_INITIATEDPARTIALLY_ENABLED"></span>

**Плановая отработка отказа Инитиатедрепурпосе инитиатедтест отработка отказа включена** (11)


</dt> <dd></dd> <dt>

<span id="Partially_disabled"></span><span id="partially_disabled"></span><span id="PARTIALLY_DISABLED"></span>

**Частично отключено** (12)


</dt> <dd></dd> <dt>

<span id="Partially_recovered"></span><span id="partially_recovered"></span><span id="PARTIALLY_RECOVERED"></span>

**Частично восстановлено** (13)


</dt> <dd></dd> <dt>



 (14)


</dt> <dd></dd> <dt>



 (15)


</dt> <dd></dd> <dt>



 (16)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_КОЛЛЕКТИОНОФМСЕС CIM**](cim-collectionofmses.md)
</dt> </dl>

 


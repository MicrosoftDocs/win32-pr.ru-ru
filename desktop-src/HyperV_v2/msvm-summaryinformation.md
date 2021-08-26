---
description: Используется в методах Жетсуммаринформатион и Жетдефинитионфилесуммаринформатион \_ класса мсвм виртуалсистемманажементсервице для быстрого получения общих сведений, связанных с виртуальной машиной или моментальным снимком.
ms.assetid: 8D188BB2-4A56-4738-94DD-64D9F9B90B73
title: Класс Msvm_SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformation
- Msvm_SummaryInformation.InstanceID
- Msvm_SummaryInformation.AllocatedGPU
- Msvm_SummaryInformation.Shielded
- Msvm_SummaryInformation.AsynchronousTasks
- Msvm_SummaryInformation.CreationTime
- Msvm_SummaryInformation.ElementName
- Msvm_SummaryInformation.EnabledState
- Msvm_SummaryInformation.OtherEnabledState
- Msvm_SummaryInformation.GuestOperatingSystem
- Msvm_SummaryInformation.HealthState
- Msvm_SummaryInformation.Heartbeat
- Msvm_SummaryInformation.MemoryUsage
- Msvm_SummaryInformation.MemoryAvailable
- Msvm_SummaryInformation.AvailableMemoryBuffer
- Msvm_SummaryInformation.SwapFilesInUse
- Msvm_SummaryInformation.Name
- Msvm_SummaryInformation.Notes
- Msvm_SummaryInformation.Version
- Msvm_SummaryInformation.NumberOfProcessors
- Msvm_SummaryInformation.OperationalStatus
- Msvm_SummaryInformation.ProcessorLoad
- Msvm_SummaryInformation.ProcessorLoadHistory
- Msvm_SummaryInformation.Snapshots
- Msvm_SummaryInformation.StatusDescriptions
- Msvm_SummaryInformation.ThumbnailImage
- Msvm_SummaryInformation.ThumbnailImageHeight
- Msvm_SummaryInformation.ThumbnailImageWidth
- Msvm_SummaryInformation.UpTime
- Msvm_SummaryInformation.ReplicationState
- Msvm_SummaryInformation.ReplicationStateEx
- Msvm_SummaryInformation.ReplicationHealth
- Msvm_SummaryInformation.ReplicationHealthEx
- Msvm_SummaryInformation.ReplicationMode
- Msvm_SummaryInformation.TestReplicaSystem
- Msvm_SummaryInformation.ApplicationHealth
- Msvm_SummaryInformation.IntegrationServicesVersionState
- Msvm_SummaryInformation.MemorySpansPhysicalNumaNodes
- Msvm_SummaryInformation.ReplicationProviderId
- Msvm_SummaryInformation.EnhancedSessionModeState
- Msvm_SummaryInformation.VirtualSwitchNames
- Msvm_SummaryInformation.VirtualSystemSubType
- Msvm_SummaryInformation.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1f7cefc27c0e4adc507276d118bcca95c274d121
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886614"
---
# <a name="msvm_summaryinformation-class"></a>\_Класс мсвм SummaryInformation

Используется в методах [**жетсуммаринформатион**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) и [**жетдефинитионфилесуммаринформатион**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) для быстрого получения общих сведений, связанных с виртуальной машиной или моментальным снимком.

Следующий синтаксис представляет собой упрощенный код MOF-файл (MOF).

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformation : Msvm_SummaryInformationBase
{
  string                       InstanceID;
  string                       AllocatedGPU;
  boolean                      Shielded;
  CIM_ConcreteJob              AsynchronousTasks[];
  DateTime                     CreationTime;
  string                       ElementName;
  uint16                       EnabledState;
  string                       OtherEnabledState;
  string                       GuestOperatingSystem;
  uint16                       HealthState;
  uint16                       Heartbeat;
  uint64                       MemoryUsage;
  sint32                       MemoryAvailable;
  sint32                       AvailableMemoryBuffer;
  boolean                      SwapFilesInUse;
  string                       Name;
  string                       Notes;
  string                       Version;
  uint16                       NumberOfProcessors;
  uint16                       OperationalStatus[];
  uint16                       ProcessorLoad;
  uint16                       ProcessorLoadHistory[];
  CIM_VirtualSystemSettingData Snapshots[];
  string                       StatusDescriptions[];
  uint8                        ThumbnailImage[];
  uint16                       ThumbnailImageHeight;
  uint16                       ThumbnailImageWidth;
  uint64                       UpTime;
  uint16                       ReplicationState;
  uint16                       ReplicationStateEx[];
  uint16                       ReplicationHealth;
  uint16                       ReplicationHealthEx[];
  uint16                       ReplicationMode;
  CIM_ComputerSystem       REF TestReplicaSystem;
  uint16                       ApplicationHealth;
  uint16                       IntegrationServicesVersionState;
  boolean                      MemorySpansPhysicalNumaNodes;
  string                       ReplicationProviderId[];
  uint16                       EnhancedSessionModeState;
  string                       VirtualSwitchNames[];
  string                       VirtualSystemSubType;
  string                       HostComputerSystemName;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ SummaryInformation** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ SummaryInformation** имеет следующие свойства.

<dl> <dt>

**аллокатедгпу**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор физического графического процессора, выделенного для этой виртуальной машины. Это свойство применяется только к виртуальным машинам, использующим RemoteFX.

</dd> <dt>

**аппликатионхеалс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние работоспособности приложения для виртуальной машины. Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.

<dt>

<span id="OK"></span><span id="ok"></span>

**ОК** (2)


</dt> <dd></dd> <dt>

<span id="Application_Critical"></span><span id="application_critical"></span><span id="APPLICATION_CRITICAL"></span>

**Критическое для приложения** (32782)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (32896)


</dt> <dd></dd> </dl>

</dd> <dt>

**асинчронаустаскс**
</dt> <dd> <dl> <dt>

Тип данных: массив **CIM \_ конкретежоб**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Массив экземпляров [**мсвм \_ конкретежоб**](msvm-concretejob.md) , которые представляют любые асинхронные операции, связанные с виртуальной машиной, выполняемой в данный момент. Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.

</dd> <dt>

**аваилаблемеморибуффер**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Процент доступной памяти буфера для виртуальной машины. Если для виртуальной машины включена динамическая память, это свойство представляет отношение объема доступного буфера памяти к идеальному буферу памяти для виртуальной машины. Идеальный размер буфера памяти настраивается с помощью свойства **таржетмеморибуффер** класса [**\_ меморисеттингдата мсвм**](msvm-memorysettingdata.md) .

Это свойство является недопустимым для экземпляров класса **мсвм \_ SummaryInformation** , представляющих виртуальные машины, для которых не включена динамическая память.

Это свойство является недопустимым для экземпляров класса **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время создания виртуальной машины или моментального снимка.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя виртуальной машины или моментального снимка.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние виртуальной машины или моментального снимка. Возможные значения см. в свойстве **EnabledState** класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) .

</dd> <dt>

**енханцедсессионмодестате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, разрешены ли для узла подключения в расширенном режиме, и если это разрешено, независимо от того, доступны ли они для виртуальной машины.

**Windows 8.1:** это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

**Разрешено и доступно** (2)


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

**Не разрешено** (3)


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

**Разрешено, но недоступно** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**гуестоператингсистем**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя гостевой операционной системы (если доступно). Если эта информация недоступна, значение этого свойства равно **null**. Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние работоспособности виртуальной машины. Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.

</dd> <dt>

**Периодический сигнал**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние пульса для виртуальной машины. Дополнительные сведения см. в документации по свойству [**статусдескриптионс**](msvm-heartbeatcomponent.md) класса **мсвм \_ хеартбеаткомпонент** . Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.

<dl> <dt>

<span id="OK"></span><span id="ok"></span>**ОК** (2)
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (6)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (12)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (13)
</dt> </dl>

</dd> <dt>

**хосткомпутерсистемнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя компьютера, на котором размещена эта виртуальная машина.

> [!Note]  
> Добавлено в Windows 10.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ манажеделемент. InstanceId"), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID — это необязательное свойство, которое можно использовать для непрозрачного и уникального определения экземпляра этого класса в области действия экземпляра пространства имен. Различные подклассы этого класса могут переопределять это свойство, чтобы сделать его обязательным, или ключ. Такие подклассы также могут изменять предпочтительные алгоритмы, чтобы обеспечить уникальность, определенную ниже.

Чтобы обеспечить уникальность в пространстве имен, значение InstanceID должно быть создано с использованием следующего "предпочтительного" алгоритма:

&lt;OrgID &gt; : &lt; LocalId&gt;

Где &lt; OrgID &gt; и &lt; LocalId &gt; разделяются двоеточием (:), а &lt; OrgID &gt; должны включать уникальное имя, которое принадлежит бизнес-сущности, создающей или ОПРЕДЕЛЯЮЩей InstanceId или зарегистрированный идентификатор, назначенный бизнес-сущностю распознаваемым глобальным центром сертификации. (Это требование аналогично <Schema Name> \_ <Class Name> Структура имен классов схемы.) Кроме того, чтобы обеспечить уникальность, &lt; OrgID &gt; не должен содержать двоеточия (:). При использовании этого алгоритма первое двоеточие должно появиться в идентификаторе InstanceID между &lt; OrgID &gt; и &lt; LocalId &gt; .

&lt;LocalID &gt; выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых (реальных) элементов. Если не равно NULL и указанный выше алгоритм не используется, определяющая сущность должна гарантировать, что результирующий InstanceID не будет повторно использоваться в любых InstanceId, созданных этим или другими поставщиками для пространства имен данного экземпляра.

Если для экземпляров, определяемых DMTF, не задано значение null, необходимо использовать "предпочтительный" алгоритм, если для &lt; OrgID &gt; задано значение CIM.

> [!Note]  
> Добавлено в Windows 10.

 

</dd> <dt>

**интегратионсервицесверсионстате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, являются ли установленные на виртуальной машине Службы Integration Services актуальными.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="UpToDate"></span><span id="uptodate"></span><span id="UPTODATE"></span>

**Уптодате** (1)


</dt> <dd></dd> <dt>

<span id="Mismatch"></span><span id="mismatch"></span><span id="MISMATCH"></span>

**Несоответствие** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**меморяваилабле**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Процент от объема текущей памяти, доступной виртуальной машине. Если для виртуальной машины включена динамическая память, это свойство представляет отношение объема доступной памяти виртуальной машины к общему объему физической памяти, назначенному виртуальной машине. Если виртуальная машина не имеет доступной памяти, это свойство будет отрицательным и будет содержать отношение объема памяти, необходимой для виртуальной машины, к общему объему физической памяти, назначенному виртуальной машине.

Это свойство является недопустимым для экземпляров класса **мсвм \_ SummaryInformation** , представляющих виртуальные машины, для которых не включена динамическая память.

Это свойство является недопустимым для экземпляров класса **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.

</dd> <dt>

**мемориспансфисикалнуманодес**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, охватывает ли память один или несколько узлов виртуальной машины (NUMA) виртуальной неоднородным доступом памяти на нескольких физических узлах NUMA системы размещающего компьютера. Содержит **значение true** , если память охватывает несколько физических узлов NUMA, или **false** в противном случае.

</dd> <dt>

**MemoryUsage**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее использование памяти виртуальной машины (в мегабайтах). Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.

</dd> <dt>

**имя**;
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальное имя виртуальной машины или моментального снимка.

</dd> <dt>

**Примечания**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Примечания, связанные с виртуальной машиной или моментальным снимком.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общее число виртуальных процессоров, выделенных виртуальной машине или моментальному снимку.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Текущие рабочие состояния виртуальной машины. Возможные значения см. в свойстве **OperationalStatus** класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) .

</dd> <dt>

**осеренабледстате**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1. Это свойство будет иметь значение **null** , если **EnabledState** имеет любое значение, отличное от 1.

</dd> <dt>

**процессорлоад**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее использование процессора виртуальной машины в процентах. Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.

</dd> <dt>

**процессорлоадхистори**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Массив из предыдущих 100 примеров использования процессора (в процентах) для виртуальной машины. Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.

</dd> <dt>

**репликатионхеалс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**мсвм \_ SummaryInformation**.**Репликатионхеалсекс**")
</dt> </dl>

Работоспособность репликации для виртуальной машины. Возможные значения см. в свойстве **репликатионхеалс** класса [**\_ ComputerSystem объекта мсвм**](msvm-computersystem.md) .

> [!Note]  
> Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте **репликатионхеалсекс**.

 

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Неприменимо** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**ОК** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Предупреждение** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Критическая** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**репликатионхеалсекс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Массив значений работоспособности репликации для различных отношений репликации виртуальной машины. Возможные значения см. в свойстве **репликатионхеалс** класса [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) .

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Неприменимо** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**ОК** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Предупреждение** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Критическая** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationMode**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип репликации для виртуальной машины. Возможные значения см. в свойстве **ReplicationMode** класса [**\_ ComputerSystem объекта мсвм**](msvm-computersystem.md) .

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


</dt> <dd></dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

**Расширенная реплика** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationProviderId**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Для виртуальной машины основной или расширенной реплики это идентификатор первичного поставщика репликации. Для реплики виртуальной машины, если включена расширенная репликация, это идентификатор поставщика для расширенной связи.

**Windows 8.1:** это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**мсвм \_ SummaryInformation**.**Репликатионстатикс**")
</dt> </dl>

Состояние репликации для виртуальной машины. Возможные значения см. в свойстве **ReplicationState** класса [**\_ ComputerSystem объекта мсвм**](msvm-computersystem.md) .

> [!Note]  
> Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте **репликатионстатикс**.

 

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

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

**Синхронизированная репликация завершена** (4)


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

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

**Повторная синхронизация приостановлена** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

**Выполняется отработка отказа** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**репликатионстатикс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Массив значений состояния репликации для различных отношений репликации виртуальной машины. Возможные значения см. в свойстве **ReplicationState** класса [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) .

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Готово к репликации** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Ожидание завершения начальной репликации** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Репликация** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Синхронизированная репликация завершена** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Восстановлено** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Зафиксировано** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Приостановлено** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Ожидание запуска повторной синхронизации** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>Повторная **Синхронизация** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Повторная синхронизация приостановлена** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Выполняется отработка отказа** (12)


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Выполняется восстановление размещения** (13)


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Восстановление размещения завершено** (14)


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Выполняется обновление диска** (15)


</dt> <dd>

> [!Note]  
> добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Критическое обновление диска** (16)


</dt> <dd>

> [!Note]  
> добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (17)


</dt> <dd>

> [!Note]  
> добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Выполняется перецель репликации** (18)


</dt> <dd>

> [!Note]  
> добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Подготовлено к репликации синхронизации** (19)


</dt> <dd>

> [!Note]  
> добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Подготовлено к групповой отмене репликации** (20)


</dt> <dd>

> [!Note]  
> добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Фиредрилл выполняется** (21)


</dt> <dd>

> [!Note]  
> добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**Экранирование**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли экранирование для виртуальной машины.

> [!Note]  
> добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> <dt>

**Моментальные снимки**
</dt> <dd> <dl> <dt>

Тип данных: массив **CIM \_ виртуалсистемсеттингдата**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Массив экземпляров [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , представляющих моментальные снимки для виртуальной машины. Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.

</dd> <dt>

**статусдескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Строки, описывающие соответствующие значения массива **OperationalStatus** . Это соответствует свойству **статусдескриптионс** класса [**\_ ComputerSystem мсвм**](msvm-computersystem.md) .

</dd> <dt>

**свапфилесинусе**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, активна ли подкачка второго уровня. Содержит **значение true** , если подкачка на второй уровень является активной, или **false** в противном случае.

</dd> <dt>

**тестрепликасистем**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ ComputerSystem**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину тестовой реплики для виртуальной машины. Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.

</dd> <dt>

**сумбнаилимаже**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **октетстринг**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексируется"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**мсвм \_ SummaryInformation**.**Сумбнаилимажевидс**","**мсвм \_ SummaryInformation**.**Сумбнаилимажехеигхт**")
</dt> </dl>

Массив, содержащий небольшой эскиз рабочего стола для виртуальной машины или моментального снимка в формате RGB565.

</dd> <dt>

**сумбнаилимажехеигхт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**мсвм \_ SummaryInformation**.**Сумбнаилимаже**")
</dt> </dl>

Высота изображения в пикселях свойства Сумбнаилимаже.

> [!Note]  
> Добавлено в Windows 10.

 

</dd> <dt>

**сумбнаилимажевидс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**мсвм \_ SummaryInformation**.**Сумбнаилимаже**")
</dt> </dl>

Ширина изображения в пикселях свойства Сумбнаилимаже.

> [!Note]  
> Добавлено в Windows 10.

 

</dd> <dt>

**Просто**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество времени, прошедшее с момента последней загрузки виртуальной машины. Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Версия виртуальной системы в формате "основная. Дополнительная", например "2,0".

> [!Note]  
> Добавлено в Windows 10.

 

</dd> <dt>

**виртуалсвитчнамес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Строки, указывающие понятные имена виртуальных коммутаторов, к которым подключена виртуальная машина.

**Windows 8.1:** это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Подтип виртуальной системы.

**Windows 8.1:** это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft: Hyper-V: подтип: 1** ()


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft: Hyper-V: подтип: 2** ()


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ SummaryInformation мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ суммаринформатионбасе**](msvm-summaryinformationbase.md)
</dt> <dt>

[Классы виртуальных систем](virtual-system-classes.md)
</dt> </dl>

 


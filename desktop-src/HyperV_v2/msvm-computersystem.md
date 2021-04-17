---
description: Представляет физическую систему компьютера или виртуальную машину.
ms.assetid: 1db9e169-1466-4898-ab95-e9d622fe43cb
title: Класс Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem
- Msvm_ComputerSystem.SetPowerState
- Msvm_ComputerSystem.InstanceID
- Msvm_ComputerSystem.Caption
- Msvm_ComputerSystem.Description
- Msvm_ComputerSystem.ElementName
- Msvm_ComputerSystem.InstallDate
- Msvm_ComputerSystem.OperationalStatus
- Msvm_ComputerSystem.StatusDescriptions
- Msvm_ComputerSystem.Status
- Msvm_ComputerSystem.HealthState
- Msvm_ComputerSystem.CommunicationStatus
- Msvm_ComputerSystem.DetailedStatus
- Msvm_ComputerSystem.OperatingStatus
- Msvm_ComputerSystem.PrimaryStatus
- Msvm_ComputerSystem.EnabledState
- Msvm_ComputerSystem.OtherEnabledState
- Msvm_ComputerSystem.RequestedState
- Msvm_ComputerSystem.EnabledDefault
- Msvm_ComputerSystem.TimeOfLastStateChange
- Msvm_ComputerSystem.AvailableRequestedStates
- Msvm_ComputerSystem.TransitioningToState
- Msvm_ComputerSystem.CreationClassName
- Msvm_ComputerSystem.Name
- Msvm_ComputerSystem.PrimaryOwnerName
- Msvm_ComputerSystem.PrimaryOwnerContact
- Msvm_ComputerSystem.Roles
- Msvm_ComputerSystem.NameFormat
- Msvm_ComputerSystem.OtherIdentifyingInfo
- Msvm_ComputerSystem.IdentifyingDescriptions
- Msvm_ComputerSystem.Dedicated
- Msvm_ComputerSystem.OtherDedicatedDescriptions
- Msvm_ComputerSystem.ResetCapability
- Msvm_ComputerSystem.PowerManagementCapabilities
- Msvm_ComputerSystem.OnTimeInMilliseconds
- Msvm_ComputerSystem.ProcessID
- Msvm_ComputerSystem.TimeOfLastConfigurationChange
- Msvm_ComputerSystem.NumberOfNumaNodes
- Msvm_ComputerSystem.ReplicationState
- Msvm_ComputerSystem.ReplicationHealth
- Msvm_ComputerSystem.ReplicationMode
- Msvm_ComputerSystem.FailedOverReplicationType
- Msvm_ComputerSystem.LastReplicationType
- Msvm_ComputerSystem.LastApplicationConsistentReplicationTime
- Msvm_ComputerSystem.LastReplicationTime
- Msvm_ComputerSystem.LastSuccessfulBackupTime
- Msvm_ComputerSystem.EnhancedSessionModeState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae36179e14b584bad4e68350e27d485cdc10c42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556877"
---
# <a name="msvm_computersystem-class"></a>\_Класс мсвм ComputerSystem

Представляет физическую систему компьютера или виртуальную машину.

Чтобы получить сведения для VMMS, используйте класс [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) .

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 1;
  uint16   PowerManagementCapabilities[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
  uint16   NumberOfNumaNodes;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   ReplicationMode;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  DateTime LastApplicationConsistentReplicationTime;
  DateTime LastReplicationTime;
  DateTime LastSuccessfulBackupTime;
  uint16   EnhancedSessionModeState;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ ComputerSystem** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **мсвм \_ ComputerSystem** содержит следующие методы.



| Метод                                                                                         | Описание                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**инжектнонмаскаблеинтеррупт**](injectnonmaskableinterrupt-msvm-computersystem.md)           | Внедряет немаскируемое прерывание в виртуальную машину. Этот метод поддерживается только для экземпляров класса **\_ ComputerSystem мсвм** , представляющих виртуальную машину.<br/> **Windows 8.1:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.<br/>                                    |
| [**рекуестрепликатионстатечанже**](msvm-computersystem-requestreplicationstatechange.md)     | Запрашивает изменение состояния репликации виртуальной машины на указанное значение. Этот метод поддерживается только для экземпляров класса **\_ ComputerSystem мсвм** , представляющих виртуальную машину.<br/>                                                                                                        |
| [**рекуестрепликатионстатечанжеекс**](msvm-requestreplicationstatechangeex-computersystem.md) | Запрашивает изменение состояния репликации виртуальной машины на указанное значение. Этот метод поддерживается только для экземпляров класса **\_ ComputerSystem мсвм** , представляющих виртуальную машину.<br/> **Windows 8.1:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.<br/> |
| [**Равен**](requeststatechange-msvm-computersystem.md)                           | Запрашивает изменение состояния виртуальной машины. Этот метод поддерживается только для экземпляров класса **\_ ComputerSystem мсвм** , представляющих виртуальную машину.<br/>                                                                                                                                           |
| **SetPowerState**                                                                              | Этот метод не поддерживается.<br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a>Свойства

Класс **мсвм \_ ComputerSystem** имеет следующие свойства.

<dl> <dt>

**аваилаблерекуестедстатес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния. Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния объекта [**\_ енабледлогикалелемент CIM**](/previous-versions//cc136818(v=vs.85)) . Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния. Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.

Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (.. )
</dt> </dl>

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) и будет содержать одно из следующих значений.



| Значение                                                                                                | Значение                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>"Виртуальная машина"</dt> </dl>         | Экземпляр представляет виртуальную машину.<br/>    |
| <dl> <dt>"Система размещения компьютера"</dt> </dl> | Экземпляр представляет компьютер размещения.<br/> |



 

</dd> <dt>

**коммуникатионстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает способность инструментирования взаимодействовать с базовым управляемым элементом. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса или подкласса, используемого при создании экземпляра. Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение "мсвм \_ ComputerSystem".

</dd> <dt>

**Выделенные**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, является ли компьютерная система специальной (выделенной для конкретного использования), а не универсальной системой. Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение 0 (не выделено).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и будет содержать одно из следующих значений.



| Значение                                                                                                          | Значение                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>«Система виртуального компьютера Microsoft»</dt> </dl> | Экземпляр представляет виртуальную машину.<br/>    |
| <dl> <dt>«Microsoft Hosting Computer System»</dt> </dl> | Экземпляр представляет компьютер размещения.<br/> |



 

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дополняет свойство **примаристатус** дополнительными сведениями о состоянии. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда устанавливается в качестве отображаемого имени компьютера для виртуальной машины или NetBIOS-имени операционной системы управления.

</dd> <dt>

**енабледдефаулт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Конфигурация по умолчанию или запуска администратора для включенного состояния элемента. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и будет иметь одно из следующих значений.

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Включено, но отключено** (6)
</dt> </dl>

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Включенные и отключенные состояния элемента. Это свойство также может указывать переходы между этими запрошенными состояниями. Это свойство наследуется от класса [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и имеет значение 2 (включено) для физического компьютера или одно из следующих значений для виртуальной машины. Графическое представление этих состояний см. в разделе Примечания.



| Значение                                                                                                                                                                                                                                                                       | Значение                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Неизвестно**</dt> <dt>0</dt> </dl>                                                 | Не удалось определить состояние элемента.<br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Другое**</dt> <dt>1</dt> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Включено**</dt> <dt>2</dt> </dl>                                                 | Элемент работает.<br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Отключено**</dt> <dt>3</dt> </dl>                                             | Элемент отключен.<br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Завершение работы**</dt> <dt>4</dt> </dl>                         | Элемент находится в процессе перехода в отключенное состояние.<br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Неприменимо**</dt> <dt>5</dt> </dl>                     | Элемент не поддерживает включение или отключение.<br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Включено, но отключено**</dt> <dt>6</dt> </dl> | Элемент может выполнять команды, и при этом будут удалены все новые запросы.<br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**В тесте**</dt> <dt>7</dt> </dl>                                                 | Элемент находится в состоянии теста.<br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <dt>**Отложено**</dt> <dt>8</dt> </dl>                                             | Элемент может быть выполнен с помощью команд, но он будет ставить в очередь новые запросы.<br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <dt>**Замораживание**</dt> <dt>9</dt> </dl>                                                 | Элемент включен, но в режиме с ограниченным доступом. Поведение элемента аналогично включенному состоянию (2), но обрабатывает только ограниченный набор команд. Все остальные запросы помещаются в очередь.<br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**Начало**</dt> <dt>10</dt> </dl>                                            | Элемент находится в процессе перехода в состояние Enabled (2). Новые запросы помещаются в очередь.<br/>                                                                                                             |



 

</dd> <dt>

**енханцедсессионмодестате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает текущее состояние режима расширенного сеанса на виртуальной машине.

Поставщик WMI Hyper-V создает [**\_ \_ инстанцемодификатионевент**](/windows/desktop/WmiSdk/--instancemodificationevent) каждый раз при изменении **енханцедсессионмодестате** класса **\_ ComputerSystem мсвм** . Если активный сеанс вмконнектион получает **\_ \_ инстанцемодификатионевент**, он пытается переключиться в режим расширенного сеанса, если пользователь включил этот параметр.

**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

**Енханцедсессионмодестате** может принимать одно из следующих значений:

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Разрешено и доступно** (2)


</dt> <dd>

Расширенный режим разрешен и доступен на виртуальной машине.

</dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Не разрешено** (3)


</dt> <dd>

Расширенный режим не разрешен на виртуальной машине.

</dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Разрешено, но недоступно** (6)


</dt> <dd>

Расширенный режим разрешен и в настоящее время недоступен на виртуальной машине.

</dd> </dl>

</dd> <dt>

**фаиледоверрепликатионтипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).**Фаиледоверрепликатионтипе**")
</dt> </dl>

Тип точки данных восстановления, которая была применена во время операции отработки отказа.

> [!Note]  
> Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте свойство с тем же именем в классе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , чтобы получить значение для первичной или расширенной связи.

 

Возможны следующие значения:

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Нет** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Обычный** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

С **совместимостью приложений** (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Запланировано** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает текущую работоспособность элемента. Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.

При возникновении критической ошибки просмотрите подробные сведения в журнале событий. Свойство **EnabledState** также может содержать дополнительные сведения. Например, если место на диске критически низкий, значение **HealthState** равно 25, виртуальная машина будет приостановлена, а параметру **EnabledState** будет присвоено значение 32768 (приостановлено).

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).



| Значение                                                                                                                                                                                                                                                            | Значение                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**ОК**</dt> <dt>5</dt> </dl>                                                                               | Виртуальная машина полностью работоспособна и работает в нормальных рабочих параметрах и без ошибок.<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Серьезный сбой**</dt> <dt>20</dt> </dl>             | Произошла серьезная ошибка виртуальной машины. Это значение используется, когда на одном или нескольких дисках, содержащих виртуальные жесткие диски виртуальной машины, недостаточно места на диске, а виртуальная машина приостановлена.<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Критический сбой**</dt> <dt>25</dt> </dl> | Элемент нефункциональный, и восстановление может быть невозможным. Это может означать, что рабочий процесс для виртуальной машины (Vmwp.exe) не отвечает на запросы контроля или информации или что на одном или нескольких дисках, содержащих виртуальные жесткие диски виртуальной машины, недостаточно места на диске.<br/> |



 

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время создания конфигурации виртуальной машины для виртуальной машины или **значение NULL** для операционной системы управления. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

В Windows 8 существует единственный экземпляр [**репликатионсеттингдата**](msvm-replicationsettingdata.md) для каждой компьютерной системы или виртуальной машины. Для Windows 8.1 виртуальная машина восстановления имеет два экземпляра **репликатионсеттингдата**. Это изменение отличает и связывает данные настройки с отношением репликации.



| Имя свойства  | Значение Windows 8               | Windows 8.1 значение                          |
|----------------|-------------------------------|--------------------------------------------|
| **InstanceID** | Microsoft: <vmguid> \\ HVR | Microsoft: <vmguid> \\ HVR \\<0/1> |



 

В Windows 8.1 значение 0 указывает на первичный, а 1 — на расширенную репликацию. Дополнительные сведения о расширенной репликации см. в разделе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).

</dd> <dt>

**ластаппликатионконсистентрепликатионтиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).**Ластаппликатионконсистентрепликатионтиме**")
</dt> </dl>

Время получения последней репликации, соответствующей приложению, для виртуальной машины.

> [!Note]  
> Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте свойство с тем же именем в классе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , чтобы получить значение для первичной или расширенной связи.

 

</dd> <dt>

**ластрепликатионтиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).**Ластрепликатионтиме**")
</dt> </dl>

Время, когда при восстановлении виртуальной машины получается Последняя репликация.

> [!Note]  
> Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте свойство с тем же именем в классе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , чтобы получить значение для первичной или расширенной связи.

 

</dd> <dt>

**ластрепликатионтипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).**Ластрепликатионтипе**")
</dt> </dl>

Тип последней репликации, полученной для виртуальной машины.

> [!Note]  
> Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте свойство с тем же именем в классе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , чтобы получить значение для первичной или расширенной связи.

 

Возможны следующие значения:

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Нет** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Обычный** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

С **совместимостью приложений** (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Запланировано** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ластсукцессфулбаккуптиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время, когда последняя успешная архивация была завершена для виртуальной машины.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Метка, по которой известен объект. Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение "*GUID*".

</dd> <dt>

**намеформат**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, которая определяет, как было создано системное имя с использованием эвристики подкласса. Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.

</dd> <dt>

**NumberOfNumaNodes**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество узлов (NUMA) неоднородным доступом системы. Если **мсвм \_ ComputerSystem** представляет компьютер размещения, это свойство содержит количество физических узлов NUMA. Когда **мсвм \_ ComputerSystem** представляет виртуальную машину, это свойство содержит число виртуальных узлов NUMA, которые представлены в гостевой операционной системе с помощью таблицы СОПОСТАВЛЕНИЯ системных ресурсов ACPI (СРАТ).

</dd> <dt>

**онтимеинмиллисекондс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды")
</dt> </dl>

Для виртуальной машины это свойство указывает время в миллисекундах, прошедшее с момента последнего включения, сброса или восстановления компьютера. В этот раз исключается время, в течение которого виртуальная машина находилась в приостановленном состоянии. Для операционной системы управления это свойство имеет значение **null**.

</dd> <dt>

**оператингстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** . Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив, содержащий текущие состояния объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement). Значение с нулевым индексом (0) является одним из следующих значений.



| Значение                                                                                                                                                                                                                                                                   | Значение                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**ОК**</dt> <dt>2</dt> </dl>                                                                                      | Виртуальная машина работоспособна и работает нормально.<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Снижение уровня работоспособности**</dt> <dt>3</dt> </dl>                                         | Виртуальная машина работает только частично. Это означает, что хранилище, которое содержит конфигурацию, недоступно. Виртуальную машину в этом состоянии можно отключить или удалить. <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**Прогнозный сбой**</dt> <dt>5</dt> </dl> | Виртуальная машина работоспособна, но может завершиться с ошибкой в будущем. Это означает, что недостаточно свободного места в хранилище, содержащем виртуальный жесткий диск виртуальной машины. Виртуальная машина будет приостановлена, если свободное место на диске не станет доступным.<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt>**Остановлено**</dt> <dt>10</dt> </dl>                                            | Это значение не поддерживается. Если виртуальная машина остановлена, свойство **EnabledState** будет иметь значение 3 (отключено).<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**В службе**</dt> <dt>11</dt> </dl>                                | Виртуальная машина обрабатывает запрос.<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>**Неактивность**</dt> <dt>15</dt> </dl>                                            | Это значение не поддерживается. Если виртуальная машина приостановлена или приостановлена, свойство **EnabledState** будет иметь значение 32769 (приостановлено) или 32768 (приостановлено).<br/>                                                                                    |



 

Значение с индексом 1 является необязательным и содержит дополнительные сведения о состоянии. Клиент должен использовать первичное состояние из нулевого индекса (0), чтобы определить, может ли новый запрос выдаться виртуальной машине. Если значение **OperationalStatus** \[ 0 \] равно 2 (ОК), операция, указанная в **OperationalStatus** \[ 1, \] может быть прервана.

Значение в **OperationalStatus** \[ 1 \] имеет одно из следующих значений.



| Значение                                                                                                                                                                                                                                                                                                   | Значение                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**Создание моментального снимка**</dt> <dt>32768</dt> </dl>                                 | Моментальный снимок находится в процессе создания для виртуальной машины.<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <dt>**Применение моментального снимка**</dt> <dt>32769</dt> </dl>                                 | Моментальный снимок находится в процессе применения к виртуальной машине.<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**Удаление моментального снимка**</dt> <dt>32770</dt> </dl>                                 | Моментальный снимок находится в процессе удаления из виртуальной машины.<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**Ожидание запуска**</dt> <dt>32771</dt> </dl>                                     | Виртуальная машина будет запущена после истечения интервала автоматической загрузки.<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**Слияние дисков**</dt> <dt>32772</dt> </dl>                                                 | Выполняется слияние виртуальных жестких дисков из ранее удаленных моментальных снимков.<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**Экспорт виртуальной машины**</dt> <dt>32773</dt> </dl> | Выполняется экспорт виртуальной машины.<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <dt>**Миграция виртуальной машины**</dt> <dt>32774</dt> </dl> | Виртуальная машина переносится с одного физического компьютера на другой.<br/>  |



 

</dd> <dt>

**OtherDedicatedDescriptions**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, описывающая, как или почему система выделяется, когда **выделенный** массив включает значение 2 (другое). Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.

</dd> <dt>

**осеренабледстате**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Состояние виртуальной машины (включено или отключено), если свойство **EnabledState** имеет значение 1 (другое). Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.

</dd> <dt>

**поверманажементкапабилитиес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), но не используется.

</dd> <dt>

**примарйовнерконтакт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, которая указывает, как можно достичь основного владельца системы (например, номер телефона или адрес электронной почты). Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение **null**.

</dd> <dt>

**примарйовнернаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя основного владельца системы. Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение **null**.

</dd> <dt>

**примаристатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Предоставляет сведения о состоянии высокого уровня. Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ProcessID**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор процесса, в котором выполняется эта виртуальная машина. Это значение можно использовать для уникальной идентификации экземпляра Vmwp.exe в системе, где работает виртуальная машина.

</dd> <dt>

**репликатионхеалс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).**Репликатионхеалс**")
</dt> </dl>

Работоспособность репликации для виртуальной машины.

> [!Note]  
> Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте свойство с тем же именем в классе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , чтобы получить значение для первичной или расширенной связи.

 

Возможны следующие значения:

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

Указывает режим репликации для виртуальной машины. Это может быть одно из следующих значений.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Нет** (0)


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Основной** (1)


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Реплика** (2)


</dt> <dd>

Восстановление

</dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Тестовая реплика** (3)


</dt> <dd>

Реплика

</dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Расширенная реплика** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).**ReplicationState**")
</dt> </dl>

Состояние репликации для виртуальной машины.

> [!Note]  
> Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте свойство с тем же именем в классе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , чтобы получить значение для первичной или расширенной связи.

 

Возможны следующие значения:

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


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

**Выполняется восстановление размещения** (13)


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

**Восстановление размещения завершено** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Последнее запрошенное или требуемое состояние виртуальной машины, переданное методу [**RequestStateChange**](requeststatechange-msvm-computersystem.md) , или 12 (неприменимо), если изменение состояния не выполняется. Фактическое состояние элемента представлено параметром **EnabledState**. Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**ресеткапабилити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение 1 (другое).

</dd> <dt>

**Роли**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив строк, описывающих роли, которые система играет в среде информационных технологий. Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение **null**.

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.

</dd> <dt>

**статусдескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **arrayType** ("индексированный")
</dt> </dl>

Массив, содержащий строки, описывающие соответствующие значения массива **OperationalStatus** . Например, если 11 (в службе) — значение, назначенное для **OperationalStatus** \[ 0 \] , то **статусдескриптионс** \[ 0 \] может содержать объяснение, почему виртуальная машина обрабатывает запрос. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**тимеофластконфигуратиончанже**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время последнего изменения файла конфигурации виртуальной машины. Файл конфигурации изменяется во время определенных операций виртуальной машины, а также при добавлении, изменении или удалении любой из параметров виртуальной машины или устройства.

</dd> <dt>

**тимеофластстатечанже**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время последнего изменения включенного состояния элемента. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**транситионингтостате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает целевое состояние, в которое переходит экземпляр. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.

</dd> </dl>

## <a name="remarks"></a>Комментарии

На следующем рисунке показаны значения **EnabledState** .

![Схема состояний для значений enabledstate для Windows Server 2008 R2](images/msvm-computersystem-enabledstate-win2008r2.png)

При изменении свойства класса **\_ ComputerSystem мсвм** поставщик WMI указывает на событие [**\_ \_ инстанцемодификатионевент**](/windows/desktop/WmiSdk/--instancemodificationevent) , описывающее изменения. Предыдущее состояние содержится в свойстве **PreviousInstance** , а новое состояние содержится в свойстве **TargetInstance** . Это событие является асинхронным; к моменту обработки события **\_ \_ инстанцемодификатионевент** свойство **TargetInstance** может не отражать текущее состояние.

Доступ к классу **\_ ComputerSystem мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Примеры

См. раздел [запросы к сетевым объектам](querying-networking-objects.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**CIM \_ ComputerSystem**](cim-computersystem.md)
</dt> <dt>

[**\_\_инстанцемодификатионевент**](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[**Мсвм \_ ComputerSystem (v1)**](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[Классы виртуальных систем](virtual-system-classes.md)
</dt> </dl>

 


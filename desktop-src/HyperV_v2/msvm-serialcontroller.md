---
description: Представляет возможности и управление последовательным контроллером.
ms.assetid: 0F4DCF98-8EE4-4005-ADD5-BA23CB4CBE82
title: Класс Msvm_SerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialController
- Msvm_SerialController.SetPowerState
- Msvm_SerialController.EnableDevice
- Msvm_SerialController.OnlineDevice
- Msvm_SerialController.QuiesceDevice
- Msvm_SerialController.SaveProperties
- Msvm_SerialController.RestoreProperties
- Msvm_SerialController.InstanceID
- Msvm_SerialController.Caption
- Msvm_SerialController.Description
- Msvm_SerialController.ElementName
- Msvm_SerialController.InstallDate
- Msvm_SerialController.Name
- Msvm_SerialController.OperationalStatus
- Msvm_SerialController.StatusDescriptions
- Msvm_SerialController.Status
- Msvm_SerialController.HealthState
- Msvm_SerialController.CommunicationStatus
- Msvm_SerialController.DetailedStatus
- Msvm_SerialController.OperatingStatus
- Msvm_SerialController.PrimaryStatus
- Msvm_SerialController.EnabledState
- Msvm_SerialController.OtherEnabledState
- Msvm_SerialController.RequestedState
- Msvm_SerialController.EnabledDefault
- Msvm_SerialController.TimeOfLastStateChange
- Msvm_SerialController.AvailableRequestedStates
- Msvm_SerialController.TransitioningToState
- Msvm_SerialController.SystemCreationClassName
- Msvm_SerialController.SystemName
- Msvm_SerialController.CreationClassName
- Msvm_SerialController.DeviceID
- Msvm_SerialController.PowerManagementSupported
- Msvm_SerialController.PowerManagementCapabilities
- Msvm_SerialController.Availability
- Msvm_SerialController.StatusInfo
- Msvm_SerialController.LastErrorCode
- Msvm_SerialController.ErrorDescription
- Msvm_SerialController.ErrorCleared
- Msvm_SerialController.OtherIdentifyingInfo
- Msvm_SerialController.PowerOnHours
- Msvm_SerialController.TotalPowerOnHours
- Msvm_SerialController.IdentifyingDescriptions
- Msvm_SerialController.AdditionalAvailability
- Msvm_SerialController.MaxQuiesceTime
- Msvm_SerialController.TimeOfLastReset
- Msvm_SerialController.ProtocolSupported
- Msvm_SerialController.MaxNumberControlled
- Msvm_SerialController.ProtocolDescription
- Msvm_SerialController.Capabilities
- Msvm_SerialController.CapabilityDescriptions
- Msvm_SerialController.MaxBaudRate
- Msvm_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3f1bbc9dabe078751d58875745a789895cb4c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650586"
---
# <a name="msvm_serialcontroller-class"></a>\_Класс мсвм сериалконтроллер

Представляет возможности и управление последовательным контроллером. Последовательные контроллеры — это логические устройства, которые всегда находятся на виртуальной машине и поэтому не распределяются через пул ресурсов. Один экземпляр последовательного контроллера всегда имеется в виртуальной машине. Последовательные контроллеры имеют фиксированное число экземпляров портов. Эта реализация поддерживает два порта на контроллере.

> [!Note]  
> Последовательные контроллеры являются необязательными в [виртуальных машинах поколения 2](virtualization-glossary.md).

 

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialController : CIM_SerialController
{
  string   InstanceID;
  string   Caption = "Serial Controller";
  string   Description = "Microsoft Virtual Serial Controller";
  string   ElementName = "Serial Controller";
  datetime InstallDate;
  string   Name = "Serial Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_SerialController";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 26;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription;
  uint16   Capabilities[] = { 5 };
  string   CapabilityDescriptions[] = { "16550 compatible" };
  uint32   MaxBaudRate = 115200;
  uint16   Security = 3;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ сериалконтроллер** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **мсвм \_ сериалконтроллер** содержит следующие методы.



| Метод                                                                 | Описание                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| **енабледевице**                                                       | Этот метод не поддерживается.<br/> |
| **онлинедевице**                                                       | Этот метод не поддерживается.<br/> |
| **куиесцедевице**                                                      | Этот метод не поддерживается.<br/> |
| [**Равен**](msvm-serialcontroller-requeststatechange.md) | Запрашивает изменение состояния.<br/>      |
| [**Перезапуск**](msvm-serialcontroller-reset.md)                           | Выполняет сброс устройства.<br/>            |
| **ресторепропертиес**                                                  | Этот метод не поддерживается.<br/> |
| **савепропертиес**                                                     | Этот метод не поддерживается.<br/> |
| **SetPowerState**                                                      | Этот метод не поддерживается.<br/> |



 

### <a name="properties"></a>Свойства

Класс **мсвм \_ сериалконтроллер** имеет следующие свойства.

<dl> <dt>

**аддитионалаваилабилити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Любая дополнительная доступность и состояние устройства. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.



| Значение                                                                            | Значение                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>1-6</dt> </dl> |                           |
| <dl> <dt>6</dt> </dl>     | Не применимо<br/> |



 

</dd> <dt>

**Доступность**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Первичная доступность и состояние устройства. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.



| Значение                                                                        | Значение                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>6</dt> </dl> | Не применимо<br/> |



 

</dd> <dt>

**аваилаблерекуестедстатес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** . Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Буферизация и другие возможности последовательного контроллера, которые могут быть встроенными в оборудование микросхемы. Это свойство наследуется от [**CIM \_ сериалконтроллер**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).

</dd> <dt>

**капабилитидескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив строк произвольной формы, предоставляющий более подробные объяснения для любой из функций последовательного контроллера, указанных в массиве **capabilities** . Это свойство наследуется от [**CIM \_ сериалконтроллер**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**коммуникатионстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает способность инструментирования взаимодействовать с базовым управляемым элементом. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)
</dt> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. )
</dt> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса или подкласса, используемого при создании экземпляра. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дополняет свойство **примаристатус** дополнительными сведениями о состоянии. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)
</dt> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)
</dt> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)
</dt> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)
</dt> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. )
</dt> </dl>

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение Microsoft: *<GUID>* .

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**енабледдефаулт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Конфигурация по умолчанию или запуска администратора для включенного состояния элемента. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).



| Значение                                                                        | Значение            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | Активировано<br/> |



 

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Включенные и отключенные состояния элемента. Он также может указывать на переходы между этими запрошенными состояниями. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).



| Значение                                                                        | Значение                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>5</dt> </dl> | Не применимо<br/> |



 

</dd> <dt>

**еррорклеаред**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, что сообщение об ошибке в свойстве **ластерроркоде** теперь отключено. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, которая предоставляет дополнительные сведения об ошибке, записанной в свойстве **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущая работоспособность элемента. Это выражает работоспособность этого элемента, но не обязательно для его подкомпонентов. Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** . Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение **null**.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время создания конфигурации виртуальной машины. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

</dd> <dt>

**ластерроркоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Последний код ошибки, сообщаемый логическим устройством. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**максбаудрате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальная скорость в битах в секунду, поддерживаемая последовательным контроллером. Это свойство наследуется от [**CIM \_ сериалконтроллер**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).

</dd> <dt>

**макснумберконтроллед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное количество напрямую доступных для адресации сущностей, поддерживаемых этим контроллером. Если число неизвестно или неограниченно, следует использовать значение 0. Протокол, используемый контроллером для доступа к контролируемым устройствам. Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).

</dd> <dt>

**макскуиесцетиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство использовать не рекомендуется. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Метка, по которой известен объект. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и совпадает со свойством **ElementName** .

</dd> <dt>

**оператингстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** . Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)
</dt> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)
</dt> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)
</dt> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)
</dt> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)
</dt> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)
</dt> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)
</dt> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)
</dt> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)
</dt> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)
</dt> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)
</dt> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. )
</dt> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**осеренабледстате**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое). Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение **null**.

</dd> <dt>

**поверманажементкапабилитиес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возможности управления питанием устройства. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**поверманажементсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, можно ли управлять питанием устройства. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**поверонхаурс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**примаристатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Предоставляет сведения о состоянии высокого уровня. Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="OK"></span><span id="ok"></span>**ОК** (1)
</dt> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. )
</dt> </dl>

</dd> <dt>

**протоколдескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, которая предоставляет дополнительные сведения, связанные с протоколом, поддерживаемым контроллером. Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).

</dd> <dt>

**протоколсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Протокол, используемый контроллером для доступа к контролируемым устройствам. Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).



| Значение                                                                         | Значение             |
|-------------------------------------------------------------------------------|---------------------|
| <dl> <dt>26</dt> </dl> | IEEE-488<br/> |



 

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Последнее запрошенное или требуемое состояние элемента. Фактическое состояние элемента представлено параметром **EnabledState**. Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).



| Значение                                                                         | Значение                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>12</dt> </dl> | Не применимо<br/> |



 

</dd> <dt>

**Безопасность**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Операционная безопасность контроллера. Это свойство наследуется от [**CIM \_ сериалконтроллер**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).



| Значение                                                                        | Значение         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <dt>3</dt> </dl> | Нет<br/> |



 

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.

</dd> <dt>

**статусдескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строки, описывающие различные значения массива **OperationalStatus** . Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние логического устройства. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса создания системы области. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальный идентификатор для области виртуальной машины. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.

</dd> <dt>

**тимеофластресет**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время последнего включения контроллера. Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).

</dd> <dt>

**тимеофластстатечанже**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата или время последнего изменения включенного состояния элемента. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.

</dd> <dt>

**тоталповеронхаурс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общее количество часов, в течение которых устройство было включено. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

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

Доступ к классу **\_ сериалконтроллер мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_СЕРИАЛКОНТРОЛЛЕР CIM**](cim-serialcontroller.md)
</dt> <dt>

[**\_СЕРИАЛКОНТРОЛЛЕР CIM**](/windows/desktop/CIMWin32Prov/cim-serialcontroller)
</dt> <dt>

[Классы последовательных устройств](serial-devices-classes.md)
</dt> </dl>

 


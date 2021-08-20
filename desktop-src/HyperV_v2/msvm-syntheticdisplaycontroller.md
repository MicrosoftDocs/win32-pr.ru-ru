---
description: Представляет состояние искусственного контроллера экрана, присутствующего в каждой конфигурации виртуальной машины.
ms.assetid: E496B887-9032-43D8-A7D2-67BB77342AFD
title: Класс Msvm_SyntheticDisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayController
- Msvm_SyntheticDisplayController.SetPowerState
- Msvm_SyntheticDisplayController.EnableDevice
- Msvm_SyntheticDisplayController.OnlineDevice
- Msvm_SyntheticDisplayController.QuiesceDevice
- Msvm_SyntheticDisplayController.SaveProperties
- Msvm_SyntheticDisplayController.RestoreProperties
- Msvm_SyntheticDisplayController.InstanceID
- Msvm_SyntheticDisplayController.Caption
- Msvm_SyntheticDisplayController.Description
- Msvm_SyntheticDisplayController.ElementName
- Msvm_SyntheticDisplayController.InstallDate
- Msvm_SyntheticDisplayController.Name
- Msvm_SyntheticDisplayController.OperationalStatus
- Msvm_SyntheticDisplayController.StatusDescriptions
- Msvm_SyntheticDisplayController.Status
- Msvm_SyntheticDisplayController.HealthState
- Msvm_SyntheticDisplayController.CommunicationStatus
- Msvm_SyntheticDisplayController.DetailedStatus
- Msvm_SyntheticDisplayController.OperatingStatus
- Msvm_SyntheticDisplayController.PrimaryStatus
- Msvm_SyntheticDisplayController.EnabledState
- Msvm_SyntheticDisplayController.OtherEnabledState
- Msvm_SyntheticDisplayController.RequestedState
- Msvm_SyntheticDisplayController.EnabledDefault
- Msvm_SyntheticDisplayController.TimeOfLastStateChange
- Msvm_SyntheticDisplayController.AvailableRequestedStates
- Msvm_SyntheticDisplayController.TransitioningToState
- Msvm_SyntheticDisplayController.SystemCreationClassName
- Msvm_SyntheticDisplayController.SystemName
- Msvm_SyntheticDisplayController.CreationClassName
- Msvm_SyntheticDisplayController.DeviceID
- Msvm_SyntheticDisplayController.PowerManagementSupported
- Msvm_SyntheticDisplayController.PowerManagementCapabilities
- Msvm_SyntheticDisplayController.Availability
- Msvm_SyntheticDisplayController.StatusInfo
- Msvm_SyntheticDisplayController.LastErrorCode
- Msvm_SyntheticDisplayController.ErrorDescription
- Msvm_SyntheticDisplayController.ErrorCleared
- Msvm_SyntheticDisplayController.PowerOnHours
- Msvm_SyntheticDisplayController.TotalPowerOnHours
- Msvm_SyntheticDisplayController.OtherIdentifyingInfo
- Msvm_SyntheticDisplayController.IdentifyingDescriptions
- Msvm_SyntheticDisplayController.AdditionalAvailability
- Msvm_SyntheticDisplayController.MaxQuiesceTime
- Msvm_SyntheticDisplayController.TimeOfLastReset
- Msvm_SyntheticDisplayController.ProtocolSupported
- Msvm_SyntheticDisplayController.MaxNumberControlled
- Msvm_SyntheticDisplayController.ProtocolDescription
- Msvm_SyntheticDisplayController.VideoProcessor
- Msvm_SyntheticDisplayController.VideoMemoryType
- Msvm_SyntheticDisplayController.OtherVideoMemoryType
- Msvm_SyntheticDisplayController.NumberOfVideoPages
- Msvm_SyntheticDisplayController.MaxMemorySupported
- Msvm_SyntheticDisplayController.AcceleratorCapabilities
- Msvm_SyntheticDisplayController.CapabilityDescriptions
- Msvm_SyntheticDisplayController.OtherVideoArchitecture
- Msvm_SyntheticDisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 156396e61fca255f7aa4fd584aa10e9386b57c4b3e86f687fb39a922ed1f2fd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949893"
---
# <a name="msvm_syntheticdisplaycontroller-class"></a>\_Класс мсвм синсетикдисплайконтроллер

Представляет состояние искусственного контроллера экрана, присутствующего в каждой конфигурации виртуальной машины. Только один контроллер экрана может быть активным на виртуальной машине в любое время, и виртуальный контроллер можно активировать только в том случае, если гостевая операционная система загрузила требуемые службы ускорения видео.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Synthetic Display Controller";
  string   ElementName = "Display Controller";
  datetime InstallDate;
  string   Name = "Display Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_SyntheticDisplayController";
  string   DeviceID = "Microsoft:GUID";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 1024;
  uint32   MaxMemorySupported = 4194304;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ синсетикдисплайконтроллер** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **мсвм \_ синсетикдисплайконтроллер** содержит следующие методы.



| Метод                                                                           | Описание                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| **енабледевице**                                                                 | Этот метод не поддерживается.<br/> |
| **онлинедевице**                                                                 | Этот метод не поддерживается.<br/> |
| **куиесцедевице**                                                                | Этот метод не поддерживается.<br/> |
| [**Равен**](msvm-syntheticdisplaycontroller-requeststatechange.md) | Запрашивает изменение состояния.<br/>      |
| [**Перезапуск**](msvm-syntheticdisplaycontroller-reset.md)                           | Сбрасывает виртуальное устройство.<br/>    |
| **ресторепропертиес**                                                            | Этот метод не поддерживается.<br/> |
| **савепропертиес**                                                               | Этот метод не поддерживается.<br/> |
| **SetPowerState**                                                                | Этот метод не поддерживается.<br/> |



 

### <a name="properties"></a>Свойства

Класс **мсвм \_ синсетикдисплайконтроллер** имеет следующие свойства.

<dl> <dt>

**акцелераторкапабилитиес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Графические и трехмерные возможности контроллера экрана. Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85))и всегда имеет значение 2 (графический ускоритель).

</dd> <dt>

**аддитионалаваилабилити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение 6 (неприменимо).

</dd> <dt>

**Доступность**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение 6 (неприменимо).

</dd> <dt>

**аваилаблерекуестедстатес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** . Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.

</dd> <dt>

**капабилитидескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив строк произвольной формы, которые предоставляют более подробные объяснения для любого из функций ускорителя видео, указанных в массиве свойств **акцелераторкапабилитиес** . Каждая запись этого массива связана с записью в массиве свойств **акцелераторкапабилитиес** , расположенной по тому же индексу. Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85))и всегда имеет значение "графический ускоритель".

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "контроллер дисплея".

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

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса или подкласса, используемого при создании экземпляра. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение "мсвм \_ синсетикдисплайконтроллер".

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "виртуальный контроллер дисплея (Майкрософт)".

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

Это свойство наследуется от [**CIM \_ ",**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)" и всегда имеет значение "Microsoft:*GUID*".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и по умолчанию всегда имеет значение "контроллер дисплея".

</dd> <dt>

**енабледдефаулт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Конфигурация по умолчанию или запуска администратора для включенного состояния элемента. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Включенные и отключенные состояния элемента. Он также может указывать на переходы между этими запрошенными состояниями. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено) или 3 (отключено).

</dd> <dt>

**еррорклеаред**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущая работоспособность элемента. Этот атрибут выражает работоспособность этого элемента, но не обязательно для его вложенных элементов. Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение **null**.

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

Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**максмеморисуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальный поддерживаемый объем памяти в байтах. Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85))и всегда имеет значение 4 194 304 (0x400000).

</dd> <dt>

**макснумберконтроллед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное количество напрямую доступных для адресации сущностей, поддерживаемых этим контроллером. Если число неизвестно или неограниченно, следует использовать значение 0. Протокол, используемый контроллером для доступа к контролируемым устройствам. Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller)и всегда имеет значение 1.

</dd> <dt>

**макскуиесцетиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Метка, по которой известен объект. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и совпадает со свойством **ElementName** .

</dd> <dt>

**нумберофвидеопажес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число поддерживаемых страниц видео с учетом текущих разрешений и доступной памяти. Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85))и всегда имеет значение 1024.

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

Текущее состояние объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).

</dd> <dt>

**осеренабледстате**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое). Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение **null**.

</dd> <dt>

**осервидеоарчитектуре**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, описывающая тип архитектуры видео, если свойство **видеоарчитектуре** имеет значение 1 ("другое"). Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).

</dd> <dt>

**осервидеомеморитипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип видеопамяти, если свойство **видеомеморитипе** экземпляра имеет значение 1 (другое). Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85))и всегда имеет значение **null**.

</dd> <dt>

**поверманажементкапабилитиес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**поверманажементсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**поверонхаурс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

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

Строка, которая предоставляет дополнительные сведения, связанные с протоколом, поддерживаемым контроллером. Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller)и всегда имеет значение "Video".

</dd> <dt>

**протоколсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Протокол, используемый контроллером для доступа к контролируемым устройствам. Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller)и всегда имеет значение 1 (другое).

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Последнее запрошенное или требуемое состояние элемента. Фактическое состояние элемента представлено параметром **EnabledState**. Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния. Конкретный экземпляр [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать **RequestStateChange**. В этом случае используется значение 12 (неприменимо). Это свойство наследуется от **CIM \_ енабледлогикалелемент** и имеет значение 2 (включено), 3 (отключено) или 12 (неприменимо).

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
</dt> </dl>

Строки, описывающие различные значения массива **OperationalStatus** . Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "ОК".

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса создания системы области. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение "мсвм \_ ComputerSystem".

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

Время последнего включения виртуальной машины. Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).

</dd> <dt>

**тимеофластстатечанже**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата или время последнего изменения включенного состояния элемента. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**тоталповеронхаурс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**транситионингтостате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает целевое состояние, в которое переходит экземпляр. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.

</dd> <dt>

**видеоарчитектуре**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает архитектуру видеоролика контроллера экрана, используемую для создания видеосигнала. Обычно выделенный видеопроцессор создает видеосигнал в соответствии с указанной архитектурой. Это индикатор максимальной возможности разрешения контроллеров экрана. Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)
</dt> <dt>

<span id="CGA"></span><span id="cga"></span>**КГА** (2)
</dt> <dt>

<span id="EGA"></span><span id="ega"></span>**Ега** (3)
</dt> <dt>

<span id="VGA"></span><span id="vga"></span>**VGA** (4)
</dt> <dt>

<span id="SVGA"></span><span id="svga"></span>**SVGA** (5)
</dt> <dt>

<span id="MDA"></span><span id="mda"></span>**MDA** (6)
</dt> <dt>

<span id="HGC"></span><span id="hgc"></span>**ХГК** (7)
</dt> <dt>

<span id="MCGA"></span><span id="mcga"></span>**Мкга** (8)
</dt> <dt>

<span id="8514A"></span><span id="8514a"></span>**8514A** (9)
</dt> <dt>

<span id="XGA"></span><span id="xga"></span>**Разрешение XGA** (10)
</dt> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Буфер линейного фрейма** (11)
</dt> <dt>

<span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. )
</dt> </dl>

</dd> <dt>

**видеомеморитипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип видеопамяти. Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85))и всегда имеет значение 2 (видеопамять).

</dd> <dt>

**видеопроцессор**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, описывающая процессор или контроллер видео. Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85))и всегда имеет значение "синтетический видеопроцессор".

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ синсетикдисплайконтроллер мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ДИСПЛАЙКОНТРОЛЛЕР CIM**](cim-displaycontroller.md)
</dt> <dt>

[**\_ДИСПЛАЙКОНТРОЛЛЕР CIM**](/previous-versions//cc136810(v=vs.85))
</dt> <dt>

[Классы видео](video-classes.md)
</dt> </dl>

 


---
description: Представляет внутренний порт Ethernet (сетевой адаптер).
ms.assetid: 43277FA7-E040-49F2-A086-AF19B29D4F75
title: Класс Msvm_InternalEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InternalEthernetPort
- Msvm_InternalEthernetPort.SetPowerState
- Msvm_InternalEthernetPort.EnableDevice
- Msvm_InternalEthernetPort.OnlineDevice
- Msvm_InternalEthernetPort.QuiesceDevice
- Msvm_InternalEthernetPort.SaveProperties
- Msvm_InternalEthernetPort.RestoreProperties
- Msvm_InternalEthernetPort.InstanceID
- Msvm_InternalEthernetPort.Caption
- Msvm_InternalEthernetPort.Description
- Msvm_InternalEthernetPort.ElementName
- Msvm_InternalEthernetPort.InstallDate
- Msvm_InternalEthernetPort.Name
- Msvm_InternalEthernetPort.OperationalStatus
- Msvm_InternalEthernetPort.StatusDescriptions
- Msvm_InternalEthernetPort.Status
- Msvm_InternalEthernetPort.HealthState
- Msvm_InternalEthernetPort.CommunicationStatus
- Msvm_InternalEthernetPort.DetailedStatus
- Msvm_InternalEthernetPort.OperatingStatus
- Msvm_InternalEthernetPort.PrimaryStatus
- Msvm_InternalEthernetPort.EnabledState
- Msvm_InternalEthernetPort.OtherEnabledState
- Msvm_InternalEthernetPort.RequestedState
- Msvm_InternalEthernetPort.EnabledDefault
- Msvm_InternalEthernetPort.TimeOfLastStateChange
- Msvm_InternalEthernetPort.AvailableRequestedStates
- Msvm_InternalEthernetPort.TransitioningToState
- Msvm_InternalEthernetPort.SystemCreationClassName
- Msvm_InternalEthernetPort.SystemName
- Msvm_InternalEthernetPort.CreationClassName
- Msvm_InternalEthernetPort.DeviceID
- Msvm_InternalEthernetPort.PowerManagementSupported
- Msvm_InternalEthernetPort.PowerManagementCapabilities
- Msvm_InternalEthernetPort.Availability
- Msvm_InternalEthernetPort.StatusInfo
- Msvm_InternalEthernetPort.LastErrorCode
- Msvm_InternalEthernetPort.ErrorDescription
- Msvm_InternalEthernetPort.ErrorCleared
- Msvm_InternalEthernetPort.OtherIdentifyingInfo
- Msvm_InternalEthernetPort.PowerOnHours
- Msvm_InternalEthernetPort.TotalPowerOnHours
- Msvm_InternalEthernetPort.IdentifyingDescriptions
- Msvm_InternalEthernetPort.AdditionalAvailability
- Msvm_InternalEthernetPort.MaxQuiesceTime
- Msvm_InternalEthernetPort.MaxSpeed
- Msvm_InternalEthernetPort.RequestedSpeed
- Msvm_InternalEthernetPort.UsageRestriction
- Msvm_InternalEthernetPort.OtherPortType
- Msvm_InternalEthernetPort.Speed
- Msvm_InternalEthernetPort.OtherNetworkPortType
- Msvm_InternalEthernetPort.PortNumber
- Msvm_InternalEthernetPort.LinkTechnology
- Msvm_InternalEthernetPort.OtherLinkTechnology
- Msvm_InternalEthernetPort.PermanentAddress
- Msvm_InternalEthernetPort.FullDuplex
- Msvm_InternalEthernetPort.AutoSense
- Msvm_InternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_InternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_InternalEthernetPort.PortType
- Msvm_InternalEthernetPort.NetworkAddresses
- Msvm_InternalEthernetPort.MaxDataSize
- Msvm_InternalEthernetPort.Capabilities
- Msvm_InternalEthernetPort.CapabilityDescriptions
- Msvm_InternalEthernetPort.EnabledCapabilities
- Msvm_InternalEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a1441055fc7b86b97c69a40758236261b20f75c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810426"
---
# <a name="msvm_internalethernetport-class"></a>\_Класс мсвм интерналесернетпорт

Представляет внутренний порт Ethernet (сетевой адаптер). Этот тип порта Ethernet предоставляет виртуальным машинам доступ к серверу виртуализации, на котором работает сетевое программное обеспечение. Внутренние сетевые адаптеры позволяют маршрутизировать или фильтровать сетевой трафик виртуальных машин до выхода из физической системы.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Internal Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
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
  string   CreationClassName = "Msvm_InternalEthernetPort";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  string   OtherPortType;
  uint64   Speed;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  uint64   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint16   PortType;
  string   NetworkAddresses[];
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ интерналесернетпорт** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **мсвм \_ интерналесернетпорт** содержит следующие методы.



| Метод                                                                     | Описание                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| **енабледевице**                                                           | Этот метод не поддерживается.<br/> |
| **онлинедевице**                                                           | Этот метод не поддерживается.<br/> |
| **куиесцедевице**                                                          | Этот метод не поддерживается.<br/> |
| [**Равен**](msvm-internalethernetport-requeststatechange.md) | Запрашивает изменение состояния.<br/>      |
| [**Перезапуск**](msvm-internalethernetport-reset.md)                           | Сбрасывает виртуальное устройство.<br/>    |
| **ресторепропертиес**                                                      | Этот метод не поддерживается.<br/> |
| **савепропертиес**                                                         | Этот метод не поддерживается.<br/> |
| **SetPowerState**                                                          | Этот метод не поддерживается.<br/> |



 

### <a name="properties"></a>Свойства

Класс **мсвм \_ интерналесернетпорт** имеет следующие свойства.

<dl> <dt>

**активемаксимумтрансмиссионунит**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Допустимое число активных или согласованных максимальных единиц передачи (MTU). Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**аддитионалаваилабилити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Любая дополнительная доступность и состояние устройства, кроме указанного в свойстве **Availability** . Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.

</dd> <dt>

**Авточувствительность**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, может ли сетевой порт автоматически определять скорость или другие характеристики связи подключенного сетевого носителя. Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**Доступность**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Первичная доступность и состояние устройства. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.

</dd> <dt>

**аваилаблерекуестедстатес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния. Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния объекта [**\_ енабледлогикалелемент CIM**](/previous-versions//cc136818(v=vs.85)) . Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния. Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.

Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возможности порта Ethernet. Если в списке перечислены возможности отработки отказа или балансировки нагрузки, необходимо также определить [**CIM \_ спареграуп**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (отработку отказа) или [**CIM \_ екстракапаЦитиграуп**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (Балансировка нагрузки), чтобы полностью описать эту возможность. Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)
</dt> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**Алертонлан** (2)
</dt> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Вакеонлан** (3)
</dt> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Отработка отказа** (4)
</dt> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)
</dt> </dl>

</dd> <dt>

**капабилитидескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив строк произвольной формы, предоставляющий более подробные объяснения для любой из функций порта Ethernet, указанных в массиве **capabilities** . Обратите внимание, что каждая запись этого массива связана с записью в массиве **capabilities** , расположенном по тому же индексу. Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

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

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса или подкласса, используемого при создании экземпляра. При использовании с другими ключевыми свойствами этого класса это свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.

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

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Адрес или другие идентифицирующие сведения, используемые для уникального имени логического устройства. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение "Microsoft:*GUID* \\ ,*зависящие от устройства*".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Отображаемое имя объекта. Это свойство позволяет каждому экземпляру определить отображаемое имя в дополнение к его ключевым свойствам, идентификационным данным и сведениям о описании. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) и создается на основе сетевого адаптера, присутствующего на узле.

</dd> <dt>

**енабледкапабилитиес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, какие возможности включаются в списке всех поддерживаемых, определенных в массиве **capabilities** . Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)
</dt> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**Алертонлан** (2)
</dt> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Вакеонлан** (3)
</dt> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Отработка отказа** (4)
</dt> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)
</dt> </dl>

</dd> <dt>

**енабледдефаулт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Конфигурация по умолчанию или запуска администратора для включенного состояния элемента. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Включенные и отключенные состояния элемента. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**еррорклеаред**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, что сообщение об ошибке в свойстве **ластерроркоде** теперь отключено. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, которая предоставляет дополнительные сведения об ошибке, записанной в свойстве **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты. Это свойство унаследовано от [**свойства \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , и не используется.

</dd> <dt>

**фуллдуплекс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, работает ли порт в режиме полного дуплекса. Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущая работоспособность элемента. Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** . Каждая запись этого массива связана с записью в массиве свойств **осеридентифингинфо** , расположенной по тому же индексу. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Значение **типа DateTime** , указывающее, когда был установлен объект. Отсутствие значения не означает, что объект не установлен. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

Последний код ошибки, сообщаемый логическим устройством. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.

</dd> <dt>

**линктечнологи**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Типы ссылок. Если задано значение 1 (другое), связанное свойство **осерлинктечнологи** содержит строковое описание типа ссылки. Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).



| Значение                                                                        | Значение             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <dt>2</dt> </dl> | Ethernet<br/> |



 

</dd> <dt>

**максдатасизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальный размер поля сведений (не MAC), которое будет получено или передано. Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

</dd> <dt>

**макскуиесцетиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство использовать не рекомендуется. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.

</dd> <dt>

**максспид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальная пропускная способность порта (в битах в секунду). Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Метка, по которой известен объект. При создании подклассов это свойство может быть переопределено как свойство ключа. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

MAC-адреса Ethernet/802.3 отформатированы как двенадцать шестнадцатеричных цифр (например, "010203040506"). Каждая пара представляет один из шести октетов MAC-адреса в каноническом порядке (бит адреса группы находится в младших битах первого символа строки). Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

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

Текущее состояние элемента. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**осеренабледкапабилитиес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив строк произвольной формы, предоставляющий более подробные объяснения для любой из включенных возможностей, указанных как 1 (другое). Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

</dd> <dt>

**осеренабледстате**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое). Это свойство должно иметь значение **null** , если свойство **EnabledState** имеет любое значение, отличное от 1. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Любые данные в дополнение к сведениям об ИДЕНТИФИКАТОРе устройства, которые можно использовать для идентификации логического устройства. Например, это свойство можно использовать для хранения отображаемого имени операционной системы для устройства. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.

</dd> <dt>

**осерлинктечнологи**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строковое значение, описывающее свойство **линктечнологи** , если оно имеет значение 1 (другое). Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**осернетворкпорттипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство использовать не рекомендуется. Используйте свойство **portType** . Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

Нерекомендуемое описание: тип модуля, если свойство **portType** имеет значение 1 (другое).

</dd> <dt>

**осерпорттипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип модуля, если свойство **portType** имеет значение 1 (другое). Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)) .

</dd> <dt>

**перманентаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Сетевой адрес, жестко закодированный в порт. Этот адрес можно изменить с помощью обновления встроенного по или конфигурации программного обеспечения. При внесении этого изменения поле должно быть обновлено одновременно. Если для сетевого адаптера не существует жестко закодированного адреса, его следует оставить пустым. Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**PortNumber**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Сетевые порты часто нумеруются относительно логического модуля или сетевого элемента. Это значение равно 1 для эмулированных сетевых карт, 0 — для всех остальных. Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**Порта**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Конкретный режим, который в данный момент включен для порта. Если задано значение 1 (другое), связанное свойство **осерпорттипе** содержит строковое описание типа порта. Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)
</dt> <dt>

<span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**50 медный** (50)
</dt> <dt>

<span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BASE** (51)
</dt> <dt>

<span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BASE** (52)
</dt> <dt>

<span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BASE** (53)
</dt> <dt>

<span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)
</dt> <dt>

<span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)
</dt> <dt>

<span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)
</dt> <dt>

<span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)
</dt> <dt>

<span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)
</dt> <dt>

<span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)
</dt> <dt>

<span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)
</dt> <dt>

<span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)
</dt> <dt>

<span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)
</dt> <dt>

<span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)
</dt> <dt>

<span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)
</dt> <dt>

<span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)
</dt> <dt>

<span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-лв** (109)
</dt> <dt>

<span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)
</dt> <dt>

<span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-ать** (111)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (16000 65535)
</dt> </dl>

</dd> <dt>

**поверманажементкапабилитиес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возможности управления питанием устройства. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.

</dd> <dt>

**поверманажементсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, можно ли управлять питанием устройства. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.

</dd> <dt>

**поверонхаурс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.

</dd> <dt>

**примаристатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Предоставляет сведения о состоянии высокого уровня. Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**рекуестедспид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Запрошенная пропускная способность порта в битах в секунду. Фактическая пропускная способность указывается в свойстве **Speed** . Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Последнее запрошенное или требуемое состояние для службы управления. Если свойство **EnabledState** имеет значение 5 (неприменимо), это свойство не имеет смысла. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**Скорость**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Переопределение**, **единицы** ("бит в секунду")
</dt> </dl>

Текущая пропускная способность порта в битах в секунду. Для портов, которые зависят от пропускной способности или для тех, для которых не удается выполнить точную оценку, это свойство должно содержать номинальную пропускную способность. Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

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

Строки, описывающие различные значения массива **OperationalStatus** . Записи в этом массиве сопоставляются с элементами в том же индексе массива в **OperationalStatus**. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Состояние логического устройства. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.

</dd> <dt>

**суппортедмаксимумтрансмиссионунит**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Поддерживаемый максимальный размер блока передачи (MTU). Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса создания системы области. Это свойство унаследовано от [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-, но не поддерживается

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя системы области. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.

</dd> <dt>

**тимеофластстатечанже**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата или время последнего изменения свойства **EnabledState** элемента. Если состояние элемента не изменилось и заполнено это свойство, то для него должно быть задано нулевое значение интервала. Если изменение состояния было запрошено, но отклонено или еще не обработано, свойство не должно обновляться. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и не используется.

</dd> <dt>

**тоталповеронхаурс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общее количество часов, в течение которых устройство было включено. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.

</dd> <dt>

**транситионингтостате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает целевое состояние, в которое переходит экземпляр. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.

</dd> <dt>

**усажерестриктион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

В некоторых случаях логический порт может идентифицироваться как интерфейсный или серверный порт. Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).



| Значение                                                                        | Значение                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>4</dt> </dl> | Не ограничено<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ интерналесернетпорт мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_ЕСЕРНЕТПОРТ CIM**](cim-ethernetport.md)
</dt> <dt>

[**\_ЕСЕРНЕТПОРТ CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 


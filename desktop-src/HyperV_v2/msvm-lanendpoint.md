---
description: Представляет логическую точку подключения для сетевого адаптера. Если конечная точка локальной сети подключена к порту коммутатора, сетевой адаптер, подключенный к конечной точке локальной сети, имеет подключение к сети.
ms.assetid: 68aad05e-64b5-44dc-ab5b-8f3051fa77ca
title: Класс Msvm_LANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LANEndpoint
- Msvm_LANEndpoint.InstanceID
- Msvm_LANEndpoint.Caption
- Msvm_LANEndpoint.Description
- Msvm_LANEndpoint.ElementName
- Msvm_LANEndpoint.InstallDate
- Msvm_LANEndpoint.Name
- Msvm_LANEndpoint.OperationalStatus
- Msvm_LANEndpoint.StatusDescriptions
- Msvm_LANEndpoint.Status
- Msvm_LANEndpoint.HealthState
- Msvm_LANEndpoint.CommunicationStatus
- Msvm_LANEndpoint.DetailedStatus
- Msvm_LANEndpoint.OperatingStatus
- Msvm_LANEndpoint.PrimaryStatus
- Msvm_LANEndpoint.EnabledState
- Msvm_LANEndpoint.OtherEnabledState
- Msvm_LANEndpoint.RequestedState
- Msvm_LANEndpoint.EnabledDefault
- Msvm_LANEndpoint.TimeOfLastStateChange
- Msvm_LANEndpoint.AvailableRequestedStates
- Msvm_LANEndpoint.TransitioningToState
- Msvm_LANEndpoint.SystemCreationClassName
- Msvm_LANEndpoint.SystemName
- Msvm_LANEndpoint.CreationClassName
- Msvm_LANEndpoint.NameFormat
- Msvm_LANEndpoint.ProtocolType
- Msvm_LANEndpoint.ProtocolIFType
- Msvm_LANEndpoint.OtherTypeDescription
- Msvm_LANEndpoint.LANID
- Msvm_LANEndpoint.LANType
- Msvm_LANEndpoint.OtherLANType
- Msvm_LANEndpoint.MACAddress
- Msvm_LANEndpoint.AliasAddresses
- Msvm_LANEndpoint.GroupAddresses
- Msvm_LANEndpoint.MaxDataSize
- Msvm_LANEndpoint.Connected
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: aef7c0a1aa3182caa4d466a76972294f306a4227fcd63d27c1cdb7acbce1f809
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521934"
---
# <a name="msvm_lanendpoint-class"></a>\_Класс мсвм ланендпоинт

Представляет логическую точку подключения для сетевого адаптера. Если конечная точка локальной сети подключена к порту коммутатора, сетевой адаптер, подключенный к конечной точке локальной сети, имеет подключение к сети.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LANEndpoint : CIM_LANEndpoint
{
  string   InstanceID;
  string   Caption = "LAN Endpoint";
  string   Description = "Microsoft Virtual LAN Endpoint";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_LANEndpoint";
  string   NameFormat = "Microsoft Virtual Device ID";
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ ланендпоинт** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **мсвм \_ ланендпоинт** содержит следующие методы.



| Метод                                                            | Описание                         |
|:------------------------------------------------------------------|:------------------------------------|
| [**Равен**](msvm-lanendpoint-requeststatechange.md) | Запрашивает изменение состояния.<br/> |



 

### <a name="properties"></a>Свойства

Класс **мсвм \_ ланендпоинт** имеет следующие свойства.

<dl> <dt>

**алиасаддрессес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Другие адреса одноадресной рассылки, которые могут использоваться для связи с конечной точкой локальной сети. Это свойство наследуется от [**CIM \_ ланендпоинт**](/previous-versions//cc136865(v=vs.85)).

</dd> <dt>

**аваилаблерекуестедстатес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния. Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния CIM- [**\_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)). Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния. Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.

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

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "КОНЕЧНАЯ точка локальной сети".

</dd> <dt>

**коммуникатионстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает способность инструментирования взаимодействовать с базовым управляемым элементом. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Подключен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство имеет значение **true** , если конечная точка локальной сети подключена к порту коммутатора.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **maxlen** (256)
</dt> </dl>

Имя класса или подкласса, используемого при создании экземпляра. Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)и всегда имеет значение "мсвм \_ ланендпоинт".

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "конечная точка виртуальной сети Microsoft".

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

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

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

Указывает включенное состояние запланированной системы. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и может принимать одно из следующих значений.



| Значение                                                                                                                                                                                                                                                                       | Значение                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Отключено**</dt> <dt>3</dt> </dl>                                             | Система отключена.<br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Неприменимо**</dt> <dt>5</dt> </dl>                     | Элемент не поддерживает включение или отключение.<br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Включено, но отключено**</dt> <dt>6</dt> </dl> | Система включена, но в автономном режиме. Все новые запросы будут удалены.<br/> |



 

</dd> <dt>

**граупаддрессес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Адреса многоадресной рассылки, на которые прослушивается конечная точка локальной сети. Это свойство наследуется от [**CIM \_ ланендпоинт**](/previous-versions//cc136865(v=vs.85)).

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущая работоспособность элемента. Это свойство выражает работоспособность этого элемента, но не обязательно для его подкомпонентов. Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).



| Значение                                                                        | Значение                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>5</dt> </dl> | Состояние работоспособности — нормальное.<br/> |



 

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

**ланид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Метка или идентификатор сегмента локальной сети, к которой подключена конечная точка. Если конечная точка в данный момент не активна или подключена, или эта информация неизвестна, это свойство будет иметь **значение NULL**. Это свойство наследуется от [**CIM \_ ланендпоинт**](/previous-versions//cc136865(v=vs.85)).

</dd> <dt>

**лантипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство не рекомендуется использовать вместо свойства **ProtocolType** . Это свойство наследуется от [**CIM \_ ланендпоинт**](/previous-versions//cc136865(v=vs.85)).

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (12)
</dt> </dl>

MAC-адрес, используемый для связи с конечной точкой локальной сети. MAC-адрес имеет формат двенадцати шестнадцатеричных цифр (например, "010203040506"), при этом каждая пара представляет один из шести октетов MAC-адреса в каноническом порядке в соответствии с RFC 2469. Это свойство наследуется от [**CIM \_ ланендпоинт**](/previous-versions//cc136865(v=vs.85)).

</dd> <dt>

**максдатасизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **единицы** ("биты")
</dt> </dl>

Самый крупный размер (в битах) информационного поля, который может быть отправлен или получен конечной точкой локальной сети. Это свойство наследуется от [**CIM \_ ланендпоинт**](/previous-versions//cc136865(v=vs.85)).

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Метка, по которой известен объект. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**намеформат**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (256)
</dt> </dl>

Содержит эвристику именования, выбранную для обеспечения уникальности значения свойства **Name** . Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)и имеет значение "Microsoft Virtual Device ID".

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

Текущее состояние объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).

</dd> <dt>

**осеренабледстате**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 ("другое"). Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.

</dd> <dt>

**осерлантипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство не рекомендуется использовать вместо свойства **осертипедескриптион** . Это свойство наследуется от [**CIM \_ ланендпоинт**](/previous-versions//cc136865(v=vs.85)).

</dd> <dt>

**осертипедескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (64)
</dt> </dl>

Строка, описывающая тип конечной точки протокола, если свойство **протоколифтипе** этого класса (или любого из его подклассов) имеет значение 1 (другое). Это свойство должно иметь значение **null** , если свойство **протоколифтипе** имеет любое значение, отличное от 1. Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).

</dd> <dt>

**примаристатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Предоставляет сведения о состоянии высокого уровня. Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**протоколифтипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Свойство используется для категоризации и классификации экземпляров этого класса. Если для **протоколифтипе** задано значение 1 (другое), то сведения о типе должны быть предоставлены в свойстве **осертипедескриптион** . Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).

> [!Note]  
> **Протоколифтипе** — это перечисление, которое синхронизируется с [IANA ифтипе MIB](https://www.iana.org/assignments/ianaiftype-mib). Также включаются дополнительные значения, определенные в DMTF.

 

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)
</dt> <dt>

<span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Регулярное 1822** (2)
</dt> <dt>

<span id="HDH_1822"></span><span id="hdh_1822"></span>**Хдх 1822** (3)
</dt> <dt>

<span id="DDN_X.25"></span><span id="ddn_x.25"></span>**ДДН X. 25** (4)
</dt> <dt>

<span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X. 25** (5)
</dt> <dt>

<span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**Ethernet КСМа/CD** (6)
</dt> <dt>

<span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802,3 КСМа/CD** (7)
</dt> <dt>

<span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**Шина маркеров ISO 802,4** (8)
</dt> <dt>

<span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**ISO 802,5 Token Ring** (9)
</dt> <dt>

<span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**Человек ISO 802,6 Man** (10)
</dt> <dt>

<span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**Старлан** (11)
</dt> <dt>

<span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Протеон 10Mbit** (12)
</dt> <dt>

<span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Протеон 80Mbit** (13)
</dt> <dt>

<span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**Канал** связи (14)
</dt> <dt>

<span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)
</dt> <dt>

<span id="LAP-B"></span><span id="lap-b"></span>**Подлинный-B** (16)
</dt> <dt>

<span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)
</dt> <dt>

<span id="DS1"></span><span id="ds1"></span>**DS1** (18)
</dt> <dt>

<span id="E1"></span><span id="e1"></span>**E1** (19)
</dt> <dt>

<span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**Базовый ISDN** (20)
</dt> <dt>

<span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**Основной ISDN** (21)
</dt> <dt>

<span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Собственная последовательное подключение "точка — точка** " (22)
</dt> <dt>

<span id="PPP"></span><span id="ppp"></span>**PPP** (23)
</dt> <dt>

<span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Замыкание программного обеспечения** (24)
</dt> <dt>

<span id="EON"></span><span id="eon"></span>**ЕОН** (25)
</dt> <dt>

<span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26)
</dt> <dt>

<span id="NSIP"></span><span id="nsip"></span>**НСИП** (27)
</dt> <dt>

<span id="SLIP"></span><span id="slip"></span>**SLIP** (28)
</dt> <dt>

<span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)
</dt> <dt>

<span id="DS3"></span><span id="ds3"></span>**DS3** (30)
</dt> <dt>

<span id="SIP"></span><span id="sip"></span>**SIP** (31)
</dt> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (32)
</dt> <dt>

<span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)
</dt> <dt>

<span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Параллельно** (34)
</dt> <dt>

<span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**АркНет** (35)
</dt> <dt>

<span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**АркНет Plus** (36)
</dt> <dt>

<span id="ATM"></span><span id="atm"></span>**ATM** (37)
</dt> <dt>

<span id="MIO_X.25"></span><span id="mio_x.25"></span>**МиО X. 25** (38)
</dt> <dt>

<span id="SONET"></span><span id="sonet"></span>**Сонет** (39)
</dt> <dt>

<span id="X.25_PLE"></span><span id="x.25_ple"></span>**X. 25 Борки** (40)
</dt> <dt>

<span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211 c** (41)
</dt> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)
</dt> <dt>

<span id="SMDS_DXI"></span><span id="smds_dxi"></span>**СМДС дкси** (43)
</dt> <dt>

<span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Служба Frame Relay** (44)
</dt> <dt>

<span id="V.35"></span><span id="v.35"></span>**V. 35** (45)
</dt> <dt>

<span id="HSSI"></span><span id="hssi"></span>**Хсси** (46)
</dt> <dt>

<span id="HIPPI"></span><span id="hippi"></span>**Хиппи** (47)
</dt> <dt>

<span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Модем** (48)
</dt> <dt>

<span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)
</dt> <dt>

<span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**Путь Сонет** (50)
</dt> <dt>

<span id="SONET_VT"></span><span id="sonet_vt"></span>**Сонет VT** (51)
</dt> <dt>

<span id="SMDS_ICIP"></span><span id="smds_icip"></span>**СМДС иЦип** (52)
</dt> <dt>

<span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Собственная виртуальная/внутренняя** (53)
</dt> <dt>

<span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Собственный мультиплексор** (54)
</dt> <dt>

<span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802,12** (55)
</dt> <dt>

<span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)
</dt> <dt>

<span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**Интерфейс хиппи** (57)
</dt> <dt>

<span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Соединение Frame Relay** (58)
</dt> <dt>

<span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**ATM-Эмуляция LAN для 802,3** (59)
</dt> <dt>

<span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**ATM-Эмуляция LAN для 802,5** (60)
</dt> <dt>

<span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**ATM-Эмуляция** (61)
</dt> <dt>

<span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Fast Ethernet (100BASE)** (62)
</dt> <dt>

<span id="ISDN"></span><span id="isdn"></span>**ISDN** (63)
</dt> <dt>

<span id="V.11"></span><span id="v.11"></span>**V. 11** (64)
</dt> <dt>

<span id="V.36"></span><span id="v.36"></span>**V. 36** (65)
</dt> <dt>

<span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 в 64 КБ** (66)
</dt> <dt>

<span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 в 2 МБ** (67)
</dt> <dt>

<span id="QLLC"></span><span id="qllc"></span>**Кллк** (68)
</dt> <dt>

<span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)
</dt> <dt>

<span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Канал** (70)
</dt> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)
</dt> <dt>

<span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**Канал IBM 260/370 оеми** (72)
</dt> <dt>

<span id="ESCON"></span><span id="escon"></span>**Ескон** (73)
</dt> <dt>

<span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Переключение каналов передачи данных** (74)
</dt> <dt>

<span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**Интерфейс ISDN S/T** (75)
</dt> <dt>

<span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**Интерфейс ISDN U** (76)
</dt> <dt>

<span id="LAP-D"></span><span id="lap-d"></span>**Длинный** (77)
</dt> <dt>

<span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**IP-параметр** (78)
</dt> <dt>

<span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Мост удаленных маршрутов удаленного источника** (79)
</dt> <dt>

<span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**Логический ATM** (80)
</dt> <dt>

<span id="DS0"></span><span id="ds0"></span>**DS0** (81)
</dt> <dt>

<span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**Пакет DS0** (82)
</dt> <dt>

<span id="BSC"></span><span id="bsc"></span>**BSC** (83)
</dt> <dt>

<span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)
</dt> <dt>

<span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Борьбы с сетевым радио** (85)
</dt> <dt>

<span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5 r DTR** (86)
</dt> <dt>

<span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Система отчетов ext POS Loc** (87)
</dt> <dt>

<span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**Протокол удаленного доступа AppleTalk** (88)
</dt> <dt>

<span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**Собственная без подключения** (89)
</dt> <dt>

<span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**Хост-приложение ITU X. 29** (90)
</dt> <dt>

<span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**Клавиатура терминала ITU X. 3** (91)
</dt> <dt>

<span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**MPI Frame Relay** (92)
</dt> <dt>

<span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X. 213** (93)
</dt> <dt>

<span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)
</dt> <dt>

<span id="RADSL"></span><span id="radsl"></span>**Радсл** (95)
</dt> <dt>

<span id="SDSL"></span><span id="sdsl"></span>**Сдсл** (96)
</dt> <dt>

<span id="VDSL"></span><span id="vdsl"></span>**Вдсл** (97)
</dt> <dt>

<span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802,5 крфп** (98)
</dt> <dt>

<span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Миринет** (99)
</dt> <dt>

<span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Получение и передача голоса** (100)
</dt> <dt>

<span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Office Exchange для внешнего голоса** (101)
</dt> <dt>

<span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**служба Voice инородных Exchange** (102)
</dt> <dt>

<span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Инкапсуляция голоса** (103)
</dt> <dt>

<span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>Передача **голоса по IP** (104)
</dt> <dt>

<span id="ATM_DXI"></span><span id="atm_dxi"></span>**ATM дкси** (105)
</dt> <dt>

<span id="ATM_FUNI"></span><span id="atm_funi"></span>**ATM Фуни** (106)
</dt> <dt>

<span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM Има** (107)
</dt> <dt>

<span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**Многоканальный пакет PPP** (108)
</dt> <dt>

<span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP через кдлк** (109)
</dt> <dt>

<span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP через клав** (110)
</dt> <dt>

<span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Стек в стек** (111)
</dt> <dt>

<span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Виртуальный IP-адрес** (112)
</dt> <dt>

<span id="MPC"></span><span id="mpc"></span>**MPC** (113)
</dt> <dt>

<span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP через ATM** (114)
</dt> <dt>

<span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**ISO 802.5 j Fibre Token Ring** (115)
</dt> <dt>

<span id="TDLC"></span><span id="tdlc"></span>**Тдлк** (116)
</dt> <dt>

<span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Гигабитный Ethernet** (117)
</dt> <dt>

<span id="HDLC"></span><span id="hdlc"></span>**Хдлк** (118)
</dt> <dt>

<span id="LAP-F"></span><span id="lap-f"></span>**Подлинный-F** (119)
</dt> <dt>

<span id="V.37"></span><span id="v.37"></span>**V. 37** (120)
</dt> <dt>

<span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X. 25 MLP** (121)
</dt> <dt>

<span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**Группа слежения X. 25** (122)
</dt> <dt>

<span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Трансп хдлк** (123)
</dt> <dt>

<span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Канал чередования** (124)
</dt> <dt>

<span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**канал FAST** (125)
</dt> <dt>

<span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP-адрес (для АППН ХПР в IP-сетях)** (126)
</dt> <dt>

<span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**КАТВ Mac Layer** (127)
</dt> <dt>

<span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**Нисходящий КАТВ** (128)
</dt> <dt>

<span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**Вышестоящий КАТВ** (129)
</dt> <dt>

<span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Параметр Avalon 12MPP** (130)
</dt> <dt>

<span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Tunnel** (131)
</dt> <dt>

<span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Кофе** (132)
</dt> <dt>

<span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Служба эмуляции канала** (133)
</dt> <dt>

<span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**Подинтерфейс ATM** (134)
</dt> <dt>

<span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**Виртуальная ЛС уровня 2 с помощью 802.1 q** (135)
</dt> <dt>

<span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**Виртуальная ЛС уровня 3 с использованием IP-адреса** (136)
</dt> <dt>

<span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**Виртуальная ЛС уровня 3 с использованием IPX** (137)
</dt> <dt>

<span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Цифровая линия электропитания** (138)
</dt> <dt>

<span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Мультимедийная почта через IP-адрес** (139)
</dt> <dt>

<span id="DTM"></span><span id="dtm"></span>**DTM** (140)
</dt> <dt>

<span id="DCN"></span><span id="dcn"></span>**ДКН** (141)
</dt> <dt>

<span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**IP-пересылка** (142)
</dt> <dt>

<span id="MSDSL"></span><span id="msdsl"></span>**MsDS** (143)
</dt> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)
</dt> <dt>

<span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**If-ГСН/хиппи-6400** (145)
</dt> <dt>

<span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**Уровень DVB-RCC Mac** (146)
</dt> <dt>

<span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**Подчиненный DVB-RCC** (147)
</dt> <dt>

<span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**Вышестоящее телевидение DVB-RCC** (148)
</dt> <dt>

<span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**Виртуальная Банкомат** (149)
</dt> <dt>

<span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**Tunnel MPLS** (150)
</dt> <dt>

<span id="SRP"></span><span id="srp"></span>**SRP** (151)
</dt> <dt>

<span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>Передача **голоса по сети ATM** (152)
</dt> <dt>

<span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>Передача **голоса через Frame Relay** (153)
</dt> <dt>

<span id="ISDL"></span><span id="isdl"></span>**Исдл** (154)
</dt> <dt>

<span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Составная ссылка** (155)
</dt> <dt>

<span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**Канал сигнализации SS7** (156)
</dt> <dt>

<span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Частная сеть P2P** (157)
</dt> <dt>

<span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Кадр вперед** (158)
</dt> <dt>

<span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 по протоколу ATM** (159)
</dt> <dt>

<span id="USB"></span><span id="usb"></span>**USB** (160)
</dt> <dt>

<span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**Агрегирование ссылок AD IEEE 802.3** (161)
</dt> <dt>

<span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**Учет политики BGP** (162)
</dt> <dt>

<span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**ФРФ .16 многоканальная связь fr** (163)
</dt> <dt>

<span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**Привратник H. 323** (164)
</dt> <dt>

<span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**H. 323-прокси** (165)
</dt> <dt>

<span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)
</dt> <dt>

<span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Многочастотная ссылка на сигнал** (167)
</dt> <dt>

<span id="HDSL-2"></span><span id="hdsl-2"></span>**Хдсл-2** (168)
</dt> <dt>

<span id="S-HDSL"></span><span id="s-hdsl"></span>**S-хдсл** (169)
</dt> <dt>

<span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**Ссылка на данные DS1-устройства** (170)
</dt> <dt>

<span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Пакет через Сонет/СДХ** (171)
</dt> <dt>

<span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**Вход DVB-АСИ** (172)
</dt> <dt>

<span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**Выходные данные DVB-АСИ** (173)
</dt> <dt>

<span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Линия электропитания** (174)
</dt> <dt>

<span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Связанные сигналы без устройства** (175)
</dt> <dt>

<span id="TR008"></span><span id="tr008"></span>**TR008** (176)
</dt> <dt>

<span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 РДТ** (177)
</dt> <dt>

<span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)
</dt> <dt>

<span id="ISUP"></span><span id="isup"></span>**ИСУП** (179)
</dt> <dt>

<span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Частный уровень беспроводной сети Mac** (180)
</dt> <dt>

<span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**Собственная беспроводная сеть** (181)
</dt> <dt>

<span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Частные Беспроводные потоки** (182)
</dt> <dt>

<span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**Тип хиперлан 2** (183)
</dt> <dt>

<span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Собственная широкополосная беспроводная точка доступа к MultiPoint** (184)
</dt> <dt>

<span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**Канал накладных расходов Сонет** (185)
</dt> <dt>

<span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Канал накладных расходов цифровых оболочек** (186)
</dt> <dt>

<span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**Уровень адаптации ATM 2** (187)
</dt> <dt>

<span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Радио Mac** (188)
</dt> <dt>

<span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**ATM-радио** (189)
</dt> <dt>

<span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Межмашинная магистраль между компьютерами** (190)
</dt> <dt>

<span id="MVL_DSL"></span><span id="mvl_dsl"></span>**МВЛ DSL** (191)
</dt> <dt>

<span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**Общедоступный для чтения DSL** (192)
</dt> <dt>

<span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Конечная точка DLCI Frame Relay** (193)
</dt> <dt>

<span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**Конечная точка ATM VCI** (194)
</dt> <dt>

<span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Оптический канал** (195)
</dt> <dt>

<span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Оптический транспорт** (196)
</dt> <dt>

<span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**Собственная ATM** (197)
</dt> <dt>

<span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Речь по кабелю** (198)
</dt> <dt>

<span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**InfiniBand** (199)
</dt> <dt>

<span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**Ссылка TE** (200)
</dt> <dt>

<span id="Q.2931"></span><span id="q.2931"></span>**Q. 2931** (201)
</dt> <dt>

<span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Виртуальная магистральная группа** (202)
</dt> <dt>

<span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**Магистральная группа SIP** (203)
</dt> <dt>

<span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**Сигнал SIP** (204)
</dt> <dt>

<span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**Вышестоящий канал КАТВ** (205)
</dt> <dt>

<span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Еконет** (206)
</dt> <dt>

<span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**ФСАН 155MB Пон** (207)
</dt> <dt>

<span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**ФСАН 622MB Пон** (208)
</dt> <dt>

<span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Прозрачный мост** (209)
</dt> <dt>

<span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Группа линий** (210)
</dt> <dt>

<span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Группа функций Voice &** (211)
</dt> <dt>

<span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voice ФГД еана** (212)
</dt> <dt>

<span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voice** (213)
</dt> <dt>

<span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**Транспорт MPEG** (214)
</dt> <dt>

<span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6to4** (215)
</dt> <dt>

<span id="GTP"></span><span id="gtp"></span>**Гтп** (216)
</dt> <dt>

<span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Парадине есерлуп 1** (217)
</dt> <dt>

<span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Парадине есерлуп 2** (218)
</dt> <dt>

<span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Группа оптических каналов** (219)
</dt> <dt>

<span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**Хомепна** (220)
</dt> <dt>

<span id="GFP"></span><span id="gfp"></span>**ГФП** (221)
</dt> <dt>

<span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**Цискоислвлан** (222)
</dt> <dt>

<span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**актелисметалуп** (223)
</dt> <dt>

<span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**ФЦип** (224)
</dt> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**Зарезервирован IANA** (225.. 4095)
</dt> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)
</dt> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)
</dt> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/V6** (4098)
</dt> <dt>

<span id="IPX"></span><span id="ipx"></span>**IPX** (4099)
</dt> <dt>

<span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>Протокол **DECnet** (4100)
</dt> <dt>

<span id="SNA"></span><span id="sna"></span>**SNA** (4101)
</dt> <dt>

<span id="CONP"></span><span id="conp"></span>**КОНП** (4102)
</dt> <dt>

<span id="CLNP"></span><span id="clnp"></span>**Клнп** (4103)
</dt> <dt>

<span id="VINES"></span><span id="vines"></span>**Vines** (4104)
</dt> <dt>

<span id="XNS"></span><span id="xns"></span>**КСНС** (4105)
</dt> <dt>

<span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**Конечная точка канала ISDN B** (4106)
</dt> <dt>

<span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**Конечная точка D канала ISDN** (4107)
</dt> <dt>

<span id="BGP"></span><span id="bgp"></span>**BGP** (4108)
</dt> <dt>

<span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)
</dt> <dt>

<span id="UDP"></span><span id="udp"></span>**UDP** (4110)
</dt> <dt>

<span id="TCP"></span><span id="tcp"></span>**TCP** (4111)
</dt> <dt>

<span id="802.11a"></span><span id="802.11A"></span>**802.11 a** (4112)
</dt> <dt>

<span id="802.11b"></span><span id="802.11B"></span>**802.11 b** (4113)
</dt> <dt>

<span id="802.11g"></span><span id="802.11G"></span>**802.11 g** (4114)
</dt> <dt>

<span id="802.11h"></span><span id="802.11H"></span>**802.11 h** (4115)
</dt> <dt>

<span id="NFS"></span><span id="nfs"></span>**NFS** (4200)
</dt> <dt>

<span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)
</dt> <dt>

<span id="DAFS"></span><span id="dafs"></span>**ДАФС** (4202)
</dt> <dt>

<span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>Протокол **WebDAV** (4203)
</dt> <dt>

<span id="HTTP"></span><span id="http"></span>**Http** (4204)
</dt> <dt>

<span id="FTP"></span><span id="ftp"></span>**FTP** (4205)
</dt> <dt>

<span id="NDMP"></span><span id="ndmp"></span>**Ндмп** (4300)
</dt> <dt>

<span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)
</dt> <dt>

<span id="SSH"></span><span id="ssh"></span>**SSH** (4401)
</dt> <dt>

<span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)
</dt> <dt>

<span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)
</dt> <dt>

<span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)
</dt> <dt>

<span id="RDP"></span><span id="rdp"></span>**RDP** (4405)
</dt> <dt>

<span id="HTTPS"></span><span id="https"></span>**HTTPS** (4406)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (32768.. )
</dt> </dl>

</dd> <dt>

**ProtocolType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство не рекомендуется использовать вместо свойства **протоколифтипе** . Это свойство наследуется от [**CIM \_ протоколендпоинт**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Последнее запрошенное или требуемое состояние для службы управления. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 12 (неприменимо).



| Значение                                                                         | Значение                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | Неприменимо.<br/> |



 

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описывает состояние элемента. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

'

План

Пониженной функциональности

Неизвестный

"Пред Fail"

Start

Идет

Служеб

Груз

"Recover"

"Нет контакта"

"Потеря связи"

</dd> <dt>

**статусдескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строки, описывающие различные значения массива **OperationalStatus** . Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "ОК".

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса создания системы размещения. Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **maxlen** (256)
</dt> </dl>

Имя системы размещения. Это свойство наследуется от [**CIM \_ сервицеакцесспоинт**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).

</dd> <dt>

**тимеофластстатечанже**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время последнего изменения включенного состояния элемента. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не поддерживается.

</dd> <dt>

**транситионингтостате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает целевое состояние, в которое переходит экземпляр. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


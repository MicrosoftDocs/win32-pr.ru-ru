---
description: Представляет текущую конфигурацию виртуального коммутатора Ethernet.
ms.assetid: a7c03517-332d-47ce-8e04-c2187bcb2977
title: Класс Msvm_VirtualEthernetSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingData
- Msvm_VirtualEthernetSwitchSettingData.InstanceID
- Msvm_VirtualEthernetSwitchSettingData.Caption
- Msvm_VirtualEthernetSwitchSettingData.Description
- Msvm_VirtualEthernetSwitchSettingData.ElementName
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemType
- Msvm_VirtualEthernetSwitchSettingData.Notes
- Msvm_VirtualEthernetSwitchSettingData.CreationTime
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationID
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationFile
- Msvm_VirtualEthernetSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SuspendDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualEthernetSwitchSettingData.LogDataRoot
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualEthernetSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualEthernetSwitchSettingData.RecoveryFile
- Msvm_VirtualEthernetSwitchSettingData.VLANConnection
- Msvm_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- Msvm_VirtualEthernetSwitchSettingData.MaxNumMACAddress
- Msvm_VirtualEthernetSwitchSettingData.IOVPreferred
- Msvm_VirtualEthernetSwitchSettingData.ExtensionOrder
- Msvm_VirtualEthernetSwitchSettingData.BandwidthReservationMode
- Msvm_VirtualEthernetSwitchSettingData.TeamingEnabled
- Msvm_VirtualEthernetSwitchSettingData.PacketDirectEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3eccbd9dabe853f01c54c78ca651d590afc49f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683166"
---
# <a name="msvm_virtualethernetswitchsettingdata-class"></a>\_Класс мсвм виртуалесернетсвитчсеттингдата

Представляет текущую конфигурацию виртуального коммутатора Ethernet.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingData : CIM_VirtualEthernetSwitchSettingData
{
  string   InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string   Caption = "Virtual Ethernet Switch Settings";
  string   Description = "Active settings for the virtual Ethernet switch";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   VLANConnection[];
  string   AssociatedResourcePool[];
  uint32   MaxNumMACAddress;
  boolean  IOVPreferred = FALSE;
  string   ExtensionOrder[];
  uint32   BandwidthReservationMode = 0;
  boolean  TeamingEnabled = FALSE;
  boolean  PacketDirectEnabled = FALSE;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалесернетсвитчсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалесернетсвитчсеттингдата** имеет следующие свойства.

<dl> <dt>

**ассоЦиатедресаурцепул**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Список пулов ресурсов узлов, которые будут связаны или которые в настоящее время связаны с коммутатором Ethernet, для распределения Ethernet-подключений между виртуальной машиной и коммутатором Ethernet. Каждое значение должно соответствовать рабочему URI производства \_ \_ унтипединстанцепас, как определено в DSP0207. Это свойство наследуется от **CIM \_ виртуалесернетсвитчсеттингдата**.

</dd> <dt>

**аутоматикрековеряктион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Действие, выполняемое для виртуальной машины при сбое программного обеспечения, выполняемого виртуальной машиной. Сбои в этом случае означают сбой, который обнаруживается платформой размещения, например условие состояния ожидания без взаимоблокировки. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.

</dd> <dt>

**аутоматикшутдовнактион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Действие, выполняемое для виртуальной машины при завершении работы узла. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.

</dd> <dt>

**аутоматикстартупактион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Действие, выполняемое для виртуальной машины при запуске узла. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.

</dd> <dt>

**аутоматикстартупактионделай**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время задержки перед автоматическим запуском виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.

</dd> <dt>

**аутоматикстартупактионсекуенценумбер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число, указывающее относительную последовательность активации виртуальной машины при запуске главной системы. Меньшее значение указывает на более раннюю активацию. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.

</dd> <dt>

**бандвидсресерватионмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Режим резервирования пропускной способности.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**По умолчанию** (0)


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

**Вес** (1)


</dt> <dd></dd> <dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

**Absolute** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Нет** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры виртуального коммутатора Ethernet".

</dd> <dt>

**конфигуратиондатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранится информация о конфигурации виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.

</dd> <dt>

**Файл ConfigurationFile**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Относительный путь и имя файла, в котором хранятся сведения о конфигурации виртуальной машины. Этот путь задается относительно свойства **конфигуратиондатарут** . Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальный идентификатор конфигурации виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время создания параметров. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "активные параметры для виртуального коммутатора Ethernet".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**екстенсионордер**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Массив внедренных экземпляров класса [**мсвм \_ есернетсвитчекстенсион**](msvm-ethernetswitchextension.md) , представляющих расширения коммутаторов, привязанные к этому коммутатору, в том порядке, в котором они применяются.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)) и всегда имеет значение "Microsoft:*GUID* \\ *девицеспеЦификдата*".

</dd> <dt>

**иовпреферред**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, является ли однокорневой сервер ввода/вывода (SR-IOV) предпочтительнее, если это возможно, на базовом адаптере.

</dd> <dt>

**логдатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранится информация журнала для виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.

</dd> <dt>

**макснуммакаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает максимальное число уникальных MAC-адресов, которые могут быть получены коммутатором для поддержки обучения MAC-адресов, как определено в стандарте IEEE 802,1. Это свойство наследуется от **CIM \_ виртуалесернетсвитчсеттингдата**.

</dd> <dt>

**Примечания**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указанные пользователем примечания, связанные с виртуальной машиной. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**паккетдиректенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, следует ли использовать PacketDirect, если он доступен. Значение по умолчанию — **false**.

> [!Note]  
> Это свойство было добавлено в Windows 10 и Windows Server 2016.

 

</dd> <dt>

**рековерифиле**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Полный путь к файлу, в котором хранится информация, связанная с восстановлением для виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.

</dd> <dt>

**снапшотдатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранятся сведения о моментальных снимках виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.

</dd> <dt>

**суспенддатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранятся сведения о приостановке виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.

</dd> <dt>

**свапфиледатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранятся файлы подкачки для виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и не используется.

</dd> <dt>

**теаминженаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, следует ли использовать объединение сетевых карт. Значение по умолчанию — **false**.

> [!Note]  
> Это свойство было добавлено в Windows 10 и Windows Server 2016.

 

</dd> <dt>

**виртуалсистемидентифиер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя объекта [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , которому принадлежат данные этого параметра. Это свойство является переопределением из [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**виртуалсистемтипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает тип виртуальной машины, которую представляют данные параметров. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**вланконнектион**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Список идентификаторов VLAN, к которым может получить доступ этот коммутатор. Это свойство наследуется от **CIM \_ виртуалесернетсвитчсеттингдата**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


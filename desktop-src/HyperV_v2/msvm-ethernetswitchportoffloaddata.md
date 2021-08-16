---
description: Представляет данные состояния функции разгрузки порта.
ms.assetid: 1117b9e4-cff7-4c9e-bf5e-74499297e84e
title: Класс Msvm_EthernetSwitchPortOffloadData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadData
- Msvm_EthernetSwitchPortOffloadData.InstanceID
- Msvm_EthernetSwitchPortOffloadData.Caption
- Msvm_EthernetSwitchPortOffloadData.Description
- Msvm_EthernetSwitchPortOffloadData.ElementName
- Msvm_EthernetSwitchPortOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchPortOffloadData.SystemName
- Msvm_EthernetSwitchPortOffloadData.DeviceCreationClassName
- Msvm_EthernetSwitchPortOffloadData.DeviceID
- Msvm_EthernetSwitchPortOffloadData.CreationClassName
- Msvm_EthernetSwitchPortOffloadData.Name
- Msvm_EthernetSwitchPortOffloadData.IpsecCurrentOffloadSaCount
- Msvm_EthernetSwitchPortOffloadData.IovOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQId
- Msvm_EthernetSwitchPortOffloadData.IovVfId
- Msvm_EthernetSwitchPortOffloadData.IovVfDataPathActive
- Msvm_EthernetSwitchPortOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchPortOffloadData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadData.VrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e6e2de8571d665dc86393708b2afcf73fc4885f0b4de26624daafcdccff995b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681484"
---
# <a name="msvm_ethernetswitchportoffloaddata-class"></a>\_Класс мсвм есернетсвитчпортоффлоаддата

Представляет данные состояния функции разгрузки порта.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadData : Msvm_EthernetPortData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Feature Status";
  string  Description = "Represents the port offload feature status data.";
  string  ElementName = "Ethernet Switch Port Offload Feature Status";
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string  DeviceID;
  string  CreationClassName = "Msvm_EthernetSwitchPortOffloadData";
  string  Name;
  uint32  IpsecCurrentOffloadSaCount = 0;
  uint32  IovOffloadUsage = 0;
  uint32  VMQOffloadUsage = 0;
  uint32  VMQId = 0;
  uint16  IovVfId = 0;
  boolean IovVfDataPathActive = FALSE;
  uint32  IovQueuePairUsage = 0;
  uint32  VmmqQueuePairs = 0;
  uint32  VrssVmbusChannelAffinityPolicy = 0;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 0;
  uint32  VrssMinQueuePairs = 0;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = FALSE;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ есернетсвитчпортоффлоаддата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ есернетсвитчпортоффлоаддата** имеет следующие свойства.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "состояние функции разгрузки порта коммутатора Ethernet".

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **maxlen** (256)
</dt> </dl>

Имя подкласса, используемого при создании этого экземпляра данных порта. Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md)и всегда имеет значение "мсвм \_ есернетсвитчпортоффлоаддата".

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "представляет данные состояния функции разгрузки порта".

</dd> <dt>

**девицекреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **maxlen** (256)
</dt> </dl>

Имя класса создания системы области. Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md)и всегда имеет значение "мсвм \_ есернетсвитчпорт".

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **maxlen** (64)
</dt> </dl>

ИДЕНТИФИКАТОР устройства, определяющего область данного экземпляра данных порта. Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "состояние функции разгрузки порта коммутатора Ethernet".

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

**иовоффлоадусаже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Текущий уровень использования при разгрузке виртуализации ввода-вывода (IOV).

</dd> <dt>

**иовкуеуепаирусаже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (7), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Текущее число пар очередей, используемых портом.

</dd> <dt>

**иоввфдатапасактиве**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (6), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Указывает, активен ли путь к данным на IOV VF.

</dd> <dt>

**иоввфид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Текущий идентификатор IOV VF, назначенный порту. Это допустимо, если **иовоффлоадусаже** не равен нулю.

</dd> <dt>

**ипсеккуррентоффлоадсакаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Текущее число слотов для разгрузки сопоставления безопасности (SA), используемых в порте.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **maxlen** (256)
</dt> </dl>

Строка, уникально идентифицирующая этот экземпляр данных порта в области действия коммутатора и порта. Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md).

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **maxlen** (256)
</dt> </dl>

Имя класса создания системы области. Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md)и всегда имеет значение "мсвм \_ виртуалесернетсвитч".

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **maxlen** (256)
</dt> </dl>

Имя виртуального коммутатора, который ограничивает область данного экземпляра данных порта. Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md).

</dd> <dt>

**вммкенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (9), **интерфацеверсион** (2), **интерфацеревисион** (0)
</dt> </dl>

Указывает, является ли ВММК активным.

> [!Note]  
> это свойство было добавлено в Windows 10 версии 1703.

 

</dd> <dt>

**вммккуеуепаирс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (10), **интерфацеверсион** (2), **интерфацеревисион** (0)
</dt> </dl>

Указывает, сколько очередей используется для VRSS/ВММК.

> [!Note]  
> это свойство было добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> <dt>

**вмкид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (4), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Текущий идентификатор очереди виртуальной машины, назначенный порту. Это допустимо, если **вмкоффлоадусаже** не равен нулю.

</dd> <dt>

**вмкоффлоадусаже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Текущее использование разгрузки очереди виртуальных машин (VMQ).

</dd> <dt>

**врссенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (8), **интерфацеверсион** (2), **интерфацеревисион** (0)
</dt> </dl>

Указывает, активна ли vRSS.

> [!Note]  
> это свойство было добавлено в Windows 10 версии 1703.

 

</dd> <dt>

**врссексклудепримарипроцессор**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (13), **интерфацеверсион** (3), **интерфацеревисион** (0)
</dt> </dl>

Указывает, исключается ли основной ЦП VMQ из таблицы косвенных обращений VRSS/ВММК.

> [!Note]  
> добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**врссиндепенденсостспреадинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (14), **интерфацеверсион** (3), **интерфацеревисион** (0)
</dt> </dl>

Указывает, происходит ли распространение VRSS или ВММК на стороне узла независимо от параметров RSS виртуального сетевого адаптера.

> [!Note]  
> добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**врссминкуеуепаирс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (11), **интерфацеверсион** (3), **интерфацеревисион** (0)
</dt> </dl>

Указывает минимальное число очередей, используемых для VRSS/ВММК.

> [!Note]  
> добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**врсскуеуесчедулингмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (12), **интерфацеверсион** (3), **интерфацеревисион** (0)
</dt> </dl>

Указывает, каким способом очереди VRSS/ВММК связаны с разными процессорами узла.

> [!Note]  
> добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**врссвмбусчаннелаффинитиполици**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (15), **интерфацеверсион** (3), **интерфацеревисион** (0)
</dt> </dl>

Указывает, как привязаны каналы VMBus для процессоров размещения.

> [!Note]  
> добавлено в Windows 10 версии 1709.

 

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


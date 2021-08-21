---
description: Представляет данные параметра функции разгрузки порта.
ms.assetid: 7b8d8bee-86f3-4c55-bb32-987bf840d995
title: Класс Msvm_EthernetSwitchPortOffloadSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadSettingData
- Msvm_EthernetSwitchPortOffloadSettingData.InstanceID
- Msvm_EthernetSwitchPortOffloadSettingData.Caption
- Msvm_EthernetSwitchPortOffloadSettingData.Description
- Msvm_EthernetSwitchPortOffloadSettingData.ElementName
- Msvm_EthernetSwitchPortOffloadSettingData.IPSecOffloadLimit
- Msvm_EthernetSwitchPortOffloadSettingData.VMQOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVQueuePairsRequested
- Msvm_EthernetSwitchPortOffloadSettingData.IOVInterruptModeration
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationInterval
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadSettingData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadSettingData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadSettingData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadSettingData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.VrssEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationCount
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectNumProcs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ddf58a10e85003a00e0d757f29db55a49f98f0ba22e8c3124b83a593f2a3908f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148303"
---
# <a name="msvm_ethernetswitchportoffloadsettingdata-class"></a>\_Класс мсвм есернетсвитчпортоффлоадсеттингдата

Представляет данные параметра функции разгрузки порта.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Settings";
  string  Description = "Represents the port offload feature setting data.";
  string  ElementName = "Ethernet Switch Port Offload Settings";
  uint32  IPSecOffloadLimit = 512;
  uint32  VMQOffloadWeight = 100;
  uint32  IOVOffloadWeight = 0;
  uint32  IOVQueuePairsRequested = 1;
  uint32  IOVInterruptModeration = 0;
  uint32  PacketDirectModerationInterval = 0;
  uint32  VmmqQueuePairs = 16;
  uint32  VrssVmbusChannelAffinityPolicy = 3;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 2;
  uint32  VrssMinQueuePairs = 1;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = TRUE;
  uint32  PacketDirectModerationCount = 0;
  uint32  PacketDirectNumProcs = 1;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ есернетсвитчпортоффлоадсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ есернетсвитчпортоффлоадсеттингдата** имеет следующие свойства.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "разгрузка порта коммутатора Ethernet Параметры".

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "представляет данные параметра функции разгрузки порта".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "разгрузка порта коммутатора Ethernet Параметры".

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

**иовинтерруптмодератион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Значение контроля прерываний для разгрузки виртуализации ввода-вывода (IOV). Значение по умолчанию равно 0.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**По умолчанию** (0)


</dt> <dd></dd> <dt>

<span id="Adaptive"></span><span id="adaptive"></span><span id="ADAPTIVE"></span>

**Адаптивное** (1)


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Off** (2)


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

**Низкий** (100)


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

**Средний** (200)


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

**Высокий** (300)


</dt> <dd></dd> </dl>

</dd> <dt>

**иовоффлоадвеигхт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Вес, назначенный этому порту для разгрузки виртуализации ввода-вывода (IOV). Вес — это относительная важность при назначении ресурсов IOV. Установка значения 0 для свойства **иовоффлоадвеигхт** отключает разгрузку IOV на порте. Значение по умолчанию равно 0.

</dd> <dt>

**иовкуеуепаирсрекуестед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (4), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Количество пар очередей, запрошенных для этого порта при разгрузке виртуализации ввода-вывода (IOV). Значение по умолчанию — 1.

</dd> <dt>

**ипсекоффлоадлимит**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Максимальное число слотов для разгрузки сопоставления безопасности (SA), разрешенных через порт.

</dd> <dt>

**паккетдиректмодератионкаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (7), **интерфацеверсион** (2), **интерфацеревисион** (0)
</dt> </dl>

Значение счетчика контроля прерываний для пакета Direct (PD). Значение по умолчанию — 0.

> [!Note]  
> Свойство добавлено в Windows 10.

 

</dd> <dt>

**паккетдиректмодератионинтервал**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (8), **интерфацеверсион** (2), **интерфацеревисион** (0)
</dt> </dl>

Значение интервала контроля прерываний для пакета Direct (PD). Значение по умолчанию — 0.

> [!Note]  
> Свойство добавлено в Windows 10.

 

</dd> <dt>

**паккетдиректнумпрокс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (6), **интерфацеверсион** (2), **интерфацеревисион** (0)
</dt> </dl>

Число процессоров, используемых узлом для обработки пакетов, отправленных с этого порта в режиме пакетного Direct. Значение по умолчанию — 1.

> [!Note]  
> Свойство добавлено в Windows 10.

 

</dd> <dt>

**вммкенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (10), **интерфацеверсион** (3), **интерфацеревисион** (0)
</dt> </dl>

Включите разгрузку ВММК, если она поддерживается оборудованием. Значение по умолчанию — false.

> [!Note]  
> это свойство было добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> <dt>

**вммккуеуепаирс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (11), **интерфацеверсион** (3), **интерфацеревисион** (0)
</dt> </dl>

Число очередей, выделяемых при включении VRSS. Значение по умолчанию равно 16.

> [!Note]  
> это свойство было добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> <dt>

**вмкоффлоадвеигхт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Вес, назначенный этому порту для разгрузки очереди виртуальных машин (VMQ). Вес — это относительная важность при назначении ресурсов VMQ. Установка значения 0 для свойства **вмкоффлоадвеигхт** отключает VMQ на порте. Значение по умолчанию — 100.

</dd> <dt>

**врссенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (9), **интерфацеверсион** (3), **интерфацеревисион** (0)
</dt> </dl>

Включите VRSS. Значение по умолчанию — true.

> [!Note]  
> это свойство было добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> <dt>

**врссексклудепримарипроцессор**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (14), **интерфацеверсион** (4), **интерфацеревисион** (0)
</dt> </dl>

Следует ли исключать основной процессор VMQ из таблицы косвенных обращений VRSS, если VRSS включен. Значение по умолчанию — false.

> [!Note]  
> добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**врссиндепенденсостспреадинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (15), **интерфацеверсион** (4), **интерфацеревисион** (0)
</dt> </dl>

Следует ли всегда выполнять VRSS на стороне узла при включении VRSS, независимо от настройки RSS виртуального сетевого адаптера. Значение по умолчанию — false.

> [!Note]  
> добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**врссминкуеуепаирс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (12), **интерфацеверсион** (4), **интерфацеревисион** (0)
</dt> </dl>

Минимальное число очередей, выделяемых при включении VRSS. Значение по умолчанию — 1.

> [!Note]  
> добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**врсскуеуесчедулингмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (13), **интерфацеверсион** (4), **интерфацеревисион** (0)
</dt> </dl>

Режим планирования очереди, используемый при включении VRSS. По умолчанию используется статическое планирование.

> [!Note]  
> добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**врссвмбусчаннелаффинитиполици**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (16), **интерфацеверсион** (4), **интерфацеревисион** (0)
</dt> </dl>

Политика сходства каналов VMBus, используемая при включении VRSS. Значение по умолчанию — strong.

> [!Note]  
> добавлено в Windows 10 версии 1709.

 

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


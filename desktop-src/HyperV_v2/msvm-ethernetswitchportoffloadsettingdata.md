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
ms.openlocfilehash: 150a7b5e54e371c11741dd7c763b0ae145354b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684697"
---
# <a name="msvm_ethernetswitchportoffloadsettingdata-class"></a><span data-ttu-id="77a75-103">\_Класс мсвм есернетсвитчпортоффлоадсеттингдата</span><span class="sxs-lookup"><span data-stu-id="77a75-103">Msvm\_EthernetSwitchPortOffloadSettingData class</span></span>

<span data-ttu-id="77a75-104">Представляет данные параметра функции разгрузки порта.</span><span class="sxs-lookup"><span data-stu-id="77a75-104">Represents the port offload feature setting data.</span></span>

<span data-ttu-id="77a75-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="77a75-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="77a75-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77a75-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="77a75-107">Члены</span><span class="sxs-lookup"><span data-stu-id="77a75-107">Members</span></span>

<span data-ttu-id="77a75-108">Класс **мсвм \_ есернетсвитчпортоффлоадсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="77a75-108">The **Msvm\_EthernetSwitchPortOffloadSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="77a75-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="77a75-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="77a75-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="77a75-110">Properties</span></span>

<span data-ttu-id="77a75-111">Класс **мсвм \_ есернетсвитчпортоффлоадсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="77a75-111">The **Msvm\_EthernetSwitchPortOffloadSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="77a75-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="77a75-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="77a75-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77a75-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77a75-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="77a75-115">A short description of the object.</span></span> <span data-ttu-id="77a75-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "параметры разгрузки порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="77a75-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Settings".</span></span>

</dd> <dt>

<span data-ttu-id="77a75-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="77a75-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="77a75-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77a75-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77a75-120">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="77a75-120">A description of the object.</span></span> <span data-ttu-id="77a75-121">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "представляет данные параметра функции разгрузки порта".</span><span class="sxs-lookup"><span data-stu-id="77a75-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port offload feature setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="77a75-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="77a75-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="77a75-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77a75-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77a75-125">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="77a75-125">A display name for the object.</span></span> <span data-ttu-id="77a75-126">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "параметры разгрузки порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="77a75-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Settings".</span></span>

</dd> <dt>

<span data-ttu-id="77a75-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="77a75-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="77a75-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77a75-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77a75-130">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="77a75-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="77a75-131">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="77a75-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="77a75-132">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="77a75-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="77a75-133">**иовинтерруптмодератион**</span><span class="sxs-lookup"><span data-stu-id="77a75-133">**IOVInterruptModeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77a75-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-136">Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-136">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-137">Значение контроля прерываний для разгрузки виртуализации ввода-вывода (IOV).</span><span class="sxs-lookup"><span data-stu-id="77a75-137">The interrupt moderation value for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="77a75-138">Значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="77a75-138">The default is 0.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="77a75-139">**По умолчанию** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-139">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Adaptive"></span><span id="adaptive"></span><span id="ADAPTIVE"></span>

<span data-ttu-id="77a75-140">**Адаптивное** (1)</span><span class="sxs-lookup"><span data-stu-id="77a75-140">**Adaptive** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="77a75-141">**Off** (2)</span><span class="sxs-lookup"><span data-stu-id="77a75-141">**Off** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="77a75-142">**Низкий** (100)</span><span class="sxs-lookup"><span data-stu-id="77a75-142">**Low** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="77a75-143">**Средний** (200)</span><span class="sxs-lookup"><span data-stu-id="77a75-143">**Medium** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="77a75-144">**Высокий** (300)</span><span class="sxs-lookup"><span data-stu-id="77a75-144">**High** (300)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="77a75-145">**иовоффлоадвеигхт**</span><span class="sxs-lookup"><span data-stu-id="77a75-145">**IOVOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77a75-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-147">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-148">Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-148">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-149">Вес, назначенный этому порту для разгрузки виртуализации ввода-вывода (IOV).</span><span class="sxs-lookup"><span data-stu-id="77a75-149">The weight assigned to this port for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="77a75-150">Вес — это относительная важность при назначении ресурсов IOV.</span><span class="sxs-lookup"><span data-stu-id="77a75-150">The weight is the relative importance when assigning IOV resources.</span></span> <span data-ttu-id="77a75-151">Установка значения 0 для свойства **иовоффлоадвеигхт** отключает разгрузку IOV на порте.</span><span class="sxs-lookup"><span data-stu-id="77a75-151">Setting the **IOVOffloadWeight** property to 0 disables IOV offloading on the port.</span></span> <span data-ttu-id="77a75-152">Значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="77a75-152">The default is 0.</span></span>

</dd> <dt>

<span data-ttu-id="77a75-153">**иовкуеуепаирсрекуестед**</span><span class="sxs-lookup"><span data-stu-id="77a75-153">**IOVQueuePairsRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-154">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77a75-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-156">Квалификаторы: **вмидатаид** (4), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-156">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-157">Количество пар очередей, запрошенных для этого порта при разгрузке виртуализации ввода-вывода (IOV).</span><span class="sxs-lookup"><span data-stu-id="77a75-157">The number of queue pairs requested for this port for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="77a75-158">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="77a75-158">The default is 1.</span></span>

</dd> <dt>

<span data-ttu-id="77a75-159">**ипсекоффлоадлимит**</span><span class="sxs-lookup"><span data-stu-id="77a75-159">**IPSecOffloadLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-160">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77a75-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-161">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-162">Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-162">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-163">Максимальное число слотов для разгрузки сопоставления безопасности (SA), разрешенных через порт.</span><span class="sxs-lookup"><span data-stu-id="77a75-163">The maximum number of security association (SA) offload slots allowed from the port.</span></span>

</dd> <dt>

<span data-ttu-id="77a75-164">**паккетдиректмодератионкаунт**</span><span class="sxs-lookup"><span data-stu-id="77a75-164">**PacketDirectModerationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-165">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77a75-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-167">Квалификаторы: **вмидатаид** (7), **интерфацеверсион** (2), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-167">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-168">Значение счетчика контроля прерываний для пакета Direct (PD). Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="77a75-168">The interrupt moderation count value for Packet Direct (PD).The default is 0.</span></span>

> [!Note]  
> <span data-ttu-id="77a75-169">Свойство добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="77a75-169">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="77a75-170">**паккетдиректмодератионинтервал**</span><span class="sxs-lookup"><span data-stu-id="77a75-170">**PacketDirectModerationInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-171">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77a75-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-172">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-173">Квалификаторы: **вмидатаид** (8), **интерфацеверсион** (2), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-173">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-174">Значение интервала контроля прерываний для пакета Direct (PD). Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="77a75-174">The interrupt moderation interval value for Packet Direct (PD).The default is 0.</span></span>

> [!Note]  
> <span data-ttu-id="77a75-175">Свойство добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="77a75-175">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="77a75-176">**паккетдиректнумпрокс**</span><span class="sxs-lookup"><span data-stu-id="77a75-176">**PacketDirectNumProcs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-177">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77a75-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-178">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-179">Квалификаторы: **вмидатаид** (6), **интерфацеверсион** (2), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-179">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-180">Число процессоров, используемых узлом для обработки пакетов, отправленных с этого порта в режиме пакетного Direct.</span><span class="sxs-lookup"><span data-stu-id="77a75-180">The number of processors used by the host for processing packets sent from this port in Packet Direct mode.</span></span> <span data-ttu-id="77a75-181">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="77a75-181">The default is 1.</span></span>

> [!Note]  
> <span data-ttu-id="77a75-182">Свойство добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="77a75-182">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="77a75-183">**вммкенаблед**</span><span class="sxs-lookup"><span data-stu-id="77a75-183">**VmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-184">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="77a75-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-185">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-186">Квалификаторы: **вмидатаид** (10), **интерфацеверсион** (3), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-186">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-187">Включите разгрузку ВММК, если она поддерживается оборудованием. Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="77a75-187">Enable VMMQ offload if supported by hardware.The default is False.</span></span>

> [!Note]  
> <span data-ttu-id="77a75-188">Это свойство было добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="77a75-188">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="77a75-189">**вммккуеуепаирс**</span><span class="sxs-lookup"><span data-stu-id="77a75-189">**VmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-190">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77a75-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-191">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-191">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-192">Квалификаторы: **вмидатаид** (11), **интерфацеверсион** (3), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-192">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-193">Число очередей, выделяемых при включении VRSS.</span><span class="sxs-lookup"><span data-stu-id="77a75-193">The number of queues to allocate when VRSS is enabled.</span></span> <span data-ttu-id="77a75-194">Значение по умолчанию равно 16.</span><span class="sxs-lookup"><span data-stu-id="77a75-194">The default is 16.</span></span>

> [!Note]  
> <span data-ttu-id="77a75-195">Это свойство было добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="77a75-195">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="77a75-196">**вмкоффлоадвеигхт**</span><span class="sxs-lookup"><span data-stu-id="77a75-196">**VMQOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-197">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77a75-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-198">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-198">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-199">Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-199">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-200">Вес, назначенный этому порту для разгрузки очереди виртуальных машин (VMQ).</span><span class="sxs-lookup"><span data-stu-id="77a75-200">The weight assigned to this port for virtual machine queue (VMQ) offloading.</span></span> <span data-ttu-id="77a75-201">Вес — это относительная важность при назначении ресурсов VMQ.</span><span class="sxs-lookup"><span data-stu-id="77a75-201">The weight is the relative importance when assigning VMQ resources.</span></span> <span data-ttu-id="77a75-202">Установка значения 0 для свойства **вмкоффлоадвеигхт** отключает VMQ на порте.</span><span class="sxs-lookup"><span data-stu-id="77a75-202">Setting the **VMQOffloadWeight** property to 0 disables VMQ on the port.</span></span> <span data-ttu-id="77a75-203">Значение по умолчанию — 100.</span><span class="sxs-lookup"><span data-stu-id="77a75-203">The default is 100.</span></span>

</dd> <dt>

<span data-ttu-id="77a75-204">**врссенаблед**</span><span class="sxs-lookup"><span data-stu-id="77a75-204">**VrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-205">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="77a75-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-206">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-206">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-207">Квалификаторы: **вмидатаид** (9), **интерфацеверсион** (3), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-207">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-208">Включите VRSS.</span><span class="sxs-lookup"><span data-stu-id="77a75-208">Enable VRSS.</span></span> <span data-ttu-id="77a75-209">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="77a75-209">The default is true.</span></span>

> [!Note]  
> <span data-ttu-id="77a75-210">Это свойство было добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="77a75-210">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="77a75-211">**врссексклудепримарипроцессор**</span><span class="sxs-lookup"><span data-stu-id="77a75-211">**VrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-212">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="77a75-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-213">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-213">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-214">Квалификаторы: **вмидатаид** (14), **интерфацеверсион** (4), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-214">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-215">Следует ли исключать основной процессор VMQ из таблицы косвенных обращений VRSS, если VRSS включен. Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="77a75-215">Whether to exclude primary VMQ processor from the VRSS indirection table when VRSS is enabled.The default is false.</span></span>

> [!Note]  
> <span data-ttu-id="77a75-216">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="77a75-216">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="77a75-217">**врссиндепенденсостспреадинг**</span><span class="sxs-lookup"><span data-stu-id="77a75-217">**VrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-218">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="77a75-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-219">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-219">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-220">Квалификаторы: **вмидатаид** (15), **интерфацеверсион** (4), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-220">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-221">Следует ли всегда выполнять VRSS на стороне узла при включении VRSS, независимо от настройки RSS виртуального сетевого адаптера. Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="77a75-221">Whether to always do host-side VRSS when VRSS is enabled, regardless of RSS setting of the virtual NIC.The default is false.</span></span>

> [!Note]  
> <span data-ttu-id="77a75-222">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="77a75-222">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="77a75-223">**врссминкуеуепаирс**</span><span class="sxs-lookup"><span data-stu-id="77a75-223">**VrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-224">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77a75-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-225">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-225">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-226">Квалификаторы: **вмидатаид** (12), **интерфацеверсион** (4), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-226">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-227">Минимальное число очередей, выделяемых при включении VRSS. Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="77a75-227">The minimum number of queues to allocate when VRSS is enabled.The default is 1.</span></span>

> [!Note]  
> <span data-ttu-id="77a75-228">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="77a75-228">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="77a75-229">**врсскуеуесчедулингмоде**</span><span class="sxs-lookup"><span data-stu-id="77a75-229">**VrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-230">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77a75-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-231">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-231">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-232">Квалификаторы: **вмидатаид** (13), **интерфацеверсион** (4), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-232">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-233">Режим планирования очереди, используемый при включении VRSS. По умолчанию используется статическое планирование.</span><span class="sxs-lookup"><span data-stu-id="77a75-233">The queue scheduling mode to use when VRSS is enabled.The default is static scheduling.</span></span>

> [!Note]  
> <span data-ttu-id="77a75-234">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="77a75-234">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="77a75-235">**врссвмбусчаннелаффинитиполици**</span><span class="sxs-lookup"><span data-stu-id="77a75-235">**VrssVmbusChannelAffinityPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77a75-236">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77a75-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77a75-237">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="77a75-237">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="77a75-238">Квалификаторы: **вмидатаид** (16), **интерфацеверсион** (4), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="77a75-238">Qualifiers: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="77a75-239">Политика сходства каналов VMBus, используемая при включении VRSS. Значение по умолчанию — strong.</span><span class="sxs-lookup"><span data-stu-id="77a75-239">The vmbus channel affinity policy to use when VRSS is enabled.The default is strong.</span></span>

> [!Note]  
> <span data-ttu-id="77a75-240">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="77a75-240">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77a75-241">Требования</span><span class="sxs-lookup"><span data-stu-id="77a75-241">Requirements</span></span>



| <span data-ttu-id="77a75-242">Требование</span><span class="sxs-lookup"><span data-stu-id="77a75-242">Requirement</span></span> | <span data-ttu-id="77a75-243">Значение</span><span class="sxs-lookup"><span data-stu-id="77a75-243">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77a75-244">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77a75-244">Minimum supported client</span></span><br/> | <span data-ttu-id="77a75-245">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="77a75-245">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="77a75-246">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77a75-246">Minimum supported server</span></span><br/> | <span data-ttu-id="77a75-247">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="77a75-247">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="77a75-248">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="77a75-248">Namespace</span></span><br/>                | <span data-ttu-id="77a75-249">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="77a75-249">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="77a75-250">MOF</span><span class="sxs-lookup"><span data-stu-id="77a75-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77a75-251"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77a75-251"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="77a75-252">DLL</span><span class="sxs-lookup"><span data-stu-id="77a75-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77a75-253"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="77a75-253"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


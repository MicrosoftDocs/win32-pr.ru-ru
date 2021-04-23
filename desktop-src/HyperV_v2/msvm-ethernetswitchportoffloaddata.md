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
ms.openlocfilehash: fd60e98c8df12b539bb51c60b34e7931b762dc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664768"
---
# <a name="msvm_ethernetswitchportoffloaddata-class"></a><span data-ttu-id="97378-103">\_Класс мсвм есернетсвитчпортоффлоаддата</span><span class="sxs-lookup"><span data-stu-id="97378-103">Msvm\_EthernetSwitchPortOffloadData class</span></span>

<span data-ttu-id="97378-104">Представляет данные состояния функции разгрузки порта.</span><span class="sxs-lookup"><span data-stu-id="97378-104">Represents the port offload feature status data.</span></span>

<span data-ttu-id="97378-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="97378-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="97378-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97378-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="97378-107">Члены</span><span class="sxs-lookup"><span data-stu-id="97378-107">Members</span></span>

<span data-ttu-id="97378-108">Класс **мсвм \_ есернетсвитчпортоффлоаддата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="97378-108">The **Msvm\_EthernetSwitchPortOffloadData** class has these types of members:</span></span>

-   [<span data-ttu-id="97378-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="97378-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97378-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="97378-110">Properties</span></span>

<span data-ttu-id="97378-111">Класс **мсвм \_ есернетсвитчпортоффлоаддата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="97378-111">The **Msvm\_EthernetSwitchPortOffloadData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97378-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="97378-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="97378-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97378-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97378-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="97378-115">A short description of the object.</span></span> <span data-ttu-id="97378-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "состояние функции разгрузки порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="97378-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="97378-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="97378-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="97378-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97378-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97378-120">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="97378-120">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="97378-121">Имя подкласса, используемого при создании этого экземпляра данных порта.</span><span class="sxs-lookup"><span data-stu-id="97378-121">The name of the subclass used in the creation of this port data instance.</span></span> <span data-ttu-id="97378-122">Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md)и всегда имеет значение "мсвм \_ есернетсвитчпортоффлоаддата".</span><span class="sxs-lookup"><span data-stu-id="97378-122">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPortOffloadData".</span></span>

</dd> <dt>

<span data-ttu-id="97378-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="97378-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="97378-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97378-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97378-126">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="97378-126">A description of the object.</span></span> <span data-ttu-id="97378-127">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "представляет данные состояния функции разгрузки порта".</span><span class="sxs-lookup"><span data-stu-id="97378-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port offload feature status data.".</span></span>

</dd> <dt>

<span data-ttu-id="97378-128">**девицекреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="97378-128">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="97378-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97378-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97378-131">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="97378-131">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="97378-132">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="97378-132">The scoping system's creation class name.</span></span> <span data-ttu-id="97378-133">Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md)и всегда имеет значение "мсвм \_ есернетсвитчпорт".</span><span class="sxs-lookup"><span data-stu-id="97378-133">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="97378-134">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="97378-134">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="97378-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97378-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97378-137">Квалификаторы: **Key**, **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="97378-137">Qualifiers: **Key**, **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="97378-138">ИДЕНТИФИКАТОР устройства, определяющего область данного экземпляра данных порта.</span><span class="sxs-lookup"><span data-stu-id="97378-138">The Device ID of the port that scopes this port data instance.</span></span> <span data-ttu-id="97378-139">Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="97378-139">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="97378-140">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="97378-140">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="97378-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97378-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97378-143">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="97378-143">A display name for the object.</span></span> <span data-ttu-id="97378-144">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "состояние функции разгрузки порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="97378-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="97378-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="97378-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="97378-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97378-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97378-148">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="97378-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="97378-149">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="97378-149">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="97378-150">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="97378-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="97378-151">**иовоффлоадусаже**</span><span class="sxs-lookup"><span data-stu-id="97378-151">**IovOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-152">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97378-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97378-153">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="97378-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="97378-154">Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="97378-154">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="97378-155">Текущий уровень использования при разгрузке виртуализации ввода-вывода (IOV).</span><span class="sxs-lookup"><span data-stu-id="97378-155">The current I/O virtualization (IOV) offload usage.</span></span>

</dd> <dt>

<span data-ttu-id="97378-156">**иовкуеуепаирусаже**</span><span class="sxs-lookup"><span data-stu-id="97378-156">**IovQueuePairUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97378-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97378-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="97378-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="97378-159">Квалификаторы: **вмидатаид** (7), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="97378-159">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="97378-160">Текущее число пар очередей, используемых портом.</span><span class="sxs-lookup"><span data-stu-id="97378-160">The current number of queue pairs being used by the port.</span></span>

</dd> <dt>

<span data-ttu-id="97378-161">**иоввфдатапасактиве**</span><span class="sxs-lookup"><span data-stu-id="97378-161">**IovVfDataPathActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-162">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="97378-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97378-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="97378-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="97378-164">Квалификаторы: **вмидатаид** (6), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="97378-164">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="97378-165">Указывает, активен ли путь к данным на IOV VF.</span><span class="sxs-lookup"><span data-stu-id="97378-165">Indicates whether the IOV VF data path is active.</span></span>

</dd> <dt>

<span data-ttu-id="97378-166">**иоввфид**</span><span class="sxs-lookup"><span data-stu-id="97378-166">**IovVfId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-167">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="97378-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="97378-168">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="97378-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="97378-169">Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="97378-169">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="97378-170">Текущий идентификатор IOV VF, назначенный порту.</span><span class="sxs-lookup"><span data-stu-id="97378-170">The current IOV VF identifier that is assigned to the port.</span></span> <span data-ttu-id="97378-171">Это допустимо, если **иовоффлоадусаже** не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="97378-171">This is valid if **IovOffloadUsage** is not zero.</span></span>

</dd> <dt>

<span data-ttu-id="97378-172">**ипсеккуррентоффлоадсакаунт**</span><span class="sxs-lookup"><span data-stu-id="97378-172">**IpsecCurrentOffloadSaCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-173">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97378-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97378-174">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="97378-174">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="97378-175">Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="97378-175">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="97378-176">Текущее число слотов для разгрузки сопоставления безопасности (SA), используемых в порте.</span><span class="sxs-lookup"><span data-stu-id="97378-176">The current number of security association (SA) offload slots in use on the port.</span></span>

</dd> <dt>

<span data-ttu-id="97378-177">**Name**</span><span class="sxs-lookup"><span data-stu-id="97378-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="97378-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97378-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97378-180">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="97378-180">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="97378-181">Строка, уникально идентифицирующая этот экземпляр данных порта в области действия коммутатора и порта.</span><span class="sxs-lookup"><span data-stu-id="97378-181">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span> <span data-ttu-id="97378-182">Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="97378-182">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="97378-183">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="97378-183">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="97378-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97378-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97378-186">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="97378-186">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="97378-187">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="97378-187">The scoping system's creation class name.</span></span> <span data-ttu-id="97378-188">Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md)и всегда имеет значение "мсвм \_ виртуалесернетсвитч".</span><span class="sxs-lookup"><span data-stu-id="97378-188">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="97378-189">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="97378-189">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="97378-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97378-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97378-192">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="97378-192">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="97378-193">Имя виртуального коммутатора, который ограничивает область данного экземпляра данных порта.</span><span class="sxs-lookup"><span data-stu-id="97378-193">The name of the virtual switch that scopes this port data instance.</span></span> <span data-ttu-id="97378-194">Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="97378-194">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="97378-195">**вммкенаблед**</span><span class="sxs-lookup"><span data-stu-id="97378-195">**VmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-196">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="97378-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97378-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97378-198">Квалификаторы: **вмидатаид** (9), **интерфацеверсион** (2), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="97378-198">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="97378-199">Указывает, является ли ВММК активным.</span><span class="sxs-lookup"><span data-stu-id="97378-199">Indicates if VMMQ is active.</span></span>

> [!Note]  
> <span data-ttu-id="97378-200">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="97378-200">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="97378-201">**вммккуеуепаирс**</span><span class="sxs-lookup"><span data-stu-id="97378-201">**VmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-202">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97378-202">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97378-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97378-204">Квалификаторы: **вмидатаид** (10), **интерфацеверсион** (2), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="97378-204">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="97378-205">Указывает, сколько очередей используется для VRSS/ВММК.</span><span class="sxs-lookup"><span data-stu-id="97378-205">Indicates how many queues are used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="97378-206">Это свойство было добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="97378-206">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="97378-207">**вмкид**</span><span class="sxs-lookup"><span data-stu-id="97378-207">**VMQId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-208">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97378-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97378-209">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="97378-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="97378-210">Квалификаторы: **вмидатаид** (4), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="97378-210">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="97378-211">Текущий идентификатор очереди виртуальной машины, назначенный порту.</span><span class="sxs-lookup"><span data-stu-id="97378-211">The current virtual machine queue identifier that is assigned to the port.</span></span> <span data-ttu-id="97378-212">Это допустимо, если **вмкоффлоадусаже** не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="97378-212">This is valid if **VMQOffloadUsage** is not zero.</span></span>

</dd> <dt>

<span data-ttu-id="97378-213">**вмкоффлоадусаже**</span><span class="sxs-lookup"><span data-stu-id="97378-213">**VMQOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-214">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97378-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97378-215">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="97378-215">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="97378-216">Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="97378-216">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="97378-217">Текущее использование разгрузки очереди виртуальных машин (VMQ).</span><span class="sxs-lookup"><span data-stu-id="97378-217">The current virtual machine queue (VMQ) offload usage.</span></span>

</dd> <dt>

<span data-ttu-id="97378-218">**врссенаблед**</span><span class="sxs-lookup"><span data-stu-id="97378-218">**VrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-219">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="97378-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97378-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97378-221">Квалификаторы: **вмидатаид** (8), **интерфацеверсион** (2), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="97378-221">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="97378-222">Указывает, активна ли vRSS.</span><span class="sxs-lookup"><span data-stu-id="97378-222">Indicates if vRSS is active.</span></span>

> [!Note]  
> <span data-ttu-id="97378-223">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="97378-223">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="97378-224">**врссексклудепримарипроцессор**</span><span class="sxs-lookup"><span data-stu-id="97378-224">**VrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-225">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="97378-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97378-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97378-227">Квалификаторы: **вмидатаид** (13), **интерфацеверсион** (3), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="97378-227">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="97378-228">Указывает, исключается ли основной ЦП VMQ из таблицы косвенных обращений VRSS/ВММК.</span><span class="sxs-lookup"><span data-stu-id="97378-228">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="97378-229">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="97378-229">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="97378-230">**врссиндепенденсостспреадинг**</span><span class="sxs-lookup"><span data-stu-id="97378-230">**VrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-231">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="97378-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97378-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97378-233">Квалификаторы: **вмидатаид** (14), **интерфацеверсион** (3), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="97378-233">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="97378-234">Указывает, происходит ли распространение VRSS или ВММК на стороне узла независимо от параметров RSS виртуального сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="97378-234">Indicates whether host side VRSS/VMMQ spreading happens, regardless of RSS settings of the virtual NIC.</span></span>

> [!Note]  
> <span data-ttu-id="97378-235">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="97378-235">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="97378-236">**врссминкуеуепаирс**</span><span class="sxs-lookup"><span data-stu-id="97378-236">**VrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-237">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97378-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97378-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97378-239">Квалификаторы: **вмидатаид** (11), **интерфацеверсион** (3), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="97378-239">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="97378-240">Указывает минимальное число очередей, используемых для VRSS/ВММК.</span><span class="sxs-lookup"><span data-stu-id="97378-240">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="97378-241">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="97378-241">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="97378-242">**врсскуеуесчедулингмоде**</span><span class="sxs-lookup"><span data-stu-id="97378-242">**VrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-243">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97378-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97378-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97378-245">Квалификаторы: **вмидатаид** (12), **интерфацеверсион** (3), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="97378-245">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="97378-246">Указывает, каким способом очереди VRSS/ВММК связаны с разными процессорами узла.</span><span class="sxs-lookup"><span data-stu-id="97378-246">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="97378-247">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="97378-247">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="97378-248">**врссвмбусчаннелаффинитиполици**</span><span class="sxs-lookup"><span data-stu-id="97378-248">**VrssVmbusChannelAffinityPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97378-249">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97378-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97378-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97378-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97378-251">Квалификаторы: **вмидатаид** (15), **интерфацеверсион** (3), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="97378-251">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="97378-252">Указывает, как привязаны каналы VMBus для процессоров размещения.</span><span class="sxs-lookup"><span data-stu-id="97378-252">Indicates how Vmbus channels are affinitized to host processors.</span></span>

> [!Note]  
> <span data-ttu-id="97378-253">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="97378-253">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97378-254">Требования</span><span class="sxs-lookup"><span data-stu-id="97378-254">Requirements</span></span>



| <span data-ttu-id="97378-255">Требование</span><span class="sxs-lookup"><span data-stu-id="97378-255">Requirement</span></span> | <span data-ttu-id="97378-256">Значение</span><span class="sxs-lookup"><span data-stu-id="97378-256">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97378-257">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97378-257">Minimum supported client</span></span><br/> | <span data-ttu-id="97378-258">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="97378-258">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="97378-259">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97378-259">Minimum supported server</span></span><br/> | <span data-ttu-id="97378-260">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="97378-260">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="97378-261">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="97378-261">Namespace</span></span><br/>                | <span data-ttu-id="97378-262">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="97378-262">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="97378-263">MOF</span><span class="sxs-lookup"><span data-stu-id="97378-263">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97378-264"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97378-264"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="97378-265">DLL</span><span class="sxs-lookup"><span data-stu-id="97378-265">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97378-266"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="97378-266"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


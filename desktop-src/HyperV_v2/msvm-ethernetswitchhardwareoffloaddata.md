---
description: Представляет состояние аппаратной разгрузки коммутатора.
ms.assetid: 77a34df7-e3c4-4d91-af5a-91a03dd8246d
title: Класс Msvm_EthernetSwitchHardwareOffloadData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadData
- Msvm_EthernetSwitchHardwareOffloadData.InstanceID
- Msvm_EthernetSwitchHardwareOffloadData.Caption
- Msvm_EthernetSwitchHardwareOffloadData.Description
- Msvm_EthernetSwitchHardwareOffloadData.ElementName
- Msvm_EthernetSwitchHardwareOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.SystemName
- Msvm_EthernetSwitchHardwareOffloadData.CreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.Name
- Msvm_EthernetSwitchHardwareOffloadData.IovVfCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovVfUsage
- Msvm_EthernetSwitchHardwareOffloadData.VmqCapacity
- Msvm_EthernetSwitchHardwareOffloadData.VmqUsage
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSACapacity
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSAUsage
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchHardwareOffloadData.PacketDirectInUse
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssMinQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b64762b824cea7d3b064636e7f7f87777e053daf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664771"
---
# <a name="msvm_ethernetswitchhardwareoffloaddata-class"></a><span data-ttu-id="ce266-103">\_Класс мсвм есернетсвитчхардвареоффлоаддата</span><span class="sxs-lookup"><span data-stu-id="ce266-103">Msvm\_EthernetSwitchHardwareOffloadData class</span></span>

<span data-ttu-id="ce266-104">Представляет состояние аппаратной разгрузки коммутатора.</span><span class="sxs-lookup"><span data-stu-id="ce266-104">Represents the switch hardware offload status.</span></span>

<span data-ttu-id="ce266-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ce266-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce266-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce266-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1C37E01C-0CD6-496F-9076-90C131033DC2"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Offload Resource Status"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadData : Msvm_EthernetSwitchData
{
  string  InstanceID;
  string  Caption = Ethernet Switch Offload Resource Status;
  string  Description = Represents the switch hardware offload status.;
  string  ElementName = Ethernet Switch Offload Resource Status;
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  CreationClassName = "Msvm_EthernetSwitchHardwareOffloadData";
  string  Name;
  uint32  IovVfCapacity = 0;
  uint32  IovVfUsage = 0;
  uint32  VmqCapacity = 0;
  uint32  VmqUsage = 0;
  uint32  IPsecSACapacity = 0;
  uint32  IPsecSAUsage = 0;
  uint32  IovQueuePairCapacity = 0;
  uint32  IovQueuePairUsage = 0;
  boolean PacketDirectInUse = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 0;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 0;
  uint32  DefaultQueueVrssMinQueuePairs = 0;
  boolean DefaultQueueVmmqEnabled = FALSE;
  boolean DefaultQueueVrssEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="ce266-107">Члены</span><span class="sxs-lookup"><span data-stu-id="ce266-107">Members</span></span>

<span data-ttu-id="ce266-108">Класс **мсвм \_ есернетсвитчхардвареоффлоаддата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ce266-108">The **Msvm\_EthernetSwitchHardwareOffloadData** class has these types of members:</span></span>

-   [<span data-ttu-id="ce266-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ce266-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce266-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ce266-110">Properties</span></span>

<span data-ttu-id="ce266-111">Класс **мсвм \_ есернетсвитчхардвареоффлоаддата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ce266-111">The **Msvm\_EthernetSwitchHardwareOffloadData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce266-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ce266-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ce266-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce266-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ce266-115">A short description of the object.</span></span> <span data-ttu-id="ce266-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ce266-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ce266-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ce266-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ce266-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-120">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="ce266-120">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-121">Имя класса или подкласса, используемого при создании этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ce266-121">The name of the class or subclass used in the creation of this instance.</span></span> <span data-ttu-id="ce266-122">Это свойство наследуется от [**мсвм \_ есернетсвитчдата**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="ce266-122">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce266-123">**дефаулткуеуевммкенаблед**</span><span class="sxs-lookup"><span data-stu-id="ce266-123">**DefaultQueueVmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-124">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ce266-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-126">Квалификаторы: **вмидатаид** (11), **интерфацеверсион** (3), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-126">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-127">Текущий параметр ВММК для очереди по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ce266-127">The current VMMQ setting for default queue</span></span>

> [!Note]  
> <span data-ttu-id="ce266-128">Свойство добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="ce266-128">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="ce266-129">**дефаулткуеуевммккуеуепаирс**</span><span class="sxs-lookup"><span data-stu-id="ce266-129">**DefaultQueueVmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce266-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-132">Квалификаторы: **вмидатаид** (12), **интерфацеверсион** (3), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-132">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-133">Текущее число очередей, выделенных для очереди по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ce266-133">The current number of queues allocated for the default queue</span></span>

> [!Note]  
> <span data-ttu-id="ce266-134">Свойство добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="ce266-134">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="ce266-135">**дефаулткуеуеврссенаблед**</span><span class="sxs-lookup"><span data-stu-id="ce266-135">**DefaultQueueVrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-136">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ce266-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-138">Квалификаторы: **вмидатаид** (10), **интерфацеверсион** (3), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-138">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-139">Текущая настройка VRss для очереди по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ce266-139">The current VRss setting for default queue</span></span>

> [!Note]  
> <span data-ttu-id="ce266-140">Свойство добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="ce266-140">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="ce266-141">**дефаулткуеуеврссексклудепримарипроцессор**</span><span class="sxs-lookup"><span data-stu-id="ce266-141">**DefaultQueueVrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-142">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ce266-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-144">Квалификаторы: **вмидатаид** (15), **интерфацеверсион** (4), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-144">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-145">Указывает, исключается ли основной ЦП VMQ из таблицы косвенных обращений VRSS/ВММК.</span><span class="sxs-lookup"><span data-stu-id="ce266-145">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="ce266-146">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="ce266-146">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="ce266-147">**дефаулткуеуеврссиндепенденсостспреадинг**</span><span class="sxs-lookup"><span data-stu-id="ce266-147">**DefaultQueueVrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-148">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ce266-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-150">Квалификаторы: **вмидатаид** (16), **интерфацеверсион** (4), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-150">Qualifiers: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-151">Указывает, следует ли всегда выполнять распространение VRSS для очереди по умолчанию независимо от состояния RSS внешней впорт.</span><span class="sxs-lookup"><span data-stu-id="ce266-151">Indicates whether to always do VRSS spreading for default queue, regardless of the RSS state of the external vPort.</span></span>

> [!Note]  
> <span data-ttu-id="ce266-152">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="ce266-152">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="ce266-153">**дефаулткуеуеврссминкуеуепаирс**</span><span class="sxs-lookup"><span data-stu-id="ce266-153">**DefaultQueueVrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-154">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce266-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-156">Квалификаторы: **вмидатаид** (13), **интерфацеверсион** (4), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-156">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-157">Указывает минимальное число очередей, используемых для VRSS/ВММК.</span><span class="sxs-lookup"><span data-stu-id="ce266-157">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="ce266-158">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="ce266-158">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="ce266-159">**дефаулткуеуеврсскуеуесчедулингмоде**</span><span class="sxs-lookup"><span data-stu-id="ce266-159">**DefaultQueueVrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-160">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce266-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-162">Квалификаторы: **вмидатаид** (14), **интерфацеверсион** (4), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-162">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-163">Указывает, каким способом очереди VRSS/ВММК связаны с разными процессорами узла.</span><span class="sxs-lookup"><span data-stu-id="ce266-163">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="ce266-164">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="ce266-164">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="ce266-165">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ce266-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ce266-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce266-168">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ce266-168">A description of the object.</span></span> <span data-ttu-id="ce266-169">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ce266-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ce266-170">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ce266-170">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ce266-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce266-173">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="ce266-173">A display name for the object.</span></span> <span data-ttu-id="ce266-174">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ce266-174">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ce266-175">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ce266-175">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ce266-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-178">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="ce266-178">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ce266-179">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="ce266-179">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ce266-180">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ce266-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ce266-181">**иовкуеуепаиркапаЦити**</span><span class="sxs-lookup"><span data-stu-id="ce266-181">**IovQueuePairCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-182">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce266-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-184">Квалификаторы: **вмидатаид** (7), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-184">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-185">Максимальное число пар очередей, поддерживаемое параметром.</span><span class="sxs-lookup"><span data-stu-id="ce266-185">The maximum number of queue pairs supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="ce266-186">**иовкуеуепаирусаже**</span><span class="sxs-lookup"><span data-stu-id="ce266-186">**IovQueuePairUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-187">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce266-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-189">Квалификаторы: **вмидатаид** (8), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-189">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-190">Текущее число пар очередей, используемых параметром.</span><span class="sxs-lookup"><span data-stu-id="ce266-190">The current number of queue pairs being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="ce266-191">**иоввфкапаЦити**</span><span class="sxs-lookup"><span data-stu-id="ce266-191">**IovVfCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-192">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce266-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-194">Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-194">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-195">Максимальное число виртуальных функций, поддерживаемое параметром.</span><span class="sxs-lookup"><span data-stu-id="ce266-195">The maximum number of virtual functions supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="ce266-196">**иоввфусаже**</span><span class="sxs-lookup"><span data-stu-id="ce266-196">**IovVfUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-197">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce266-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-199">Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-199">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-200">Текущее число виртуальных функций, используемых параметром.</span><span class="sxs-lookup"><span data-stu-id="ce266-200">The current number of virtual functions being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="ce266-201">**ипсексакапаЦити**</span><span class="sxs-lookup"><span data-stu-id="ce266-201">**IPsecSACapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-202">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce266-202">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-204">Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-204">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-205">Максимальное число разгруженных сопоставлений безопасности IPsec, поддерживаемое коммутатором.</span><span class="sxs-lookup"><span data-stu-id="ce266-205">The maximum number of IPsec security association offloads supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="ce266-206">**ипсексаусаже**</span><span class="sxs-lookup"><span data-stu-id="ce266-206">**IPsecSAUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-207">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce266-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-209">Квалификаторы: **вмидатаид** (6), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-209">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-210">Текущее число разгрузок сопоставления безопасности IPsec, используемых параметром.</span><span class="sxs-lookup"><span data-stu-id="ce266-210">The current number of IPsec security association offloads being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="ce266-211">**Name**</span><span class="sxs-lookup"><span data-stu-id="ce266-211">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-212">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ce266-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-214">Квалификаторы: **ключ**, **Переопределение**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="ce266-214">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-215">Уникальное имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="ce266-215">The unique name of the resource.</span></span> <span data-ttu-id="ce266-216">Это свойство наследуется от [**мсвм \_ есернетсвитчдата**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="ce266-216">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce266-217">**паккетдиректинусе**</span><span class="sxs-lookup"><span data-stu-id="ce266-217">**PacketDirectInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-218">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ce266-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-220">Квалификаторы: **вмидатаид** (9), **интерфацеверсион** (2), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-220">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-221">Указывает, используется ли параметр Direct с пакетом</span><span class="sxs-lookup"><span data-stu-id="ce266-221">Indicates if packet direct is being used by the switch</span></span>

> [!Note]  
> <span data-ttu-id="ce266-222">Свойство добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ce266-222">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="ce266-223">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="ce266-223">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-224">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ce266-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-226">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="ce266-226">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-227">Имя класса создания системы размещения.</span><span class="sxs-lookup"><span data-stu-id="ce266-227">The hosting system's creation class name.</span></span> <span data-ttu-id="ce266-228">Это свойство наследуется от [**мсвм \_ есернетсвитчдата**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="ce266-228">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce266-229">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ce266-229">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ce266-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-232">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="ce266-232">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-233">Имя виртуального коммутатора, к которому привязан связанный экземпляр ресурса.</span><span class="sxs-lookup"><span data-stu-id="ce266-233">The name of the virtual switch to which the associated resource instance is bound.</span></span> <span data-ttu-id="ce266-234">Это свойство наследуется от [**мсвм \_ есернетсвитчдата**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="ce266-234">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce266-235">**вмккапаЦити**</span><span class="sxs-lookup"><span data-stu-id="ce266-235">**VmqCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-236">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce266-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-238">Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-238">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-239">Максимальное число разгрузок очереди виртуальной машины, поддерживаемое коммутатором.</span><span class="sxs-lookup"><span data-stu-id="ce266-239">The maximum number of virtual machine queue offloads supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="ce266-240">**вмкусаже**</span><span class="sxs-lookup"><span data-stu-id="ce266-240">**VmqUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce266-241">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce266-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce266-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce266-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce266-243">Квалификаторы: **вмидатаид** (4), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ce266-243">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ce266-244">Текущее число разгрузок очереди виртуальной машины, используемых параметром.</span><span class="sxs-lookup"><span data-stu-id="ce266-244">The current number of virtual machine queue offloads being used by the switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce266-245">Требования</span><span class="sxs-lookup"><span data-stu-id="ce266-245">Requirements</span></span>



| <span data-ttu-id="ce266-246">Требование</span><span class="sxs-lookup"><span data-stu-id="ce266-246">Requirement</span></span> | <span data-ttu-id="ce266-247">Значение</span><span class="sxs-lookup"><span data-stu-id="ce266-247">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce266-248">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce266-248">Minimum supported client</span></span><br/> | <span data-ttu-id="ce266-249">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ce266-249">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ce266-250">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce266-250">Minimum supported server</span></span><br/> | <span data-ttu-id="ce266-251">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ce266-251">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ce266-252">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ce266-252">Namespace</span></span><br/>                | <span data-ttu-id="ce266-253">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ce266-253">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ce266-254">MOF</span><span class="sxs-lookup"><span data-stu-id="ce266-254">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce266-255"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce266-255"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce266-256">DLL</span><span class="sxs-lookup"><span data-stu-id="ce266-256">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce266-257"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ce266-257"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


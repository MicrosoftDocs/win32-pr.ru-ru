---
description: Используется в методах Жетсуммаринформатион и Жетдефинитионфилесуммаринформатион \_ класса мсвм виртуалсистемманажементсервице для быстрого получения общих сведений, связанных с виртуальной машиной или моментальным снимком.
ms.assetid: 8D188BB2-4A56-4738-94DD-64D9F9B90B73
title: Класс Msvm_SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformation
- Msvm_SummaryInformation.InstanceID
- Msvm_SummaryInformation.AllocatedGPU
- Msvm_SummaryInformation.Shielded
- Msvm_SummaryInformation.AsynchronousTasks
- Msvm_SummaryInformation.CreationTime
- Msvm_SummaryInformation.ElementName
- Msvm_SummaryInformation.EnabledState
- Msvm_SummaryInformation.OtherEnabledState
- Msvm_SummaryInformation.GuestOperatingSystem
- Msvm_SummaryInformation.HealthState
- Msvm_SummaryInformation.Heartbeat
- Msvm_SummaryInformation.MemoryUsage
- Msvm_SummaryInformation.MemoryAvailable
- Msvm_SummaryInformation.AvailableMemoryBuffer
- Msvm_SummaryInformation.SwapFilesInUse
- Msvm_SummaryInformation.Name
- Msvm_SummaryInformation.Notes
- Msvm_SummaryInformation.Version
- Msvm_SummaryInformation.NumberOfProcessors
- Msvm_SummaryInformation.OperationalStatus
- Msvm_SummaryInformation.ProcessorLoad
- Msvm_SummaryInformation.ProcessorLoadHistory
- Msvm_SummaryInformation.Snapshots
- Msvm_SummaryInformation.StatusDescriptions
- Msvm_SummaryInformation.ThumbnailImage
- Msvm_SummaryInformation.ThumbnailImageHeight
- Msvm_SummaryInformation.ThumbnailImageWidth
- Msvm_SummaryInformation.UpTime
- Msvm_SummaryInformation.ReplicationState
- Msvm_SummaryInformation.ReplicationStateEx
- Msvm_SummaryInformation.ReplicationHealth
- Msvm_SummaryInformation.ReplicationHealthEx
- Msvm_SummaryInformation.ReplicationMode
- Msvm_SummaryInformation.TestReplicaSystem
- Msvm_SummaryInformation.ApplicationHealth
- Msvm_SummaryInformation.IntegrationServicesVersionState
- Msvm_SummaryInformation.MemorySpansPhysicalNumaNodes
- Msvm_SummaryInformation.ReplicationProviderId
- Msvm_SummaryInformation.EnhancedSessionModeState
- Msvm_SummaryInformation.VirtualSwitchNames
- Msvm_SummaryInformation.VirtualSystemSubType
- Msvm_SummaryInformation.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 817d025551ae10002b008a181edd8a7dfd2ec68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650560"
---
# <a name="msvm_summaryinformation-class"></a><span data-ttu-id="d323e-103">\_Класс мсвм SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="d323e-103">Msvm\_SummaryInformation class</span></span>

<span data-ttu-id="d323e-104">Используется в методах [**жетсуммаринформатион**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) и [**жетдефинитионфилесуммаринформатион**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) для быстрого получения общих сведений, связанных с виртуальной машиной или моментальным снимком.</span><span class="sxs-lookup"><span data-stu-id="d323e-104">Used in the [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) and [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) methods in the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to quickly retrieve common information related to a virtual machine or snapshot.</span></span>

<span data-ttu-id="d323e-105">Следующий синтаксис представляет собой упрощенный код MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="d323e-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d323e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d323e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformation : Msvm_SummaryInformationBase
{
  string                       InstanceID;
  string                       AllocatedGPU;
  boolean                      Shielded;
  CIM_ConcreteJob              AsynchronousTasks[];
  DateTime                     CreationTime;
  string                       ElementName;
  uint16                       EnabledState;
  string                       OtherEnabledState;
  string                       GuestOperatingSystem;
  uint16                       HealthState;
  uint16                       Heartbeat;
  uint64                       MemoryUsage;
  sint32                       MemoryAvailable;
  sint32                       AvailableMemoryBuffer;
  boolean                      SwapFilesInUse;
  string                       Name;
  string                       Notes;
  string                       Version;
  uint16                       NumberOfProcessors;
  uint16                       OperationalStatus[];
  uint16                       ProcessorLoad;
  uint16                       ProcessorLoadHistory[];
  CIM_VirtualSystemSettingData Snapshots[];
  string                       StatusDescriptions[];
  uint8                        ThumbnailImage[];
  uint16                       ThumbnailImageHeight;
  uint16                       ThumbnailImageWidth;
  uint64                       UpTime;
  uint16                       ReplicationState;
  uint16                       ReplicationStateEx[];
  uint16                       ReplicationHealth;
  uint16                       ReplicationHealthEx[];
  uint16                       ReplicationMode;
  CIM_ComputerSystem       REF TestReplicaSystem;
  uint16                       ApplicationHealth;
  uint16                       IntegrationServicesVersionState;
  boolean                      MemorySpansPhysicalNumaNodes;
  string                       ReplicationProviderId[];
  uint16                       EnhancedSessionModeState;
  string                       VirtualSwitchNames[];
  string                       VirtualSystemSubType;
  string                       HostComputerSystemName;
};
```

## <a name="members"></a><span data-ttu-id="d323e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d323e-107">Members</span></span>

<span data-ttu-id="d323e-108">Класс **мсвм \_ SummaryInformation** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d323e-108">The **Msvm\_SummaryInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="d323e-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="d323e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d323e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d323e-110">Properties</span></span>

<span data-ttu-id="d323e-111">Класс **мсвм \_ SummaryInformation** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d323e-111">The **Msvm\_SummaryInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d323e-112">**аллокатедгпу**</span><span class="sxs-lookup"><span data-stu-id="d323e-112">**AllocatedGPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d323e-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-115">Идентификатор физического графического процессора, выделенного для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-115">The identifier of the physical graphics processing unit (GPU) allocated to this virtual machine.</span></span> <span data-ttu-id="d323e-116">Это свойство применяется только к виртуальным машинам, использующим RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="d323e-116">This property only applies to virtual machines that use RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-117">**аппликатионхеалс**</span><span class="sxs-lookup"><span data-stu-id="d323e-117">**ApplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-118">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d323e-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-120">Текущее состояние работоспособности приложения для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-120">The current application health status for the virtual machine.</span></span> <span data-ttu-id="d323e-121">Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-121">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d323e-122">**ОК** (2)</span><span class="sxs-lookup"><span data-stu-id="d323e-122">**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Critical"></span><span id="application_critical"></span><span id="APPLICATION_CRITICAL"></span>

<span data-ttu-id="d323e-123">**Критическое для приложения** (32782)</span><span class="sxs-lookup"><span data-stu-id="d323e-123">**Application Critical** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d323e-124">**Отключено** (32896)</span><span class="sxs-lookup"><span data-stu-id="d323e-124">**Disabled** (32896)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d323e-125">**асинчронаустаскс**</span><span class="sxs-lookup"><span data-stu-id="d323e-125">**AsynchronousTasks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-126">Тип данных: массив **CIM \_ конкретежоб**</span><span class="sxs-lookup"><span data-stu-id="d323e-126">Data type: **CIM\_ConcreteJob** array</span></span>
</dt> <dt>

<span data-ttu-id="d323e-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d323e-128">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="d323e-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d323e-129">Массив экземпляров [**мсвм \_ конкретежоб**](msvm-concretejob.md) , которые представляют любые асинхронные операции, связанные с виртуальной машиной, выполняемой в данный момент.</span><span class="sxs-lookup"><span data-stu-id="d323e-129">An array of [**Msvm\_ConcreteJob**](msvm-concretejob.md) instances that represent any asynchronous operations related to the virtual machine that are currently executing.</span></span> <span data-ttu-id="d323e-130">Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-130">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-131">**аваилаблемеморибуффер**</span><span class="sxs-lookup"><span data-stu-id="d323e-131">**AvailableMemoryBuffer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="d323e-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-134">Процент доступной памяти буфера для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-134">The percentage of available memory buffer for the virtual machine.</span></span> <span data-ttu-id="d323e-135">Если для виртуальной машины включена динамическая память, это свойство представляет отношение объема доступного буфера памяти к идеальному буферу памяти для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-135">When dynamic memory is enabled for a virtual machine, this property represents the ratio of available memory buffer to the ideal memory buffer for the virtual machine.</span></span> <span data-ttu-id="d323e-136">Идеальный размер буфера памяти настраивается с помощью свойства **таржетмеморибуффер** класса [**\_ меморисеттингдата мсвм**](msvm-memorysettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="d323e-136">The ideal memory buffer size is configured by using the **TargetMemoryBuffer** property of the [**Msvm\_MemorySettingData**](msvm-memorysettingdata.md) class.</span></span>

<span data-ttu-id="d323e-137">Это свойство является недопустимым для экземпляров класса **мсвм \_ SummaryInformation** , представляющих виртуальные машины, для которых не включена динамическая память.</span><span class="sxs-lookup"><span data-stu-id="d323e-137">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent virtual machines for which dynamic memory is not enabled.</span></span>

<span data-ttu-id="d323e-138">Это свойство является недопустимым для экземпляров класса **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-138">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-139">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="d323e-139">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-140">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d323e-140">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-142">Время создания виртуальной машины или моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d323e-142">The time at which the virtual machine or snapshot was created.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d323e-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d323e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-146">Отображаемое имя виртуальной машины или моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d323e-146">The display name for the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-147">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d323e-147">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-148">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d323e-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-150">Текущее состояние виртуальной машины или моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d323e-150">The current state of the virtual machine or snapshot.</span></span> <span data-ttu-id="d323e-151">Возможные значения см. в свойстве **EnabledState** класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="d323e-151">See the **EnabledState** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-152">**енханцедсессионмодестате**</span><span class="sxs-lookup"><span data-stu-id="d323e-152">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-153">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d323e-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-155">Указывает, разрешены ли для узла подключения в расширенном режиме, и если это разрешено, независимо от того, доступны ли они для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-155">Indicates whether enhanced mode connections are allowed by the host, and if allowed, whether they are available to the virtual machine.</span></span>

<span data-ttu-id="d323e-156">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="d323e-156">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="d323e-157">**Разрешено и доступно** (2)</span><span class="sxs-lookup"><span data-stu-id="d323e-157">**Allowed and available** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="d323e-158">**Не разрешено** (3)</span><span class="sxs-lookup"><span data-stu-id="d323e-158">**Not allowed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="d323e-159">**Разрешено, но недоступно** (6)</span><span class="sxs-lookup"><span data-stu-id="d323e-159">**Allowed but not available** (6 )</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d323e-160">**гуестоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="d323e-160">**GuestOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d323e-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-163">Имя гостевой операционной системы (если доступно).</span><span class="sxs-lookup"><span data-stu-id="d323e-163">The name of the guest operating system, if available.</span></span> <span data-ttu-id="d323e-164">Если эта информация недоступна, значение этого свойства равно **null**.</span><span class="sxs-lookup"><span data-stu-id="d323e-164">If this information is not available, the value of this property is **Null**.</span></span> <span data-ttu-id="d323e-165">Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-165">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-166">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d323e-166">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-167">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d323e-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-169">Текущее состояние работоспособности виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-169">The current health state for the virtual machine.</span></span> <span data-ttu-id="d323e-170">Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-170">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-171">**Периодический сигнал**</span><span class="sxs-lookup"><span data-stu-id="d323e-171">**Heartbeat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-172">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d323e-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-174">Текущее состояние пульса для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-174">The current heartbeat status for the virtual machine.</span></span> <span data-ttu-id="d323e-175">Дополнительные сведения см. в документации по свойству [**статусдескриптионс**](msvm-heartbeatcomponent.md) класса **мсвм \_ хеартбеаткомпонент** .</span><span class="sxs-lookup"><span data-stu-id="d323e-175">For more information, see the documentation for the [**StatusDescriptions**](msvm-heartbeatcomponent.md) property of the **Msvm\_HeartbeatComponent** class.</span></span> <span data-ttu-id="d323e-176">Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-176">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

<dl> <dt>

<span data-ttu-id="d323e-177"><span id="OK"></span><span id="ok"></span>**ОК** (2)</span><span class="sxs-lookup"><span data-stu-id="d323e-177"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d323e-178"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (6)</span><span class="sxs-lookup"><span data-stu-id="d323e-178"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d323e-179"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (12)</span><span class="sxs-lookup"><span data-stu-id="d323e-179"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d323e-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (13)</span><span class="sxs-lookup"><span data-stu-id="d323e-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d323e-181">**хосткомпутерсистемнаме**</span><span class="sxs-lookup"><span data-stu-id="d323e-181">**HostComputerSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d323e-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-184">Имя компьютера, на котором размещена эта виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="d323e-184">The name of the computer hosting this virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="d323e-185">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d323e-185">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="d323e-186">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d323e-186">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d323e-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d323e-189">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ манажеделемент. InstanceId"), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d323e-189">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d323e-190">InstanceID — это необязательное свойство, которое можно использовать для непрозрачного и уникального определения экземпляра этого класса в области действия экземпляра пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d323e-190">InstanceID is an optional property that may be used to opaquely and uniquely identify an instance of this class within the scope of the instantiating Namespace.</span></span> <span data-ttu-id="d323e-191">Различные подклассы этого класса могут переопределять это свойство, чтобы сделать его обязательным, или ключ.</span><span class="sxs-lookup"><span data-stu-id="d323e-191">Various subclasses of this class may override this property to make it required, or a key.</span></span> <span data-ttu-id="d323e-192">Такие подклассы также могут изменять предпочтительные алгоритмы, чтобы обеспечить уникальность, определенную ниже.</span><span class="sxs-lookup"><span data-stu-id="d323e-192">Such subclasses may also modify the preferred algorithms for ensuring uniqueness that are defined below.</span></span>

<span data-ttu-id="d323e-193">Чтобы обеспечить уникальность в пространстве имен, значение InstanceID должно быть создано с использованием следующего "предпочтительного" алгоритма:</span><span class="sxs-lookup"><span data-stu-id="d323e-193">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm:</span></span>

<span data-ttu-id="d323e-194"><OrgID>:<LocalID></span><span class="sxs-lookup"><span data-stu-id="d323e-194"><OrgID>:<LocalID></span></span>

<span data-ttu-id="d323e-195">Где <OrgID> и <LocalID> разделяются двоеточием (:), а <OrgID> в месте должно быть указано уникальное имя, которое принадлежит бизнес-сущности, создающему или определяющему InstanceId или зарегистрированный идентификатор, назначенный бизнес-сущностю распознанным глобальным центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="d323e-195">Where <OrgID> and <LocalID> are separated by a colon (:), and where <OrgID> must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="d323e-196">(Это требование аналогично <Schema Name> \_ <Class Name> Структура имен классов схемы.) Кроме того, чтобы обеспечить уникальность, <OrgID> не следует включать двоеточие (:).</span><span class="sxs-lookup"><span data-stu-id="d323e-196">(This requirement is similar to the <Schema Name>\_<Class Name> structure of Schema class names.) In addition, to ensure uniqueness, <OrgID> must not contain a colon (:).</span></span> <span data-ttu-id="d323e-197">При использовании этого алгоритма первым двоеточием, которое должно находиться в InstanceID, должен находиться в диапазоне от <OrgID> до <LocalID> .</span><span class="sxs-lookup"><span data-stu-id="d323e-197">When using this algorithm, the first colon to appear in InstanceID must appear between <OrgID> and <LocalID>.</span></span>

<span data-ttu-id="d323e-198"><LocalID> выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых (реальных) элементов.</span><span class="sxs-lookup"><span data-stu-id="d323e-198"><LocalID> is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="d323e-199">Если не равно NULL и указанный выше алгоритм не используется, определяющая сущность должна гарантировать, что результирующий InstanceID не будет повторно использоваться в любых InstanceId, созданных этим или другими поставщиками для пространства имен данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d323e-199">If not null and the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span>

<span data-ttu-id="d323e-200">Если для экземпляров, определяемых DMTF, не задано значение null, то для набора, для которого задано значение CIM, необходимо использовать "предпочтительный" алгоритм <OrgID> .</span><span class="sxs-lookup"><span data-stu-id="d323e-200">If not set to null for DMTF-defined instances, the "preferred" algorithm must be used with the <OrgID> set to CIM.</span></span>

> [!Note]  
> <span data-ttu-id="d323e-201">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d323e-201">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="d323e-202">**интегратионсервицесверсионстате**</span><span class="sxs-lookup"><span data-stu-id="d323e-202">**IntegrationServicesVersionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-203">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d323e-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-205">Указывает, являются ли установленные на виртуальной машине Службы Integration Services актуальными.</span><span class="sxs-lookup"><span data-stu-id="d323e-205">Indicates whether the integration services installed in the virtual machine are up to date.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d323e-206">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d323e-206">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="UpToDate"></span><span id="uptodate"></span><span id="UPTODATE"></span>

<span data-ttu-id="d323e-207">**Уптодате** (1)</span><span class="sxs-lookup"><span data-stu-id="d323e-207">**UpToDate** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mismatch"></span><span id="mismatch"></span><span id="MISMATCH"></span>

<span data-ttu-id="d323e-208">**Несоответствие** (2)</span><span class="sxs-lookup"><span data-stu-id="d323e-208">**Mismatch** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d323e-209">**меморяваилабле**</span><span class="sxs-lookup"><span data-stu-id="d323e-209">**MemoryAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-210">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="d323e-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-212">Процент от объема текущей памяти, доступной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d323e-212">The percentage of the current memory available to the virtual machine.</span></span> <span data-ttu-id="d323e-213">Если для виртуальной машины включена динамическая память, это свойство представляет отношение объема доступной памяти виртуальной машины к общему объему физической памяти, назначенному виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d323e-213">When dynamic memory is enabled for a virtual machine, this property represents the ratio of available memory of the virtual machine to the total physical memory assigned to the virtual machine.</span></span> <span data-ttu-id="d323e-214">Если виртуальная машина не имеет доступной памяти, это свойство будет отрицательным и будет содержать отношение объема памяти, необходимой для виртуальной машины, к общему объему физической памяти, назначенному виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d323e-214">When a virtual machine has no available memory, this property will be negative, and it will contain the ratio of memory needed for the virtual machine to the total physical memory assigned to the virtual machine.</span></span>

<span data-ttu-id="d323e-215">Это свойство является недопустимым для экземпляров класса **мсвм \_ SummaryInformation** , представляющих виртуальные машины, для которых не включена динамическая память.</span><span class="sxs-lookup"><span data-stu-id="d323e-215">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent virtual machines for which dynamic memory is not enabled.</span></span>

<span data-ttu-id="d323e-216">Это свойство является недопустимым для экземпляров класса **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-216">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-217">**мемориспансфисикалнуманодес**</span><span class="sxs-lookup"><span data-stu-id="d323e-217">**MemorySpansPhysicalNumaNodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-218">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d323e-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-220">Указывает, охватывает ли память один или несколько узлов виртуальной машины (NUMA) виртуальной неоднородным доступом памяти на нескольких физических узлах NUMA системы размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="d323e-220">Indicates whether the memory of the one or more of the virtual nonuniform memory access (NUMA) nodes of the virtual machine spans multiple physical NUMA nodes of the hosting computer system.</span></span> <span data-ttu-id="d323e-221">Содержит **значение true** , если память охватывает несколько физических узлов NUMA, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d323e-221">Contains **True** if the memory spans multiple physical NUMA nodes or **False** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-222">**MemoryUsage**</span><span class="sxs-lookup"><span data-stu-id="d323e-222">**MemoryUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-223">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d323e-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-225">Текущее использование памяти виртуальной машины (в мегабайтах).</span><span class="sxs-lookup"><span data-stu-id="d323e-225">The current memory usage, in megabytes, of the virtual machine.</span></span> <span data-ttu-id="d323e-226">Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-226">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-227">**Name**</span><span class="sxs-lookup"><span data-stu-id="d323e-227">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-228">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d323e-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-230">Уникальное имя виртуальной машины или моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="d323e-230">The unique name for the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-231">**Примечания**</span><span class="sxs-lookup"><span data-stu-id="d323e-231">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-232">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d323e-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-234">Примечания, связанные с виртуальной машиной или моментальным снимком.</span><span class="sxs-lookup"><span data-stu-id="d323e-234">The notes associated with the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-235">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="d323e-235">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-236">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d323e-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-238">Общее число виртуальных процессоров, выделенных виртуальной машине или моментальному снимку.</span><span class="sxs-lookup"><span data-stu-id="d323e-238">The total number of virtual processors allocated to the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-239">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d323e-239">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-240">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d323e-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d323e-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d323e-242">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="d323e-242">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d323e-243">Текущие рабочие состояния виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-243">The current operational statuses of the virtual machine.</span></span> <span data-ttu-id="d323e-244">Возможные значения см. в свойстве **OperationalStatus** класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="d323e-244">See the **OperationalStatus** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-245">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="d323e-245">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-246">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d323e-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-248">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="d323e-248">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1.</span></span> <span data-ttu-id="d323e-249">Это свойство будет иметь значение **null** , если **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="d323e-249">This property will be set to **Null** when **EnabledState** is any value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-250">**процессорлоад**</span><span class="sxs-lookup"><span data-stu-id="d323e-250">**ProcessorLoad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-251">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d323e-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-253">Текущее использование процессора виртуальной машины в процентах.</span><span class="sxs-lookup"><span data-stu-id="d323e-253">The current processor usage of the virtual machine, in percentage.</span></span> <span data-ttu-id="d323e-254">Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-254">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-255">**процессорлоадхистори**</span><span class="sxs-lookup"><span data-stu-id="d323e-255">**ProcessorLoadHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-256">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d323e-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d323e-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d323e-258">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="d323e-258">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d323e-259">Массив из предыдущих 100 примеров использования процессора (в процентах) для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-259">An array of the previous 100 samples of the processor usage, in percentage, for the virtual machine.</span></span> <span data-ttu-id="d323e-260">Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-260">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-261">**репликатионхеалс**</span><span class="sxs-lookup"><span data-stu-id="d323e-261">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-262">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d323e-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d323e-264">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**мсвм \_ SummaryInformation**.**Репликатионхеалсекс**")</span><span class="sxs-lookup"><span data-stu-id="d323e-264">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm\_SummaryInformation**.**ReplicationHealthEx**")</span></span>
</dt> </dl>

<span data-ttu-id="d323e-265">Работоспособность репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-265">The replication health for the virtual machine.</span></span> <span data-ttu-id="d323e-266">Возможные значения см. в свойстве **репликатионхеалс** класса [**\_ ComputerSystem объекта мсвм**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="d323e-266">See the **ReplicationHealth** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

> [!Note]  
> <span data-ttu-id="d323e-267">Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте **репликатионхеалсекс**.</span><span class="sxs-lookup"><span data-stu-id="d323e-267">This property is deprecated starting with Windows 8.1; instead, use the **ReplicationHealthEx**.</span></span>

 

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d323e-268">**Неприменимо** (0)</span><span class="sxs-lookup"><span data-stu-id="d323e-268">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="d323e-269">**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="d323e-269">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d323e-270">**Предупреждение** (2)</span><span class="sxs-lookup"><span data-stu-id="d323e-270">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="d323e-271">**Критическая** (3)</span><span class="sxs-lookup"><span data-stu-id="d323e-271">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d323e-272">**репликатионхеалсекс**</span><span class="sxs-lookup"><span data-stu-id="d323e-272">**ReplicationHealthEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-273">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d323e-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d323e-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d323e-275">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="d323e-275">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d323e-276">Массив значений работоспособности репликации для различных отношений репликации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-276">The array of replication health values for the various replication relationships of the virtual machine.</span></span> <span data-ttu-id="d323e-277">Возможные значения см. в свойстве **репликатионхеалс** класса [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="d323e-277">See the **ReplicationHealth** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class for possible values.</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d323e-278">**Неприменимо** (0)</span><span class="sxs-lookup"><span data-stu-id="d323e-278">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="d323e-279">**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="d323e-279">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d323e-280">**Предупреждение** (2)</span><span class="sxs-lookup"><span data-stu-id="d323e-280">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="d323e-281">**Критическая** (3)</span><span class="sxs-lookup"><span data-stu-id="d323e-281">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d323e-282">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="d323e-282">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-283">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d323e-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-285">Тип репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-285">The replication type for the virtual machine.</span></span> <span data-ttu-id="d323e-286">Возможные значения см. в свойстве **ReplicationMode** класса [**\_ ComputerSystem объекта мсвм**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="d323e-286">See the **ReplicationMode** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="d323e-287">**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="d323e-287">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="d323e-288">**Основной** (1)</span><span class="sxs-lookup"><span data-stu-id="d323e-288">**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="d323e-289">**Реплика** (2)</span><span class="sxs-lookup"><span data-stu-id="d323e-289">**Replica** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="d323e-290">**Тестовая реплика** (3)</span><span class="sxs-lookup"><span data-stu-id="d323e-290">**Test Replica** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span data-ttu-id="d323e-291">**Расширенная реплика** (4)</span><span class="sxs-lookup"><span data-stu-id="d323e-291">**Extended Replica** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d323e-292">**ReplicationProviderId**</span><span class="sxs-lookup"><span data-stu-id="d323e-292">**ReplicationProviderId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-293">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d323e-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d323e-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d323e-295">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="d323e-295">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d323e-296">Для виртуальной машины основной или расширенной реплики это идентификатор первичного поставщика репликации.</span><span class="sxs-lookup"><span data-stu-id="d323e-296">For the primary or extended replica virtual machine, this is the primary replication provider ID.</span></span> <span data-ttu-id="d323e-297">Для реплики виртуальной машины, если включена расширенная репликация, это идентификатор поставщика для расширенной связи.</span><span class="sxs-lookup"><span data-stu-id="d323e-297">For a replica virtual machine and if extended replication is enabled, this is the provider ID for extended relationship.</span></span>

<span data-ttu-id="d323e-298">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="d323e-298">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-299">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="d323e-299">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-300">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d323e-300">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d323e-302">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**мсвм \_ SummaryInformation**.**Репликатионстатикс**")</span><span class="sxs-lookup"><span data-stu-id="d323e-302">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm\_SummaryInformation**.**ReplicationStateEx**")</span></span>
</dt> </dl>

<span data-ttu-id="d323e-303">Состояние репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-303">The replication state for the virtual machine.</span></span> <span data-ttu-id="d323e-304">Возможные значения см. в свойстве **ReplicationState** класса [**\_ ComputerSystem объекта мсвм**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="d323e-304">See the **ReplicationState** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

> [!Note]  
> <span data-ttu-id="d323e-305">Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте **репликатионстатикс**.</span><span class="sxs-lookup"><span data-stu-id="d323e-305">This property is deprecated starting with Windows 8.1; instead, use the **ReplicationStateEx**.</span></span>

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d323e-306">**Отключено** (0)</span><span class="sxs-lookup"><span data-stu-id="d323e-306">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="d323e-307">**Готово к репликации** (1)</span><span class="sxs-lookup"><span data-stu-id="d323e-307">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="d323e-308">**Ожидание завершения начальной репликации** (2)</span><span class="sxs-lookup"><span data-stu-id="d323e-308">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="d323e-309">**Репликация** (3)</span><span class="sxs-lookup"><span data-stu-id="d323e-309">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="d323e-310">**Синхронизированная репликация завершена** (4)</span><span class="sxs-lookup"><span data-stu-id="d323e-310">**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="d323e-311">**Восстановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="d323e-311">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="d323e-312">**Зафиксировано** (6)</span><span class="sxs-lookup"><span data-stu-id="d323e-312">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="d323e-313">**Приостановлено** (7)</span><span class="sxs-lookup"><span data-stu-id="d323e-313">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="d323e-314">**Критическая** (8)</span><span class="sxs-lookup"><span data-stu-id="d323e-314">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="d323e-315">**Ожидание запуска повторной синхронизации** (9)</span><span class="sxs-lookup"><span data-stu-id="d323e-315">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="d323e-316">Повторная **Синхронизация** (10)</span><span class="sxs-lookup"><span data-stu-id="d323e-316">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="d323e-317">**Повторная синхронизация приостановлена** (11)</span><span class="sxs-lookup"><span data-stu-id="d323e-317">**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="d323e-318">**Выполняется отработка отказа** (12)</span><span class="sxs-lookup"><span data-stu-id="d323e-318">**Failover in progress** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d323e-319">**репликатионстатикс**</span><span class="sxs-lookup"><span data-stu-id="d323e-319">**ReplicationStateEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-320">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d323e-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d323e-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d323e-322">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="d323e-322">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d323e-323">Массив значений состояния репликации для различных отношений репликации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-323">The array of replication state values for the various replication relationships of the virtual machine.</span></span> <span data-ttu-id="d323e-324">Возможные значения см. в свойстве **ReplicationState** класса [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="d323e-324">See the **ReplicationState** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class for possible values.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d323e-325"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (0)</span><span class="sxs-lookup"><span data-stu-id="d323e-325"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="d323e-326"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Готово к репликации** (1)</span><span class="sxs-lookup"><span data-stu-id="d323e-326"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="d323e-327"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Ожидание завершения начальной репликации** (2)</span><span class="sxs-lookup"><span data-stu-id="d323e-327"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="d323e-328"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Репликация** (3)</span><span class="sxs-lookup"><span data-stu-id="d323e-328"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="d323e-329"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Синхронизированная репликация завершена** (4)</span><span class="sxs-lookup"><span data-stu-id="d323e-329"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="d323e-330"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Восстановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="d323e-330"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="d323e-331"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Зафиксировано** (6)</span><span class="sxs-lookup"><span data-stu-id="d323e-331"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="d323e-332"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Приостановлено** (7)</span><span class="sxs-lookup"><span data-stu-id="d323e-332"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="d323e-333"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** (8)</span><span class="sxs-lookup"><span data-stu-id="d323e-333"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="d323e-334"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Ожидание запуска повторной синхронизации** (9)</span><span class="sxs-lookup"><span data-stu-id="d323e-334"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="d323e-335"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>Повторная **Синхронизация** (10)</span><span class="sxs-lookup"><span data-stu-id="d323e-335"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="d323e-336"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Повторная синхронизация приостановлена** (11)</span><span class="sxs-lookup"><span data-stu-id="d323e-336"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="d323e-337"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Выполняется отработка отказа** (12)</span><span class="sxs-lookup"><span data-stu-id="d323e-337"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="d323e-338"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Выполняется восстановление размещения** (13)</span><span class="sxs-lookup"><span data-stu-id="d323e-338"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="d323e-339"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Восстановление размещения завершено** (14)</span><span class="sxs-lookup"><span data-stu-id="d323e-339"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback complete** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span data-ttu-id="d323e-340"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Выполняется обновление диска** (15)</span><span class="sxs-lookup"><span data-stu-id="d323e-340"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Disk update in progress** (15)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="d323e-341">Добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d323e-341">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span data-ttu-id="d323e-342"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Критическое обновление диска** (16)</span><span class="sxs-lookup"><span data-stu-id="d323e-342"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Disk update critical** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="d323e-343">Добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d323e-343">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d323e-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (17)</span><span class="sxs-lookup"><span data-stu-id="d323e-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (17)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="d323e-345">Добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d323e-345">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="d323e-346"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Выполняется перецель репликации** (18)</span><span class="sxs-lookup"><span data-stu-id="d323e-346"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose replication in progress** (18)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="d323e-347">Добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d323e-347">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span data-ttu-id="d323e-348"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Подготовлено к репликации синхронизации** (19)</span><span class="sxs-lookup"><span data-stu-id="d323e-348"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Prepared for sync replication** (19)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="d323e-349">Добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d323e-349">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span data-ttu-id="d323e-350"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Подготовлено к групповой отмене репликации** (20)</span><span class="sxs-lookup"><span data-stu-id="d323e-350"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Prepared for group reverse replication** (20)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="d323e-351">Добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d323e-351">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span data-ttu-id="d323e-352"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Фиредрилл выполняется** (21)</span><span class="sxs-lookup"><span data-stu-id="d323e-352"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in progress** (21)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="d323e-353">Добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d323e-353">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d323e-354">**Экранирование**</span><span class="sxs-lookup"><span data-stu-id="d323e-354">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-355">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d323e-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-357">Указывает, настроено ли экранирование для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-357">Indicates whether or not shielding is configured for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="d323e-358">Добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d323e-358">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="d323e-359">**Моментальные снимки**</span><span class="sxs-lookup"><span data-stu-id="d323e-359">**Snapshots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-360">Тип данных: массив **CIM \_ виртуалсистемсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="d323e-360">Data type: **CIM\_VirtualSystemSettingData** array</span></span>
</dt> <dt>

<span data-ttu-id="d323e-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d323e-362">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="d323e-362">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d323e-363">Массив экземпляров [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , представляющих моментальные снимки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-363">An array of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instances that represent the snapshots for the virtual machine.</span></span> <span data-ttu-id="d323e-364">Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-364">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-365">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="d323e-365">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-366">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d323e-366">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d323e-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d323e-368">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="d323e-368">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d323e-369">Строки, описывающие соответствующие значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d323e-369">Strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="d323e-370">Это соответствует свойству **статусдескриптионс** класса [**\_ ComputerSystem мсвм**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="d323e-370">This corresponds to the **StatusDescriptions** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-371">**свапфилесинусе**</span><span class="sxs-lookup"><span data-stu-id="d323e-371">**SwapFilesInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-372">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d323e-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-374">Указывает, активна ли подкачка второго уровня.</span><span class="sxs-lookup"><span data-stu-id="d323e-374">Indicates whether second level paging is active.</span></span> <span data-ttu-id="d323e-375">Содержит **значение true** , если подкачка на второй уровень является активной, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d323e-375">Contains **True** if second level paging is active or **False** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-376">**тестрепликасистем**</span><span class="sxs-lookup"><span data-stu-id="d323e-376">**TestReplicaSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-377">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="d323e-377">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-378">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-379">Ссылка на экземпляр [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину тестовой реплики для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-379">Reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the test replica virtual machine for the virtual machine.</span></span> <span data-ttu-id="d323e-380">Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-380">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-381">**сумбнаилимаже**</span><span class="sxs-lookup"><span data-stu-id="d323e-381">**ThumbnailImage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-382">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d323e-382">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d323e-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d323e-384">Квалификаторы: **октетстринг**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексируется"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**мсвм \_ SummaryInformation**.**Сумбнаилимажевидс**","**мсвм \_ SummaryInformation**.**Сумбнаилимажехеигхт**")</span><span class="sxs-lookup"><span data-stu-id="d323e-384">Qualifiers: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImageWidth**", "**Msvm\_SummaryInformation**.**ThumbnailImageHeight**")</span></span>
</dt> </dl>

<span data-ttu-id="d323e-385">Массив, содержащий небольшой эскиз рабочего стола для виртуальной машины или моментального снимка в формате RGB565.</span><span class="sxs-lookup"><span data-stu-id="d323e-385">An array that contains a small, thumbnail-sized image of the desktop for the virtual machine or snapshot in RGB565 format.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-386">**сумбнаилимажехеигхт**</span><span class="sxs-lookup"><span data-stu-id="d323e-386">**ThumbnailImageHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-387">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d323e-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d323e-389">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**мсвм \_ SummaryInformation**.**Сумбнаилимаже**")</span><span class="sxs-lookup"><span data-stu-id="d323e-389">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImage**")</span></span>
</dt> </dl>

<span data-ttu-id="d323e-390">Высота изображения в пикселях свойства Сумбнаилимаже.</span><span class="sxs-lookup"><span data-stu-id="d323e-390">The height in pixels of the image in the ThumbnailImage property.</span></span>

> [!Note]  
> <span data-ttu-id="d323e-391">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d323e-391">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="d323e-392">**сумбнаилимажевидс**</span><span class="sxs-lookup"><span data-stu-id="d323e-392">**ThumbnailImageWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-393">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d323e-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d323e-395">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**мсвм \_ SummaryInformation**.**Сумбнаилимаже**")</span><span class="sxs-lookup"><span data-stu-id="d323e-395">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImage**")</span></span>
</dt> </dl>

<span data-ttu-id="d323e-396">Ширина изображения в пикселях свойства Сумбнаилимаже.</span><span class="sxs-lookup"><span data-stu-id="d323e-396">The width in pixels of the image in the ThumbnailImage property.</span></span>

> [!Note]  
> <span data-ttu-id="d323e-397">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d323e-397">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="d323e-398">**Просто**</span><span class="sxs-lookup"><span data-stu-id="d323e-398">**UpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-399">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d323e-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-401">Количество времени, прошедшее с момента последней загрузки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-401">The amount of time since the virtual machine was last booted.</span></span> <span data-ttu-id="d323e-402">Это свойство недопустимо для экземпляров **мсвм \_ SummaryInformation** , представляющих моментальный снимок виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d323e-402">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-403">**Version**</span><span class="sxs-lookup"><span data-stu-id="d323e-403">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-404">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d323e-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-405">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-406">Версия виртуальной системы в формате "основная. Дополнительная", например "2,0".</span><span class="sxs-lookup"><span data-stu-id="d323e-406">The version of the virtual system in a format of "major.minor", for example "2.0".</span></span>

> [!Note]  
> <span data-ttu-id="d323e-407">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d323e-407">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="d323e-408">**виртуалсвитчнамес**</span><span class="sxs-lookup"><span data-stu-id="d323e-408">**VirtualSwitchNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-409">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d323e-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d323e-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d323e-411">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="d323e-411">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d323e-412">Строки, указывающие понятные имена виртуальных коммутаторов, к которым подключена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="d323e-412">Strings that specify the friendly names of the virtual switches the virtual machine is connected to.</span></span>

<span data-ttu-id="d323e-413">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="d323e-413">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="d323e-414">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="d323e-414">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d323e-415">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d323e-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d323e-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d323e-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d323e-417">Подтип виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="d323e-417">The subtype of the virtual system.</span></span>

<span data-ttu-id="d323e-418">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="d323e-418">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="d323e-419">**Microsoft: Hyper-V: подтип: 1** ()</span><span class="sxs-lookup"><span data-stu-id="d323e-419">**Microsoft:Hyper-V:SubType:1** ()</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="d323e-420">**Microsoft: Hyper-V: подтип: 2** ()</span><span class="sxs-lookup"><span data-stu-id="d323e-420">**Microsoft:Hyper-V:SubType:2** ()</span></span>


<span data-ttu-id="d323e-421"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d323e-421"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="d323e-422">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d323e-422">Remarks</span></span>

<span data-ttu-id="d323e-423">Доступ к классу **\_ SummaryInformation мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="d323e-423">Access to the **Msvm\_SummaryInformation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d323e-424">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d323e-424">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d323e-425">Требования</span><span class="sxs-lookup"><span data-stu-id="d323e-425">Requirements</span></span>



| <span data-ttu-id="d323e-426">Требование</span><span class="sxs-lookup"><span data-stu-id="d323e-426">Requirement</span></span> | <span data-ttu-id="d323e-427">Значение</span><span class="sxs-lookup"><span data-stu-id="d323e-427">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d323e-428">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d323e-428">Minimum supported client</span></span><br/> | <span data-ttu-id="d323e-429">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d323e-429">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d323e-430">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d323e-430">Minimum supported server</span></span><br/> | <span data-ttu-id="d323e-431">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d323e-431">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d323e-432">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d323e-432">Namespace</span></span><br/>                | <span data-ttu-id="d323e-433">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d323e-433">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d323e-434">MOF</span><span class="sxs-lookup"><span data-stu-id="d323e-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d323e-435"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d323e-435"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d323e-436">DLL</span><span class="sxs-lookup"><span data-stu-id="d323e-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d323e-437"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d323e-437"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d323e-438">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d323e-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d323e-439">**Мсвм \_ суммаринформатионбасе**</span><span class="sxs-lookup"><span data-stu-id="d323e-439">**Msvm\_SummaryInformationBase**</span></span>](msvm-summaryinformationbase.md)
</dt> <dt>

[<span data-ttu-id="d323e-440">Классы виртуальных систем</span><span class="sxs-lookup"><span data-stu-id="d323e-440">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 


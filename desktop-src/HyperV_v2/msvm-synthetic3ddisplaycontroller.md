---
description: Представляет синтетический трехмерный контроллер дисплея, назначенный виртуальной машине.
ms.assetid: 5679668B-7D0B-421C-92B6-8A320090DFF7
title: Класс Msvm_Synthetic3DDisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayController
- Msvm_Synthetic3DDisplayController.RequestStateChange
- Msvm_Synthetic3DDisplayController.SetPowerState
- Msvm_Synthetic3DDisplayController.Reset
- Msvm_Synthetic3DDisplayController.EnableDevice
- Msvm_Synthetic3DDisplayController.OnlineDevice
- Msvm_Synthetic3DDisplayController.QuiesceDevice
- Msvm_Synthetic3DDisplayController.SaveProperties
- Msvm_Synthetic3DDisplayController.RestoreProperties
- Msvm_Synthetic3DDisplayController.InstanceID
- Msvm_Synthetic3DDisplayController.Caption
- Msvm_Synthetic3DDisplayController.Description
- Msvm_Synthetic3DDisplayController.ElementName
- Msvm_Synthetic3DDisplayController.InstallDate
- Msvm_Synthetic3DDisplayController.Name
- Msvm_Synthetic3DDisplayController.OperationalStatus
- Msvm_Synthetic3DDisplayController.StatusDescriptions
- Msvm_Synthetic3DDisplayController.Status
- Msvm_Synthetic3DDisplayController.HealthState
- Msvm_Synthetic3DDisplayController.CommunicationStatus
- Msvm_Synthetic3DDisplayController.DetailedStatus
- Msvm_Synthetic3DDisplayController.OperatingStatus
- Msvm_Synthetic3DDisplayController.PrimaryStatus
- Msvm_Synthetic3DDisplayController.EnabledState
- Msvm_Synthetic3DDisplayController.OtherEnabledState
- Msvm_Synthetic3DDisplayController.RequestedState
- Msvm_Synthetic3DDisplayController.EnabledDefault
- Msvm_Synthetic3DDisplayController.TimeOfLastStateChange
- Msvm_Synthetic3DDisplayController.AvailableRequestedStates
- Msvm_Synthetic3DDisplayController.TransitioningToState
- Msvm_Synthetic3DDisplayController.SystemCreationClassName
- Msvm_Synthetic3DDisplayController.SystemName
- Msvm_Synthetic3DDisplayController.CreationClassName
- Msvm_Synthetic3DDisplayController.DeviceID
- Msvm_Synthetic3DDisplayController.PowerManagementSupported
- Msvm_Synthetic3DDisplayController.PowerManagementCapabilities
- Msvm_Synthetic3DDisplayController.Availability
- Msvm_Synthetic3DDisplayController.StatusInfo
- Msvm_Synthetic3DDisplayController.LastErrorCode
- Msvm_Synthetic3DDisplayController.ErrorDescription
- Msvm_Synthetic3DDisplayController.ErrorCleared
- Msvm_Synthetic3DDisplayController.PowerOnHours
- Msvm_Synthetic3DDisplayController.TotalPowerOnHours
- Msvm_Synthetic3DDisplayController.OtherIdentifyingInfo
- Msvm_Synthetic3DDisplayController.IdentifyingDescriptions
- Msvm_Synthetic3DDisplayController.AdditionalAvailability
- Msvm_Synthetic3DDisplayController.MaxQuiesceTime
- Msvm_Synthetic3DDisplayController.TimeOfLastReset
- Msvm_Synthetic3DDisplayController.ProtocolSupported
- Msvm_Synthetic3DDisplayController.MaxNumberControlled
- Msvm_Synthetic3DDisplayController.ProtocolDescription
- Msvm_Synthetic3DDisplayController.VideoProcessor
- Msvm_Synthetic3DDisplayController.VideoMemoryType
- Msvm_Synthetic3DDisplayController.OtherVideoMemoryType
- Msvm_Synthetic3DDisplayController.NumberOfVideoPages
- Msvm_Synthetic3DDisplayController.MaxMemorySupported
- Msvm_Synthetic3DDisplayController.AcceleratorCapabilities
- Msvm_Synthetic3DDisplayController.CapabilityDescriptions
- Msvm_Synthetic3DDisplayController.OtherVideoArchitecture
- Msvm_Synthetic3DDisplayController.VideoArchitecture
- Msvm_Synthetic3DDisplayController.AllocatedGPU
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0cd102fe29cf34aa0930ca264c8820868da7daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683171"
---
# <a name="msvm_synthetic3ddisplaycontroller-class"></a><span data-ttu-id="1d9cd-103">\_Класс мсвм Synthetic3DDisplayController</span><span class="sxs-lookup"><span data-stu-id="1d9cd-103">Msvm\_Synthetic3DDisplayController class</span></span>

<span data-ttu-id="1d9cd-104">Представляет синтетический трехмерный контроллер дисплея, назначенный виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-104">Represents the synthetic 3-D display controller that is assigned to a virtual machine.</span></span> <span data-ttu-id="1d9cd-105">Этот класс используется только с виртуальными машинами, использующими RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-105">This class is only used with virtual machines that use RemoteFX.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d9cd-106">При добавлении искусственного контроллера дисплея в виртуальную машину необходимо отключить все синтетические контроллеры экрана ([**мсвм \_ синсетикдисплайконтроллер**](msvm-syntheticdisplaycontroller.md)), подключенные к этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-106">When you add a synthetic 3-D display controller to a virtual machine, you must disable any synthetic display controller ([**Msvm\_SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)) that is attached to that virtual machine.</span></span>

 

<span data-ttu-id="1d9cd-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d9cd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d9cd-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_Synthetic3DDisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 2048;
  uint32   MaxMemorySupported = 8388608;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
  string   AllocatedGPU;
};
```

## <a name="members"></a><span data-ttu-id="1d9cd-109">Члены</span><span class="sxs-lookup"><span data-stu-id="1d9cd-109">Members</span></span>

<span data-ttu-id="1d9cd-110">Класс **мсвм \_ Synthetic3DDisplayController** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1d9cd-110">The **Msvm\_Synthetic3DDisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="1d9cd-111">Методы</span><span class="sxs-lookup"><span data-stu-id="1d9cd-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="1d9cd-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="1d9cd-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1d9cd-113">Методы</span><span class="sxs-lookup"><span data-stu-id="1d9cd-113">Methods</span></span>

<span data-ttu-id="1d9cd-114">Класс **мсвм \_ Synthetic3DDisplayController** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-114">The **Msvm\_Synthetic3DDisplayController** class has these methods.</span></span>



| <span data-ttu-id="1d9cd-115">Метод</span><span class="sxs-lookup"><span data-stu-id="1d9cd-115">Method</span></span>                 | <span data-ttu-id="1d9cd-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1d9cd-116">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="1d9cd-117">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-117">**EnableDevice**</span></span>       | <span data-ttu-id="1d9cd-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1d9cd-119">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-119">**OnlineDevice**</span></span>       | <span data-ttu-id="1d9cd-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1d9cd-121">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-121">**QuiesceDevice**</span></span>      | <span data-ttu-id="1d9cd-122">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1d9cd-123">**Равен**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-123">**RequestStateChange**</span></span> | <span data-ttu-id="1d9cd-124">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1d9cd-125">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-125">**Reset**</span></span>              | <span data-ttu-id="1d9cd-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1d9cd-127">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-127">**RestoreProperties**</span></span>  | <span data-ttu-id="1d9cd-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1d9cd-129">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-129">**SaveProperties**</span></span>     | <span data-ttu-id="1d9cd-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1d9cd-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-131">**SetPowerState**</span></span>      | <span data-ttu-id="1d9cd-132">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1d9cd-133">Свойства</span><span class="sxs-lookup"><span data-stu-id="1d9cd-133">Properties</span></span>

<span data-ttu-id="1d9cd-134">Класс **мсвм \_ Synthetic3DDisplayController** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-134">The **Msvm\_Synthetic3DDisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d9cd-135">**акцелераторкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-135">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-136">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="1d9cd-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-138">Графические и трехмерные возможности контроллера экрана.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-138">The graphics and 3-D capabilities of the display controller.</span></span> <span data-ttu-id="1d9cd-139">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-139">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-140">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-141">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="1d9cd-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-143">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение 6 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-144">**аллокатедгпу**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-144">**AllocatedGPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-147">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-147">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-148">Идентификатор физического графического процессора, выделенного для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-148">The identifier of the physical graphics processing unit (GPU) allocated to this virtual machine.</span></span> <span data-ttu-id="1d9cd-149">Это свойство применяется только к виртуальным машинам, использующим RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-149">This property only applies to virtual machines that use RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-150">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-151">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-153">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение 6 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-154">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-155">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="1d9cd-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-157">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="1d9cd-157">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="1d9cd-158">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-158">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-159">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-159">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-160">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-160">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-162">Массив строк произвольной формы, которые предоставляют более подробные объяснения для любого из функций ускорителя видео, указанных в массиве свойств **акцелераторкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="1d9cd-162">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** property array.</span></span> <span data-ttu-id="1d9cd-163">Каждая запись этого массива связана с записью в массиве свойств **акцелераторкапабилитиес** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-163">Each entry of this array is related to the entry in the **AcceleratorCapabilities** property array that is located at the same index.</span></span> <span data-ttu-id="1d9cd-164">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-164">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-165">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-168">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-168">A short description of the object.</span></span> <span data-ttu-id="1d9cd-169">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-170">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-170">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-171">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-173">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-173">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1d9cd-174">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-174">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1d9cd-175">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-175">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1d9cd-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1d9cd-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1d9cd-183">)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-183">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d9cd-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-185">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-187">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-187">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1d9cd-188">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-189">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-192">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-192">A description of the object.</span></span> <span data-ttu-id="1d9cd-193">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-195">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-197">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-197">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1d9cd-198">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1d9cd-199">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1d9cd-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1d9cd-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1d9cd-208">)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-208">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d9cd-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-212">Идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-212">The device identifier.</span></span> <span data-ttu-id="1d9cd-213">Это свойство наследуется от [**CIM \_ ",**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)" и всегда имеет значение "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="1d9cd-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-215">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-217">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-217">A display name for the object.</span></span> <span data-ttu-id="1d9cd-218">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-219">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-219">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-220">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-222">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-222">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="1d9cd-223">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-224">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-224">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-227">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-227">The enabled and disabled states of an element.</span></span> <span data-ttu-id="1d9cd-228">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-228">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="1d9cd-229">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено) или 3 (отключено).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-229">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to either 2 (Enabled) or 3 (Disabled).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-230">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-230">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-231">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-233">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-235">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-237">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-237">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-238">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-238">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-239">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-241">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-241">The current health of the element.</span></span> <span data-ttu-id="1d9cd-242">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-242">This attribute expresses the health of this element but not necessarily that of its subelements.</span></span> <span data-ttu-id="1d9cd-243">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-243">The possible values are from 0 through 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="1d9cd-244">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-244">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-245">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-245">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-246">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-246">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-248">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-248">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-250">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-252">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-252">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="1d9cd-253">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-253">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-254">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-254">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-255">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-257">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-257">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-258">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-258">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1d9cd-259">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-259">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-260">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-260">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-261">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-263">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-264">**максмеморисуппортед**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-264">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-265">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-266">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-267">Максимальный поддерживаемый объем памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-267">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="1d9cd-268">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-268">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-269">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-269">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-270">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-271">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-272">Максимальное количество напрямую доступных для адресации сущностей, поддерживаемых этим контроллером.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-272">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="1d9cd-273">Если число неизвестно или неограниченно, следует использовать значение 0.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-273">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="1d9cd-274">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-274">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="1d9cd-275">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-275">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-276">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-276">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-277">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-277">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-279">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-279">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-280">**Name**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-280">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-281">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-283">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-283">The label by which the object is known.</span></span> <span data-ttu-id="1d9cd-284">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-285">**нумберофвидеопажес**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-285">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-286">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-286">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-288">Число поддерживаемых страниц видео с учетом текущих разрешений и доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-288">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="1d9cd-289">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-289">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-290">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-290">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-291">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-293">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="1d9cd-293">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1d9cd-294">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-294">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1d9cd-295">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1d9cd-296"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-296"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-297"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-297"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-298"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-298"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-299"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-299"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-300"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-300"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-301"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-301"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-302"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-302"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-303"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-303"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-304"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-304"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-305"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-305"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-306"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-306"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-307"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-307"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-308"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-308"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-309"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-309"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-310"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-310"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-311"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-311"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-312"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-312"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-313"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-313"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-314"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1d9cd-314"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1d9cd-315">)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-315">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d9cd-316">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-316">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-317">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="1d9cd-317">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-319">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-319">The current statuses of the object.</span></span> <span data-ttu-id="1d9cd-320">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-320">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-321">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-321">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-322">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-324">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-324">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="1d9cd-325">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-325">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="1d9cd-326">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-326">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-327">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-327">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-328">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-328">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-330">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-330">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-331">**осервидеоарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-331">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-332">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-334">Строка, описывающая тип архитектуры видео, если свойство **видеоарчитектуре** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="1d9cd-334">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="1d9cd-335">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-335">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-336">**осервидеомеморитипе**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-336">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-337">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-339">Тип видеопамяти, если свойство **видеомеморитипе** экземпляра имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-339">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="1d9cd-340">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-340">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-341">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-341">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-342">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="1d9cd-342">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-344">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-345">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-345">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-346">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-346">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-348">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-349">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-349">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-350">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-352">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-353">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-353">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-354">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-354">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-356">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-356">Provides high level status information.</span></span> <span data-ttu-id="1d9cd-357">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-357">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="1d9cd-358">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-358">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1d9cd-359">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-359">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1d9cd-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-361"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1d9cd-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1d9cd-366">)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-366">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d9cd-367">**протоколдескриптион**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-367">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-368">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-370">Строка, которая предоставляет дополнительные сведения, связанные с протоколом, поддерживаемым контроллером.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-370">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="1d9cd-371">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-371">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-372">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-372">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-373">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-375">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-375">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="1d9cd-376">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-376">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-377">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-377">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-378">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-378">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-379">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-380">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-380">The last requested or desired state for the element.</span></span> <span data-ttu-id="1d9cd-381">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-381">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="1d9cd-382">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-382">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="1d9cd-383">Конкретный экземпляр [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-383">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="1d9cd-384">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-384">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="1d9cd-385">Это свойство наследуется от **CIM \_ енабледлогикалелемент** и всегда имеет значение 2 (включено), 3 (отключено) или 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-385">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 2 (Enabled), 3 (Disabled), or 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-386">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-386">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-387">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-389">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-390">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-390">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-391">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-391">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-393">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="1d9cd-393">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="1d9cd-394">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-394">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-395">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-395">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-396">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-398">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-398">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-399">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-399">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-400">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-401">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-402">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-402">The scoping system's creation class name.</span></span> <span data-ttu-id="1d9cd-403">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-403">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-404">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-405">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-406">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-407">Уникальный идентификатор для области виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-407">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="1d9cd-408">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-408">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-409">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-409">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-410">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-411">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-412">Время последнего включения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-412">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="1d9cd-413">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-413">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-414">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-414">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-415">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-417">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-417">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="1d9cd-418">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-418">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-419">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-419">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-420">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-420">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-422">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-422">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-423">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-423">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-424">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-426">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-426">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="1d9cd-427">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-427">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-428">**видеоарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-428">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-429">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-430">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-431">Указывает архитектуру видеоролика контроллера экрана, используемую для создания видеосигнала.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-431">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="1d9cd-432">Обычно выделенный видеопроцессор создает видеосигнал в соответствии с указанной архитектурой.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-432">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="1d9cd-433">Это индикатор максимальной возможности разрешения контроллеров экрана.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-433">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="1d9cd-434">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-434">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="1d9cd-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-436"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-436"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-437"><span id="CGA"></span><span id="cga"></span>**КГА** (2)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-437"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-438"><span id="EGA"></span><span id="ega"></span>**Ега** (3)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-438"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-439"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-439"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-440"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-440"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-441"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-441"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-442"><span id="HGC"></span><span id="hgc"></span>**ХГК** (7)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-442"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-443"><span id="MCGA"></span><span id="mcga"></span>**Мкга** (8)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-443"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-444"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-444"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-445"><span id="XGA"></span><span id="xga"></span>**Разрешение XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-445"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-446"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Буфер линейного фрейма** (11)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-446"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-447"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-447"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-448"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-448"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-449"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1d9cd-449"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1d9cd-450">)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-450">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d9cd-451">**видеомеморитипе**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-451">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-452">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-452">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-453">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-454">Тип видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-454">The type of video memory.</span></span> <span data-ttu-id="1d9cd-455">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-455">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1d9cd-456">**видеопроцессор**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-456">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9cd-457">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9cd-458">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d9cd-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d9cd-459">Строка, описывающая процессор или контроллер видео.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-459">A string that describes the video processor/controller.</span></span> <span data-ttu-id="1d9cd-460">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d9cd-460">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d9cd-461">Требования</span><span class="sxs-lookup"><span data-stu-id="1d9cd-461">Requirements</span></span>



| <span data-ttu-id="1d9cd-462">Требование</span><span class="sxs-lookup"><span data-stu-id="1d9cd-462">Requirement</span></span> | <span data-ttu-id="1d9cd-463">Значение</span><span class="sxs-lookup"><span data-stu-id="1d9cd-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d9cd-464">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d9cd-464">Minimum supported client</span></span><br/> | <span data-ttu-id="1d9cd-465">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1d9cd-465">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1d9cd-466">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d9cd-466">Minimum supported server</span></span><br/> | <span data-ttu-id="1d9cd-467">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d9cd-467">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1d9cd-468">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1d9cd-468">Namespace</span></span><br/>                | <span data-ttu-id="1d9cd-469">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="1d9cd-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1d9cd-470">MOF</span><span class="sxs-lookup"><span data-stu-id="1d9cd-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d9cd-471"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d9cd-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d9cd-472">DLL</span><span class="sxs-lookup"><span data-stu-id="1d9cd-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d9cd-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1d9cd-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1d9cd-474">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d9cd-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d9cd-475">**\_ДИСПЛАЙКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="1d9cd-475">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> </dl>

 


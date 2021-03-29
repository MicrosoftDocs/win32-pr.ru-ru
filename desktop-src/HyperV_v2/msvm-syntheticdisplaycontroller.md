---
description: Представляет состояние искусственного контроллера экрана, присутствующего в каждой конфигурации виртуальной машины.
ms.assetid: E496B887-9032-43D8-A7D2-67BB77342AFD
title: Класс Msvm_SyntheticDisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayController
- Msvm_SyntheticDisplayController.SetPowerState
- Msvm_SyntheticDisplayController.EnableDevice
- Msvm_SyntheticDisplayController.OnlineDevice
- Msvm_SyntheticDisplayController.QuiesceDevice
- Msvm_SyntheticDisplayController.SaveProperties
- Msvm_SyntheticDisplayController.RestoreProperties
- Msvm_SyntheticDisplayController.InstanceID
- Msvm_SyntheticDisplayController.Caption
- Msvm_SyntheticDisplayController.Description
- Msvm_SyntheticDisplayController.ElementName
- Msvm_SyntheticDisplayController.InstallDate
- Msvm_SyntheticDisplayController.Name
- Msvm_SyntheticDisplayController.OperationalStatus
- Msvm_SyntheticDisplayController.StatusDescriptions
- Msvm_SyntheticDisplayController.Status
- Msvm_SyntheticDisplayController.HealthState
- Msvm_SyntheticDisplayController.CommunicationStatus
- Msvm_SyntheticDisplayController.DetailedStatus
- Msvm_SyntheticDisplayController.OperatingStatus
- Msvm_SyntheticDisplayController.PrimaryStatus
- Msvm_SyntheticDisplayController.EnabledState
- Msvm_SyntheticDisplayController.OtherEnabledState
- Msvm_SyntheticDisplayController.RequestedState
- Msvm_SyntheticDisplayController.EnabledDefault
- Msvm_SyntheticDisplayController.TimeOfLastStateChange
- Msvm_SyntheticDisplayController.AvailableRequestedStates
- Msvm_SyntheticDisplayController.TransitioningToState
- Msvm_SyntheticDisplayController.SystemCreationClassName
- Msvm_SyntheticDisplayController.SystemName
- Msvm_SyntheticDisplayController.CreationClassName
- Msvm_SyntheticDisplayController.DeviceID
- Msvm_SyntheticDisplayController.PowerManagementSupported
- Msvm_SyntheticDisplayController.PowerManagementCapabilities
- Msvm_SyntheticDisplayController.Availability
- Msvm_SyntheticDisplayController.StatusInfo
- Msvm_SyntheticDisplayController.LastErrorCode
- Msvm_SyntheticDisplayController.ErrorDescription
- Msvm_SyntheticDisplayController.ErrorCleared
- Msvm_SyntheticDisplayController.PowerOnHours
- Msvm_SyntheticDisplayController.TotalPowerOnHours
- Msvm_SyntheticDisplayController.OtherIdentifyingInfo
- Msvm_SyntheticDisplayController.IdentifyingDescriptions
- Msvm_SyntheticDisplayController.AdditionalAvailability
- Msvm_SyntheticDisplayController.MaxQuiesceTime
- Msvm_SyntheticDisplayController.TimeOfLastReset
- Msvm_SyntheticDisplayController.ProtocolSupported
- Msvm_SyntheticDisplayController.MaxNumberControlled
- Msvm_SyntheticDisplayController.ProtocolDescription
- Msvm_SyntheticDisplayController.VideoProcessor
- Msvm_SyntheticDisplayController.VideoMemoryType
- Msvm_SyntheticDisplayController.OtherVideoMemoryType
- Msvm_SyntheticDisplayController.NumberOfVideoPages
- Msvm_SyntheticDisplayController.MaxMemorySupported
- Msvm_SyntheticDisplayController.AcceleratorCapabilities
- Msvm_SyntheticDisplayController.CapabilityDescriptions
- Msvm_SyntheticDisplayController.OtherVideoArchitecture
- Msvm_SyntheticDisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7f566bf2a75b3ed4f503da245d7b6ce428dce5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898326"
---
# <a name="msvm_syntheticdisplaycontroller-class"></a><span data-ttu-id="3e9b9-103">\_Класс мсвм синсетикдисплайконтроллер</span><span class="sxs-lookup"><span data-stu-id="3e9b9-103">Msvm\_SyntheticDisplayController class</span></span>

<span data-ttu-id="3e9b9-104">Представляет состояние искусственного контроллера экрана, присутствующего в каждой конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-104">Represents the state of the synthetic display controller that is present in each virtual machine configuration.</span></span> <span data-ttu-id="3e9b9-105">Только один контроллер экрана может быть активным на виртуальной машине в любое время, и виртуальный контроллер можно активировать только в том случае, если гостевая операционная система загрузила требуемые службы ускорения видео.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-105">Only one display controller can be active in a virtual machine at any time and the synthetic controller can be activated only when the guest operating system has loaded the required video acceleration services.</span></span>

<span data-ttu-id="3e9b9-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e9b9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e9b9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Synthetic Display Controller";
  string   ElementName = "Display Controller";
  datetime InstallDate;
  string   Name = "Display Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_SyntheticDisplayController";
  string   DeviceID = "Microsoft:GUID";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 1024;
  uint32   MaxMemorySupported = 4194304;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="3e9b9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="3e9b9-108">Members</span></span>

<span data-ttu-id="3e9b9-109">Класс **мсвм \_ синсетикдисплайконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3e9b9-109">The **Msvm\_SyntheticDisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="3e9b9-110">Методы</span><span class="sxs-lookup"><span data-stu-id="3e9b9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3e9b9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3e9b9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3e9b9-112">Методы</span><span class="sxs-lookup"><span data-stu-id="3e9b9-112">Methods</span></span>

<span data-ttu-id="3e9b9-113">Класс **мсвм \_ синсетикдисплайконтроллер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-113">The **Msvm\_SyntheticDisplayController** class has these methods.</span></span>



| <span data-ttu-id="3e9b9-114">Метод</span><span class="sxs-lookup"><span data-stu-id="3e9b9-114">Method</span></span>                                                                           | <span data-ttu-id="3e9b9-115">Описание</span><span class="sxs-lookup"><span data-stu-id="3e9b9-115">Description</span></span>                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="3e9b9-116">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-116">**EnableDevice**</span></span>                                                                 | <span data-ttu-id="3e9b9-117">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3e9b9-118">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-118">**OnlineDevice**</span></span>                                                                 | <span data-ttu-id="3e9b9-119">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3e9b9-120">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-120">**QuiesceDevice**</span></span>                                                                | <span data-ttu-id="3e9b9-121">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="3e9b9-122">**Равен**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-122">**RequestStateChange**</span></span>](msvm-syntheticdisplaycontroller-requeststatechange.md) | <span data-ttu-id="3e9b9-123">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="3e9b9-124">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-124">**Reset**</span></span>](msvm-syntheticdisplaycontroller-reset.md)                           | <span data-ttu-id="3e9b9-125">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="3e9b9-126">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-126">**RestoreProperties**</span></span>                                                            | <span data-ttu-id="3e9b9-127">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3e9b9-128">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-128">**SaveProperties**</span></span>                                                               | <span data-ttu-id="3e9b9-129">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3e9b9-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-130">**SetPowerState**</span></span>                                                                | <span data-ttu-id="3e9b9-131">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3e9b9-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="3e9b9-132">Properties</span></span>

<span data-ttu-id="3e9b9-133">Класс **мсвм \_ синсетикдисплайконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-133">The **Msvm\_SyntheticDisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e9b9-134">**акцелераторкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-134">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-135">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3e9b9-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-137">Графические и трехмерные возможности контроллера экрана.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-137">The graphics and 3-D capabilities of the display controller.</span></span> <span data-ttu-id="3e9b9-138">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85))и всегда имеет значение 2 (графический ускоритель).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-138">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 2 (Graphics Accelerator).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-139">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-140">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3e9b9-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-142">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение 6 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-143">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-144">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-146">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение 6 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-147">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-148">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3e9b9-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-150">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="3e9b9-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="3e9b9-151">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-152">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-152">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-153">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-155">Массив строк произвольной формы, которые предоставляют более подробные объяснения для любого из функций ускорителя видео, указанных в массиве свойств **акцелераторкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="3e9b9-155">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** property array.</span></span> <span data-ttu-id="3e9b9-156">Каждая запись этого массива связана с записью в массиве свойств **акцелераторкапабилитиес** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-156">Each entry of this array is related to the entry in the **AcceleratorCapabilities** property array that is located at the same index.</span></span> <span data-ttu-id="3e9b9-157">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85))и всегда имеет значение "графический ускоритель".</span><span class="sxs-lookup"><span data-stu-id="3e9b9-157">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to "Graphics Accelerator".</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-158">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-161">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-161">A short description of the object.</span></span> <span data-ttu-id="3e9b9-162">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "контроллер дисплея".</span><span class="sxs-lookup"><span data-stu-id="3e9b9-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Display Controller".</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-163">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-163">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-164">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-166">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-166">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="3e9b9-167">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-167">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3e9b9-168">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-168">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3e9b9-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3e9b9-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3e9b9-176">)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e9b9-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-178">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-180">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-180">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3e9b9-181">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение "мсвм \_ синсетикдисплайконтроллер".</span><span class="sxs-lookup"><span data-stu-id="3e9b9-181">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_SyntheticDisplayController".</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-182">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-182">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-185">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-185">A description of the object.</span></span> <span data-ttu-id="3e9b9-186">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "виртуальный контроллер дисплея (Майкрософт)".</span><span class="sxs-lookup"><span data-stu-id="3e9b9-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Synthetic Display Controller".</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-187">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-187">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-188">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-190">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-190">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="3e9b9-191">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3e9b9-192">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3e9b9-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3e9b9-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3e9b9-201">)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-201">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e9b9-202">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-202">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-205">Это свойство наследуется от [**CIM \_ ",**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)" и всегда имеет значение "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="3e9b9-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-209">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-209">A display name for the object.</span></span> <span data-ttu-id="3e9b9-210">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и по умолчанию всегда имеет значение "контроллер дисплея".</span><span class="sxs-lookup"><span data-stu-id="3e9b9-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Display Controller" by default.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-211">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-212">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-214">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-214">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="3e9b9-215">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-216">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-216">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-219">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-219">The enabled and disabled states of an element.</span></span> <span data-ttu-id="3e9b9-220">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-220">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="3e9b9-221">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено) или 3 (отключено).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-221">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled) or 3 (Disabled).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-222">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-222">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-223">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-225">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-225">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-226">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-226">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-229">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-229">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-230">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-230">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-231">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-231">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-233">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-233">The current health of the element.</span></span> <span data-ttu-id="3e9b9-234">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-234">This attribute expresses the health of this element but not necessarily that of its subelements.</span></span> <span data-ttu-id="3e9b9-235">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-235">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="3e9b9-236">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-237">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-237">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-238">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-238">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-240">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-240">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-241">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-241">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-242">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-242">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-244">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-244">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="3e9b9-245">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-249">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-250">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3e9b9-251">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-252">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-252">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-253">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-253">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-255">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-256">**максмеморисуппортед**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-256">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-257">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-257">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-259">Максимальный поддерживаемый объем памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-259">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="3e9b9-260">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85))и всегда имеет значение 4 194 304 (0x400000).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-260">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 4,194,304 (0x400000).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-261">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-261">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-262">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-264">Максимальное количество напрямую доступных для адресации сущностей, поддерживаемых этим контроллером.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-264">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="3e9b9-265">Если число неизвестно или неограниченно, следует использовать значение 0.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-265">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="3e9b9-266">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-266">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="3e9b9-267">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller)и всегда имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-267">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-268">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-268">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-269">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-271">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-272">**Name**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-272">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-273">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-275">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-275">The label by which the object is known.</span></span> <span data-ttu-id="3e9b9-276">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и совпадает со свойством **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="3e9b9-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-277">**нумберофвидеопажес**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-277">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-278">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-280">Число поддерживаемых страниц видео с учетом текущих разрешений и доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-280">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="3e9b9-281">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85))и всегда имеет значение 1024.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-281">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 1024.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-282">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-282">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-283">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-285">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="3e9b9-285">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="3e9b9-286">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-286">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3e9b9-287">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3e9b9-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3e9b9-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3e9b9-307">)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-307">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e9b9-308">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-308">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-309">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3e9b9-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-311">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-311">The current statuses of the object.</span></span> <span data-ttu-id="3e9b9-312">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-313">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-313">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-314">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-316">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-316">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="3e9b9-317">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-317">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="3e9b9-318">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-319">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-319">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-320">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-320">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-322">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-322">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-323">**осервидеоарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-323">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-326">Строка, описывающая тип архитектуры видео, если свойство **видеоарчитектуре** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="3e9b9-326">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="3e9b9-327">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-327">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-328">**осервидеомеморитипе**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-328">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-329">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-331">Тип видеопамяти, если свойство **видеомеморитипе** экземпляра имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-331">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="3e9b9-332">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-332">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-333">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-333">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-334">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3e9b9-334">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-336">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-336">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-337">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-337">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-338">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-338">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-340">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-341">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-341">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-342">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-344">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-345">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-345">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-346">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-348">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-348">Provides high level status information.</span></span> <span data-ttu-id="3e9b9-349">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-349">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="3e9b9-350">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-350">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3e9b9-351">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-351">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3e9b9-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-353"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-353"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-354"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-354"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-355"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-355"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-356"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-356"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-357"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3e9b9-357"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3e9b9-358">)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-358">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e9b9-359">**протоколдескриптион**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-359">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-360">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-362">Строка, которая предоставляет дополнительные сведения, связанные с протоколом, поддерживаемым контроллером.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-362">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="3e9b9-363">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller)и всегда имеет значение "Video".</span><span class="sxs-lookup"><span data-stu-id="3e9b9-363">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to "Video".</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-364">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-364">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-365">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-365">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-367">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-367">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="3e9b9-368">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller)и всегда имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-368">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-369">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-369">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-370">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-372">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-372">The last requested or desired state for the element.</span></span> <span data-ttu-id="3e9b9-373">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-373">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="3e9b9-374">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-374">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="3e9b9-375">Конкретный экземпляр [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-375">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="3e9b9-376">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-376">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="3e9b9-377">Это свойство наследуется от **CIM \_ енабледлогикалелемент** и имеет значение 2 (включено), 3 (отключено) или 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-377">This property is inherited from **CIM\_EnabledLogicalElement**, and it is set to 2 (Enabled), 3 (Disabled), or 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-378">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-379">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-381">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-381">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-382">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-382">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-383">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-383">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-384">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-385">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="3e9b9-385">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="3e9b9-386">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="3e9b9-386">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-387">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-387">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-388">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-388">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-389">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-390">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-390">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-391">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-391">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-392">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-394">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-394">The scoping system's creation class name.</span></span> <span data-ttu-id="3e9b9-395">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение "мсвм \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="3e9b9-395">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-396">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-396">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-397">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-398">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-399">Уникальный идентификатор для области виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-399">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="3e9b9-400">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-401">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-401">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-402">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-402">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-404">Время последнего включения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-404">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="3e9b9-405">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-405">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-406">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-406">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-407">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-407">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-408">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-409">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-409">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="3e9b9-410">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-410">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-411">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-411">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-412">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-412">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-414">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-414">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-415">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-415">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-416">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-417">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-418">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-418">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="3e9b9-419">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-419">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-420">**видеоарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-420">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-421">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-423">Указывает архитектуру видеоролика контроллера экрана, используемую для создания видеосигнала.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-423">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="3e9b9-424">Обычно выделенный видеопроцессор создает видеосигнал в соответствии с указанной архитектурой.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-424">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="3e9b9-425">Это индикатор максимальной возможности разрешения контроллеров экрана.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-425">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="3e9b9-426">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-426">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="3e9b9-427"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-427"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-428"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-428"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-429"><span id="CGA"></span><span id="cga"></span>**КГА** (2)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-429"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-430"><span id="EGA"></span><span id="ega"></span>**Ега** (3)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-430"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-431"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-431"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-432"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-432"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-433"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-433"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-434"><span id="HGC"></span><span id="hgc"></span>**ХГК** (7)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-434"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-435"><span id="MCGA"></span><span id="mcga"></span>**Мкга** (8)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-435"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-436"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-436"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-437"><span id="XGA"></span><span id="xga"></span>**Разрешение XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-437"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-438"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Буфер линейного фрейма** (11)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-438"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-439"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-439"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-440"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-440"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-441"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3e9b9-441"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3e9b9-442">)</span><span class="sxs-lookup"><span data-stu-id="3e9b9-442">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e9b9-443">**видеомеморитипе**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-443">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-444">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-444">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-445">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-446">Тип видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-446">The type of video memory.</span></span> <span data-ttu-id="3e9b9-447">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85))и всегда имеет значение 2 (видеопамять).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-447">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 2 (VRAM).</span></span>

</dd> <dt>

<span data-ttu-id="3e9b9-448">**видеопроцессор**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-448">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b9-449">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-449">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9b9-450">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e9b9-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9b9-451">Строка, описывающая процессор или контроллер видео.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-451">A string that describes the video processor/controller.</span></span> <span data-ttu-id="3e9b9-452">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85))и всегда имеет значение "синтетический видеопроцессор".</span><span class="sxs-lookup"><span data-stu-id="3e9b9-452">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to "Synthetic Video Processor".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e9b9-453">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3e9b9-453">Remarks</span></span>

<span data-ttu-id="3e9b9-454">Доступ к классу **\_ синсетикдисплайконтроллер мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="3e9b9-454">Access to the **Msvm\_SyntheticDisplayController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3e9b9-455">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3e9b9-455">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e9b9-456">Требования</span><span class="sxs-lookup"><span data-stu-id="3e9b9-456">Requirements</span></span>



| <span data-ttu-id="3e9b9-457">Требование</span><span class="sxs-lookup"><span data-stu-id="3e9b9-457">Requirement</span></span> | <span data-ttu-id="3e9b9-458">Значение</span><span class="sxs-lookup"><span data-stu-id="3e9b9-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e9b9-459">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e9b9-459">Minimum supported client</span></span><br/> | <span data-ttu-id="3e9b9-460">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3e9b9-460">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3e9b9-461">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e9b9-461">Minimum supported server</span></span><br/> | <span data-ttu-id="3e9b9-462">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3e9b9-462">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e9b9-463">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3e9b9-463">Namespace</span></span><br/>                | <span data-ttu-id="3e9b9-464">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3e9b9-464">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3e9b9-465">MOF</span><span class="sxs-lookup"><span data-stu-id="3e9b9-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e9b9-466"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e9b9-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e9b9-467">DLL</span><span class="sxs-lookup"><span data-stu-id="3e9b9-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e9b9-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3e9b9-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3e9b9-469">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e9b9-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e9b9-470">**\_ДИСПЛАЙКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="3e9b9-470">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> <dt>

<span data-ttu-id="3e9b9-471">[**\_ДИСПЛАЙКОНТРОЛЛЕР CIM**](/previous-versions//cc136810(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3e9b9-471">[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3e9b9-472">Классы видео</span><span class="sxs-lookup"><span data-stu-id="3e9b9-472">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 


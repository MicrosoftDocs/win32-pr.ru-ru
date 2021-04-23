---
description: Представляет состояние эмулированного контроллера S3, присутствующего в каждой конфигурации виртуальной машины.
ms.assetid: 194E0195-1AFF-4298-8000-2249495818C2
title: Класс Msvm_S3DisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_S3DisplayController
- Msvm_S3DisplayController.SetPowerState
- Msvm_S3DisplayController.EnableDevice
- Msvm_S3DisplayController.OnlineDevice
- Msvm_S3DisplayController.QuiesceDevice
- Msvm_S3DisplayController.SaveProperties
- Msvm_S3DisplayController.RestoreProperties
- Msvm_S3DisplayController.InstanceID
- Msvm_S3DisplayController.Caption
- Msvm_S3DisplayController.Description
- Msvm_S3DisplayController.ElementName
- Msvm_S3DisplayController.InstallDate
- Msvm_S3DisplayController.Name
- Msvm_S3DisplayController.OperationalStatus
- Msvm_S3DisplayController.StatusDescriptions
- Msvm_S3DisplayController.Status
- Msvm_S3DisplayController.HealthState
- Msvm_S3DisplayController.CommunicationStatus
- Msvm_S3DisplayController.DetailedStatus
- Msvm_S3DisplayController.OperatingStatus
- Msvm_S3DisplayController.PrimaryStatus
- Msvm_S3DisplayController.EnabledState
- Msvm_S3DisplayController.OtherEnabledState
- Msvm_S3DisplayController.RequestedState
- Msvm_S3DisplayController.EnabledDefault
- Msvm_S3DisplayController.TimeOfLastStateChange
- Msvm_S3DisplayController.AvailableRequestedStates
- Msvm_S3DisplayController.TransitioningToState
- Msvm_S3DisplayController.SystemCreationClassName
- Msvm_S3DisplayController.SystemName
- Msvm_S3DisplayController.CreationClassName
- Msvm_S3DisplayController.DeviceID
- Msvm_S3DisplayController.PowerManagementSupported
- Msvm_S3DisplayController.PowerManagementCapabilities
- Msvm_S3DisplayController.Availability
- Msvm_S3DisplayController.StatusInfo
- Msvm_S3DisplayController.LastErrorCode
- Msvm_S3DisplayController.ErrorDescription
- Msvm_S3DisplayController.ErrorCleared
- Msvm_S3DisplayController.OtherIdentifyingInfo
- Msvm_S3DisplayController.PowerOnHours
- Msvm_S3DisplayController.TotalPowerOnHours
- Msvm_S3DisplayController.IdentifyingDescriptions
- Msvm_S3DisplayController.AdditionalAvailability
- Msvm_S3DisplayController.MaxQuiesceTime
- Msvm_S3DisplayController.TimeOfLastReset
- Msvm_S3DisplayController.ProtocolSupported
- Msvm_S3DisplayController.MaxNumberControlled
- Msvm_S3DisplayController.ProtocolDescription
- Msvm_S3DisplayController.VideoProcessor
- Msvm_S3DisplayController.VideoMemoryType
- Msvm_S3DisplayController.OtherVideoMemoryType
- Msvm_S3DisplayController.NumberOfVideoPages
- Msvm_S3DisplayController.MaxMemorySupported
- Msvm_S3DisplayController.AcceleratorCapabilities
- Msvm_S3DisplayController.CapabilityDescriptions
- Msvm_S3DisplayController.OtherVideoArchitecture
- Msvm_S3DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a4195ff8947bf92d8e4af3a95df320ed950ab21e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156943"
---
# <a name="msvm_s3displaycontroller-class"></a><span data-ttu-id="d371d-103">\_Класс мсвм S3DisplayController</span><span class="sxs-lookup"><span data-stu-id="d371d-103">Msvm\_S3DisplayController class</span></span>

<span data-ttu-id="d371d-104">Представляет состояние эмулированного контроллера S3, присутствующего в каждой конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d371d-104">Represents the state of the emulated S3 controller that is present in each virtual machine configuration.</span></span> <span data-ttu-id="d371d-105">Только один контроллер экрана может быть активным на виртуальной машине в любое время.</span><span class="sxs-lookup"><span data-stu-id="d371d-105">Only one display controller can be active in a virtual machine at any time.</span></span>

> [!Note]  
> <span data-ttu-id="d371d-106">Этот класс применяется только к виртуальным машинам поколения 1.</span><span class="sxs-lookup"><span data-stu-id="d371d-106">This class only applies to generation 1 virtual machines.</span></span>

 

<span data-ttu-id="d371d-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d371d-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d371d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d371d-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_S3DisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Emulated Display Controller";
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
  string   EnabledState = 3;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_S3DisplayController";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Virtual S3 Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 32768;
  uint32   MaxMemorySupported = 134217728;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="d371d-109">Члены</span><span class="sxs-lookup"><span data-stu-id="d371d-109">Members</span></span>

<span data-ttu-id="d371d-110">Класс **мсвм \_ S3DisplayController** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d371d-110">The **Msvm\_S3DisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="d371d-111">Методы</span><span class="sxs-lookup"><span data-stu-id="d371d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d371d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="d371d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d371d-113">Методы</span><span class="sxs-lookup"><span data-stu-id="d371d-113">Methods</span></span>

<span data-ttu-id="d371d-114">Класс **мсвм \_ S3DisplayController** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d371d-114">The **Msvm\_S3DisplayController** class has these methods.</span></span>



| <span data-ttu-id="d371d-115">Метод</span><span class="sxs-lookup"><span data-stu-id="d371d-115">Method</span></span>                                                                    | <span data-ttu-id="d371d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d371d-116">Description</span></span>                              |
|:--------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="d371d-117">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="d371d-117">**EnableDevice**</span></span>                                                          | <span data-ttu-id="d371d-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d371d-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d371d-119">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="d371d-119">**OnlineDevice**</span></span>                                                          | <span data-ttu-id="d371d-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d371d-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d371d-121">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="d371d-121">**QuiesceDevice**</span></span>                                                         | <span data-ttu-id="d371d-122">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d371d-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="d371d-123">**Равен**</span><span class="sxs-lookup"><span data-stu-id="d371d-123">**RequestStateChange**</span></span>](msvm-s3displaycontroller-requeststatechange.md) | <span data-ttu-id="d371d-124">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="d371d-124">Requests a state change.</span></span> <br/>     |
| [<span data-ttu-id="d371d-125">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="d371d-125">**Reset**</span></span>](msvm-s3displaycontroller-reset.md)                           | <span data-ttu-id="d371d-126">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="d371d-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="d371d-127">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="d371d-127">**RestoreProperties**</span></span>                                                     | <span data-ttu-id="d371d-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d371d-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d371d-129">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="d371d-129">**SaveProperties**</span></span>                                                        | <span data-ttu-id="d371d-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d371d-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d371d-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d371d-131">**SetPowerState**</span></span>                                                         | <span data-ttu-id="d371d-132">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d371d-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d371d-133">Свойства</span><span class="sxs-lookup"><span data-stu-id="d371d-133">Properties</span></span>

<span data-ttu-id="d371d-134">Класс **мсвм \_ S3DisplayController** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d371d-134">The **Msvm\_S3DisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d371d-135">**акцелераторкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="d371d-135">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-136">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d371d-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d371d-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-138">Графические и трехмерные возможности контроллера экрана.</span><span class="sxs-lookup"><span data-stu-id="d371d-138">The graphics and 3D capabilities of the display controller.</span></span> <span data-ttu-id="d371d-139">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d371d-139">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-140">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="d371d-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-141">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d371d-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d371d-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-143">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="d371d-143">Any additional availability and status of the device.</span></span> <span data-ttu-id="d371d-144">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d371d-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-145">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="d371d-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-146">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d371d-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-148">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="d371d-148">The primary availability and status of the device.</span></span> <span data-ttu-id="d371d-149">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d371d-149">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="d371d-150">Значение</span><span class="sxs-lookup"><span data-stu-id="d371d-150">Value</span></span>                                                                        | <span data-ttu-id="d371d-151">Значение</span><span class="sxs-lookup"><span data-stu-id="d371d-151">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="d371d-152"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d371d-152"><dt>6</dt></span></span> </dl> | <span data-ttu-id="d371d-153">Не применимо</span><span class="sxs-lookup"><span data-stu-id="d371d-153">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d371d-154">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="d371d-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-155">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d371d-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d371d-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-157">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="d371d-157">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="d371d-158">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="d371d-158">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d371d-159">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="d371d-159">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-160">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d371d-160">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d371d-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-162">Массив строк произвольной формы, которые предоставляют более подробные объяснения для любого из функций ускорителя видео, указанных в массиве **акцелераторкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="d371d-162">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="d371d-163">Каждая запись этого массива связана с записью в массиве **акцелераторкапабилитиес** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="d371d-163">Each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span> <span data-ttu-id="d371d-164">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d371d-164">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-165">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d371d-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-168">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d371d-168">A short description of the object.</span></span> <span data-ttu-id="d371d-169">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d371d-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-170">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="d371d-170">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-171">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d371d-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-173">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="d371d-173">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d371d-174">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="d371d-174">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d371d-175">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d371d-175">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d371d-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d371d-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="d371d-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="d371d-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="d371d-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="d371d-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="d371d-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d371d-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d371d-183">)</span><span class="sxs-lookup"><span data-stu-id="d371d-183">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d371d-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d371d-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-185">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d371d-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-187">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d371d-187">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d371d-188">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение "мсвм \_ S3DisplayController".</span><span class="sxs-lookup"><span data-stu-id="d371d-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_S3DisplayController".</span></span>

</dd> <dt>

<span data-ttu-id="d371d-189">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d371d-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-192">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d371d-192">A description of the object.</span></span> <span data-ttu-id="d371d-193">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d371d-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d371d-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-195">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d371d-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-197">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="d371d-197">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d371d-198">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="d371d-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d371d-199">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d371d-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d371d-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="d371d-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="d371d-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="d371d-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="d371d-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="d371d-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="d371d-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="d371d-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d371d-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d371d-208">)</span><span class="sxs-lookup"><span data-stu-id="d371d-208">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d371d-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d371d-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-212">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="d371d-212">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="d371d-213">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d371d-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d371d-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-215">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-217">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="d371d-217">A display name for the object.</span></span> <span data-ttu-id="d371d-218">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d371d-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-219">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="d371d-219">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-220">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d371d-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-222">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="d371d-222">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d371d-223">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d371d-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="d371d-224">Значение</span><span class="sxs-lookup"><span data-stu-id="d371d-224">Value</span></span>                                                                        | <span data-ttu-id="d371d-225">Значение</span><span class="sxs-lookup"><span data-stu-id="d371d-225">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="d371d-226"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d371d-226"><dt>2</dt></span></span> </dl> | <span data-ttu-id="d371d-227">Активировано</span><span class="sxs-lookup"><span data-stu-id="d371d-227">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="d371d-228"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d371d-228"><dt>3</dt></span></span> </dl> | <span data-ttu-id="d371d-229">Выключено</span><span class="sxs-lookup"><span data-stu-id="d371d-229">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d371d-230">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d371d-230">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-231">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-233">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="d371d-233">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d371d-234">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="d371d-234">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="d371d-235">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено) или 3 (отключено).</span><span class="sxs-lookup"><span data-stu-id="d371d-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="d371d-236">Значение</span><span class="sxs-lookup"><span data-stu-id="d371d-236">Value</span></span>                                                                        | <span data-ttu-id="d371d-237">Значение</span><span class="sxs-lookup"><span data-stu-id="d371d-237">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="d371d-238"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d371d-238"><dt>2</dt></span></span> </dl> | <span data-ttu-id="d371d-239">Активировано</span><span class="sxs-lookup"><span data-stu-id="d371d-239">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="d371d-240"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d371d-240"><dt>3</dt></span></span> </dl> | <span data-ttu-id="d371d-241">Выключено</span><span class="sxs-lookup"><span data-stu-id="d371d-241">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d371d-242">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="d371d-242">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-243">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d371d-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-245">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="d371d-245">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="d371d-246">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d371d-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d371d-247">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d371d-247">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-248">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-250">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="d371d-250">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="d371d-251">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d371d-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d371d-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d371d-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-253">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d371d-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-255">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="d371d-255">The current health of the element.</span></span> <span data-ttu-id="d371d-256">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="d371d-256">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="d371d-257">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="d371d-257">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="d371d-258">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d371d-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="d371d-259">Значение</span><span class="sxs-lookup"><span data-stu-id="d371d-259">Value</span></span>                                                                        | <span data-ttu-id="d371d-260">Значение</span><span class="sxs-lookup"><span data-stu-id="d371d-260">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="d371d-261"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d371d-261"><dt>5</dt></span></span> </dl> | <span data-ttu-id="d371d-262">ОК</span><span class="sxs-lookup"><span data-stu-id="d371d-262">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d371d-263">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d371d-263">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-264">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d371d-264">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d371d-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-266">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="d371d-266">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="d371d-267">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="d371d-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d371d-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d371d-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-269">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d371d-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-271">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d371d-271">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="d371d-272">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d371d-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-273">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d371d-273">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-274">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d371d-276">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="d371d-276">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d371d-277">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="d371d-277">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d371d-278">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d371d-278">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-279">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="d371d-279">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-280">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d371d-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-282">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="d371d-282">The last error code reported by the logical device.</span></span> <span data-ttu-id="d371d-283">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d371d-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d371d-284">**максмеморисуппортед**</span><span class="sxs-lookup"><span data-stu-id="d371d-284">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-285">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d371d-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-287">Максимальный поддерживаемый объем памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="d371d-287">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="d371d-288">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d371d-288">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-289">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="d371d-289">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-290">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d371d-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-292">Максимальное количество напрямую доступных для адресации сущностей, поддерживаемых этим контроллером.</span><span class="sxs-lookup"><span data-stu-id="d371d-292">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="d371d-293">Если число неизвестно или неограниченно, следует использовать значение 0.</span><span class="sxs-lookup"><span data-stu-id="d371d-293">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="d371d-294">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="d371d-294">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="d371d-295">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="d371d-295">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-296">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="d371d-296">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-297">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d371d-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-299">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d371d-299">This property has been deprecated.</span></span> <span data-ttu-id="d371d-300">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d371d-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-301">**Name**</span><span class="sxs-lookup"><span data-stu-id="d371d-301">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-302">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-304">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="d371d-304">The label by which the object is known.</span></span> <span data-ttu-id="d371d-305">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d371d-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-306">**нумберофвидеопажес**</span><span class="sxs-lookup"><span data-stu-id="d371d-306">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-307">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d371d-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-309">Число поддерживаемых страниц видео с учетом текущих разрешений и доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="d371d-309">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="d371d-310">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d371d-310">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-311">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="d371d-311">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-312">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d371d-312">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-314">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="d371d-314">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d371d-315">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="d371d-315">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d371d-316">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d371d-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d371d-317"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d371d-317"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-318"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="d371d-318"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-319"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="d371d-319"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-320"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="d371d-320"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-321"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="d371d-321"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-322"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="d371d-322"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-323"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="d371d-323"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-324"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="d371d-324"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-325"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="d371d-325"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-326"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="d371d-326"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-327"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="d371d-327"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-328"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="d371d-328"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-329"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="d371d-329"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-330"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="d371d-330"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-331"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="d371d-331"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-332"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="d371d-332"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-333"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="d371d-333"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-334"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="d371d-334"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-335"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d371d-335"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d371d-336">)</span><span class="sxs-lookup"><span data-stu-id="d371d-336">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d371d-337">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d371d-337">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-338">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d371d-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d371d-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-340">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="d371d-340">The current statuses of the object.</span></span> <span data-ttu-id="d371d-341">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="d371d-341">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-342">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="d371d-342">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-343">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-345">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="d371d-345">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d371d-346">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="d371d-346">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="d371d-347">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="d371d-347">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d371d-348">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d371d-348">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-349">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d371d-349">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d371d-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-351">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="d371d-351">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="d371d-352">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="d371d-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d371d-353">**осервидеоарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="d371d-353">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-354">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-356">Строка, описывающая тип архитектуры видео, если свойство **видеоарчитектуре** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="d371d-356">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="d371d-357">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d371d-357">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-358">**осервидеомеморитипе**</span><span class="sxs-lookup"><span data-stu-id="d371d-358">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-359">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-360">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-361">Тип видеопамяти, если свойство **видеомеморитипе** экземпляра имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="d371d-361">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="d371d-362">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d371d-362">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-363">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="d371d-363">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-364">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d371d-364">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d371d-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-366">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="d371d-366">The power management capabilities of the device.</span></span> <span data-ttu-id="d371d-367">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d371d-367">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d371d-368">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="d371d-368">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-369">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d371d-369">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-371">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="d371d-371">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="d371d-372">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d371d-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d371d-373">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="d371d-373">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-374">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d371d-374">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-376">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="d371d-376">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="d371d-377">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d371d-377">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d371d-378">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="d371d-378">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-379">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d371d-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-381">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="d371d-381">Provides high level status information.</span></span> <span data-ttu-id="d371d-382">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="d371d-382">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="d371d-383">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="d371d-383">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d371d-384">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d371d-384">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d371d-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d371d-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-386"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="d371d-386"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-387"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="d371d-387"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-388"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="d371d-388"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-389"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="d371d-389"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-390"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d371d-390"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d371d-391">)</span><span class="sxs-lookup"><span data-stu-id="d371d-391">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d371d-392">**протоколдескриптион**</span><span class="sxs-lookup"><span data-stu-id="d371d-392">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-393">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-395">Строка, которая предоставляет дополнительные сведения, связанные с протоколом, поддерживаемым контроллером.</span><span class="sxs-lookup"><span data-stu-id="d371d-395">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="d371d-396">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="d371d-396">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-397">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="d371d-397">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-398">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d371d-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-400">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="d371d-400">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="d371d-401">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="d371d-401">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-402">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d371d-402">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-403">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d371d-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-405">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="d371d-405">The last requested or desired state for the element.</span></span> <span data-ttu-id="d371d-406">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="d371d-406">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="d371d-407">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="d371d-407">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="d371d-408">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d371d-408">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="d371d-409">Значение</span><span class="sxs-lookup"><span data-stu-id="d371d-409">Value</span></span>                                                                         | <span data-ttu-id="d371d-410">Значение</span><span class="sxs-lookup"><span data-stu-id="d371d-410">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="d371d-411"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="d371d-411"><dt>12</dt></span></span> </dl> | <span data-ttu-id="d371d-412">Не применимо</span><span class="sxs-lookup"><span data-stu-id="d371d-412">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d371d-413">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="d371d-413">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-414">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-415">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-416">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="d371d-416">The current status of the object.</span></span> <span data-ttu-id="d371d-417">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="d371d-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d371d-418">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="d371d-418">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-419">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d371d-419">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d371d-420">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-421">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d371d-421">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d371d-422">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="d371d-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="d371d-423">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d371d-423">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-424">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d371d-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-426">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="d371d-426">The current state of the logical device.</span></span> <span data-ttu-id="d371d-427">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d371d-427">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d371d-428">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="d371d-428">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-429">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-430">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-431">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="d371d-431">The scoping system's creation class name.</span></span> <span data-ttu-id="d371d-432">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d371d-432">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d371d-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-434">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-436">Уникальный идентификатор для области виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d371d-436">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="d371d-437">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d371d-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-438">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="d371d-438">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-439">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d371d-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-441">Время последнего включения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d371d-441">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="d371d-442">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="d371d-442">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-443">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="d371d-443">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-444">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d371d-444">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-445">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-446">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="d371d-446">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d371d-447">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d371d-447">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-448">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="d371d-448">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-449">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d371d-449">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-450">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-451">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="d371d-451">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="d371d-452">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d371d-452">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d371d-453">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="d371d-453">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-454">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d371d-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-455">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-456">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="d371d-456">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d371d-457">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="d371d-457">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d371d-458">**видеоарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="d371d-458">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-459">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d371d-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-460">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-461">Указывает архитектуру видеоролика контроллера экрана, используемую для создания видеосигнала.</span><span class="sxs-lookup"><span data-stu-id="d371d-461">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="d371d-462">Обычно выделенный видеопроцессор создает видеосигнал в соответствии с указанной архитектурой.</span><span class="sxs-lookup"><span data-stu-id="d371d-462">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="d371d-463">Это индикатор максимальной возможности разрешения контроллеров экрана.</span><span class="sxs-lookup"><span data-stu-id="d371d-463">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="d371d-464">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d371d-464">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="d371d-465"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d371d-465"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-466"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d371d-466"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-467"><span id="CGA"></span><span id="cga"></span>**КГА** (2)</span><span class="sxs-lookup"><span data-stu-id="d371d-467"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-468"><span id="EGA"></span><span id="ega"></span>**Ега** (3)</span><span class="sxs-lookup"><span data-stu-id="d371d-468"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-469"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="d371d-469"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-470"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="d371d-470"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-471"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="d371d-471"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-472"><span id="HGC"></span><span id="hgc"></span>**ХГК** (7)</span><span class="sxs-lookup"><span data-stu-id="d371d-472"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-473"><span id="MCGA"></span><span id="mcga"></span>**Мкга** (8)</span><span class="sxs-lookup"><span data-stu-id="d371d-473"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-474"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="d371d-474"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-475"><span id="XGA"></span><span id="xga"></span>**Разрешение XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="d371d-475"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-476"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Буфер линейного фрейма** (11)</span><span class="sxs-lookup"><span data-stu-id="d371d-476"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-477"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="d371d-477"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-478"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="d371d-478"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d371d-479"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d371d-479"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d371d-480">)</span><span class="sxs-lookup"><span data-stu-id="d371d-480">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d371d-481">**видеомеморитипе**</span><span class="sxs-lookup"><span data-stu-id="d371d-481">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-482">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d371d-482">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-483">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-484">Тип видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="d371d-484">The type of video memory.</span></span> <span data-ttu-id="d371d-485">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d371d-485">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d371d-486">**видеопроцессор**</span><span class="sxs-lookup"><span data-stu-id="d371d-486">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d371d-487">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d371d-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d371d-488">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d371d-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d371d-489">Строка, описывающая процессор или контроллер видео.</span><span class="sxs-lookup"><span data-stu-id="d371d-489">A string that describes the video processor/controller.</span></span> <span data-ttu-id="d371d-490">Это свойство наследуется от [**CIM \_ дисплайконтроллер**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d371d-490">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d371d-491">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d371d-491">Remarks</span></span>

<span data-ttu-id="d371d-492">Доступ к классу **\_ S3DisplayController мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="d371d-492">Access to the **Msvm\_S3DisplayController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d371d-493">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d371d-493">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d371d-494">Требования</span><span class="sxs-lookup"><span data-stu-id="d371d-494">Requirements</span></span>



| <span data-ttu-id="d371d-495">Требование</span><span class="sxs-lookup"><span data-stu-id="d371d-495">Requirement</span></span> | <span data-ttu-id="d371d-496">Значение</span><span class="sxs-lookup"><span data-stu-id="d371d-496">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d371d-497">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d371d-497">Minimum supported client</span></span><br/> | <span data-ttu-id="d371d-498">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d371d-498">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d371d-499">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d371d-499">Minimum supported server</span></span><br/> | <span data-ttu-id="d371d-500">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d371d-500">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d371d-501">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d371d-501">Namespace</span></span><br/>                | <span data-ttu-id="d371d-502">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d371d-502">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d371d-503">MOF</span><span class="sxs-lookup"><span data-stu-id="d371d-503">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d371d-504"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d371d-504"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d371d-505">DLL</span><span class="sxs-lookup"><span data-stu-id="d371d-505">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d371d-506"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d371d-506"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d371d-507">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d371d-507">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d371d-508">**\_ДИСПЛАЙКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="d371d-508">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> <dt>

<span data-ttu-id="d371d-509">[**\_ДИСПЛАЙКОНТРОЛЛЕР CIM**](/previous-versions//cc136810(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d371d-509">[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d371d-510">Классы видео</span><span class="sxs-lookup"><span data-stu-id="d371d-510">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 


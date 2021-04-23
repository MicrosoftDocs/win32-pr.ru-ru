---
description: Представляет возможности и управление последовательным контроллером.
ms.assetid: 0F4DCF98-8EE4-4005-ADD5-BA23CB4CBE82
title: Класс Msvm_SerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialController
- Msvm_SerialController.SetPowerState
- Msvm_SerialController.EnableDevice
- Msvm_SerialController.OnlineDevice
- Msvm_SerialController.QuiesceDevice
- Msvm_SerialController.SaveProperties
- Msvm_SerialController.RestoreProperties
- Msvm_SerialController.InstanceID
- Msvm_SerialController.Caption
- Msvm_SerialController.Description
- Msvm_SerialController.ElementName
- Msvm_SerialController.InstallDate
- Msvm_SerialController.Name
- Msvm_SerialController.OperationalStatus
- Msvm_SerialController.StatusDescriptions
- Msvm_SerialController.Status
- Msvm_SerialController.HealthState
- Msvm_SerialController.CommunicationStatus
- Msvm_SerialController.DetailedStatus
- Msvm_SerialController.OperatingStatus
- Msvm_SerialController.PrimaryStatus
- Msvm_SerialController.EnabledState
- Msvm_SerialController.OtherEnabledState
- Msvm_SerialController.RequestedState
- Msvm_SerialController.EnabledDefault
- Msvm_SerialController.TimeOfLastStateChange
- Msvm_SerialController.AvailableRequestedStates
- Msvm_SerialController.TransitioningToState
- Msvm_SerialController.SystemCreationClassName
- Msvm_SerialController.SystemName
- Msvm_SerialController.CreationClassName
- Msvm_SerialController.DeviceID
- Msvm_SerialController.PowerManagementSupported
- Msvm_SerialController.PowerManagementCapabilities
- Msvm_SerialController.Availability
- Msvm_SerialController.StatusInfo
- Msvm_SerialController.LastErrorCode
- Msvm_SerialController.ErrorDescription
- Msvm_SerialController.ErrorCleared
- Msvm_SerialController.OtherIdentifyingInfo
- Msvm_SerialController.PowerOnHours
- Msvm_SerialController.TotalPowerOnHours
- Msvm_SerialController.IdentifyingDescriptions
- Msvm_SerialController.AdditionalAvailability
- Msvm_SerialController.MaxQuiesceTime
- Msvm_SerialController.TimeOfLastReset
- Msvm_SerialController.ProtocolSupported
- Msvm_SerialController.MaxNumberControlled
- Msvm_SerialController.ProtocolDescription
- Msvm_SerialController.Capabilities
- Msvm_SerialController.CapabilityDescriptions
- Msvm_SerialController.MaxBaudRate
- Msvm_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3f1bbc9dabe078751d58875745a789895cb4c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650586"
---
# <a name="msvm_serialcontroller-class"></a><span data-ttu-id="8ef94-103">\_Класс мсвм сериалконтроллер</span><span class="sxs-lookup"><span data-stu-id="8ef94-103">Msvm\_SerialController class</span></span>

<span data-ttu-id="8ef94-104">Представляет возможности и управление последовательным контроллером.</span><span class="sxs-lookup"><span data-stu-id="8ef94-104">Represents the capabilities and management of the serial controller.</span></span> <span data-ttu-id="8ef94-105">Последовательные контроллеры — это логические устройства, которые всегда находятся на виртуальной машине и поэтому не распределяются через пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ef94-105">Serial controllers are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="8ef94-106">Один экземпляр последовательного контроллера всегда имеется в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="8ef94-106">One serial controller instance is always present in a virtual machine.</span></span> <span data-ttu-id="8ef94-107">Последовательные контроллеры имеют фиксированное число экземпляров портов.</span><span class="sxs-lookup"><span data-stu-id="8ef94-107">Serial controllers have a fixed number of port instances.</span></span> <span data-ttu-id="8ef94-108">Эта реализация поддерживает два порта на контроллере.</span><span class="sxs-lookup"><span data-stu-id="8ef94-108">This implementation supports two ports per controller.</span></span>

> [!Note]  
> <span data-ttu-id="8ef94-109">Последовательные контроллеры являются необязательными в [виртуальных машинах поколения 2](virtualization-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="8ef94-109">Serial controllers are optional in [generation 2 virtual machines](virtualization-glossary.md).</span></span>

 

<span data-ttu-id="8ef94-110">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="8ef94-110">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ef94-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ef94-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialController : CIM_SerialController
{
  string   InstanceID;
  string   Caption = "Serial Controller";
  string   Description = "Microsoft Virtual Serial Controller";
  string   ElementName = "Serial Controller";
  datetime InstallDate;
  string   Name = "Serial Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_SerialController";
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 26;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription;
  uint16   Capabilities[] = { 5 };
  string   CapabilityDescriptions[] = { "16550 compatible" };
  uint32   MaxBaudRate = 115200;
  uint16   Security = 3;
};
```

## <a name="members"></a><span data-ttu-id="8ef94-112">Члены</span><span class="sxs-lookup"><span data-stu-id="8ef94-112">Members</span></span>

<span data-ttu-id="8ef94-113">Класс **мсвм \_ сериалконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8ef94-113">The **Msvm\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="8ef94-114">Методы</span><span class="sxs-lookup"><span data-stu-id="8ef94-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="8ef94-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="8ef94-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8ef94-116">Методы</span><span class="sxs-lookup"><span data-stu-id="8ef94-116">Methods</span></span>

<span data-ttu-id="8ef94-117">Класс **мсвм \_ сериалконтроллер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8ef94-117">The **Msvm\_SerialController** class has these methods.</span></span>



| <span data-ttu-id="8ef94-118">Метод</span><span class="sxs-lookup"><span data-stu-id="8ef94-118">Method</span></span>                                                                 | <span data-ttu-id="8ef94-119">Описание</span><span class="sxs-lookup"><span data-stu-id="8ef94-119">Description</span></span>                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="8ef94-120">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="8ef94-120">**EnableDevice**</span></span>                                                       | <span data-ttu-id="8ef94-121">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8ef94-121">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8ef94-122">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="8ef94-122">**OnlineDevice**</span></span>                                                       | <span data-ttu-id="8ef94-123">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8ef94-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8ef94-124">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="8ef94-124">**QuiesceDevice**</span></span>                                                      | <span data-ttu-id="8ef94-125">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8ef94-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="8ef94-126">**Равен**</span><span class="sxs-lookup"><span data-stu-id="8ef94-126">**RequestStateChange**</span></span>](msvm-serialcontroller-requeststatechange.md) | <span data-ttu-id="8ef94-127">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="8ef94-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="8ef94-128">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="8ef94-128">**Reset**</span></span>](msvm-serialcontroller-reset.md)                           | <span data-ttu-id="8ef94-129">Выполняет сброс устройства.</span><span class="sxs-lookup"><span data-stu-id="8ef94-129">Resets the device.</span></span><br/>            |
| <span data-ttu-id="8ef94-130">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="8ef94-130">**RestoreProperties**</span></span>                                                  | <span data-ttu-id="8ef94-131">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8ef94-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8ef94-132">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="8ef94-132">**SaveProperties**</span></span>                                                     | <span data-ttu-id="8ef94-133">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8ef94-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8ef94-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8ef94-134">**SetPowerState**</span></span>                                                      | <span data-ttu-id="8ef94-135">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8ef94-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8ef94-136">Свойства</span><span class="sxs-lookup"><span data-stu-id="8ef94-136">Properties</span></span>

<span data-ttu-id="8ef94-137">Класс **мсвм \_ сериалконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8ef94-137">The **Msvm\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8ef94-138">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="8ef94-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-139">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8ef94-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-141">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="8ef94-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="8ef94-142">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8ef94-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="8ef94-143">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef94-143">Value</span></span>                                                                            | <span data-ttu-id="8ef94-144">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef94-144">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="8ef94-145"><dt>1-6</dt></span><span class="sxs-lookup"><span data-stu-id="8ef94-145"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="8ef94-146"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="8ef94-146"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="8ef94-147">Не применимо</span><span class="sxs-lookup"><span data-stu-id="8ef94-147">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8ef94-148">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="8ef94-148">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-149">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ef94-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-151">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="8ef94-151">The primary availability and status of the device.</span></span> <span data-ttu-id="8ef94-152">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8ef94-152">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="8ef94-153">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef94-153">Value</span></span>                                                                        | <span data-ttu-id="8ef94-154">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef94-154">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="8ef94-155"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="8ef94-155"><dt>6</dt></span></span> </dl> | <span data-ttu-id="8ef94-156">Не применимо</span><span class="sxs-lookup"><span data-stu-id="8ef94-156">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8ef94-157">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="8ef94-157">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-158">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8ef94-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-160">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="8ef94-160">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="8ef94-161">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="8ef94-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="8ef94-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-163">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8ef94-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-165">Буферизация и другие возможности последовательного контроллера, которые могут быть встроенными в оборудование микросхемы.</span><span class="sxs-lookup"><span data-stu-id="8ef94-165">The buffering and other capabilities of the serial controller that might be inherent in the chip hardware.</span></span> <span data-ttu-id="8ef94-166">Это свойство наследуется от [**CIM \_ сериалконтроллер**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="8ef94-166">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-167">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="8ef94-167">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-168">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8ef94-168">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-170">Массив строк произвольной формы, предоставляющий более подробные объяснения для любой из функций последовательного контроллера, указанных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="8ef94-170">An array of free-form strings that provides more detailed explanations for any of the serial controller features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="8ef94-171">Это свойство наследуется от [**CIM \_ сериалконтроллер**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="8ef94-171">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-172">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="8ef94-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8ef94-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-175">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8ef94-175">A short description of the object.</span></span> <span data-ttu-id="8ef94-176">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8ef94-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-177">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="8ef94-177">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-178">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ef94-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-180">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="8ef94-180">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8ef94-181">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8ef94-181">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8ef94-182">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ef94-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8ef94-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="8ef94-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="8ef94-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="8ef94-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="8ef94-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="8ef94-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="8ef94-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8ef94-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8ef94-190">)</span><span class="sxs-lookup"><span data-stu-id="8ef94-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ef94-191">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8ef94-191">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8ef94-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-194">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8ef94-194">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8ef94-195">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8ef94-195">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-196">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8ef94-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8ef94-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-199">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8ef94-199">A description of the object.</span></span> <span data-ttu-id="8ef94-200">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8ef94-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8ef94-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-202">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ef94-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-204">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="8ef94-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8ef94-205">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8ef94-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8ef94-206">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ef94-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8ef94-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="8ef94-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="8ef94-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="8ef94-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="8ef94-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="8ef94-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="8ef94-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="8ef94-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8ef94-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8ef94-215">)</span><span class="sxs-lookup"><span data-stu-id="8ef94-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ef94-216">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8ef94-216">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8ef94-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-219">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение Microsoft: *<GUID>* .</span><span class="sxs-lookup"><span data-stu-id="8ef94-219">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*<GUID>*".</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-220">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8ef94-220">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-221">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8ef94-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-223">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="8ef94-223">A display name for the object.</span></span> <span data-ttu-id="8ef94-224">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8ef94-224">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-225">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="8ef94-225">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-226">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ef94-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-227">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-228">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="8ef94-228">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="8ef94-229">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8ef94-229">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="8ef94-230">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef94-230">Value</span></span>                                                                        | <span data-ttu-id="8ef94-231">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef94-231">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="8ef94-232"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8ef94-232"><dt>2</dt></span></span> </dl> | <span data-ttu-id="8ef94-233">Активировано</span><span class="sxs-lookup"><span data-stu-id="8ef94-233">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8ef94-234">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8ef94-234">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-235">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ef94-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-237">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="8ef94-237">The enabled and disabled states of an element.</span></span> <span data-ttu-id="8ef94-238">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="8ef94-238">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="8ef94-239">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8ef94-239">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="8ef94-240">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef94-240">Value</span></span>                                                                        | <span data-ttu-id="8ef94-241">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef94-241">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="8ef94-242"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="8ef94-242"><dt>5</dt></span></span> </dl> | <span data-ttu-id="8ef94-243">Не применимо</span><span class="sxs-lookup"><span data-stu-id="8ef94-243">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8ef94-244">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="8ef94-244">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-245">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8ef94-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-247">Указывает, что сообщение об ошибке в свойстве **ластерроркоде** теперь отключено.</span><span class="sxs-lookup"><span data-stu-id="8ef94-247">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="8ef94-248">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8ef94-248">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-249">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8ef94-249">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-250">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8ef94-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-252">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в свойстве **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="8ef94-252">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="8ef94-253">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8ef94-253">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-254">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8ef94-254">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-255">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ef94-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-257">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="8ef94-257">The current health of the element.</span></span> <span data-ttu-id="8ef94-258">Это выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="8ef94-258">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="8ef94-259">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="8ef94-259">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="8ef94-260">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ef94-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-261">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8ef94-261">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-262">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8ef94-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-264">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="8ef94-264">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="8ef94-265">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="8ef94-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-266">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8ef94-266">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-267">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8ef94-267">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-269">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8ef94-269">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="8ef94-270">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ef94-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8ef94-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-272">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8ef94-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-274">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="8ef94-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-275">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="8ef94-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8ef94-276">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8ef94-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-277">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="8ef94-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-278">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ef94-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-280">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="8ef94-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="8ef94-281">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8ef94-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-282">**максбаудрате**</span><span class="sxs-lookup"><span data-stu-id="8ef94-282">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-283">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ef94-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-285">Максимальная скорость в битах в секунду, поддерживаемая последовательным контроллером.</span><span class="sxs-lookup"><span data-stu-id="8ef94-285">The maximum baud rate, in bits per second, that is supported by the serial controller.</span></span> <span data-ttu-id="8ef94-286">Это свойство наследуется от [**CIM \_ сериалконтроллер**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="8ef94-286">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-287">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="8ef94-287">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-288">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ef94-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-290">Максимальное количество напрямую доступных для адресации сущностей, поддерживаемых этим контроллером.</span><span class="sxs-lookup"><span data-stu-id="8ef94-290">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="8ef94-291">Если число неизвестно или неограниченно, следует использовать значение 0.</span><span class="sxs-lookup"><span data-stu-id="8ef94-291">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="8ef94-292">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="8ef94-292">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="8ef94-293">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="8ef94-293">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-294">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="8ef94-294">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-295">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8ef94-295">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-297">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="8ef94-297">This property has been deprecated.</span></span> <span data-ttu-id="8ef94-298">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8ef94-298">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-299">**Name**</span><span class="sxs-lookup"><span data-stu-id="8ef94-299">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8ef94-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-302">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="8ef94-302">The label by which the object is known.</span></span> <span data-ttu-id="8ef94-303">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и совпадает со свойством **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="8ef94-303">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-304">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="8ef94-304">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-305">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ef94-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-307">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="8ef94-307">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8ef94-308">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8ef94-308">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8ef94-309">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ef94-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8ef94-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="8ef94-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-311"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="8ef94-311"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-312"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="8ef94-312"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-313"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="8ef94-313"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-314"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="8ef94-314"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-315"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="8ef94-315"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-316"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="8ef94-316"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-317"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="8ef94-317"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-318"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="8ef94-318"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-319"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="8ef94-319"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-320"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="8ef94-320"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-321"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="8ef94-321"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-322"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="8ef94-322"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-323"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="8ef94-323"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-324"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="8ef94-324"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-325"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="8ef94-325"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-326"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="8ef94-326"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-327"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="8ef94-327"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-328"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8ef94-328"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8ef94-329">)</span><span class="sxs-lookup"><span data-stu-id="8ef94-329">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ef94-330">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8ef94-330">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-331">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8ef94-331">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-333">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="8ef94-333">The current statuses of the object.</span></span> <span data-ttu-id="8ef94-334">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ef94-334">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-335">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="8ef94-335">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-336">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8ef94-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-338">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="8ef94-338">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="8ef94-339">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="8ef94-339">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="8ef94-340">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8ef94-340">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="8ef94-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-342">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8ef94-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-344">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="8ef94-344">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="8ef94-345">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="8ef94-345">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-346">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="8ef94-346">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-347">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8ef94-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-349">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="8ef94-349">The power management capabilities of the device.</span></span> <span data-ttu-id="8ef94-350">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8ef94-350">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-351">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="8ef94-351">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-352">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8ef94-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-354">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="8ef94-354">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="8ef94-355">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8ef94-355">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-356">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="8ef94-356">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-357">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8ef94-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-359">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="8ef94-359">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="8ef94-360">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8ef94-360">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-361">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="8ef94-361">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-362">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ef94-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-364">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="8ef94-364">Provides high level status information.</span></span> <span data-ttu-id="8ef94-365">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="8ef94-365">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="8ef94-366">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8ef94-366">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8ef94-367">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ef94-367">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8ef94-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="8ef94-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-369"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="8ef94-369"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-370"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="8ef94-370"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-371"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="8ef94-371"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-372"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="8ef94-372"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-373"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8ef94-373"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8ef94-374">)</span><span class="sxs-lookup"><span data-stu-id="8ef94-374">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ef94-375">**протоколдескриптион**</span><span class="sxs-lookup"><span data-stu-id="8ef94-375">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-376">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8ef94-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-378">Строка, которая предоставляет дополнительные сведения, связанные с протоколом, поддерживаемым контроллером.</span><span class="sxs-lookup"><span data-stu-id="8ef94-378">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="8ef94-379">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="8ef94-379">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-380">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="8ef94-380">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-381">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ef94-381">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-383">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="8ef94-383">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="8ef94-384">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="8ef94-384">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>



| <span data-ttu-id="8ef94-385">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef94-385">Value</span></span>                                                                         | <span data-ttu-id="8ef94-386">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef94-386">Meaning</span></span>             |
|-------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="8ef94-387"><dt>26</dt></span><span class="sxs-lookup"><span data-stu-id="8ef94-387"><dt>26</dt></span></span> </dl> | <span data-ttu-id="8ef94-388">IEEE-488</span><span class="sxs-lookup"><span data-stu-id="8ef94-388">IEEE-488</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8ef94-389">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="8ef94-389">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-390">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ef94-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-391">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-392">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="8ef94-392">The last requested or desired state for the element.</span></span> <span data-ttu-id="8ef94-393">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="8ef94-393">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="8ef94-394">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="8ef94-394">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="8ef94-395">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8ef94-395">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="8ef94-396">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef94-396">Value</span></span>                                                                         | <span data-ttu-id="8ef94-397">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef94-397">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="8ef94-398"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="8ef94-398"><dt>12</dt></span></span> </dl> | <span data-ttu-id="8ef94-399">Не применимо</span><span class="sxs-lookup"><span data-stu-id="8ef94-399">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8ef94-400">**Безопасность**</span><span class="sxs-lookup"><span data-stu-id="8ef94-400">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-401">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ef94-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-403">Операционная безопасность контроллера.</span><span class="sxs-lookup"><span data-stu-id="8ef94-403">The operational security for the controller.</span></span> <span data-ttu-id="8ef94-404">Это свойство наследуется от [**CIM \_ сериалконтроллер**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="8ef94-404">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>



| <span data-ttu-id="8ef94-405">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef94-405">Value</span></span>                                                                        | <span data-ttu-id="8ef94-406">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef94-406">Meaning</span></span>         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <span data-ttu-id="8ef94-407"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8ef94-407"><dt>3</dt></span></span> </dl> | <span data-ttu-id="8ef94-408">Нет</span><span class="sxs-lookup"><span data-stu-id="8ef94-408">None</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8ef94-409">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="8ef94-409">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-410">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8ef94-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-411">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-412">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="8ef94-412">The current status of the object.</span></span> <span data-ttu-id="8ef94-413">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="8ef94-413">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-414">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="8ef94-414">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-415">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8ef94-415">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-417">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="8ef94-417">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="8ef94-418">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ef94-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-419">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8ef94-419">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-420">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ef94-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-422">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="8ef94-422">The current state of the logical device.</span></span> <span data-ttu-id="8ef94-423">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8ef94-423">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-424">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="8ef94-424">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-425">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8ef94-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-426">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-427">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="8ef94-427">The scoping system's creation class name.</span></span> <span data-ttu-id="8ef94-428">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8ef94-428">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-429">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8ef94-429">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-430">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8ef94-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-431">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-432">Уникальный идентификатор для области виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8ef94-432">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="8ef94-433">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8ef94-433">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-434">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="8ef94-434">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-435">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8ef94-435">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-436">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-437">Время последнего включения контроллера.</span><span class="sxs-lookup"><span data-stu-id="8ef94-437">The last time the controller was powered on.</span></span> <span data-ttu-id="8ef94-438">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="8ef94-438">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-439">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="8ef94-439">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-440">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8ef94-440">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-441">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-442">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="8ef94-442">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="8ef94-443">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="8ef94-443">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-444">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="8ef94-444">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-445">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8ef94-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-446">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-447">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="8ef94-447">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="8ef94-448">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8ef94-448">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ef94-449">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="8ef94-449">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ef94-450">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ef94-450">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ef94-451">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ef94-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ef94-452">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="8ef94-452">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="8ef94-453">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="8ef94-453">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ef94-454">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ef94-454">Remarks</span></span>

<span data-ttu-id="8ef94-455">Доступ к классу **\_ сериалконтроллер мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="8ef94-455">Access to the **Msvm\_SerialController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8ef94-456">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8ef94-456">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ef94-457">Требования</span><span class="sxs-lookup"><span data-stu-id="8ef94-457">Requirements</span></span>



| <span data-ttu-id="8ef94-458">Требование</span><span class="sxs-lookup"><span data-stu-id="8ef94-458">Requirement</span></span> | <span data-ttu-id="8ef94-459">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef94-459">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef94-460">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ef94-460">Minimum supported client</span></span><br/> | <span data-ttu-id="8ef94-461">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8ef94-461">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8ef94-462">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ef94-462">Minimum supported server</span></span><br/> | <span data-ttu-id="8ef94-463">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8ef94-463">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8ef94-464">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8ef94-464">Namespace</span></span><br/>                | <span data-ttu-id="8ef94-465">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="8ef94-465">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8ef94-466">MOF</span><span class="sxs-lookup"><span data-stu-id="8ef94-466">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ef94-467"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ef94-467"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ef94-468">DLL</span><span class="sxs-lookup"><span data-stu-id="8ef94-468">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ef94-469"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8ef94-469"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8ef94-470">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ef94-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ef94-471">**\_СЕРИАЛКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="8ef94-471">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dt>

[<span data-ttu-id="8ef94-472">**\_СЕРИАЛКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="8ef94-472">**CIM\_SerialController**</span></span>](/windows/desktop/CIMWin32Prov/cim-serialcontroller)
</dt> <dt>

[<span data-ttu-id="8ef94-473">Классы последовательных устройств</span><span class="sxs-lookup"><span data-stu-id="8ef94-473">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 


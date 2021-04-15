---
description: Представляет контроллер IDE.
ms.assetid: DFD4D90E-CA91-42B3-AC88-9E9D26089C36
title: Класс Msvm_IDEController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_IDEController
- Msvm_IDEController.SetPowerState
- Msvm_IDEController.EnableDevice
- Msvm_IDEController.OnlineDevice
- Msvm_IDEController.QuiesceDevice
- Msvm_IDEController.SaveProperties
- Msvm_IDEController.RestoreProperties
- Msvm_IDEController.InstanceID
- Msvm_IDEController.Caption
- Msvm_IDEController.Description
- Msvm_IDEController.ElementName
- Msvm_IDEController.InstallDate
- Msvm_IDEController.Name
- Msvm_IDEController.OperationalStatus
- Msvm_IDEController.StatusDescriptions
- Msvm_IDEController.Status
- Msvm_IDEController.HealthState
- Msvm_IDEController.CommunicationStatus
- Msvm_IDEController.DetailedStatus
- Msvm_IDEController.OperatingStatus
- Msvm_IDEController.PrimaryStatus
- Msvm_IDEController.EnabledState
- Msvm_IDEController.OtherEnabledState
- Msvm_IDEController.RequestedState
- Msvm_IDEController.EnabledDefault
- Msvm_IDEController.TimeOfLastStateChange
- Msvm_IDEController.AvailableRequestedStates
- Msvm_IDEController.TransitioningToState
- Msvm_IDEController.SystemCreationClassName
- Msvm_IDEController.SystemName
- Msvm_IDEController.CreationClassName
- Msvm_IDEController.DeviceID
- Msvm_IDEController.PowerManagementSupported
- Msvm_IDEController.PowerManagementCapabilities
- Msvm_IDEController.Availability
- Msvm_IDEController.StatusInfo
- Msvm_IDEController.LastErrorCode
- Msvm_IDEController.ErrorDescription
- Msvm_IDEController.ErrorCleared
- Msvm_IDEController.OtherIdentifyingInfo
- Msvm_IDEController.PowerOnHours
- Msvm_IDEController.TotalPowerOnHours
- Msvm_IDEController.IdentifyingDescriptions
- Msvm_IDEController.AdditionalAvailability
- Msvm_IDEController.MaxQuiesceTime
- Msvm_IDEController.TimeOfLastReset
- Msvm_IDEController.ProtocolSupported
- Msvm_IDEController.MaxNumberControlled
- Msvm_IDEController.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 25da1bddfa029ca5a6892006283e322d91a328a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682849"
---
# <a name="msvm_idecontroller-class"></a><span data-ttu-id="8bf37-103">\_Класс мсвм идеконтроллер</span><span class="sxs-lookup"><span data-stu-id="8bf37-103">Msvm\_IDEController class</span></span>

<span data-ttu-id="8bf37-104">Представляет контроллер IDE.</span><span class="sxs-lookup"><span data-stu-id="8bf37-104">Represents an IDE controller.</span></span> <span data-ttu-id="8bf37-105">Этот класс может поддерживать до четырех дисков, подключенных к контроллеру.</span><span class="sxs-lookup"><span data-stu-id="8bf37-105">This class can support up to four drives attached to the controller.</span></span> <span data-ttu-id="8bf37-106">Контроллер IDE зафиксирован на виртуальной машине и поэтому не имеет связанного с ним пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8bf37-106">The IDE controller is fixed in the virtual machine and therefore does not have a resource pool associated with it.</span></span>

> [!Note]  
> <span data-ttu-id="8bf37-107">Этот класс недоступен для виртуальных машин поколения 2.</span><span class="sxs-lookup"><span data-stu-id="8bf37-107">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="8bf37-108">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="8bf37-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf37-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bf37-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_IDEController : CIM_IDEController
{
  string   InstanceID;
  string   Caption;
  string   Description = "Microsoft Virtual IDE Controller";
  string   ElementName;
  datetime InstallDate;
  string   Name;
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
  string   CreationClassName = "Msvm_IDEController";
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
  uint16   ProtocolSupported = 37;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription = "IDE";
};
```

## <a name="members"></a><span data-ttu-id="8bf37-110">Члены</span><span class="sxs-lookup"><span data-stu-id="8bf37-110">Members</span></span>

<span data-ttu-id="8bf37-111">Класс **мсвм \_ идеконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8bf37-111">The **Msvm\_IDEController** class has these types of members:</span></span>

-   [<span data-ttu-id="8bf37-112">Методы</span><span class="sxs-lookup"><span data-stu-id="8bf37-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="8bf37-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="8bf37-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8bf37-114">Методы</span><span class="sxs-lookup"><span data-stu-id="8bf37-114">Methods</span></span>

<span data-ttu-id="8bf37-115">Класс **мсвм \_ идеконтроллер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8bf37-115">The **Msvm\_IDEController** class has these methods.</span></span>



| <span data-ttu-id="8bf37-116">Метод</span><span class="sxs-lookup"><span data-stu-id="8bf37-116">Method</span></span>                                                              | <span data-ttu-id="8bf37-117">Описание</span><span class="sxs-lookup"><span data-stu-id="8bf37-117">Description</span></span>                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="8bf37-118">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="8bf37-118">**EnableDevice**</span></span>                                                    | <span data-ttu-id="8bf37-119">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8bf37-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8bf37-120">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="8bf37-120">**OnlineDevice**</span></span>                                                    | <span data-ttu-id="8bf37-121">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8bf37-121">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8bf37-122">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="8bf37-122">**QuiesceDevice**</span></span>                                                   | <span data-ttu-id="8bf37-123">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8bf37-123">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="8bf37-124">**Равен**</span><span class="sxs-lookup"><span data-stu-id="8bf37-124">**RequestStateChange**</span></span>](msvm-idecontroller-requeststatechange.md) | <span data-ttu-id="8bf37-125">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="8bf37-125">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="8bf37-126">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="8bf37-126">**Reset**</span></span>](msvm-idecontroller-reset.md)                           | <span data-ttu-id="8bf37-127">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="8bf37-127">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="8bf37-128">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="8bf37-128">**RestoreProperties**</span></span>                                               | <span data-ttu-id="8bf37-129">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8bf37-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8bf37-130">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="8bf37-130">**SaveProperties**</span></span>                                                  | <span data-ttu-id="8bf37-131">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8bf37-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8bf37-132">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8bf37-132">**SetPowerState**</span></span>                                                   | <span data-ttu-id="8bf37-133">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8bf37-133">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8bf37-134">Свойства</span><span class="sxs-lookup"><span data-stu-id="8bf37-134">Properties</span></span>

<span data-ttu-id="8bf37-135">Класс **мсвм \_ идеконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8bf37-135">The **Msvm\_IDEController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8bf37-136">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="8bf37-136">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-137">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8bf37-137">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-139">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="8bf37-139">Any additional availability and status of the device.</span></span> <span data-ttu-id="8bf37-140">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8bf37-140">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-141">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="8bf37-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-142">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf37-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-144">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="8bf37-144">The primary availability and status of the device.</span></span> <span data-ttu-id="8bf37-145">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8bf37-145">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-146">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="8bf37-146">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-147">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8bf37-147">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-149">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="8bf37-149">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="8bf37-150">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния объекта [**\_ енабледлогикалелемент CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8bf37-150">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="8bf37-151">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="8bf37-151">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="8bf37-152">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="8bf37-152">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="8bf37-153">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8bf37-153">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-154">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="8bf37-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf37-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-157">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8bf37-157">A short description of the object.</span></span> <span data-ttu-id="8bf37-158">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8bf37-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>



| <span data-ttu-id="8bf37-159">Значение</span><span class="sxs-lookup"><span data-stu-id="8bf37-159">Value</span></span>                                                                                         | <span data-ttu-id="8bf37-160">Значение</span><span class="sxs-lookup"><span data-stu-id="8bf37-160">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="8bf37-161"><dt>"IDE Controller 0"</dt></span><span class="sxs-lookup"><span data-stu-id="8bf37-161"><dt>"IDE Controller 0"</dt></span></span> </dl> | <span data-ttu-id="8bf37-162">Экземпляр представляет основной контроллер.</span><span class="sxs-lookup"><span data-stu-id="8bf37-162">The instance represents the primary controller.</span></span><br/>   |
| <dl> <span data-ttu-id="8bf37-163"><dt>"IDE Controller 1"</dt></span><span class="sxs-lookup"><span data-stu-id="8bf37-163"><dt>"IDE Controller 1"</dt></span></span> </dl> | <span data-ttu-id="8bf37-164">Экземпляр представляет вторичный контроллер.</span><span class="sxs-lookup"><span data-stu-id="8bf37-164">The instance represents the secondary controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8bf37-165">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="8bf37-165">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-166">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf37-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-168">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="8bf37-168">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8bf37-169">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8bf37-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8bf37-170">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf37-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8bf37-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf37-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-174">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8bf37-174">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8bf37-175">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8bf37-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-176">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8bf37-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf37-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-179">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8bf37-179">A description of the object.</span></span> <span data-ttu-id="8bf37-180">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8bf37-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8bf37-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-182">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf37-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-184">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="8bf37-184">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8bf37-185">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8bf37-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8bf37-186">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf37-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-187">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8bf37-187">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-188">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf37-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-190">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение «Microsoft:*GUID* \\ *устройства-данные*».</span><span class="sxs-lookup"><span data-stu-id="8bf37-190">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-191">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8bf37-191">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf37-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-194">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="8bf37-194">A display name for the object.</span></span> <span data-ttu-id="8bf37-195">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8bf37-195">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>



| <span data-ttu-id="8bf37-196">Значение</span><span class="sxs-lookup"><span data-stu-id="8bf37-196">Value</span></span>                                                                                         | <span data-ttu-id="8bf37-197">Значение</span><span class="sxs-lookup"><span data-stu-id="8bf37-197">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="8bf37-198"><dt>"IDE Controller 0"</dt></span><span class="sxs-lookup"><span data-stu-id="8bf37-198"><dt>"IDE Controller 0"</dt></span></span> </dl> | <span data-ttu-id="8bf37-199">Экземпляр представляет основной контроллер.</span><span class="sxs-lookup"><span data-stu-id="8bf37-199">The instance represents the primary controller.</span></span><br/>   |
| <dl> <span data-ttu-id="8bf37-200"><dt>"IDE Controller 1"</dt></span><span class="sxs-lookup"><span data-stu-id="8bf37-200"><dt>"IDE Controller 1"</dt></span></span> </dl> | <span data-ttu-id="8bf37-201">Экземпляр представляет вторичный контроллер.</span><span class="sxs-lookup"><span data-stu-id="8bf37-201">The instance represents the secondary controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8bf37-202">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="8bf37-202">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-203">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf37-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-205">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="8bf37-205">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="8bf37-206">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8bf37-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-207">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8bf37-207">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-208">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf37-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-210">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="8bf37-210">The enabled and disabled states of an element.</span></span> <span data-ttu-id="8bf37-211">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="8bf37-211">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="8bf37-212">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8bf37-212">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-213">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="8bf37-213">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-214">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8bf37-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-216">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="8bf37-216">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="8bf37-217">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8bf37-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-218">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8bf37-218">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf37-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-221">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="8bf37-221">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="8bf37-222">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8bf37-222">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-223">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8bf37-223">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-224">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf37-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-226">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="8bf37-226">The current health of the element.</span></span> <span data-ttu-id="8bf37-227">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="8bf37-227">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="8bf37-228">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="8bf37-228">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="8bf37-229">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf37-229">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-230">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8bf37-230">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-231">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8bf37-231">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-233">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="8bf37-233">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="8bf37-234">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8bf37-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-235">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8bf37-235">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-236">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8bf37-236">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-238">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8bf37-238">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="8bf37-239">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf37-239">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-240">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8bf37-240">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-241">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf37-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-243">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="8bf37-243">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-244">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="8bf37-244">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8bf37-245">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8bf37-245">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-246">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="8bf37-246">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-247">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8bf37-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-249">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="8bf37-249">The last error code reported by the logical device.</span></span> <span data-ttu-id="8bf37-250">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8bf37-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-251">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="8bf37-251">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-252">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8bf37-252">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-254">Максимальное количество напрямую доступных для адресации сущностей, поддерживаемых этим контроллером.</span><span class="sxs-lookup"><span data-stu-id="8bf37-254">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="8bf37-255">Если число неизвестно или неограниченно, следует использовать значение 0.</span><span class="sxs-lookup"><span data-stu-id="8bf37-255">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="8bf37-256">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="8bf37-256">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="8bf37-257">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="8bf37-257">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-258">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="8bf37-258">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-259">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8bf37-259">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-261">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="8bf37-261">This property has been deprecated.</span></span> <span data-ttu-id="8bf37-262">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8bf37-262">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-263">**Name**</span><span class="sxs-lookup"><span data-stu-id="8bf37-263">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf37-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-266">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="8bf37-266">The label by which the object is known.</span></span> <span data-ttu-id="8bf37-267">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и совпадает со свойством **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="8bf37-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-268">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="8bf37-268">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-269">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf37-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-271">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="8bf37-271">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8bf37-272">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8bf37-272">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8bf37-273">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf37-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-274">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8bf37-274">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-275">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8bf37-275">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-277">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="8bf37-277">The current statuses of the object.</span></span> <span data-ttu-id="8bf37-278">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf37-278">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-279">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="8bf37-279">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-280">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf37-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-282">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="8bf37-282">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="8bf37-283">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="8bf37-283">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="8bf37-284">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8bf37-284">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-285">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="8bf37-285">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-286">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8bf37-286">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-288">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="8bf37-288">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="8bf37-289">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="8bf37-289">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-290">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="8bf37-290">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-291">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8bf37-291">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-293">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="8bf37-293">The power management capabilities of the device.</span></span> <span data-ttu-id="8bf37-294">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8bf37-294">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-295">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="8bf37-295">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-296">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8bf37-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-298">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="8bf37-298">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="8bf37-299">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8bf37-299">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-300">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="8bf37-300">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-301">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8bf37-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-303">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="8bf37-303">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="8bf37-304">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8bf37-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-305">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="8bf37-305">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-306">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf37-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-308">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="8bf37-308">Provides high level status information.</span></span> <span data-ttu-id="8bf37-309">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="8bf37-309">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="8bf37-310">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8bf37-310">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8bf37-311">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf37-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-312">**протоколдескриптион**</span><span class="sxs-lookup"><span data-stu-id="8bf37-312">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-313">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf37-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-315">Строка, которая предоставляет дополнительные сведения, связанные с протоколом, поддерживаемым контроллером.</span><span class="sxs-lookup"><span data-stu-id="8bf37-315">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="8bf37-316">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="8bf37-316">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-317">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="8bf37-317">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-318">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf37-318">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-320">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="8bf37-320">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="8bf37-321">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="8bf37-321">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>



| <span data-ttu-id="8bf37-322">Значение</span><span class="sxs-lookup"><span data-stu-id="8bf37-322">Value</span></span>                                                                         | <span data-ttu-id="8bf37-323">Значение</span><span class="sxs-lookup"><span data-stu-id="8bf37-323">Meaning</span></span>        |
|-------------------------------------------------------------------------------|----------------|
| <dl> <span data-ttu-id="8bf37-324"><dt>37</dt></span><span class="sxs-lookup"><span data-stu-id="8bf37-324"><dt>37</dt></span></span> </dl> | <span data-ttu-id="8bf37-325">IDE</span><span class="sxs-lookup"><span data-stu-id="8bf37-325">IDE</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8bf37-326">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="8bf37-326">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-327">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf37-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-329">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="8bf37-329">The last requested or desired state for the element.</span></span> <span data-ttu-id="8bf37-330">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="8bf37-330">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="8bf37-331">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="8bf37-331">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="8bf37-332">Конкретный экземпляр включенного логического элемента может не поддерживать **рекуестедстатечанже**.</span><span class="sxs-lookup"><span data-stu-id="8bf37-332">A particular instance of an enabled logical element might not support **RequestedStateChange**.</span></span> <span data-ttu-id="8bf37-333">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="8bf37-333">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="8bf37-334">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8bf37-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-335">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="8bf37-335">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-336">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf37-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-338">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="8bf37-338">The current status of the object.</span></span> <span data-ttu-id="8bf37-339">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="8bf37-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-340">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="8bf37-340">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-341">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8bf37-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-343">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="8bf37-343">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="8bf37-344">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8bf37-344">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-345">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8bf37-345">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-346">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf37-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-348">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="8bf37-348">The current state of the logical device.</span></span> <span data-ttu-id="8bf37-349">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8bf37-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-350">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="8bf37-350">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-351">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf37-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-353">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="8bf37-353">The scoping system's creation class name.</span></span> <span data-ttu-id="8bf37-354">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8bf37-354">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-355">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8bf37-355">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-356">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8bf37-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-358">Уникальный идентификатор для области виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8bf37-358">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="8bf37-359">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8bf37-359">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-360">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="8bf37-360">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-361">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8bf37-361">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-363">Время последнего включения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8bf37-363">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="8bf37-364">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="8bf37-364">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-365">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="8bf37-365">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-366">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8bf37-366">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-368">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="8bf37-368">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="8bf37-369">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8bf37-369">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-370">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="8bf37-370">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-371">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8bf37-371">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-373">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="8bf37-373">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="8bf37-374">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="8bf37-374">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8bf37-375">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="8bf37-375">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf37-376">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bf37-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bf37-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8bf37-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bf37-378">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="8bf37-378">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="8bf37-379">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="8bf37-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8bf37-380">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8bf37-380">Remarks</span></span>

<span data-ttu-id="8bf37-381">Доступ к классу **\_ идеконтроллер мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="8bf37-381">Access to the **Msvm\_IDEController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8bf37-382">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8bf37-382">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="8bf37-383">Требования</span><span class="sxs-lookup"><span data-stu-id="8bf37-383">Requirements</span></span>



| <span data-ttu-id="8bf37-384">Требование</span><span class="sxs-lookup"><span data-stu-id="8bf37-384">Requirement</span></span> | <span data-ttu-id="8bf37-385">Значение</span><span class="sxs-lookup"><span data-stu-id="8bf37-385">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf37-386">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8bf37-386">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf37-387">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8bf37-387">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8bf37-388">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8bf37-388">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf37-389">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8bf37-389">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8bf37-390">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8bf37-390">Namespace</span></span><br/>                | <span data-ttu-id="8bf37-391">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="8bf37-391">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8bf37-392">MOF</span><span class="sxs-lookup"><span data-stu-id="8bf37-392">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bf37-393"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bf37-393"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bf37-394">DLL</span><span class="sxs-lookup"><span data-stu-id="8bf37-394">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bf37-395"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8bf37-395"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8bf37-396">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8bf37-396">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf37-397">**\_ИДЕКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="8bf37-397">**CIM\_IDEController**</span></span>](cim-idecontroller.md)
</dt> <dt>

<span data-ttu-id="8bf37-398">[**\_ИДЕКОНТРОЛЛЕР CIM**](/previous-versions//cc136863(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8bf37-398">[**CIM\_IDEController**](/previous-versions//cc136863(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8bf37-399">Классы хранения</span><span class="sxs-lookup"><span data-stu-id="8bf37-399">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 


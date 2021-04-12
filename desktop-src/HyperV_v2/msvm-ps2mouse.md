---
description: Представляет устройство мыши PS2.
ms.assetid: 5e02ec15-95e6-4d82-833e-a48ca117a890
title: Класс Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse
- Msvm_Ps2Mouse.SetPowerState
- Msvm_Ps2Mouse.EnableDevice
- Msvm_Ps2Mouse.OnlineDevice
- Msvm_Ps2Mouse.QuiesceDevice
- Msvm_Ps2Mouse.SaveProperties
- Msvm_Ps2Mouse.RestoreProperties
- Msvm_Ps2Mouse.InstanceID
- Msvm_Ps2Mouse.Caption
- Msvm_Ps2Mouse.Description
- Msvm_Ps2Mouse.ElementName
- Msvm_Ps2Mouse.InstallDate
- Msvm_Ps2Mouse.Name
- Msvm_Ps2Mouse.OperationalStatus
- Msvm_Ps2Mouse.StatusDescriptions
- Msvm_Ps2Mouse.Status
- Msvm_Ps2Mouse.HealthState
- Msvm_Ps2Mouse.CommunicationStatus
- Msvm_Ps2Mouse.DetailedStatus
- Msvm_Ps2Mouse.OperatingStatus
- Msvm_Ps2Mouse.PrimaryStatus
- Msvm_Ps2Mouse.EnabledState
- Msvm_Ps2Mouse.OtherEnabledState
- Msvm_Ps2Mouse.RequestedState
- Msvm_Ps2Mouse.EnabledDefault
- Msvm_Ps2Mouse.TimeOfLastStateChange
- Msvm_Ps2Mouse.AvailableRequestedStates
- Msvm_Ps2Mouse.TransitioningToState
- Msvm_Ps2Mouse.SystemCreationClassName
- Msvm_Ps2Mouse.SystemName
- Msvm_Ps2Mouse.CreationClassName
- Msvm_Ps2Mouse.DeviceID
- Msvm_Ps2Mouse.PowerManagementSupported
- Msvm_Ps2Mouse.PowerManagementCapabilities
- Msvm_Ps2Mouse.Availability
- Msvm_Ps2Mouse.StatusInfo
- Msvm_Ps2Mouse.LastErrorCode
- Msvm_Ps2Mouse.ErrorDescription
- Msvm_Ps2Mouse.ErrorCleared
- Msvm_Ps2Mouse.OtherIdentifyingInfo
- Msvm_Ps2Mouse.PowerOnHours
- Msvm_Ps2Mouse.TotalPowerOnHours
- Msvm_Ps2Mouse.IdentifyingDescriptions
- Msvm_Ps2Mouse.AdditionalAvailability
- Msvm_Ps2Mouse.MaxQuiesceTime
- Msvm_Ps2Mouse.IsLocked
- Msvm_Ps2Mouse.PointingType
- Msvm_Ps2Mouse.NumberOfButtons
- Msvm_Ps2Mouse.Handedness
- Msvm_Ps2Mouse.Resolution
- Msvm_Ps2Mouse.AbsoluteCoordinates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d25d168b85a79c5212afc719ce6ec83ca9780395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345775"
---
# <a name="msvm_ps2mouse-class"></a><span data-ttu-id="7030c-103">\_Класс мсвм Ps2Mouse</span><span class="sxs-lookup"><span data-stu-id="7030c-103">Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="7030c-104">Представляет устройство мыши PS2.</span><span class="sxs-lookup"><span data-stu-id="7030c-104">Represents a PS2 mouse device.</span></span> <span data-ttu-id="7030c-105">Экземпляры этого класса — это логические устройства, которые всегда находятся на виртуальной машине и поэтому не распределяются через пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7030c-105">Instances of this class are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="7030c-106">Один экземпляр всегда содержится в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="7030c-106">One instance is always present in a virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="7030c-107">Этот класс недоступен для виртуальных машин поколения 2.</span><span class="sxs-lookup"><span data-stu-id="7030c-107">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="7030c-108">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7030c-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7030c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7030c-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Ps2Mouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Emulated Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_PS2Mouse";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = False;
};
```

## <a name="members"></a><span data-ttu-id="7030c-110">Члены</span><span class="sxs-lookup"><span data-stu-id="7030c-110">Members</span></span>

<span data-ttu-id="7030c-111">Класс **мсвм \_ Ps2Mouse** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7030c-111">The **Msvm\_Ps2Mouse** class has these types of members:</span></span>

-   [<span data-ttu-id="7030c-112">Методы</span><span class="sxs-lookup"><span data-stu-id="7030c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="7030c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="7030c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7030c-114">Методы</span><span class="sxs-lookup"><span data-stu-id="7030c-114">Methods</span></span>

<span data-ttu-id="7030c-115">Класс **мсвм \_ Ps2Mouse** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7030c-115">The **Msvm\_Ps2Mouse** class has these methods.</span></span>



| <span data-ttu-id="7030c-116">Метод</span><span class="sxs-lookup"><span data-stu-id="7030c-116">Method</span></span>                                                           | <span data-ttu-id="7030c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="7030c-117">Description</span></span>                                                                                           |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7030c-118">**кликкбуттон**</span><span class="sxs-lookup"><span data-stu-id="7030c-118">**ClickButton**</span></span>](clickbutton-msvm-ps2mouse.md)                 | <span data-ttu-id="7030c-119">Имитирует нажатие кнопки вниз на указанной кнопке устройства.</span><span class="sxs-lookup"><span data-stu-id="7030c-119">Simulates a button click, a down-up sequence, on the specified device button.</span></span><br/>              |
| <span data-ttu-id="7030c-120">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="7030c-120">**EnableDevice**</span></span>                                                 | <span data-ttu-id="7030c-121">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7030c-121">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="7030c-122">**жетбуттонстате**</span><span class="sxs-lookup"><span data-stu-id="7030c-122">**GetButtonState**</span></span>](getbuttonstate-msvm-ps2mouse.md)           | <span data-ttu-id="7030c-123">Извлекает текущее состояние указанной кнопки устройства.</span><span class="sxs-lookup"><span data-stu-id="7030c-123">Retrieves the current state of the specified device button.</span></span><br/>                                |
| <span data-ttu-id="7030c-124">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="7030c-124">**OnlineDevice**</span></span>                                                 | <span data-ttu-id="7030c-125">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7030c-125">This method is not supported.</span></span><br/>                                                              |
| <span data-ttu-id="7030c-126">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="7030c-126">**QuiesceDevice**</span></span>                                                | <span data-ttu-id="7030c-127">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7030c-127">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="7030c-128">**Равен**</span><span class="sxs-lookup"><span data-stu-id="7030c-128">**RequestStateChange**</span></span>](msvm-ps2mouse-requeststatechange.md)   | <span data-ttu-id="7030c-129">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="7030c-129">Requests a state change.</span></span><br/>                                                                   |
| [<span data-ttu-id="7030c-130">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="7030c-130">**Reset**</span></span>](msvm-ps2mouse-reset.md)                             | <span data-ttu-id="7030c-131">Выполняет сброс устройства.</span><span class="sxs-lookup"><span data-stu-id="7030c-131">Resets the device.</span></span><br/>                                                                         |
| <span data-ttu-id="7030c-132">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="7030c-132">**RestoreProperties**</span></span>                                            | <span data-ttu-id="7030c-133">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7030c-133">This method is not supported.</span></span><br/>                                                              |
| <span data-ttu-id="7030c-134">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="7030c-134">**SaveProperties**</span></span>                                               | <span data-ttu-id="7030c-135">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7030c-135">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="7030c-136">**сетбуттонстате**</span><span class="sxs-lookup"><span data-stu-id="7030c-136">**SetButtonState**</span></span>](setbuttonstate-msvm-ps2mouse.md)           | <span data-ttu-id="7030c-137">Задает текущее состояние указанной кнопки устройства.</span><span class="sxs-lookup"><span data-stu-id="7030c-137">Sets the current state of the specified device button.</span></span><br/>                                     |
| <span data-ttu-id="7030c-138">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7030c-138">**SetPowerState**</span></span>                                                | <span data-ttu-id="7030c-139">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7030c-139">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="7030c-140">**сетрелативепоситион**</span><span class="sxs-lookup"><span data-stu-id="7030c-140">**SetRelativePosition**</span></span>](setrelativeposition-msvm-ps2mouse.md) | <span data-ttu-id="7030c-141">Сдвигает указатель мыши на заданную горизонтальную и вертикальную разности.</span><span class="sxs-lookup"><span data-stu-id="7030c-141">Offsets the position of the mouse pointer by the specified horizontal and vertical deltas.</span></span><br/> |
| [<span data-ttu-id="7030c-142">**сетскроллпоситион**</span><span class="sxs-lookup"><span data-stu-id="7030c-142">**SetScrollPosition**</span></span>](setscrollposition-msvm-ps2mouse.md)     | <span data-ttu-id="7030c-143">Настраивает z-координату элемента управления "колесо" для указывающего устройства.</span><span class="sxs-lookup"><span data-stu-id="7030c-143">Adjusts the z-coordinate of the wheel control of the pointing device.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="7030c-144">Свойства</span><span class="sxs-lookup"><span data-stu-id="7030c-144">Properties</span></span>

<span data-ttu-id="7030c-145">Класс **мсвм \_ Ps2Mouse** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7030c-145">The **Msvm\_Ps2Mouse** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7030c-146">**абсолутекурдинатес**</span><span class="sxs-lookup"><span data-stu-id="7030c-146">**AbsoluteCoordinates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-147">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7030c-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-149">Указывает, работает ли устройство в абсолютных координатах.</span><span class="sxs-lookup"><span data-stu-id="7030c-149">Indicates whether the device operates on absolute coordinates.</span></span> <span data-ttu-id="7030c-150">Если значение не задано, координаты устройства являются относительными.</span><span class="sxs-lookup"><span data-stu-id="7030c-150">If not set, the device's coordinates are relative.</span></span>

</dd> <dt>

<span data-ttu-id="7030c-151">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="7030c-151">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-152">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="7030c-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7030c-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-154">Любая дополнительная доступность и состояние устройства, кроме указанного в свойстве **Availability** .</span><span class="sxs-lookup"><span data-stu-id="7030c-154">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="7030c-155">Свойство **Availability** указывает основное состояние и доступность устройства.</span><span class="sxs-lookup"><span data-stu-id="7030c-155">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="7030c-156">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7030c-156">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="7030c-157">Значение</span><span class="sxs-lookup"><span data-stu-id="7030c-157">Value</span></span>                                                                        | <span data-ttu-id="7030c-158">Значение</span><span class="sxs-lookup"><span data-stu-id="7030c-158">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="7030c-159"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7030c-159"><dt>6</dt></span></span> </dl> | <span data-ttu-id="7030c-160">Не применимо</span><span class="sxs-lookup"><span data-stu-id="7030c-160">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7030c-161">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="7030c-161">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-162">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7030c-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-164">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="7030c-164">The primary availability and status of the device.</span></span> <span data-ttu-id="7030c-165">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7030c-165">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="7030c-166">Значение</span><span class="sxs-lookup"><span data-stu-id="7030c-166">Value</span></span>                                                                        | <span data-ttu-id="7030c-167">Значение</span><span class="sxs-lookup"><span data-stu-id="7030c-167">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="7030c-168"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7030c-168"><dt>6</dt></span></span> </dl> | <span data-ttu-id="7030c-169">Не применимо</span><span class="sxs-lookup"><span data-stu-id="7030c-169">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7030c-170">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="7030c-170">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-171">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="7030c-171">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7030c-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-173">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="7030c-173">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="7030c-174">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="7030c-174">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7030c-175">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7030c-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7030c-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-178">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7030c-178">A short description of the object.</span></span> <span data-ttu-id="7030c-179">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7030c-179">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-180">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="7030c-180">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-181">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7030c-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-183">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="7030c-183">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="7030c-184">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="7030c-184">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7030c-185">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7030c-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7030c-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7030c-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="7030c-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-188"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="7030c-188"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-189"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="7030c-189"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-190"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="7030c-190"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-191"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="7030c-191"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-192"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7030c-192"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7030c-193">)</span><span class="sxs-lookup"><span data-stu-id="7030c-193">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7030c-194">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7030c-194">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7030c-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7030c-197">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="7030c-197">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="7030c-198">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7030c-198">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7030c-199">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="7030c-199">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="7030c-200">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7030c-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-201">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7030c-201">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7030c-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-204">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7030c-204">A description of the object.</span></span> <span data-ttu-id="7030c-205">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7030c-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-206">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="7030c-206">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-207">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7030c-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-209">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="7030c-209">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="7030c-210">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="7030c-210">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7030c-211">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7030c-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7030c-212"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="7030c-212"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-213"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="7030c-213"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-214"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="7030c-214"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-215"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="7030c-215"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-216"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="7030c-216"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-217"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="7030c-217"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="7030c-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-219"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7030c-219"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7030c-220">)</span><span class="sxs-lookup"><span data-stu-id="7030c-220">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7030c-221">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7030c-221">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7030c-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7030c-224">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="7030c-224">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="7030c-225">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7030c-225">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="7030c-226">Это свойство наследуется от [**CIM \_ ",**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)" и всегда имеет значение "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="7030c-226">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="7030c-227">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7030c-227">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-228">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7030c-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-230">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="7030c-230">A display name for the object.</span></span> <span data-ttu-id="7030c-231">Это свойство позволяет каждому экземпляру определить отображаемое имя в дополнение к его ключевым свойствам, идентификационным данным и сведениям о описании.</span><span class="sxs-lookup"><span data-stu-id="7030c-231">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="7030c-232">Свойство [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) класса **CIM \_ манажедсистемелемент** также определяется как отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="7030c-232">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="7030c-233">Но часто этот класс является ключом.</span><span class="sxs-lookup"><span data-stu-id="7030c-233">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="7030c-234">Не целесообразно, что одно и то же свойство может передать как удостоверение, так и отображаемое имя без несогласованности.</span><span class="sxs-lookup"><span data-stu-id="7030c-234">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="7030c-235">Если [**имя**](msvm-keyboard.md) существует и не является ключом (например, для экземпляров CIM- [**класса \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), то одни и те же сведения могут присутствовать как в свойствах **Name** , так и в **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="7030c-235">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="7030c-236">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Mouse".</span><span class="sxs-lookup"><span data-stu-id="7030c-236">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Mouse".</span></span>

</dd> <dt>

<span data-ttu-id="7030c-237">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="7030c-237">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-238">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7030c-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-240">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="7030c-240">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="7030c-241">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7030c-241">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-242">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="7030c-242">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-243">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7030c-243">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-245">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="7030c-245">The enabled and disabled states of an element.</span></span> <span data-ttu-id="7030c-246">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7030c-246">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-247">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="7030c-247">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-248">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7030c-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-250">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="7030c-250">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="7030c-251">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7030c-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7030c-252">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7030c-252">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-253">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7030c-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-255">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="7030c-255">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="7030c-256">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7030c-256">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7030c-257">**Правой или левой**</span><span class="sxs-lookup"><span data-stu-id="7030c-257">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-258">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7030c-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-260">Конфигурация указывающего устройства для правой или левой операции.</span><span class="sxs-lookup"><span data-stu-id="7030c-260">The configuration of the pointing device for right-hand or left-hand operation.</span></span> <span data-ttu-id="7030c-261">Это свойство наследуется от [**CIM \_ поинтингдевице**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="7030c-261">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="7030c-262">Значение</span><span class="sxs-lookup"><span data-stu-id="7030c-262">Value</span></span>                                                                        | <span data-ttu-id="7030c-263">Значение</span><span class="sxs-lookup"><span data-stu-id="7030c-263">Meaning</span></span>                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="7030c-264"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7030c-264"><dt>0</dt></span></span> </dl> | <span data-ttu-id="7030c-265">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="7030c-265">Unknown</span></span><br/>                 |
| <dl> <span data-ttu-id="7030c-266"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7030c-266"><dt>1</dt></span></span> </dl> | <span data-ttu-id="7030c-267">Не применяется</span><span class="sxs-lookup"><span data-stu-id="7030c-267">Not applicable.</span></span><br/>         |
| <dl> <span data-ttu-id="7030c-268"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7030c-268"><dt>2</dt></span></span> </dl> | <span data-ttu-id="7030c-269">Правая операция.</span><span class="sxs-lookup"><span data-stu-id="7030c-269">Right handed operation.</span></span><br/> |
| <dl> <span data-ttu-id="7030c-270"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7030c-270"><dt>3</dt></span></span> </dl> | <span data-ttu-id="7030c-271">Операция с левой стороны.</span><span class="sxs-lookup"><span data-stu-id="7030c-271">Left handed operation.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="7030c-272">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="7030c-272">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-273">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7030c-273">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-275">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="7030c-275">The current health of the element.</span></span> <span data-ttu-id="7030c-276">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="7030c-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK)</span></span>

</dd> <dt>

<span data-ttu-id="7030c-277">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7030c-277">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-278">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="7030c-278">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7030c-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-280">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве [**осеридентифингинфо**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="7030c-280">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="7030c-281">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7030c-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-282">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7030c-282">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-283">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7030c-283">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-285">Дата и время создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7030c-285">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="7030c-286">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7030c-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-287">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7030c-287">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7030c-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7030c-290">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="7030c-290">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7030c-291">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="7030c-291">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7030c-292">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7030c-292">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-293">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="7030c-293">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-294">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7030c-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-296">Указывает, заблокировано ли устройство, предотвращая ввод или вывод пользователя.</span><span class="sxs-lookup"><span data-stu-id="7030c-296">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="7030c-297">Это свойство наследуется от [**CIM \_ усердевице**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="7030c-297">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-298">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="7030c-298">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-299">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7030c-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-301">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="7030c-301">The last error code reported by the logical device.</span></span> <span data-ttu-id="7030c-302">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7030c-302">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7030c-303">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="7030c-303">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-304">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7030c-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-306">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="7030c-306">This property has been deprecated.</span></span> <span data-ttu-id="7030c-307">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7030c-307">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-308">**Name**</span><span class="sxs-lookup"><span data-stu-id="7030c-308">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-309">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7030c-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7030c-311">Квалификаторы: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="7030c-311">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="7030c-312">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="7030c-312">The label by which the object is known.</span></span> <span data-ttu-id="7030c-313">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="7030c-313">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="7030c-314">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7030c-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-315">**нумберофбуттонс**</span><span class="sxs-lookup"><span data-stu-id="7030c-315">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-316">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7030c-316">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-318">Количество кнопок на указывающем устройстве.</span><span class="sxs-lookup"><span data-stu-id="7030c-318">The number of buttons on the pointing device.</span></span> <span data-ttu-id="7030c-319">Это свойство наследуется от [**CIM \_ поинтингдевице**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="7030c-319">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-320">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="7030c-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-321">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7030c-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-323">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="7030c-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="7030c-324">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="7030c-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7030c-325">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7030c-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7030c-326"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7030c-326"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-327"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="7030c-327"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-328"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="7030c-328"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-329"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="7030c-329"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-330"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="7030c-330"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-331"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="7030c-331"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-332"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="7030c-332"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-333"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="7030c-333"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-334"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="7030c-334"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-335"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="7030c-335"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-336"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="7030c-336"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-337"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="7030c-337"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-338"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="7030c-338"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-339"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="7030c-339"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-340"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="7030c-340"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-341"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="7030c-341"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-342"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="7030c-342"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-343"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="7030c-343"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-344"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7030c-344"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7030c-345">)</span><span class="sxs-lookup"><span data-stu-id="7030c-345">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7030c-346">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="7030c-346">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-347">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="7030c-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7030c-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-349">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="7030c-349">The current status of the element.</span></span> <span data-ttu-id="7030c-350">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="7030c-350">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-351">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="7030c-351">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7030c-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-354">Состояние включения или отключения элемента, если свойство [**EnabledState**](msvm-keyboard.md) имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="7030c-354">The enabled or disabled state of the element when the [**EnabledState**](msvm-keyboard.md) property is set to 1 (Other).</span></span> <span data-ttu-id="7030c-355">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="7030c-355">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="7030c-356">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7030c-356">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-357">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="7030c-357">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-358">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="7030c-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7030c-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-360">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7030c-360">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="7030c-361">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7030c-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-362">**поинтингтипе**</span><span class="sxs-lookup"><span data-stu-id="7030c-362">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-363">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7030c-363">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-364">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-365">Тип указывающего устройства.</span><span class="sxs-lookup"><span data-stu-id="7030c-365">The type of the pointing device.</span></span> <span data-ttu-id="7030c-366">Это свойство наследуется от [**CIM \_ поинтингдевице**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="7030c-366">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="7030c-367">Значение</span><span class="sxs-lookup"><span data-stu-id="7030c-367">Value</span></span>                                                                        | <span data-ttu-id="7030c-368">Значение</span><span class="sxs-lookup"><span data-stu-id="7030c-368">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="7030c-369"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7030c-369"><dt>3</dt></span></span> </dl> | <span data-ttu-id="7030c-370">Мышь</span><span class="sxs-lookup"><span data-stu-id="7030c-370">Mouse</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7030c-371">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="7030c-371">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-372">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="7030c-372">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7030c-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-374">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="7030c-374">The power management capabilities of the device.</span></span> <span data-ttu-id="7030c-375">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7030c-375">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7030c-376">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="7030c-376">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-377">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7030c-377">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-378">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-379">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="7030c-379">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="7030c-380">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7030c-380">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7030c-381">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="7030c-381">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-382">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7030c-382">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-384">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="7030c-384">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="7030c-385">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7030c-385">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7030c-386">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="7030c-386">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-387">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7030c-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-389">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="7030c-389">Provides high level status information.</span></span> <span data-ttu-id="7030c-390">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="7030c-390">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="7030c-391">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="7030c-391">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7030c-392">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7030c-392">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7030c-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7030c-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-394"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="7030c-394"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-395"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="7030c-395"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-396"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="7030c-396"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-397"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="7030c-397"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7030c-398"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7030c-398"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7030c-399">)</span><span class="sxs-lookup"><span data-stu-id="7030c-399">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7030c-400">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="7030c-400">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-401">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7030c-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-403">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="7030c-403">The last requested or desired state for the element.</span></span> <span data-ttu-id="7030c-404">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7030c-404">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="7030c-405">Значение</span><span class="sxs-lookup"><span data-stu-id="7030c-405">Value</span></span>                                                                         | <span data-ttu-id="7030c-406">Значение</span><span class="sxs-lookup"><span data-stu-id="7030c-406">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="7030c-407"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="7030c-407"><dt>12</dt></span></span> </dl> | <span data-ttu-id="7030c-408">Не применяется</span><span class="sxs-lookup"><span data-stu-id="7030c-408">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7030c-409">**Решение**</span><span class="sxs-lookup"><span data-stu-id="7030c-409">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-410">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7030c-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-411">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-412">Разрешение отслежения указывающего устройства в счетчиках на дюйм.</span><span class="sxs-lookup"><span data-stu-id="7030c-412">The tracking resolution of the pointing device, in counts per inch.</span></span> <span data-ttu-id="7030c-413">Это свойство наследуется от [**CIM \_ поинтингдевице**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="7030c-413">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-414">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="7030c-414">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-415">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7030c-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-417">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="7030c-417">The current status of the object.</span></span> <span data-ttu-id="7030c-418">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="7030c-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7030c-419">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="7030c-419">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-420">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="7030c-420">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7030c-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-422">Строки, описывающие различные значения массива [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="7030c-422">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="7030c-423">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) и всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="7030c-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="7030c-424">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7030c-424">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-425">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7030c-425">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-426">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-427">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7030c-427">The current state of the logical device.</span></span> <span data-ttu-id="7030c-428">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7030c-428">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7030c-429">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="7030c-429">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-430">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7030c-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-431">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7030c-432">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="7030c-432">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="7030c-433">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="7030c-433">The scoping system's creation class name.</span></span> <span data-ttu-id="7030c-434">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7030c-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-435">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7030c-435">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-436">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7030c-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-437">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7030c-438">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="7030c-438">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="7030c-439">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="7030c-439">The scoping system's name.</span></span> <span data-ttu-id="7030c-440">Это значение соответствует значению свойства [**Name**](msvm-computersystem.md) класса **мсвм \_ ComputerSystem** для виртуальной машины с областями.</span><span class="sxs-lookup"><span data-stu-id="7030c-440">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="7030c-441">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7030c-441">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-442">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="7030c-442">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-443">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7030c-443">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-444">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-445">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="7030c-445">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="7030c-446">Если состояние элемента не изменилось и заполнено это свойство, то для него должно быть задано нулевое значение интервала.</span><span class="sxs-lookup"><span data-stu-id="7030c-446">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="7030c-447">Если изменение состояния было запрошено, но отклонено или еще не обработано, свойство не должно обновляться.</span><span class="sxs-lookup"><span data-stu-id="7030c-447">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="7030c-448">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7030c-448">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7030c-449">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="7030c-449">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-450">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7030c-450">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-451">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-452">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="7030c-452">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="7030c-453">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7030c-453">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7030c-454">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="7030c-454">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7030c-455">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7030c-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7030c-456">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7030c-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7030c-457">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="7030c-457">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="7030c-458">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="7030c-458">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7030c-459">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7030c-459">Remarks</span></span>

<span data-ttu-id="7030c-460">Доступ к классу **\_ Ps2Mouse мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="7030c-460">Access to the **Msvm\_Ps2Mouse** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7030c-461">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7030c-461">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7030c-462">Требования</span><span class="sxs-lookup"><span data-stu-id="7030c-462">Requirements</span></span>



| <span data-ttu-id="7030c-463">Требование</span><span class="sxs-lookup"><span data-stu-id="7030c-463">Requirement</span></span> | <span data-ttu-id="7030c-464">Значение</span><span class="sxs-lookup"><span data-stu-id="7030c-464">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7030c-465">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7030c-465">Minimum supported client</span></span><br/> | <span data-ttu-id="7030c-466">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7030c-466">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7030c-467">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7030c-467">Minimum supported server</span></span><br/> | <span data-ttu-id="7030c-468">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7030c-468">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7030c-469">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7030c-469">Namespace</span></span><br/>                | <span data-ttu-id="7030c-470">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7030c-470">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7030c-471">MOF</span><span class="sxs-lookup"><span data-stu-id="7030c-471">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7030c-472"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7030c-472"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7030c-473">DLL</span><span class="sxs-lookup"><span data-stu-id="7030c-473">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7030c-474"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7030c-474"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7030c-475">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7030c-475">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7030c-476">**\_ПОИНТИНГДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="7030c-476">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="7030c-477">**\_ПОИНТИНГДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="7030c-477">**CIM\_PointingDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[<span data-ttu-id="7030c-478">Входные классы</span><span class="sxs-lookup"><span data-stu-id="7030c-478">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 


---
description: Представляет устройство искусственного мыши.
ms.assetid: c04b7aa1-44fe-41f5-943f-ff49ce64be96
title: Класс Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse
- Msvm_SyntheticMouse.SetPowerState
- Msvm_SyntheticMouse.EnableDevice
- Msvm_SyntheticMouse.OnlineDevice
- Msvm_SyntheticMouse.QuiesceDevice
- Msvm_SyntheticMouse.SaveProperties
- Msvm_SyntheticMouse.RestoreProperties
- Msvm_SyntheticMouse.InstanceID
- Msvm_SyntheticMouse.Caption
- Msvm_SyntheticMouse.Description
- Msvm_SyntheticMouse.ElementName
- Msvm_SyntheticMouse.InstallDate
- Msvm_SyntheticMouse.Name
- Msvm_SyntheticMouse.OperationalStatus
- Msvm_SyntheticMouse.StatusDescriptions
- Msvm_SyntheticMouse.Status
- Msvm_SyntheticMouse.HealthState
- Msvm_SyntheticMouse.CommunicationStatus
- Msvm_SyntheticMouse.DetailedStatus
- Msvm_SyntheticMouse.OperatingStatus
- Msvm_SyntheticMouse.PrimaryStatus
- Msvm_SyntheticMouse.EnabledState
- Msvm_SyntheticMouse.OtherEnabledState
- Msvm_SyntheticMouse.RequestedState
- Msvm_SyntheticMouse.EnabledDefault
- Msvm_SyntheticMouse.TimeOfLastStateChange
- Msvm_SyntheticMouse.AvailableRequestedStates
- Msvm_SyntheticMouse.TransitioningToState
- Msvm_SyntheticMouse.SystemCreationClassName
- Msvm_SyntheticMouse.SystemName
- Msvm_SyntheticMouse.CreationClassName
- Msvm_SyntheticMouse.DeviceID
- Msvm_SyntheticMouse.PowerManagementSupported
- Msvm_SyntheticMouse.PowerManagementCapabilities
- Msvm_SyntheticMouse.Availability
- Msvm_SyntheticMouse.StatusInfo
- Msvm_SyntheticMouse.LastErrorCode
- Msvm_SyntheticMouse.ErrorDescription
- Msvm_SyntheticMouse.ErrorCleared
- Msvm_SyntheticMouse.OtherIdentifyingInfo
- Msvm_SyntheticMouse.PowerOnHours
- Msvm_SyntheticMouse.TotalPowerOnHours
- Msvm_SyntheticMouse.IdentifyingDescriptions
- Msvm_SyntheticMouse.AdditionalAvailability
- Msvm_SyntheticMouse.MaxQuiesceTime
- Msvm_SyntheticMouse.IsLocked
- Msvm_SyntheticMouse.PointingType
- Msvm_SyntheticMouse.NumberOfButtons
- Msvm_SyntheticMouse.Handedness
- Msvm_SyntheticMouse.Resolution
- Msvm_SyntheticMouse.AbsoluteCoordinates
- Msvm_SyntheticMouse.HorizontalPosition
- Msvm_SyntheticMouse.VerticalPosition
- Msvm_SyntheticMouse.ScrollPosition
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c5be44637c91ebd57867c5062eba6f9e57ee543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808795"
---
# <a name="msvm_syntheticmouse-class"></a><span data-ttu-id="98b88-103">\_Класс мсвм синсетикмаусе</span><span class="sxs-lookup"><span data-stu-id="98b88-103">Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="98b88-104">Представляет устройство искусственного мыши.</span><span class="sxs-lookup"><span data-stu-id="98b88-104">Represents a synthetic mouse device.</span></span>

<span data-ttu-id="98b88-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="98b88-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="98b88-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98b88-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticMouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Synthetic Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = {
                "OK"
              };
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
  string   CreationClassName = "Msvm_SyntheticMouse";
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
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = True;
  sint32   HorizontalPosition;
  sint32   VerticalPosition;
  sint32   ScrollPosition;
};
```

## <a name="members"></a><span data-ttu-id="98b88-107">Члены</span><span class="sxs-lookup"><span data-stu-id="98b88-107">Members</span></span>

<span data-ttu-id="98b88-108">Класс **мсвм \_ синсетикмаусе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="98b88-108">The **Msvm\_SyntheticMouse** class has these types of members:</span></span>

-   [<span data-ttu-id="98b88-109">Методы</span><span class="sxs-lookup"><span data-stu-id="98b88-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="98b88-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="98b88-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="98b88-111">Методы</span><span class="sxs-lookup"><span data-stu-id="98b88-111">Methods</span></span>

<span data-ttu-id="98b88-112">Класс **мсвм \_ синсетикмаусе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="98b88-112">The **Msvm\_SyntheticMouse** class has these methods.</span></span>



| <span data-ttu-id="98b88-113">Метод</span><span class="sxs-lookup"><span data-stu-id="98b88-113">Method</span></span>                                                                 | <span data-ttu-id="98b88-114">Описание</span><span class="sxs-lookup"><span data-stu-id="98b88-114">Description</span></span>                                                                   |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="98b88-115">**кликкбуттон**</span><span class="sxs-lookup"><span data-stu-id="98b88-115">**ClickButton**</span></span>](clickbutton-msvm-syntheticmouse.md)                 | <span data-ttu-id="98b88-116">Имитирует нажатие кнопки указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="98b88-116">Simulates a button click of the specified device button.</span></span><br/>           |
| <span data-ttu-id="98b88-117">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="98b88-117">**EnableDevice**</span></span>                                                       | <span data-ttu-id="98b88-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="98b88-118">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="98b88-119">**жетбуттонстате**</span><span class="sxs-lookup"><span data-stu-id="98b88-119">**GetButtonState**</span></span>](getbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="98b88-120">Извлекает текущее состояние указанной кнопки устройства.</span><span class="sxs-lookup"><span data-stu-id="98b88-120">Retrieves the current state of the specified device button.</span></span><br/>        |
| <span data-ttu-id="98b88-121">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="98b88-121">**OnlineDevice**</span></span>                                                       | <span data-ttu-id="98b88-122">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="98b88-122">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="98b88-123">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="98b88-123">**QuiesceDevice**</span></span>                                                      | <span data-ttu-id="98b88-124">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="98b88-124">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="98b88-125">**Равен**</span><span class="sxs-lookup"><span data-stu-id="98b88-125">**RequestStateChange**</span></span>](msvm-syntheticmouse-requeststatechange.md)   | <span data-ttu-id="98b88-126">Запрашивает изменение состояния</span><span class="sxs-lookup"><span data-stu-id="98b88-126">Requests a state change</span></span><br/>                                            |
| [<span data-ttu-id="98b88-127">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="98b88-127">**Reset**</span></span>](msvm-syntheticmouse-reset.md)                             | <span data-ttu-id="98b88-128">Выполняет сброс устройства.</span><span class="sxs-lookup"><span data-stu-id="98b88-128">Resets the device.</span></span><br/>                                                 |
| <span data-ttu-id="98b88-129">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="98b88-129">**RestoreProperties**</span></span>                                                  | <span data-ttu-id="98b88-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="98b88-130">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="98b88-131">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="98b88-131">**SaveProperties**</span></span>                                                     | <span data-ttu-id="98b88-132">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="98b88-132">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="98b88-133">**сетабсолутепоситион**</span><span class="sxs-lookup"><span data-stu-id="98b88-133">**SetAbsolutePosition**</span></span>](setabsoluteposition-msvm-syntheticmouse.md) | <span data-ttu-id="98b88-134">Задает горизонтальное и вертикальное расположение курсора мыши.</span><span class="sxs-lookup"><span data-stu-id="98b88-134">Sets the horizontal and vertical position of the mouse cursor.</span></span><br/>     |
| [<span data-ttu-id="98b88-135">**сетбуттонстате**</span><span class="sxs-lookup"><span data-stu-id="98b88-135">**SetButtonState**</span></span>](setbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="98b88-136">Задает текущее состояние указанной кнопки устройства.</span><span class="sxs-lookup"><span data-stu-id="98b88-136">Sets the current state of the specified device button.</span></span><br/>             |
| <span data-ttu-id="98b88-137">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="98b88-137">**SetPowerState**</span></span>                                                      | <span data-ttu-id="98b88-138">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="98b88-138">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="98b88-139">**сетскроллпоситион**</span><span class="sxs-lookup"><span data-stu-id="98b88-139">**SetScrollPosition**</span></span>](setscrollposition-msvm-syntheticmouse.md)     | <span data-ttu-id="98b88-140">Задает z-координату элемента управления "колесо" для указывающего устройства.</span><span class="sxs-lookup"><span data-stu-id="98b88-140">Sets the z-coordinate of the wheel control of the pointing device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="98b88-141">Свойства</span><span class="sxs-lookup"><span data-stu-id="98b88-141">Properties</span></span>

<span data-ttu-id="98b88-142">Класс **мсвм \_ синсетикмаусе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="98b88-142">The **Msvm\_SyntheticMouse** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98b88-143">**абсолутекурдинатес**</span><span class="sxs-lookup"><span data-stu-id="98b88-143">**AbsoluteCoordinates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-144">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="98b88-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-146">Указывает, работает ли устройство с абсолютными или относительными координатами.</span><span class="sxs-lookup"><span data-stu-id="98b88-146">Indicates whether the device operates on absolute or relative coordinates.</span></span>



| <span data-ttu-id="98b88-147">Значение</span><span class="sxs-lookup"><span data-stu-id="98b88-147">Value</span></span>                                                                                | <span data-ttu-id="98b88-148">Значение</span><span class="sxs-lookup"><span data-stu-id="98b88-148">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="98b88-149"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="98b88-149"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="98b88-150">Координаты устройства являются абсолютными.</span><span class="sxs-lookup"><span data-stu-id="98b88-150">The device's coordinates are absolute.</span></span><br/> |
| <dl> <span data-ttu-id="98b88-151"><dt>**Неверно**</dt></span><span class="sxs-lookup"><span data-stu-id="98b88-151"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="98b88-152">Координаты устройства являются относительными.</span><span class="sxs-lookup"><span data-stu-id="98b88-152">The device's coordinates are relative.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="98b88-153">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="98b88-153">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-154">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="98b88-154">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="98b88-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-156">Любая дополнительная доступность и состояние устройства, кроме указанного в свойстве **Availability** .</span><span class="sxs-lookup"><span data-stu-id="98b88-156">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="98b88-157">Свойство **Availability** указывает основное состояние и доступность устройства.</span><span class="sxs-lookup"><span data-stu-id="98b88-157">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="98b88-158">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="98b88-158">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="98b88-159">Значение</span><span class="sxs-lookup"><span data-stu-id="98b88-159">Value</span></span>                                                                          | <span data-ttu-id="98b88-160">Значение</span><span class="sxs-lookup"><span data-stu-id="98b88-160">Meaning</span></span>                   |
|--------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>{6}</dt> </dl> | <span data-ttu-id="98b88-161">Не применимо</span><span class="sxs-lookup"><span data-stu-id="98b88-161">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="98b88-162">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="98b88-162">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-163">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98b88-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-165">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="98b88-165">The primary availability and status of the device.</span></span> <span data-ttu-id="98b88-166">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="98b88-166">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="98b88-167">Значение</span><span class="sxs-lookup"><span data-stu-id="98b88-167">Value</span></span>                                                                        | <span data-ttu-id="98b88-168">Значение</span><span class="sxs-lookup"><span data-stu-id="98b88-168">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="98b88-169"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="98b88-169"><dt>6</dt></span></span> </dl> | <span data-ttu-id="98b88-170">Не применимо</span><span class="sxs-lookup"><span data-stu-id="98b88-170">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="98b88-171">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="98b88-171">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-172">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="98b88-172">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="98b88-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-174">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="98b88-174">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="98b88-175">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="98b88-175">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="98b88-176">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="98b88-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98b88-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-179">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="98b88-179">A short description of the object.</span></span> <span data-ttu-id="98b88-180">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="98b88-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-181">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="98b88-181">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-182">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98b88-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-184">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="98b88-184">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="98b88-185">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="98b88-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="98b88-186">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="98b88-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="98b88-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="98b88-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="98b88-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="98b88-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="98b88-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="98b88-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="98b88-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="98b88-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="98b88-194">)</span><span class="sxs-lookup"><span data-stu-id="98b88-194">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="98b88-195">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="98b88-195">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-196">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98b88-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98b88-198">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="98b88-198">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="98b88-199">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="98b88-199">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="98b88-200">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="98b88-200">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="98b88-201">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="98b88-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-202">**Описание**</span><span class="sxs-lookup"><span data-stu-id="98b88-202">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98b88-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-205">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="98b88-205">A description of the object.</span></span> <span data-ttu-id="98b88-206">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="98b88-206">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-207">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="98b88-207">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-208">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98b88-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-210">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="98b88-210">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="98b88-211">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="98b88-211">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="98b88-212">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="98b88-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="98b88-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="98b88-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="98b88-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="98b88-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="98b88-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="98b88-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="98b88-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="98b88-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="98b88-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="98b88-221">)</span><span class="sxs-lookup"><span data-stu-id="98b88-221">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="98b88-222">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="98b88-222">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98b88-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98b88-225">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="98b88-225">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="98b88-226">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="98b88-226">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="98b88-227">Это свойство наследуется от [**CIM \_ ",**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)" и всегда имеет значение "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="98b88-227">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="98b88-228">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="98b88-228">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-229">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98b88-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-231">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="98b88-231">A display name for the object.</span></span> <span data-ttu-id="98b88-232">Это свойство позволяет каждому экземпляру определить отображаемое имя в дополнение к его ключевым свойствам, идентификационным данным и сведениям о описании.</span><span class="sxs-lookup"><span data-stu-id="98b88-232">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="98b88-233">Свойство [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) класса **CIM \_ манажедсистемелемент** также определяется как отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="98b88-233">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="98b88-234">Но часто этот класс является ключом.</span><span class="sxs-lookup"><span data-stu-id="98b88-234">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="98b88-235">Не целесообразно, что одно и то же свойство может передать как удостоверение, так и отображаемое имя без несогласованности.</span><span class="sxs-lookup"><span data-stu-id="98b88-235">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="98b88-236">Если [**имя**](msvm-keyboard.md) существует и не является ключом (например, для экземпляров класса с ключом), то одни и те же данные могут присутствовать в свойствах **Name** и **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="98b88-236">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="98b88-237">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="98b88-237">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-238">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="98b88-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-239">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98b88-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-241">Конфигурация по умолчанию или запуск администратора для элемента **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="98b88-241">An administrator's default or startup configuration for the **EnabledState** of an element.</span></span> <span data-ttu-id="98b88-242">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="98b88-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-243">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="98b88-243">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-244">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98b88-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-246">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="98b88-246">The enabled and disabled states of an element.</span></span> <span data-ttu-id="98b88-247">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="98b88-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="98b88-248">Значение</span><span class="sxs-lookup"><span data-stu-id="98b88-248">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="98b88-249">Значение</span><span class="sxs-lookup"><span data-stu-id="98b88-249">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="98b88-250"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="98b88-250"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="98b88-251">Гостевая виртуальная машина поддерживает искусственную мышь.</span><span class="sxs-lookup"><span data-stu-id="98b88-251">The guest virtual machine supports a synthetic mouse.</span></span><br/>         |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="98b88-252"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="98b88-252"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="98b88-253">Гостевая виртуальная машина не поддерживает искусственную мышь.</span><span class="sxs-lookup"><span data-stu-id="98b88-253">The guest virtual machine does not support a synthetic mouse.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="98b88-254">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="98b88-254">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-255">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="98b88-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-257">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="98b88-257">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="98b88-258">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="98b88-258">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="98b88-259">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="98b88-259">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-260">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98b88-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-262">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="98b88-262">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="98b88-263">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="98b88-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="98b88-264">**Правой или левой**</span><span class="sxs-lookup"><span data-stu-id="98b88-264">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-265">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98b88-265">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-266">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-267">Конфигурация указывающего устройства для правой или левой операции.</span><span class="sxs-lookup"><span data-stu-id="98b88-267">The configuration of the pointing device for right-hand or left-hand operation.</span></span> <span data-ttu-id="98b88-268">Это свойство наследуется от [**CIM \_ поинтингдевице**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="98b88-268">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="98b88-269">Значение</span><span class="sxs-lookup"><span data-stu-id="98b88-269">Value</span></span>                                                                        | <span data-ttu-id="98b88-270">Значение</span><span class="sxs-lookup"><span data-stu-id="98b88-270">Meaning</span></span>                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="98b88-271"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="98b88-271"><dt>0</dt></span></span> </dl> | <span data-ttu-id="98b88-272">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="98b88-272">Unknown</span></span><br/>                 |
| <dl> <span data-ttu-id="98b88-273"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="98b88-273"><dt>1</dt></span></span> </dl> | <span data-ttu-id="98b88-274">Не применяется</span><span class="sxs-lookup"><span data-stu-id="98b88-274">Not applicable.</span></span><br/>         |
| <dl> <span data-ttu-id="98b88-275"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="98b88-275"><dt>2</dt></span></span> </dl> | <span data-ttu-id="98b88-276">Правая операция.</span><span class="sxs-lookup"><span data-stu-id="98b88-276">Right handed operation.</span></span><br/> |
| <dl> <span data-ttu-id="98b88-277"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="98b88-277"><dt>3</dt></span></span> </dl> | <span data-ttu-id="98b88-278">Операция с левой стороны.</span><span class="sxs-lookup"><span data-stu-id="98b88-278">Left handed operation.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="98b88-279">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="98b88-279">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-280">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98b88-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-282">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="98b88-282">The current health of the element.</span></span> <span data-ttu-id="98b88-283">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="98b88-283">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-284">**хоризонталпоситион**</span><span class="sxs-lookup"><span data-stu-id="98b88-284">**HorizontalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-285">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="98b88-285">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-287">Абсолютная координата x указывающего устройства.</span><span class="sxs-lookup"><span data-stu-id="98b88-287">The absolute x-coordinate of the pointing device.</span></span>

</dd> <dt>

<span data-ttu-id="98b88-288">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="98b88-288">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-289">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="98b88-289">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="98b88-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-291">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве [**осеридентифингинфо**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="98b88-291">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="98b88-292">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="98b88-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-293">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="98b88-293">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-294">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="98b88-294">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-296">Дата и время создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="98b88-296">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="98b88-297">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="98b88-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-298">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="98b88-298">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-299">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98b88-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98b88-301">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="98b88-301">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="98b88-302">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="98b88-302">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="98b88-303">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="98b88-303">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-304">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="98b88-304">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-305">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="98b88-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-307">Указывает, заблокировано ли устройство, предотвращая ввод или вывод пользователя.</span><span class="sxs-lookup"><span data-stu-id="98b88-307">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="98b88-308">Это свойство наследуется от [**CIM \_ усердевице**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="98b88-308">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-309">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="98b88-309">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-310">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98b88-310">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-312">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="98b88-312">The last error code reported by the logical device.</span></span> <span data-ttu-id="98b88-313">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="98b88-313">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="98b88-314">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="98b88-314">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-315">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="98b88-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-317">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="98b88-317">This property has been deprecated.</span></span> <span data-ttu-id="98b88-318">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="98b88-318">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-319">**Name**</span><span class="sxs-lookup"><span data-stu-id="98b88-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-320">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98b88-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98b88-322">Квалификаторы: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="98b88-322">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="98b88-323">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="98b88-323">The label by which the object is known.</span></span> <span data-ttu-id="98b88-324">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="98b88-324">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="98b88-325">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="98b88-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-326">**нумберофбуттонс**</span><span class="sxs-lookup"><span data-stu-id="98b88-326">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-327">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="98b88-327">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-329">Количество кнопок на указывающем устройстве.</span><span class="sxs-lookup"><span data-stu-id="98b88-329">The number of buttons on the pointing device.</span></span> <span data-ttu-id="98b88-330">Это свойство наследуется от [**CIM \_ поинтингдевице**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="98b88-330">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-331">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="98b88-331">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-332">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98b88-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-334">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="98b88-334">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="98b88-335">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="98b88-335">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="98b88-336">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="98b88-336">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="98b88-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="98b88-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="98b88-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="98b88-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="98b88-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="98b88-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="98b88-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="98b88-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="98b88-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="98b88-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="98b88-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="98b88-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="98b88-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="98b88-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="98b88-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="98b88-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="98b88-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="98b88-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="98b88-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="98b88-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="98b88-356">)</span><span class="sxs-lookup"><span data-stu-id="98b88-356">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="98b88-357">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="98b88-357">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-358">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="98b88-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="98b88-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-360">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="98b88-360">The current status of the element.</span></span> <span data-ttu-id="98b88-361">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="98b88-361">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-362">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="98b88-362">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-363">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98b88-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-364">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-365">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="98b88-365">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="98b88-366">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="98b88-366">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="98b88-367">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="98b88-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-368">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="98b88-368">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-369">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="98b88-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="98b88-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-371">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="98b88-371">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="98b88-372">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="98b88-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-373">**поинтингтипе**</span><span class="sxs-lookup"><span data-stu-id="98b88-373">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-374">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98b88-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-376">Тип указывающего устройства.</span><span class="sxs-lookup"><span data-stu-id="98b88-376">The type of pointing device.</span></span> <span data-ttu-id="98b88-377">Это свойство наследуется от [**CIM \_ поинтингдевице**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="98b88-377">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="98b88-378">Значение</span><span class="sxs-lookup"><span data-stu-id="98b88-378">Value</span></span>                                                                        | <span data-ttu-id="98b88-379">Значение</span><span class="sxs-lookup"><span data-stu-id="98b88-379">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="98b88-380"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="98b88-380"><dt>3</dt></span></span> </dl> | <span data-ttu-id="98b88-381">Мышь</span><span class="sxs-lookup"><span data-stu-id="98b88-381">Mouse</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="98b88-382">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="98b88-382">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-383">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="98b88-383">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="98b88-384">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-385">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="98b88-385">The power management capabilities of the device.</span></span> <span data-ttu-id="98b88-386">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="98b88-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="98b88-387">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="98b88-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-388">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="98b88-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-389">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-390">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="98b88-390">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="98b88-391">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="98b88-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="98b88-392">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="98b88-392">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-393">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="98b88-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-395">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="98b88-395">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="98b88-396">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="98b88-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="98b88-397">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="98b88-397">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-398">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98b88-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-400">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="98b88-400">Provides high level status information.</span></span> <span data-ttu-id="98b88-401">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="98b88-401">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="98b88-402">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="98b88-402">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="98b88-403">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="98b88-403">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="98b88-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="98b88-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-405"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="98b88-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="98b88-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="98b88-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="98b88-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="98b88-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="98b88-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="98b88-410">)</span><span class="sxs-lookup"><span data-stu-id="98b88-410">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="98b88-411">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="98b88-411">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-412">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98b88-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-414">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="98b88-414">The last requested or desired state for the element.</span></span> <span data-ttu-id="98b88-415">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="98b88-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="98b88-416">Значение</span><span class="sxs-lookup"><span data-stu-id="98b88-416">Value</span></span>                                                                         | <span data-ttu-id="98b88-417">Значение</span><span class="sxs-lookup"><span data-stu-id="98b88-417">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="98b88-418"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="98b88-418"><dt>12</dt></span></span> </dl> | <span data-ttu-id="98b88-419">Не применимо</span><span class="sxs-lookup"><span data-stu-id="98b88-419">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="98b88-420">**Решение**</span><span class="sxs-lookup"><span data-stu-id="98b88-420">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-421">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98b88-421">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-423">Разрешение отслежения указывающего устройства в счетчиках на дюйм.</span><span class="sxs-lookup"><span data-stu-id="98b88-423">The tracking resolution of the pointing device, in counts per inch.</span></span> <span data-ttu-id="98b88-424">Это свойство наследуется от [**CIM \_ поинтингдевице**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="98b88-424">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-425">**скроллпоситион**</span><span class="sxs-lookup"><span data-stu-id="98b88-425">**ScrollPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-426">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="98b88-426">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-427">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98b88-428">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("миккэйс")</span><span class="sxs-lookup"><span data-stu-id="98b88-428">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="98b88-429">Положение координаты z устройства мыши.</span><span class="sxs-lookup"><span data-stu-id="98b88-429">The z-coordinate position of the mouse device.</span></span>

</dd> <dt>

<span data-ttu-id="98b88-430">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="98b88-430">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-431">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98b88-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-432">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-433">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="98b88-433">The current status of the object.</span></span> <span data-ttu-id="98b88-434">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="98b88-434">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="98b88-435">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="98b88-435">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-436">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="98b88-436">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="98b88-437">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-438">Строки, описывающие различные значения массива [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="98b88-438">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="98b88-439">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="98b88-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-440">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="98b88-440">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-441">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98b88-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-442">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-443">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="98b88-443">The current state of the logical device.</span></span> <span data-ttu-id="98b88-444">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="98b88-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="98b88-445">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="98b88-445">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-446">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98b88-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-447">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98b88-448">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="98b88-448">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="98b88-449">Имя класса создания для системы области.</span><span class="sxs-lookup"><span data-stu-id="98b88-449">The creation class name of the scoping system.</span></span> <span data-ttu-id="98b88-450">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="98b88-450">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-451">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="98b88-451">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-452">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="98b88-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-453">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98b88-454">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="98b88-454">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="98b88-455">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="98b88-455">The name of the scoping system.</span></span> <span data-ttu-id="98b88-456">Это значение соответствует значению свойства [**Name**](msvm-computersystem.md) класса **мсвм \_ ComputerSystem** для виртуальной машины с областями.</span><span class="sxs-lookup"><span data-stu-id="98b88-456">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="98b88-457">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="98b88-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="98b88-458">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="98b88-458">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-459">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="98b88-459">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-460">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-461">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="98b88-461">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="98b88-462">Если состояние элемента не изменилось и заполнено это свойство, то для него должно быть задано нулевое значение интервала.</span><span class="sxs-lookup"><span data-stu-id="98b88-462">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="98b88-463">Если изменение состояния было запрошено, но отклонено или еще не обработано, свойство не должно обновляться.</span><span class="sxs-lookup"><span data-stu-id="98b88-463">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="98b88-464">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="98b88-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="98b88-465">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="98b88-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-466">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="98b88-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-467">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-468">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="98b88-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="98b88-469">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="98b88-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="98b88-470">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="98b88-470">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-471">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98b88-471">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-472">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-473">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="98b88-473">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="98b88-474">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="98b88-474">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="98b88-475">**вертикалпоситион**</span><span class="sxs-lookup"><span data-stu-id="98b88-475">**VerticalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b88-476">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="98b88-476">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="98b88-477">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b88-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b88-478">Абсолютная координата y указывающего устройства.</span><span class="sxs-lookup"><span data-stu-id="98b88-478">The absolute y-coordinate of the pointing device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98b88-479">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98b88-479">Remarks</span></span>

<span data-ttu-id="98b88-480">Доступ к классу **\_ синсетикмаусе мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="98b88-480">Access to the **Msvm\_SyntheticMouse** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="98b88-481">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="98b88-481">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="98b88-482">Требования</span><span class="sxs-lookup"><span data-stu-id="98b88-482">Requirements</span></span>



| <span data-ttu-id="98b88-483">Требование</span><span class="sxs-lookup"><span data-stu-id="98b88-483">Requirement</span></span> | <span data-ttu-id="98b88-484">Значение</span><span class="sxs-lookup"><span data-stu-id="98b88-484">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98b88-485">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98b88-485">Minimum supported client</span></span><br/> | <span data-ttu-id="98b88-486">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="98b88-486">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="98b88-487">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98b88-487">Minimum supported server</span></span><br/> | <span data-ttu-id="98b88-488">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="98b88-488">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="98b88-489">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="98b88-489">Namespace</span></span><br/>                | <span data-ttu-id="98b88-490">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="98b88-490">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="98b88-491">MOF</span><span class="sxs-lookup"><span data-stu-id="98b88-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98b88-492"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98b88-492"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="98b88-493">DLL</span><span class="sxs-lookup"><span data-stu-id="98b88-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98b88-494"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="98b88-494"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="98b88-495">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98b88-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98b88-496">**\_ПОИНТИНГДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="98b88-496">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="98b88-497">**\_ПОИНТИНГДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="98b88-497">**CIM\_PointingDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[<span data-ttu-id="98b88-498">Входные классы</span><span class="sxs-lookup"><span data-stu-id="98b88-498">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 


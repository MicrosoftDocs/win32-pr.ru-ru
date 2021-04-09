---
description: Представляет устройство клавиатуры.
ms.assetid: 2a59fe90-12e2-471c-b49e-dfb4f4a31e0c
title: Класс Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard
- Msvm_Keyboard.SetPowerState
- Msvm_Keyboard.EnableDevice
- Msvm_Keyboard.OnlineDevice
- Msvm_Keyboard.QuiesceDevice
- Msvm_Keyboard.SaveProperties
- Msvm_Keyboard.RestoreProperties
- Msvm_Keyboard.InstanceID
- Msvm_Keyboard.Caption
- Msvm_Keyboard.Description
- Msvm_Keyboard.ElementName
- Msvm_Keyboard.InstallDate
- Msvm_Keyboard.Name
- Msvm_Keyboard.OperationalStatus
- Msvm_Keyboard.StatusDescriptions
- Msvm_Keyboard.Status
- Msvm_Keyboard.HealthState
- Msvm_Keyboard.CommunicationStatus
- Msvm_Keyboard.DetailedStatus
- Msvm_Keyboard.OperatingStatus
- Msvm_Keyboard.PrimaryStatus
- Msvm_Keyboard.EnabledState
- Msvm_Keyboard.OtherEnabledState
- Msvm_Keyboard.RequestedState
- Msvm_Keyboard.EnabledDefault
- Msvm_Keyboard.TimeOfLastStateChange
- Msvm_Keyboard.AvailableRequestedStates
- Msvm_Keyboard.TransitioningToState
- Msvm_Keyboard.SystemCreationClassName
- Msvm_Keyboard.SystemName
- Msvm_Keyboard.CreationClassName
- Msvm_Keyboard.DeviceID
- Msvm_Keyboard.PowerManagementSupported
- Msvm_Keyboard.PowerManagementCapabilities
- Msvm_Keyboard.Availability
- Msvm_Keyboard.StatusInfo
- Msvm_Keyboard.LastErrorCode
- Msvm_Keyboard.ErrorDescription
- Msvm_Keyboard.ErrorCleared
- Msvm_Keyboard.OtherIdentifyingInfo
- Msvm_Keyboard.PowerOnHours
- Msvm_Keyboard.TotalPowerOnHours
- Msvm_Keyboard.IdentifyingDescriptions
- Msvm_Keyboard.AdditionalAvailability
- Msvm_Keyboard.MaxQuiesceTime
- Msvm_Keyboard.IsLocked
- Msvm_Keyboard.Layout
- Msvm_Keyboard.NumberOfFunctionKeys
- Msvm_Keyboard.Password
- Msvm_Keyboard.UnicodeSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37c4faceb9072c1851868eb23c031e715cb6e1c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080768"
---
# <a name="msvm_keyboard-class"></a><span data-ttu-id="872ec-103">\_Класс клавиатуры мсвм</span><span class="sxs-lookup"><span data-stu-id="872ec-103">Msvm\_Keyboard class</span></span>

<span data-ttu-id="872ec-104">Представляет устройство клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="872ec-104">Represents a keyboard device.</span></span> <span data-ttu-id="872ec-105">Клавиатуры — это логические устройства, которые всегда находятся на виртуальной машине и поэтому не распределяются через пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="872ec-105">Keyboards are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="872ec-106">Один экземпляр всегда имеется в системе виртуальных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="872ec-106">One instance is always present in a virtual computer system.</span></span>

<span data-ttu-id="872ec-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="872ec-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="872ec-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="872ec-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Keyboard : CIM_UserDevice
{
  string   InstanceID;
  string   Caption = "Keyboard";
  string   Description = "Microsoft Virtual Keyboard";
  string   ElementName = "Keyboard";
  datetime InstallDate;
  string   Name = "Keyboard";
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
  string   CreationClassName = "Msvm_Keyboard";
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
  boolean  IsLocked = False;
  string   Layout = "00000409";
  uint16   NumberOfFunctionKeys = 12;
  uint16   Password = 5;
  boolean  UnicodeSupported;
};
```

## <a name="members"></a><span data-ttu-id="872ec-109">Члены</span><span class="sxs-lookup"><span data-stu-id="872ec-109">Members</span></span>

<span data-ttu-id="872ec-110">Класс **\_ клавиатуры мсвм** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="872ec-110">The **Msvm\_Keyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="872ec-111">Методы</span><span class="sxs-lookup"><span data-stu-id="872ec-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="872ec-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="872ec-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="872ec-113">Методы</span><span class="sxs-lookup"><span data-stu-id="872ec-113">Methods</span></span>

<span data-ttu-id="872ec-114">Класс **\_ клавиатуры мсвм** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="872ec-114">The **Msvm\_Keyboard** class has these methods.</span></span>



| <span data-ttu-id="872ec-115">Метод</span><span class="sxs-lookup"><span data-stu-id="872ec-115">Method</span></span>                                                         | <span data-ttu-id="872ec-116">Описание</span><span class="sxs-lookup"><span data-stu-id="872ec-116">Description</span></span>                                                   |
|:---------------------------------------------------------------|:--------------------------------------------------------------|
| <span data-ttu-id="872ec-117">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="872ec-117">**EnableDevice**</span></span>                                               | <span data-ttu-id="872ec-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="872ec-118">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="872ec-119">**С нажатием клавиши**</span><span class="sxs-lookup"><span data-stu-id="872ec-119">**IsKeyPressed**</span></span>](iskeypressed-msvm-keyboard.md)             | <span data-ttu-id="872ec-120">Получает состояние ключа для ключа.</span><span class="sxs-lookup"><span data-stu-id="872ec-120">Retrieves the key state of a key.</span></span><br/>                  |
| <span data-ttu-id="872ec-121">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="872ec-121">**OnlineDevice**</span></span>                                               | <span data-ttu-id="872ec-122">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="872ec-122">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="872ec-123">**PressKey**</span><span class="sxs-lookup"><span data-stu-id="872ec-123">**PressKey**</span></span>](presskey-msvm-keyboard.md)                     | <span data-ttu-id="872ec-124">Имитирует нажатие клавиши.</span><span class="sxs-lookup"><span data-stu-id="872ec-124">Simulates a key press.</span></span><br/>                             |
| <span data-ttu-id="872ec-125">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="872ec-125">**QuiesceDevice**</span></span>                                              | <span data-ttu-id="872ec-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="872ec-126">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="872ec-127">**релеасекэй**</span><span class="sxs-lookup"><span data-stu-id="872ec-127">**ReleaseKey**</span></span>](releasekey-msvm-keyboard.md)                 | <span data-ttu-id="872ec-128">Имитирует основной выпуск.</span><span class="sxs-lookup"><span data-stu-id="872ec-128">Simulates a key release.</span></span><br/>                           |
| [<span data-ttu-id="872ec-129">**Равен**</span><span class="sxs-lookup"><span data-stu-id="872ec-129">**RequestStateChange**</span></span>](msvm-keyboard-requeststatechange.md) | <span data-ttu-id="872ec-130">Запрашивает изменение состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="872ec-130">Requests that the state of the element be changed.</span></span><br/> |
| [<span data-ttu-id="872ec-131">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="872ec-131">**Reset**</span></span>](msvm-keyboard-reset.md)                           | <span data-ttu-id="872ec-132">Сбрасывает виртуальную клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="872ec-132">Resets the virtual keyboard.</span></span><br/>                       |
| <span data-ttu-id="872ec-133">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="872ec-133">**RestoreProperties**</span></span>                                          | <span data-ttu-id="872ec-134">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="872ec-134">This method is not supported.</span></span><br/>                      |
| <span data-ttu-id="872ec-135">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="872ec-135">**SaveProperties**</span></span>                                             | <span data-ttu-id="872ec-136">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="872ec-136">This method is not supported.</span></span><br/>                      |
| <span data-ttu-id="872ec-137">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="872ec-137">**SetPowerState**</span></span>                                              | <span data-ttu-id="872ec-138">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="872ec-138">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="872ec-139">**типектрлалтдел**</span><span class="sxs-lookup"><span data-stu-id="872ec-139">**TypeCtrlAltDel**</span></span>](typectrlaltdel-msvm-keyboard.md)         | <span data-ttu-id="872ec-140">Имитирует сочетание клавиш Ctrl + Alt + Del.</span><span class="sxs-lookup"><span data-stu-id="872ec-140">Simulates a Ctrl+Alt+Del key sequence.</span></span><br/>             |
| [<span data-ttu-id="872ec-141">**типекэй**</span><span class="sxs-lookup"><span data-stu-id="872ec-141">**TypeKey**</span></span>](typekey-msvm-keyboard.md)                       | <span data-ttu-id="872ec-142">Имитирует последовательность клавиш для пресс-релизов.</span><span class="sxs-lookup"><span data-stu-id="872ec-142">Simulates a press-release key sequence.</span></span><br/>            |
| [<span data-ttu-id="872ec-143">**типесканкодес**</span><span class="sxs-lookup"><span data-stu-id="872ec-143">**TypeScancodes**</span></span>](msvm-keyboard-typescancodes.md)           | <span data-ttu-id="872ec-144">Имитирует последовательность ключей с помощью кодов сканирования.</span><span class="sxs-lookup"><span data-stu-id="872ec-144">Simulates a key sequence using scan codes.</span></span><br/>         |
| [<span data-ttu-id="872ec-145">**TypeText**</span><span class="sxs-lookup"><span data-stu-id="872ec-145">**TypeText**</span></span>](typetext-msvm-keyboard.md)                     | <span data-ttu-id="872ec-146">Имитирует ряд типизированных символов.</span><span class="sxs-lookup"><span data-stu-id="872ec-146">Simulates a series of typed characters.</span></span><br/>            |



 

### <a name="properties"></a><span data-ttu-id="872ec-147">Свойства</span><span class="sxs-lookup"><span data-stu-id="872ec-147">Properties</span></span>

<span data-ttu-id="872ec-148">Класс **\_ клавиатуры мсвм** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="872ec-148">The **Msvm\_Keyboard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="872ec-149">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="872ec-149">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-150">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="872ec-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="872ec-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-152">Любая дополнительная доступность и состояние устройства, кроме указанного в свойстве **Availability** .</span><span class="sxs-lookup"><span data-stu-id="872ec-152">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="872ec-153">Свойство **Availability** указывает основное состояние и доступность устройства.</span><span class="sxs-lookup"><span data-stu-id="872ec-153">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="872ec-154">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="872ec-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="872ec-155">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="872ec-155">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-156">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="872ec-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-158">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="872ec-158">The primary availability and status of the device.</span></span> <span data-ttu-id="872ec-159">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="872ec-159">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="872ec-160">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="872ec-160">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-161">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="872ec-161">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="872ec-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-163">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="872ec-163">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="872ec-164">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="872ec-164">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-165">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="872ec-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872ec-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872ec-168">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="872ec-168">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="872ec-169">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="872ec-169">A short description of the object.</span></span> <span data-ttu-id="872ec-170">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="872ec-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="872ec-171">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="872ec-171">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-172">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="872ec-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-174">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="872ec-174">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="872ec-175">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="872ec-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="872ec-176">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="872ec-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="872ec-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="872ec-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-178"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="872ec-178"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-179"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="872ec-179"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="872ec-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-181"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="872ec-181"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="872ec-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-183"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="872ec-183"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="872ec-184">)</span><span class="sxs-lookup"><span data-stu-id="872ec-184">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="872ec-185">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="872ec-185">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872ec-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872ec-188">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="872ec-188">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="872ec-189">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="872ec-189">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="872ec-190">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="872ec-190">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="872ec-191">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="872ec-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="872ec-192">**Описание**</span><span class="sxs-lookup"><span data-stu-id="872ec-192">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-193">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872ec-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-195">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="872ec-195">A description of the object.</span></span> <span data-ttu-id="872ec-196">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="872ec-196">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="872ec-197">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="872ec-197">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-198">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="872ec-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-200">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="872ec-200">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="872ec-201">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="872ec-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="872ec-202">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="872ec-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="872ec-203"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="872ec-203"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-204"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="872ec-204"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-205"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="872ec-205"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-206"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="872ec-206"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-207"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="872ec-207"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-208"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="872ec-208"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-209"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="872ec-209"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-210"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="872ec-210"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="872ec-211">)</span><span class="sxs-lookup"><span data-stu-id="872ec-211">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="872ec-212">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="872ec-212">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872ec-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-215">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="872ec-215">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="872ec-216">Это свойство наследуется от [**CIM \_ ",**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)" и всегда имеет значение "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="872ec-216">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="872ec-217">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="872ec-217">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-218">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872ec-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-220">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="872ec-220">A display name for the object.</span></span> <span data-ttu-id="872ec-221">Это свойство позволяет каждому экземпляру определить отображаемое имя в дополнение к его ключевым свойствам, идентификационным данным и сведениям о описании.</span><span class="sxs-lookup"><span data-stu-id="872ec-221">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="872ec-222">Свойство [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) класса **CIM \_ манажедсистемелемент** также определяется как отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="872ec-222">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="872ec-223">Но часто этот класс является ключом.</span><span class="sxs-lookup"><span data-stu-id="872ec-223">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="872ec-224">Не целесообразно, что одно и то же свойство может передать как удостоверение, так и отображаемое имя без несогласованности.</span><span class="sxs-lookup"><span data-stu-id="872ec-224">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="872ec-225">Если **имя** существует и не является ключом (например, для экземпляров CIM- [**класса \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), то одни и те же сведения могут присутствовать как в свойствах **Name** , так и в **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="872ec-225">Where **Name** exists and is not a Key (such as for instances of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="872ec-226">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="872ec-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="872ec-227">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="872ec-227">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-228">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="872ec-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-230">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="872ec-230">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="872ec-231">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="872ec-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="872ec-232">Значение</span><span class="sxs-lookup"><span data-stu-id="872ec-232">Value</span></span>                                                                        | <span data-ttu-id="872ec-233">Значение</span><span class="sxs-lookup"><span data-stu-id="872ec-233">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="872ec-234"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-234"><dt>2</dt></span></span> </dl> | <span data-ttu-id="872ec-235">Активировано</span><span class="sxs-lookup"><span data-stu-id="872ec-235">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="872ec-236">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="872ec-236">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-237">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="872ec-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-239">Указывает включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="872ec-239">Indicates the enabled and disabled states of an element.</span></span> <span data-ttu-id="872ec-240">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="872ec-240">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="872ec-241">Например, завершение работы (value = 4) и Start (value = 10) являются временными состояниями между включенным и отключенным.</span><span class="sxs-lookup"><span data-stu-id="872ec-241">For example, shutting down (value=4) and starting (value=10) are transient states between enabled and disabled.</span></span>



| <span data-ttu-id="872ec-242">Значение</span><span class="sxs-lookup"><span data-stu-id="872ec-242">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="872ec-243">Значение</span><span class="sxs-lookup"><span data-stu-id="872ec-243">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="872ec-244"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-244"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="872ec-245">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="872ec-245">Unknown</span></span><br/>                                                                                                                                                                                              |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="872ec-246"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-246"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         | <span data-ttu-id="872ec-247">Другое</span><span class="sxs-lookup"><span data-stu-id="872ec-247">Other</span></span><br/>                                                                                                                                                                                                |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="872ec-248"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-248"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="872ec-249">Элемент или может выполнять команды, обрабатывает все команды в очереди и помещает новые запросы в очередь.</span><span class="sxs-lookup"><span data-stu-id="872ec-249">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                            |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="872ec-250"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-250"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="872ec-251">Элемент не будет выполнять команды и удалит все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="872ec-251">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="872ec-252"><dt>**Завершение работы**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-252"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="872ec-253">Элемент находится в процессе перехода в отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="872ec-253">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="872ec-254"><dt>**Неприменимо**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-254"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="872ec-255">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="872ec-255">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="872ec-256"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-256"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="872ec-257">Элемент может выполнять команды и удалять все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="872ec-257">The element might be completing commands and will drop any new requests.</span></span><br/>                                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="872ec-258"><dt>**В тесте**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-258"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="872ec-259">Элемент находится в состоянии теста.</span><span class="sxs-lookup"><span data-stu-id="872ec-259">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="872ec-260"><dt>**Отложено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-260"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="872ec-261">Элемент может быть выполнен с помощью команд, но он будет ставить в очередь новые запросы.</span><span class="sxs-lookup"><span data-stu-id="872ec-261">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="872ec-262"><dt>**Замораживание**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-262"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="872ec-263">Элемент включен, но в режиме с ограниченным доступом.</span><span class="sxs-lookup"><span data-stu-id="872ec-263">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="872ec-264">Поведение элемента аналогично включенному состоянию (2), но обрабатывает только ограниченный набор команд.</span><span class="sxs-lookup"><span data-stu-id="872ec-264">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="872ec-265">Все остальные запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="872ec-265">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="872ec-266"><dt>**Начало**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-266"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="872ec-267">Элемент находится в процессе перехода в состояние Enabled (2).</span><span class="sxs-lookup"><span data-stu-id="872ec-267">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="872ec-268">Новые запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="872ec-268">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="872ec-269"><dt>**Зарезервировано**</dt> <dt>11 32767</dt> в формате DMTF</span><span class="sxs-lookup"><span data-stu-id="872ec-269"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="872ec-270">Это значение зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="872ec-270">This value is reserved.</span></span><br/>                                                                                                                                                                              |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="872ec-271"><dt>**Поставщик Зарезервированный**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-271"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="872ec-272">Это значение зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="872ec-272">This value is reserved.</span></span><br/>                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="872ec-273">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="872ec-273">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-274">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="872ec-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-276">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="872ec-276">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="872ec-277">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="872ec-277">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-278">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="872ec-278">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-279">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872ec-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-281">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="872ec-281">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="872ec-282">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="872ec-282">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-283">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="872ec-283">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-284">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="872ec-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-286">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="872ec-286">The current health of the element.</span></span> <span data-ttu-id="872ec-287">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="872ec-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="872ec-288">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="872ec-288">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-289">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="872ec-289">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="872ec-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-291">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="872ec-291">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="872ec-292">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="872ec-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="872ec-293">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="872ec-293">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-294">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="872ec-294">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-296">Дата и время создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="872ec-296">The date and time when the virtual machine was created.</span></span> <span data-ttu-id="872ec-297">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="872ec-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="872ec-298">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="872ec-298">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-299">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872ec-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872ec-301">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="872ec-301">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="872ec-302">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="872ec-302">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="872ec-303">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="872ec-303">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="872ec-304">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="872ec-304">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-305">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="872ec-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-307">Указывает, заблокировано ли устройство, предотвращая ввод или вывод пользователя.</span><span class="sxs-lookup"><span data-stu-id="872ec-307">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="872ec-308">Это свойство наследуется от [**CIM \_ усердевице**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="872ec-308">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="872ec-309">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="872ec-309">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-310">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="872ec-310">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-312">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="872ec-312">The last error code reported by the logical device.</span></span> <span data-ttu-id="872ec-313">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="872ec-313">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-314">**Макет**</span><span class="sxs-lookup"><span data-stu-id="872ec-314">**Layout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-315">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872ec-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-317">Строка, указывающая формат и расположение клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="872ec-317">A string indicating the format and layout of the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-318">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="872ec-318">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-319">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="872ec-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-321">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="872ec-321">This property has been deprecated.</span></span> <span data-ttu-id="872ec-322">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="872ec-322">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-323">**Name**</span><span class="sxs-lookup"><span data-stu-id="872ec-323">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872ec-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872ec-326">Квалификаторы: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="872ec-326">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="872ec-327">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="872ec-327">The label by which the object is known.</span></span> <span data-ttu-id="872ec-328">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="872ec-328">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="872ec-329">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="872ec-329">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="872ec-330">**нумбероффунктионкэйс**</span><span class="sxs-lookup"><span data-stu-id="872ec-330">**NumberOfFunctionKeys**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-331">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="872ec-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-333">Число функциональных клавиш на клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="872ec-333">The number of function keys on the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-334">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="872ec-334">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-335">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="872ec-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-337">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="872ec-337">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="872ec-338">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="872ec-338">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="872ec-339">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="872ec-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="872ec-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="872ec-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-341"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="872ec-341"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-342"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="872ec-342"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-343"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="872ec-343"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-344"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="872ec-344"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-345"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="872ec-345"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-346"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="872ec-346"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-347"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="872ec-347"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-348"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="872ec-348"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-349"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="872ec-349"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-350"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="872ec-350"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-351"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="872ec-351"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-352"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="872ec-352"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-353"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="872ec-353"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-354"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="872ec-354"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-355"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="872ec-355"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-356"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="872ec-356"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="872ec-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="872ec-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="872ec-359">)</span><span class="sxs-lookup"><span data-stu-id="872ec-359">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="872ec-360">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="872ec-360">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-361">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="872ec-361">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="872ec-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-363">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="872ec-363">The current status of the element.</span></span> <span data-ttu-id="872ec-364">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="872ec-364">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="872ec-365">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="872ec-365">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-366">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872ec-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-368">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="872ec-368">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="872ec-369">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="872ec-369">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="872ec-370">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="872ec-370">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="872ec-371">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="872ec-371">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-372">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="872ec-372">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="872ec-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-374">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="872ec-374">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="872ec-375">Это свойство наследуется от CIM с параметром и всегда имеет значение **null**. [**\_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)</span><span class="sxs-lookup"><span data-stu-id="872ec-375">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-376">**Пароль**</span><span class="sxs-lookup"><span data-stu-id="872ec-376">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-377">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="872ec-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-378">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-379">Указывает, включен ли пароль аппаратного уровня на клавиатуре, предотвращая локальный вход.</span><span class="sxs-lookup"><span data-stu-id="872ec-379">Indicates whether a hardware-level password is enabled at the keyboard, preventing local input.</span></span>

<dt>

<span data-ttu-id="872ec-380">5</span><span class="sxs-lookup"><span data-stu-id="872ec-380">5</span></span>
</dt> <dd>

<span data-ttu-id="872ec-381">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="872ec-381">Not implemented.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="872ec-382">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="872ec-382">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-383">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="872ec-383">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="872ec-384">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-385">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="872ec-385">The power management capabilities of the device.</span></span> <span data-ttu-id="872ec-386">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="872ec-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-387">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="872ec-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-388">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="872ec-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-389">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-390">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="872ec-390">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="872ec-391">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="872ec-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-392">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="872ec-392">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-393">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="872ec-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-395">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="872ec-395">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="872ec-396">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="872ec-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-397">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="872ec-397">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-398">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="872ec-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-400">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="872ec-400">Provides high level status information.</span></span> <span data-ttu-id="872ec-401">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="872ec-401">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="872ec-402">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="872ec-402">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="872ec-403">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="872ec-403">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="872ec-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="872ec-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-405"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="872ec-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="872ec-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="872ec-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="872ec-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="872ec-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="872ec-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="872ec-410">)</span><span class="sxs-lookup"><span data-stu-id="872ec-410">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="872ec-411">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="872ec-411">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-412">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="872ec-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-414">Последнее запрошенное состояние для элемента.</span><span class="sxs-lookup"><span data-stu-id="872ec-414">The last requested state for the element.</span></span>



| <span data-ttu-id="872ec-415">Значение</span><span class="sxs-lookup"><span data-stu-id="872ec-415">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="872ec-416">Значение</span><span class="sxs-lookup"><span data-stu-id="872ec-416">Meaning</span></span>                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="872ec-417"><dt>**Не применимо**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-417"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl> | <span data-ttu-id="872ec-418">Не применяется</span><span class="sxs-lookup"><span data-stu-id="872ec-418">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="872ec-419">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="872ec-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-420">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872ec-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-422">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="872ec-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-423">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="872ec-423">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-424">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="872ec-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="872ec-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-426">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="872ec-426">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="872ec-427">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="872ec-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="872ec-428">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="872ec-428">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-429">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="872ec-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-430">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-431">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="872ec-431">The current state of the logical device.</span></span> <span data-ttu-id="872ec-432">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="872ec-432">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-433">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="872ec-433">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-434">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872ec-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872ec-436">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="872ec-436">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="872ec-437">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="872ec-437">The scoping system's creation class name.</span></span> <span data-ttu-id="872ec-438">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение "мсвм \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="872ec-438">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="872ec-439">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="872ec-439">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-440">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="872ec-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-441">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="872ec-442">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="872ec-442">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="872ec-443">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="872ec-443">The scoping system's name.</span></span> <span data-ttu-id="872ec-444">Это значение соответствует значению свойства **Name** класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) для виртуальной машины с областями.</span><span class="sxs-lookup"><span data-stu-id="872ec-444">This value corresponds to the value of the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for the scoping virtual machine.</span></span> <span data-ttu-id="872ec-445">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="872ec-445">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="872ec-446">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="872ec-446">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-447">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="872ec-447">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-448">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-449">Дата и время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="872ec-449">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="872ec-450">Если состояние элемента не изменилось и заполнено это свойство, то для него должно быть задано нулевое значение интервала.</span><span class="sxs-lookup"><span data-stu-id="872ec-450">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="872ec-451">Если изменение состояния было запрошено, но отклонено или еще не обработано, свойство не должно обновляться.</span><span class="sxs-lookup"><span data-stu-id="872ec-451">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="872ec-452">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="872ec-452">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-453">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="872ec-453">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-454">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="872ec-454">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-455">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-456">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="872ec-456">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="872ec-457">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="872ec-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-458">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="872ec-458">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-459">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="872ec-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-460">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-461">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="872ec-461">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="872ec-462">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="872ec-462">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="872ec-463">**уникодесуппортед**</span><span class="sxs-lookup"><span data-stu-id="872ec-463">**UnicodeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="872ec-464">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="872ec-464">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="872ec-465">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="872ec-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="872ec-466">Указывает, поддерживает ли виртуальная клавиатура символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="872ec-466">Indicates if the virtual keyboard supports Unicode characters.</span></span> <span data-ttu-id="872ec-467">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="872ec-467">This can be one of the following values.</span></span>



| <span data-ttu-id="872ec-468">Значение</span><span class="sxs-lookup"><span data-stu-id="872ec-468">Value</span></span>                                                                            | <span data-ttu-id="872ec-469">Значение</span><span class="sxs-lookup"><span data-stu-id="872ec-469">Meaning</span></span>                                                              |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="872ec-470"><dt>True</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-470"><dt>True</dt></span></span> </dl>  | <span data-ttu-id="872ec-471">Виртуальная клавиатура поддерживает символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="872ec-471">The virtual keyboard supports Unicode characters.</span></span><br/>         |
| <dl> <span data-ttu-id="872ec-472"><dt>False</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-472"><dt>False</dt></span></span> </dl> | <span data-ttu-id="872ec-473">Виртуальная клавиатура не поддерживает символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="872ec-473">The virtual keyboard does not support Unicode characters.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="872ec-474">Комментарии</span><span class="sxs-lookup"><span data-stu-id="872ec-474">Remarks</span></span>

<span data-ttu-id="872ec-475">Доступ к классу **\_ клавиатуры мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="872ec-475">Access to the **Msvm\_Keyboard** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="872ec-476">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="872ec-476">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="872ec-477">Требования</span><span class="sxs-lookup"><span data-stu-id="872ec-477">Requirements</span></span>



| <span data-ttu-id="872ec-478">Требование</span><span class="sxs-lookup"><span data-stu-id="872ec-478">Requirement</span></span> | <span data-ttu-id="872ec-479">Значение</span><span class="sxs-lookup"><span data-stu-id="872ec-479">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="872ec-480">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="872ec-480">Minimum supported client</span></span><br/> | <span data-ttu-id="872ec-481">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="872ec-481">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="872ec-482">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="872ec-482">Minimum supported server</span></span><br/> | <span data-ttu-id="872ec-483">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="872ec-483">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="872ec-484">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="872ec-484">Namespace</span></span><br/>                | <span data-ttu-id="872ec-485">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="872ec-485">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="872ec-486">MOF</span><span class="sxs-lookup"><span data-stu-id="872ec-486">MOF</span></span><br/>                      | <dl> <span data-ttu-id="872ec-487"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-487"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="872ec-488">DLL</span><span class="sxs-lookup"><span data-stu-id="872ec-488">DLL</span></span><br/>                      | <dl> <span data-ttu-id="872ec-489"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="872ec-489"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="872ec-490">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="872ec-490">See also</span></span>

<dl> <dt>

[<span data-ttu-id="872ec-491">**\_УСЕРДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="872ec-491">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> <dt>

[<span data-ttu-id="872ec-492">**\_УСЕРДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="872ec-492">**CIM\_UserDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-userdevice)
</dt> <dt>

[<span data-ttu-id="872ec-493">Входные классы</span><span class="sxs-lookup"><span data-stu-id="872ec-493">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 


---
description: Представляет контроллер флоппи-дисковода в виртуальной машине.
ms.assetid: 38A19BF3-0E8F-4DCE-B2DB-B2E3F8100E00
title: Класс Msvm_DisketteController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteController
- Msvm_DisketteController.SetPowerState
- Msvm_DisketteController.EnableDevice
- Msvm_DisketteController.OnlineDevice
- Msvm_DisketteController.QuiesceDevice
- Msvm_DisketteController.SaveProperties
- Msvm_DisketteController.RestoreProperties
- Msvm_DisketteController.InstanceID
- Msvm_DisketteController.Caption
- Msvm_DisketteController.Description
- Msvm_DisketteController.ElementName
- Msvm_DisketteController.InstallDate
- Msvm_DisketteController.Name
- Msvm_DisketteController.OperationalStatus
- Msvm_DisketteController.StatusDescriptions
- Msvm_DisketteController.Status
- Msvm_DisketteController.HealthState
- Msvm_DisketteController.CommunicationStatus
- Msvm_DisketteController.DetailedStatus
- Msvm_DisketteController.OperatingStatus
- Msvm_DisketteController.PrimaryStatus
- Msvm_DisketteController.EnabledState
- Msvm_DisketteController.OtherEnabledState
- Msvm_DisketteController.RequestedState
- Msvm_DisketteController.EnabledDefault
- Msvm_DisketteController.TimeOfLastStateChange
- Msvm_DisketteController.AvailableRequestedStates
- Msvm_DisketteController.TransitioningToState
- Msvm_DisketteController.SystemCreationClassName
- Msvm_DisketteController.SystemName
- Msvm_DisketteController.CreationClassName
- Msvm_DisketteController.DeviceID
- Msvm_DisketteController.PowerManagementSupported
- Msvm_DisketteController.PowerManagementCapabilities
- Msvm_DisketteController.Availability
- Msvm_DisketteController.StatusInfo
- Msvm_DisketteController.LastErrorCode
- Msvm_DisketteController.ErrorDescription
- Msvm_DisketteController.ErrorCleared
- Msvm_DisketteController.OtherIdentifyingInfo
- Msvm_DisketteController.PowerOnHours
- Msvm_DisketteController.TotalPowerOnHours
- Msvm_DisketteController.IdentifyingDescriptions
- Msvm_DisketteController.AdditionalAvailability
- Msvm_DisketteController.MaxQuiesceTime
- Msvm_DisketteController.TimeOfLastReset
- Msvm_DisketteController.ProtocolSupported
- Msvm_DisketteController.MaxNumberControlled
- Msvm_DisketteController.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f1e4e731464e25dc8e871ebd17cdcddd4e262673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809532"
---
# <a name="msvm_diskettecontroller-class"></a><span data-ttu-id="09f48-103">\_Класс мсвм дискеттеконтроллер</span><span class="sxs-lookup"><span data-stu-id="09f48-103">Msvm\_DisketteController class</span></span>

<span data-ttu-id="09f48-104">Представляет контроллер флоппи-дисковода в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="09f48-104">Represents the floppy controller in the virtual machine.</span></span> <span data-ttu-id="09f48-105">Контроллер флоппи-дисковода зафиксирован, поэтому с ним не связан ни один пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="09f48-105">The floppy controller is fixed, therefore there is no resource pool associated with it.</span></span>

<span data-ttu-id="09f48-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="09f48-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="09f48-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09f48-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DisketteController : CIM_Controller
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
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName = "Msvm_DisketteController";
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
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 7;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Diskette Protocol";
};
```

## <a name="members"></a><span data-ttu-id="09f48-108">Члены</span><span class="sxs-lookup"><span data-stu-id="09f48-108">Members</span></span>

<span data-ttu-id="09f48-109">Класс **мсвм \_ дискеттеконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="09f48-109">The **Msvm\_DisketteController** class has these types of members:</span></span>

-   [<span data-ttu-id="09f48-110">Методы</span><span class="sxs-lookup"><span data-stu-id="09f48-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="09f48-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="09f48-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="09f48-112">Методы</span><span class="sxs-lookup"><span data-stu-id="09f48-112">Methods</span></span>

<span data-ttu-id="09f48-113">Класс **мсвм \_ дискеттеконтроллер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="09f48-113">The **Msvm\_DisketteController** class has these methods.</span></span>



| <span data-ttu-id="09f48-114">Метод</span><span class="sxs-lookup"><span data-stu-id="09f48-114">Method</span></span>                                                                   | <span data-ttu-id="09f48-115">Описание</span><span class="sxs-lookup"><span data-stu-id="09f48-115">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="09f48-116">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="09f48-116">**EnableDevice**</span></span>                                                         | <span data-ttu-id="09f48-117">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="09f48-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="09f48-118">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="09f48-118">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="09f48-119">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="09f48-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="09f48-120">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="09f48-120">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="09f48-121">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="09f48-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="09f48-122">**Равен**</span><span class="sxs-lookup"><span data-stu-id="09f48-122">**RequestStateChange**</span></span>](msvm-diskettecontroller-requeststatechange.md) | <span data-ttu-id="09f48-123">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="09f48-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="09f48-124">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="09f48-124">**Reset**</span></span>](msvm-diskettecontroller-reset.md)                           | <span data-ttu-id="09f48-125">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="09f48-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="09f48-126">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="09f48-126">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="09f48-127">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="09f48-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="09f48-128">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="09f48-128">**SaveProperties**</span></span>                                                       | <span data-ttu-id="09f48-129">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="09f48-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="09f48-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="09f48-130">**SetPowerState**</span></span>                                                        | <span data-ttu-id="09f48-131">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="09f48-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="09f48-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="09f48-132">Properties</span></span>

<span data-ttu-id="09f48-133">Класс **мсвм \_ дискеттеконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="09f48-133">The **Msvm\_DisketteController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09f48-134">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="09f48-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-135">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="09f48-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="09f48-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-137">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение 6 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="09f48-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-138">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="09f48-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09f48-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-141">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение 6 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="09f48-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-142">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="09f48-142">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-143">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="09f48-143">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="09f48-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-145">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="09f48-145">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="09f48-146">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09f48-146">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-147">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="09f48-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="09f48-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-150">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="09f48-150">A short description of the object.</span></span> <span data-ttu-id="09f48-151">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="09f48-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-152">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="09f48-152">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-153">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09f48-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-155">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="09f48-155">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="09f48-156">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="09f48-156">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="09f48-157">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09f48-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="09f48-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="09f48-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-159"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="09f48-159"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-160"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="09f48-160"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-161"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="09f48-161"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-162"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="09f48-162"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-163"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="09f48-163"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-164"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="09f48-164"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="09f48-165">)</span><span class="sxs-lookup"><span data-stu-id="09f48-165">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="09f48-166">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="09f48-166">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="09f48-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-169">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="09f48-169">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="09f48-170">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение "мсвм \_ дискеттеконтроллер".</span><span class="sxs-lookup"><span data-stu-id="09f48-170">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Msvm\_DisketteController".</span></span>

</dd> <dt>

<span data-ttu-id="09f48-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="09f48-171">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="09f48-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-174">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="09f48-174">A description of the object.</span></span> <span data-ttu-id="09f48-175">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="09f48-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-176">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="09f48-176">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-177">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09f48-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-179">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="09f48-179">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="09f48-180">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="09f48-180">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="09f48-181">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09f48-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="09f48-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="09f48-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="09f48-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="09f48-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="09f48-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="09f48-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="09f48-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="09f48-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="09f48-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="09f48-190">)</span><span class="sxs-lookup"><span data-stu-id="09f48-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="09f48-191">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="09f48-191">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="09f48-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-194">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="09f48-194">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="09f48-195">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="09f48-195">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-196">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="09f48-196">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="09f48-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-199">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="09f48-199">A display name for the object.</span></span> <span data-ttu-id="09f48-200">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="09f48-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-201">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="09f48-201">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-202">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09f48-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-204">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="09f48-204">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="09f48-205">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09f48-205">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-206">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="09f48-206">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-207">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09f48-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-209">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="09f48-209">The enabled and disabled states of an element.</span></span> <span data-ttu-id="09f48-210">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="09f48-210">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="09f48-211">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09f48-211">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="09f48-212">Значение</span><span class="sxs-lookup"><span data-stu-id="09f48-212">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="09f48-213">Значение</span><span class="sxs-lookup"><span data-stu-id="09f48-213">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="09f48-214"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="09f48-214"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="09f48-215">Не удалось определить состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="09f48-215">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="09f48-216"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="09f48-216"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="09f48-217"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="09f48-217"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="09f48-218">Элемент работает.</span><span class="sxs-lookup"><span data-stu-id="09f48-218">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="09f48-219"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="09f48-219"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="09f48-220">Элемент отключен.</span><span class="sxs-lookup"><span data-stu-id="09f48-220">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="09f48-221"><dt>**Завершение работы**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="09f48-221"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="09f48-222">Элемент находится в процессе перехода в отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="09f48-222">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="09f48-223"><dt>**Неприменимо**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="09f48-223"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="09f48-224">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="09f48-224">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="09f48-225"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="09f48-225"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="09f48-226">Элемент может выполнять команды, и при этом будут удалены все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="09f48-226">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="09f48-227"><dt>**В тесте**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="09f48-227"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="09f48-228">Элемент находится в состоянии теста.</span><span class="sxs-lookup"><span data-stu-id="09f48-228">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="09f48-229"><dt>**Отложено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="09f48-229"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="09f48-230">Элемент может быть выполнен с помощью команд, но он будет ставить в очередь новые запросы.</span><span class="sxs-lookup"><span data-stu-id="09f48-230">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="09f48-231"><dt>**Замораживание**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="09f48-231"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="09f48-232">Элемент включен, но находится в ограниченном режиме.</span><span class="sxs-lookup"><span data-stu-id="09f48-232">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="09f48-233">Поведение элемента аналогично включенному состоянию (2), но обрабатывает только ограниченный набор команд.</span><span class="sxs-lookup"><span data-stu-id="09f48-233">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="09f48-234">Все остальные запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="09f48-234">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="09f48-235"><dt>**Начало**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="09f48-235"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="09f48-236">Элемент находится в процессе перехода в состояние Enabled (2).</span><span class="sxs-lookup"><span data-stu-id="09f48-236">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="09f48-237">Новые запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="09f48-237">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="09f48-238">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="09f48-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-239">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="09f48-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-241">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="09f48-241">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09f48-242">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="09f48-242">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-243">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="09f48-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-245">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="09f48-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09f48-246">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="09f48-246">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-247">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09f48-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-249">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="09f48-249">The current health of the element.</span></span> <span data-ttu-id="09f48-250">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="09f48-250">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="09f48-251">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="09f48-251">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="09f48-252">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09f48-252">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-253">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="09f48-253">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-254">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="09f48-254">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="09f48-255">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-256">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="09f48-256">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="09f48-257">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="09f48-257">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-258">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="09f48-258">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-260">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="09f48-260">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="09f48-261">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09f48-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-262">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="09f48-262">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-263">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="09f48-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09f48-265">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="09f48-265">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="09f48-266">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="09f48-266">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="09f48-267">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="09f48-267">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-268">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="09f48-268">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-269">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="09f48-269">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-271">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="09f48-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09f48-272">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="09f48-272">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-273">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="09f48-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-275">Максимальное количество напрямую доступных для адресации сущностей, поддерживаемых этим контроллером.</span><span class="sxs-lookup"><span data-stu-id="09f48-275">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="09f48-276">Если число неизвестно или неограниченно, следует использовать значение 0.</span><span class="sxs-lookup"><span data-stu-id="09f48-276">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="09f48-277">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="09f48-277">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="09f48-278">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller)и имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="09f48-278">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="09f48-279">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="09f48-279">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-280">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="09f48-280">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-282">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="09f48-282">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09f48-283">**Name**</span><span class="sxs-lookup"><span data-stu-id="09f48-283">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-284">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="09f48-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-286">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="09f48-286">The label by which the object is known.</span></span> <span data-ttu-id="09f48-287">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09f48-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-288">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="09f48-288">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-289">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09f48-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-291">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="09f48-291">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="09f48-292">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="09f48-292">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="09f48-293">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09f48-293">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="09f48-294"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="09f48-294"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-295"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="09f48-295"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-296"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="09f48-296"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-297"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="09f48-297"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-298"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="09f48-298"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-299"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="09f48-299"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-300"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="09f48-300"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-301"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="09f48-301"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-302"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="09f48-302"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-303"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="09f48-303"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-304"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="09f48-304"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-305"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="09f48-305"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-306"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="09f48-306"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-307"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="09f48-307"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-308"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="09f48-308"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-309"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="09f48-309"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-310"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="09f48-310"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-311"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="09f48-311"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-312"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="09f48-312"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="09f48-313">)</span><span class="sxs-lookup"><span data-stu-id="09f48-313">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="09f48-314">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="09f48-314">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-315">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="09f48-315">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="09f48-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-317">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="09f48-317">The current statuses of the object.</span></span> <span data-ttu-id="09f48-318">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09f48-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-319">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="09f48-319">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-320">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="09f48-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-322">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="09f48-322">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="09f48-323">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="09f48-323">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="09f48-324">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="09f48-324">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="09f48-325">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="09f48-325">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-326">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="09f48-326">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="09f48-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-328">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="09f48-328">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="09f48-329">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="09f48-329">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-330">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="09f48-330">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="09f48-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-332">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="09f48-332">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09f48-333">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="09f48-333">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-334">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="09f48-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-336">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="09f48-336">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09f48-337">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="09f48-337">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-338">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="09f48-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-340">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="09f48-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09f48-341">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="09f48-341">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-342">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09f48-342">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-344">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="09f48-344">Provides high level status information.</span></span> <span data-ttu-id="09f48-345">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="09f48-345">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="09f48-346">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="09f48-346">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="09f48-347">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09f48-347">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="09f48-348"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="09f48-348"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-349"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="09f48-349"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-350"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="09f48-350"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-351"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="09f48-351"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-352"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="09f48-352"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="09f48-353"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="09f48-353"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="09f48-354">)</span><span class="sxs-lookup"><span data-stu-id="09f48-354">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="09f48-355">**протоколдескриптион**</span><span class="sxs-lookup"><span data-stu-id="09f48-355">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-356">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="09f48-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-358">Строка, которая предоставляет дополнительные сведения, связанные с протоколом, поддерживаемым контроллером.</span><span class="sxs-lookup"><span data-stu-id="09f48-358">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="09f48-359">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller)и имеет значение "протокол флоппи-дисковода".</span><span class="sxs-lookup"><span data-stu-id="09f48-359">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to "Diskette Protocol".</span></span>

</dd> <dt>

<span data-ttu-id="09f48-360">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="09f48-360">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-361">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09f48-361">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-363">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="09f48-363">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="09f48-364">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller)и имеет значение 7 (гибкая дискета).</span><span class="sxs-lookup"><span data-stu-id="09f48-364">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to 7 (Flexible Diskette).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-365">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="09f48-365">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-366">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09f48-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-368">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="09f48-368">The last requested or desired state for the element.</span></span> <span data-ttu-id="09f48-369">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="09f48-369">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="09f48-370">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="09f48-370">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="09f48-371">Конкретный экземпляр включенного логического элемента может не поддерживать **рекуестедстатечанже**.</span><span class="sxs-lookup"><span data-stu-id="09f48-371">A particular instance of an enabled logical element might not support **RequestedStateChange**.</span></span> <span data-ttu-id="09f48-372">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="09f48-372">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="09f48-373">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09f48-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-374">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="09f48-374">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-375">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="09f48-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-376">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-377">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="09f48-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09f48-378">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="09f48-378">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-379">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="09f48-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="09f48-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-381">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="09f48-381">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="09f48-382">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09f48-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="09f48-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-384">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09f48-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-386">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="09f48-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09f48-387">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="09f48-387">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-388">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="09f48-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-389">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-390">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="09f48-390">The scoping system's creation class name.</span></span> <span data-ttu-id="09f48-391">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="09f48-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-392">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="09f48-392">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-393">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="09f48-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-395">Уникальный идентификатор для области виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="09f48-395">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="09f48-396">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="09f48-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-397">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="09f48-397">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-398">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="09f48-398">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-400">Время последнего включения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="09f48-400">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="09f48-401">Это свойство наследуется [**от \_ контроллера CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="09f48-401">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="09f48-402">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="09f48-402">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-403">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="09f48-403">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-405">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="09f48-405">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="09f48-406">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="09f48-406">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="09f48-407">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="09f48-407">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-408">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="09f48-408">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-409">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-410">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="09f48-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09f48-411">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="09f48-411">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09f48-412">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09f48-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09f48-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09f48-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09f48-414">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="09f48-414">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="09f48-415">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09f48-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09f48-416">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09f48-416">Remarks</span></span>

<span data-ttu-id="09f48-417">Доступ к классу **\_ дискеттеконтроллер мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="09f48-417">Access to the **Msvm\_DisketteController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="09f48-418">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="09f48-418">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="09f48-419">Требования</span><span class="sxs-lookup"><span data-stu-id="09f48-419">Requirements</span></span>



| <span data-ttu-id="09f48-420">Требование</span><span class="sxs-lookup"><span data-stu-id="09f48-420">Requirement</span></span> | <span data-ttu-id="09f48-421">Значение</span><span class="sxs-lookup"><span data-stu-id="09f48-421">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09f48-422">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09f48-422">Minimum supported client</span></span><br/> | <span data-ttu-id="09f48-423">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="09f48-423">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="09f48-424">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09f48-424">Minimum supported server</span></span><br/> | <span data-ttu-id="09f48-425">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="09f48-425">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="09f48-426">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="09f48-426">Namespace</span></span><br/>                | <span data-ttu-id="09f48-427">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="09f48-427">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="09f48-428">MOF</span><span class="sxs-lookup"><span data-stu-id="09f48-428">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09f48-429"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09f48-429"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="09f48-430">DLL</span><span class="sxs-lookup"><span data-stu-id="09f48-430">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09f48-431"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09f48-431"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="09f48-432">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09f48-432">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09f48-433">**\_Контроллер CIM**</span><span class="sxs-lookup"><span data-stu-id="09f48-433">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dt>

[<span data-ttu-id="09f48-434">**\_Контроллер CIM**</span><span class="sxs-lookup"><span data-stu-id="09f48-434">**CIM\_Controller**</span></span>](/windows/desktop/CIMWin32Prov/cim-controller)
</dt> <dt>

[<span data-ttu-id="09f48-435">Классы хранения</span><span class="sxs-lookup"><span data-stu-id="09f48-435">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 


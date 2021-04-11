---
description: Представляет состояние компонента RDV, отвечающего за предоставление транспорта для родительского элемента Guest в целях настройки.
ms.assetid: 240d2659-01ec-4300-a17e-0b1ec90483df
title: Класс Msvm_RdvComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent
- Msvm_RdvComponent.RequestStateChange
- Msvm_RdvComponent.SetPowerState
- Msvm_RdvComponent.Reset
- Msvm_RdvComponent.EnableDevice
- Msvm_RdvComponent.OnlineDevice
- Msvm_RdvComponent.QuiesceDevice
- Msvm_RdvComponent.SaveProperties
- Msvm_RdvComponent.RestoreProperties
- Msvm_RdvComponent.InstanceID
- Msvm_RdvComponent.Caption
- Msvm_RdvComponent.Description
- Msvm_RdvComponent.ElementName
- Msvm_RdvComponent.InstallDate
- Msvm_RdvComponent.Name
- Msvm_RdvComponent.OperationalStatus
- Msvm_RdvComponent.StatusDescriptions
- Msvm_RdvComponent.Status
- Msvm_RdvComponent.HealthState
- Msvm_RdvComponent.CommunicationStatus
- Msvm_RdvComponent.DetailedStatus
- Msvm_RdvComponent.OperatingStatus
- Msvm_RdvComponent.PrimaryStatus
- Msvm_RdvComponent.EnabledState
- Msvm_RdvComponent.OtherEnabledState
- Msvm_RdvComponent.RequestedState
- Msvm_RdvComponent.EnabledDefault
- Msvm_RdvComponent.TimeOfLastStateChange
- Msvm_RdvComponent.AvailableRequestedStates
- Msvm_RdvComponent.TransitioningToState
- Msvm_RdvComponent.SystemCreationClassName
- Msvm_RdvComponent.SystemName
- Msvm_RdvComponent.CreationClassName
- Msvm_RdvComponent.DeviceID
- Msvm_RdvComponent.PowerManagementSupported
- Msvm_RdvComponent.PowerManagementCapabilities
- Msvm_RdvComponent.Availability
- Msvm_RdvComponent.StatusInfo
- Msvm_RdvComponent.LastErrorCode
- Msvm_RdvComponent.ErrorDescription
- Msvm_RdvComponent.ErrorCleared
- Msvm_RdvComponent.OtherIdentifyingInfo
- Msvm_RdvComponent.PowerOnHours
- Msvm_RdvComponent.TotalPowerOnHours
- Msvm_RdvComponent.IdentifyingDescriptions
- Msvm_RdvComponent.AdditionalAvailability
- Msvm_RdvComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e1dbffb7db18ef2441d4c8e06cff23af2648e5a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264724"
---
# <a name="msvm_rdvcomponent-class"></a><span data-ttu-id="d4ebd-103">\_Класс мсвм рдвкомпонент</span><span class="sxs-lookup"><span data-stu-id="d4ebd-103">Msvm\_RdvComponent class</span></span>

<span data-ttu-id="d4ebd-104">Представляет состояние компонента RDV, отвечающего за предоставление транспорта для родительского элемента Guest в целях настройки.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-104">Represents the state of the RDV component, which is responsible for providing a transport for the parent to the guest for configuration purposes.</span></span>

<span data-ttu-id="d4ebd-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ebd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4ebd-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "RDV";
  string   Description = "Remote Desktop Virtualization Service";
  string   ElementName = "RDV";
  datetime InstallDate;
  string   Name = "RDV";
  uint16   OperationalStatus[] = {2};
  string   StatusDescriptions[] = {"OK"};
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_RdvComponent";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="d4ebd-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d4ebd-107">Members</span></span>

<span data-ttu-id="d4ebd-108">Класс **мсвм \_ рдвкомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d4ebd-108">The **Msvm\_RdvComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="d4ebd-109">Методы</span><span class="sxs-lookup"><span data-stu-id="d4ebd-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d4ebd-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d4ebd-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d4ebd-111">Методы</span><span class="sxs-lookup"><span data-stu-id="d4ebd-111">Methods</span></span>

<span data-ttu-id="d4ebd-112">Класс **мсвм \_ рдвкомпонент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-112">The **Msvm\_RdvComponent** class has these methods.</span></span>



| <span data-ttu-id="d4ebd-113">Метод</span><span class="sxs-lookup"><span data-stu-id="d4ebd-113">Method</span></span>                                                       | <span data-ttu-id="d4ebd-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d4ebd-114">Description</span></span>                                                                                                                                                                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ebd-115">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-115">**EnableDevice**</span></span>                                             | <span data-ttu-id="d4ebd-116">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-116">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="d4ebd-117">**енаблиндпоинтс**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-117">**EnableEndPoints**</span></span>](enableendpoints-msvm-rdvcomponent.md) | <span data-ttu-id="d4ebd-118">Запрашивает службы удаленных рабочих столов виртуальное устройство для запуска канала подключения к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-118">Requests the Remote Desktop Services virtual device to start a pipe connection with the virtual machine.</span></span> <span data-ttu-id="d4ebd-119">Если возвращается ноль (0), операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-119">If zero (0) is returned, then the operation was successful.</span></span> <span data-ttu-id="d4ebd-120">Любой другой код возврата указывает на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-120">Any other return code indicates an error condition.</span></span><br/> |
| <span data-ttu-id="d4ebd-121">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-121">**OnlineDevice**</span></span>                                             | <span data-ttu-id="d4ebd-122">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-122">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="d4ebd-123">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-123">**QuiesceDevice**</span></span>                                            | <span data-ttu-id="d4ebd-124">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-124">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="d4ebd-125">**Равен**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-125">**RequestStateChange**</span></span>                                       | <span data-ttu-id="d4ebd-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-126">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="d4ebd-127">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-127">**Reset**</span></span>                                                    | <span data-ttu-id="d4ebd-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-128">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="d4ebd-129">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-129">**RestoreProperties**</span></span>                                        | <span data-ttu-id="d4ebd-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-130">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="d4ebd-131">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-131">**SaveProperties**</span></span>                                           | <span data-ttu-id="d4ebd-132">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-132">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="d4ebd-133">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-133">**SetPowerState**</span></span>                                            | <span data-ttu-id="d4ebd-134">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-134">This method is not supported.</span></span><br/>                                                                                                                                                                                            |



 

### <a name="properties"></a><span data-ttu-id="d4ebd-135">Свойства</span><span class="sxs-lookup"><span data-stu-id="d4ebd-135">Properties</span></span>

<span data-ttu-id="d4ebd-136">Класс **мсвм \_ рдвкомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-136">The **Msvm\_RdvComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4ebd-137">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-138">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d4ebd-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-140">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-140">Any additional availability and status of the device.</span></span> <span data-ttu-id="d4ebd-141">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-142">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-143">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-145">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-145">The primary availability and status of the device.</span></span> <span data-ttu-id="d4ebd-146">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-147">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-148">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d4ebd-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-150">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="d4ebd-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="d4ebd-151">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-152">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-155">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-155">A short description of the object.</span></span> <span data-ttu-id="d4ebd-156">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-157">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-158">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-160">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d4ebd-161">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d4ebd-162">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d4ebd-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d4ebd-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d4ebd-170">)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d4ebd-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-174">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-174">The scoping system's creation class name.</span></span> <span data-ttu-id="d4ebd-175">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-176">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-179">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-179">A description of the object.</span></span> <span data-ttu-id="d4ebd-180">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-182">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-184">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d4ebd-185">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d4ebd-186">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d4ebd-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d4ebd-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d4ebd-195">)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d4ebd-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-199">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="d4ebd-200">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-204">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-204">A display name for the object.</span></span> <span data-ttu-id="d4ebd-205">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-206">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-207">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-209">Конфигурация по умолчанию или запуск администратора для свойства **EnabledState** элемента.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-209">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="d4ebd-210">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-210">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-211">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-211">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-212">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-214">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-214">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d4ebd-215">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и будет иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="d4ebd-216">Значение</span><span class="sxs-lookup"><span data-stu-id="d4ebd-216">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="d4ebd-217">Значение</span><span class="sxs-lookup"><span data-stu-id="d4ebd-217">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="d4ebd-218"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebd-218"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="d4ebd-219">Не удалось определить состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-219">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="d4ebd-220"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebd-220"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="d4ebd-221"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebd-221"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="d4ebd-222">Элемент работает.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-222">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="d4ebd-223"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebd-223"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="d4ebd-224">Элемент отключен.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-224">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="d4ebd-225"><dt>**Завершение работы**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebd-225"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="d4ebd-226">Элемент находится в процессе перехода в отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-226">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="d4ebd-227"><dt>**Неприменимо**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebd-227"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="d4ebd-228">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-228">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="d4ebd-229"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebd-229"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="d4ebd-230">Элемент может выполнять команды, и при этом будут удалены все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-230">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="d4ebd-231"><dt>**В тесте**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebd-231"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="d4ebd-232">Элемент находится в состоянии теста.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-232">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="d4ebd-233"><dt>**Отложено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebd-233"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="d4ebd-234">Элемент может быть выполнен с помощью команд, но он будет ставить в очередь новые запросы.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-234">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="d4ebd-235"><dt>**Замораживание**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebd-235"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="d4ebd-236">Элемент включен, но в режиме с ограниченным доступом.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-236">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="d4ebd-237">Поведение элемента аналогично включенному состоянию (2), но обрабатывает только ограниченный набор команд.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-237">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="d4ebd-238">Все остальные запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-238">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="d4ebd-239"><dt>**Начало**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebd-239"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="d4ebd-240">Элемент находится в процессе перехода в состояние Enabled (2).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-240">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="d4ebd-241">Новые запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-241">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="d4ebd-242">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-242">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-243">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-245">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="d4ebd-245">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="d4ebd-246">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-247">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-247">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-248">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-250">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-250">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="d4ebd-251">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-253">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-255">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-255">The current health of the element.</span></span> <span data-ttu-id="d4ebd-256">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-257">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-257">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-258">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-258">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-260">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="d4ebd-260">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="d4ebd-261">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-261">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-262">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-262">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-263">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-263">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-265">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-265">The date and time when the object was installed.</span></span> <span data-ttu-id="d4ebd-266">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-266">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="d4ebd-267">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-268">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-268">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-269">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-271">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-271">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-272">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-272">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d4ebd-273">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-273">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-274">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-274">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-275">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-277">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-277">The last error code reported by the logical device.</span></span> <span data-ttu-id="d4ebd-278">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-279">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-279">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-280">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-280">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-282">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-282">This property has been deprecated.</span></span> <span data-ttu-id="d4ebd-283">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-284">**Name**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-284">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-285">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-287">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-287">The label by which the object is known.</span></span> <span data-ttu-id="d4ebd-288">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-289">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-289">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-290">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-292">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="d4ebd-292">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d4ebd-293">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-293">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d4ebd-294">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-294">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d4ebd-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-296"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-296"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-297"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-297"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-298"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-298"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-299"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-299"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-300"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-300"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-301"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-301"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-302"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-302"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-303"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-303"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-304"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-304"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-305"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-305"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-306"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-306"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-307"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-307"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-308"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-308"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-309"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-309"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-310"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-310"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-311"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-311"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-312"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-312"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-313"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d4ebd-313"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d4ebd-314">)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-314">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d4ebd-315">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-315">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-316">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d4ebd-316">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-318">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-318">The current statuses of the object.</span></span> <span data-ttu-id="d4ebd-319">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-320">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-320">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-321">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-323">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-323">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d4ebd-324">Это свойство должно иметь значение **null** , если свойство **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-324">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="d4ebd-325">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-326">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-326">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-327">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-327">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-329">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-329">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="d4ebd-330">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-330">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-331">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-331">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-332">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d4ebd-332">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-334">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-334">The power management capabilities of the device.</span></span> <span data-ttu-id="d4ebd-335">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-335">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-336">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-336">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-337">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-337">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-339">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-339">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="d4ebd-340">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-341">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-341">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-342">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-344">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-344">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="d4ebd-345">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-345">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-346">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-346">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-347">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-347">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-349">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-349">Provides high level status information.</span></span> <span data-ttu-id="d4ebd-350">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-350">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="d4ebd-351">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-351">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d4ebd-352">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d4ebd-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-354"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-354"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-355"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-355"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-356"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-356"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d4ebd-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d4ebd-359">)</span><span class="sxs-lookup"><span data-stu-id="d4ebd-359">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d4ebd-360">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-360">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-361">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-361">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-363">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-363">The last requested or desired state for the element.</span></span> <span data-ttu-id="d4ebd-364">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-364">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-365">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-366">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-368">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-368">The current status of the object.</span></span> <span data-ttu-id="d4ebd-369">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-369">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-370">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-370">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-371">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-371">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-373">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d4ebd-373">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d4ebd-374">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d4ebd-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-375">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-375">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-376">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-378">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-378">The current state of the logical device.</span></span> <span data-ttu-id="d4ebd-379">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-379">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-380">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-380">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-381">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-383">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-383">The scoping system's creation class name.</span></span> <span data-ttu-id="d4ebd-384">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-385">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-385">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-386">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-388">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-388">The scoping system's name.</span></span> <span data-ttu-id="d4ebd-389">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-390">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-390">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-391">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-391">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-393">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-393">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d4ebd-394">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-394">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-395">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-395">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-396">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-396">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-398">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-398">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="d4ebd-399">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d4ebd-400">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-400">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4ebd-401">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4ebd-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4ebd-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4ebd-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4ebd-403">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-403">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d4ebd-404">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="d4ebd-404">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4ebd-405">Требования</span><span class="sxs-lookup"><span data-stu-id="d4ebd-405">Requirements</span></span>



| <span data-ttu-id="d4ebd-406">Требование</span><span class="sxs-lookup"><span data-stu-id="d4ebd-406">Requirement</span></span> | <span data-ttu-id="d4ebd-407">Значение</span><span class="sxs-lookup"><span data-stu-id="d4ebd-407">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ebd-408">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4ebd-408">Minimum supported client</span></span><br/> | <span data-ttu-id="d4ebd-409">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d4ebd-409">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d4ebd-410">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4ebd-410">Minimum supported server</span></span><br/> | <span data-ttu-id="d4ebd-411">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d4ebd-411">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d4ebd-412">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d4ebd-412">Namespace</span></span><br/>                | <span data-ttu-id="d4ebd-413">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d4ebd-413">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d4ebd-414">MOF</span><span class="sxs-lookup"><span data-stu-id="d4ebd-414">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4ebd-415"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebd-415"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4ebd-416">DLL</span><span class="sxs-lookup"><span data-stu-id="d4ebd-416">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4ebd-417"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebd-417"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


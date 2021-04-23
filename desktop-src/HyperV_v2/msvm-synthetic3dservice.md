---
description: Описание искусственной службы трехмерного графического процессора.
ms.assetid: fe3d6105-3def-453a-ad81-97cd0bb4613f
title: Класс Msvm_Synthetic3DService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService
- Msvm_Synthetic3DService.RequestStateChange
- Msvm_Synthetic3DService.StartService
- Msvm_Synthetic3DService.StopService
- Msvm_Synthetic3DService.InstanceID
- Msvm_Synthetic3DService.Caption
- Msvm_Synthetic3DService.Description
- Msvm_Synthetic3DService.ElementName
- Msvm_Synthetic3DService.InstallDate
- Msvm_Synthetic3DService.OperationalStatus
- Msvm_Synthetic3DService.StatusDescriptions
- Msvm_Synthetic3DService.Status
- Msvm_Synthetic3DService.HealthState
- Msvm_Synthetic3DService.CommunicationStatus
- Msvm_Synthetic3DService.DetailedStatus
- Msvm_Synthetic3DService.OperatingStatus
- Msvm_Synthetic3DService.PrimaryStatus
- Msvm_Synthetic3DService.EnabledState
- Msvm_Synthetic3DService.OtherEnabledState
- Msvm_Synthetic3DService.RequestedState
- Msvm_Synthetic3DService.EnabledDefault
- Msvm_Synthetic3DService.TimeOfLastStateChange
- Msvm_Synthetic3DService.AvailableRequestedStates
- Msvm_Synthetic3DService.TransitioningToState
- Msvm_Synthetic3DService.SystemCreationClassName
- Msvm_Synthetic3DService.SystemName
- Msvm_Synthetic3DService.Name
- Msvm_Synthetic3DService.CreationClassName
- Msvm_Synthetic3DService.PrimaryOwnerName
- Msvm_Synthetic3DService.PrimaryOwnerContact
- Msvm_Synthetic3DService.StartMode
- Msvm_Synthetic3DService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e5bdacb764051f4bee2c9a646a00b09615ee5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683044"
---
# <a name="msvm_synthetic3dservice-class"></a><span data-ttu-id="4eceb-103">\_Класс мсвм Synthetic3DService</span><span class="sxs-lookup"><span data-stu-id="4eceb-103">Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="4eceb-104">Описание искусственной службы трехмерного графического процессора.</span><span class="sxs-lookup"><span data-stu-id="4eceb-104">Describes the synthetic 3-D GPU service.</span></span>

> [!Note]  
> <span data-ttu-id="4eceb-105">Этот класс недоступен для виртуальных машин поколения 2.</span><span class="sxs-lookup"><span data-stu-id="4eceb-105">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="4eceb-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="4eceb-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eceb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4eceb-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Synthetic3D Service";
  string   Description = "Microsoft Synthetic3D Service";
  string   ElementName = "Synthetic3D Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The Synthetic 3D service is fully operational." };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "synth3d";
  string   CreationClassName = "Msvm_Synthetic3DService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="4eceb-108">Члены</span><span class="sxs-lookup"><span data-stu-id="4eceb-108">Members</span></span>

<span data-ttu-id="4eceb-109">Класс **мсвм \_ Synthetic3DService** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4eceb-109">The **Msvm\_Synthetic3DService** class has these types of members:</span></span>

-   [<span data-ttu-id="4eceb-110">Методы</span><span class="sxs-lookup"><span data-stu-id="4eceb-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="4eceb-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="4eceb-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4eceb-112">Методы</span><span class="sxs-lookup"><span data-stu-id="4eceb-112">Methods</span></span>

<span data-ttu-id="4eceb-113">Класс **мсвм \_ Synthetic3DService** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4eceb-113">The **Msvm\_Synthetic3DService** class has these methods.</span></span>



| <span data-ttu-id="4eceb-114">Метод</span><span class="sxs-lookup"><span data-stu-id="4eceb-114">Method</span></span>                                                                                     | <span data-ttu-id="4eceb-115">Описание</span><span class="sxs-lookup"><span data-stu-id="4eceb-115">Description</span></span>                                                         |
|:-------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="4eceb-116">**дисаблегпуфорвиртуализатион**</span><span class="sxs-lookup"><span data-stu-id="4eceb-116">**DisableGPUForVirtualization**</span></span>](disablegpuforvirtualization-msvm-synthetic3dservice.md) | <span data-ttu-id="4eceb-117">Отключает физический GPU для виртуализации.</span><span class="sxs-lookup"><span data-stu-id="4eceb-117">Disables a physical GPU for virtualization.</span></span><br/>              |
| [<span data-ttu-id="4eceb-118">**енаблегпуфорвиртуализатион**</span><span class="sxs-lookup"><span data-stu-id="4eceb-118">**EnableGPUForVirtualization**</span></span>](enablegpuforvirtualization-msvm-synthetic3dservice.md)   | <span data-ttu-id="4eceb-119">Включает физический GPU для виртуализации.</span><span class="sxs-lookup"><span data-stu-id="4eceb-119">Enables a physical GPU for virtualization.</span></span><br/>               |
| [<span data-ttu-id="4eceb-120">**модифисервицесеттингс**</span><span class="sxs-lookup"><span data-stu-id="4eceb-120">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-synthetic3dservice.md)             | <span data-ttu-id="4eceb-121">Изменяет данные параметра для искусственной трехмерной службы.</span><span class="sxs-lookup"><span data-stu-id="4eceb-121">Modifies the setting data for the synthetic 3-D service.</span></span><br/> |
| <span data-ttu-id="4eceb-122">**Равен**</span><span class="sxs-lookup"><span data-stu-id="4eceb-122">**RequestStateChange**</span></span>                                                                     | <span data-ttu-id="4eceb-123">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4eceb-123">This method is not supported.</span></span><br/>                            |
| <span data-ttu-id="4eceb-124">**StartService**</span><span class="sxs-lookup"><span data-stu-id="4eceb-124">**StartService**</span></span>                                                                           | <span data-ttu-id="4eceb-125">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4eceb-125">This method is not supported.</span></span><br/>                            |
| <span data-ttu-id="4eceb-126">**StopService**</span><span class="sxs-lookup"><span data-stu-id="4eceb-126">**StopService**</span></span>                                                                            | <span data-ttu-id="4eceb-127">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4eceb-127">This method is not supported.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="4eceb-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="4eceb-128">Properties</span></span>

<span data-ttu-id="4eceb-129">Класс **мсвм \_ Synthetic3DService** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4eceb-129">The **Msvm\_Synthetic3DService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4eceb-130">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="4eceb-130">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-131">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="4eceb-131">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-133">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="4eceb-133">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="4eceb-134">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4eceb-134">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-135">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="4eceb-135">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4eceb-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-138">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="4eceb-138">A short description of the object.</span></span> <span data-ttu-id="4eceb-139">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4eceb-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-140">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="4eceb-140">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-141">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4eceb-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-143">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="4eceb-143">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="4eceb-144">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="4eceb-144">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4eceb-145">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4eceb-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4eceb-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="4eceb-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-147"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="4eceb-147"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-148"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="4eceb-148"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-149"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="4eceb-149"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-150"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="4eceb-150"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-151"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="4eceb-151"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-152"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4eceb-152"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4eceb-153">)</span><span class="sxs-lookup"><span data-stu-id="4eceb-153">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4eceb-154">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4eceb-154">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4eceb-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-157">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4eceb-157">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4eceb-158">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="4eceb-158">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-159">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4eceb-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4eceb-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-162">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="4eceb-162">A description of the object.</span></span> <span data-ttu-id="4eceb-163">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4eceb-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-164">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="4eceb-164">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-165">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4eceb-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-167">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="4eceb-167">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="4eceb-168">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="4eceb-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4eceb-169">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4eceb-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4eceb-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="4eceb-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="4eceb-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="4eceb-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="4eceb-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="4eceb-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="4eceb-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="4eceb-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4eceb-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4eceb-178">)</span><span class="sxs-lookup"><span data-stu-id="4eceb-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4eceb-179">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4eceb-179">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4eceb-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-182">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="4eceb-182">A display name for the object.</span></span> <span data-ttu-id="4eceb-183">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4eceb-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-184">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="4eceb-184">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-185">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4eceb-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-187">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="4eceb-187">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="4eceb-188">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4eceb-188">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-189">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="4eceb-189">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4eceb-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-192">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="4eceb-192">The enabled and disabled states of an element.</span></span> <span data-ttu-id="4eceb-193">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="4eceb-193">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="4eceb-194">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4eceb-194">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-195">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="4eceb-195">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-196">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4eceb-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-198">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="4eceb-198">The current health of the element.</span></span> <span data-ttu-id="4eceb-199">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="4eceb-199">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="4eceb-200">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="4eceb-200">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="4eceb-201">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4eceb-201">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-202">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4eceb-202">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-203">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4eceb-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-205">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4eceb-205">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="4eceb-206">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4eceb-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-207">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4eceb-207">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4eceb-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-210">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="4eceb-210">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-211">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="4eceb-211">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4eceb-212">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="4eceb-212">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-213">**Name**</span><span class="sxs-lookup"><span data-stu-id="4eceb-213">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-214">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4eceb-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-216">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="4eceb-216">The label by which the object is known.</span></span> <span data-ttu-id="4eceb-217">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="4eceb-217">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-218">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="4eceb-218">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-219">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4eceb-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-221">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="4eceb-221">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="4eceb-222">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="4eceb-222">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4eceb-223">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4eceb-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4eceb-224"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="4eceb-224"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-225"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="4eceb-225"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-226"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="4eceb-226"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-227"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="4eceb-227"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-228"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="4eceb-228"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-229"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="4eceb-229"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-230"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="4eceb-230"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-231"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="4eceb-231"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-232"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="4eceb-232"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-233"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="4eceb-233"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-234"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="4eceb-234"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-235"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="4eceb-235"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-236"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="4eceb-236"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-237"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="4eceb-237"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-238"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="4eceb-238"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-239"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="4eceb-239"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-240"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="4eceb-240"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-241"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="4eceb-241"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-242"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4eceb-242"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4eceb-243">)</span><span class="sxs-lookup"><span data-stu-id="4eceb-243">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4eceb-244">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="4eceb-244">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-245">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="4eceb-245">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-247">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="4eceb-247">The current statuses of the object.</span></span> <span data-ttu-id="4eceb-248">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4eceb-248">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-249">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="4eceb-249">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-250">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4eceb-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-252">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="4eceb-252">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="4eceb-253">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="4eceb-253">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="4eceb-254">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4eceb-254">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-255">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="4eceb-255">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-256">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4eceb-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-258">Значение, которое предоставляет сведения о том, как можно достичь основного владельца службы (например, номер телефона, адрес электронной почты и т. д.).</span><span class="sxs-lookup"><span data-stu-id="4eceb-258">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="4eceb-259">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="4eceb-259">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-260">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="4eceb-260">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4eceb-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-263">Имя основного владельца службы, если она определена.</span><span class="sxs-lookup"><span data-stu-id="4eceb-263">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="4eceb-264">Первичный владелец — это первоначальный контактный контакт для службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="4eceb-264">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="4eceb-265">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="4eceb-265">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-266">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="4eceb-266">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-267">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4eceb-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-269">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="4eceb-269">Provides high level status information.</span></span> <span data-ttu-id="4eceb-270">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="4eceb-270">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="4eceb-271">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="4eceb-271">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4eceb-272">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4eceb-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4eceb-273"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="4eceb-273"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-274"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="4eceb-274"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-275"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="4eceb-275"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-276"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="4eceb-276"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-277"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="4eceb-277"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-278"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4eceb-278"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4eceb-279">)</span><span class="sxs-lookup"><span data-stu-id="4eceb-279">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4eceb-280">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="4eceb-280">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-281">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4eceb-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-283">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="4eceb-283">The last requested or desired state for the element.</span></span> <span data-ttu-id="4eceb-284">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="4eceb-284">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="4eceb-285">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="4eceb-285">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="4eceb-286">Конкретный экземпляр класса [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать метод **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="4eceb-286">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="4eceb-287">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="4eceb-287">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="4eceb-288">Это свойство наследуется от **CIM \_ енабледлогикалелемент**.</span><span class="sxs-lookup"><span data-stu-id="4eceb-288">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-289">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="4eceb-289">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-290">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4eceb-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-292">Указывает, запущена ли служба в данный момент.</span><span class="sxs-lookup"><span data-stu-id="4eceb-292">Indicates whether the service is currently running.</span></span> <span data-ttu-id="4eceb-293">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="4eceb-293">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-294">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="4eceb-294">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-295">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4eceb-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-297">Строковое значение, указывающее, запускается ли служба автоматически системой, операционной системой или запускается только по запросу.</span><span class="sxs-lookup"><span data-stu-id="4eceb-297">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="4eceb-298">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="4eceb-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-299">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="4eceb-299">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4eceb-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-302">Состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="4eceb-302">The status of the element.</span></span> <span data-ttu-id="4eceb-303">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4eceb-303">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-304">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="4eceb-304">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-305">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="4eceb-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-307">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="4eceb-307">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="4eceb-308">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4eceb-308">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-309">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="4eceb-309">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-310">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4eceb-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-312">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="4eceb-312">The scoping system's creation class name.</span></span> <span data-ttu-id="4eceb-313">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="4eceb-313">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-314">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4eceb-314">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-315">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4eceb-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-317">Имя системы размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="4eceb-317">The name of the hosting computer system.</span></span> <span data-ttu-id="4eceb-318">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="4eceb-318">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-319">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="4eceb-319">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-320">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4eceb-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-322">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="4eceb-322">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="4eceb-323">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4eceb-323">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4eceb-324">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="4eceb-324">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eceb-325">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4eceb-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4eceb-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4eceb-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4eceb-327">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="4eceb-327">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="4eceb-328">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4eceb-328">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4eceb-329">Требования</span><span class="sxs-lookup"><span data-stu-id="4eceb-329">Requirements</span></span>



| <span data-ttu-id="4eceb-330">Требование</span><span class="sxs-lookup"><span data-stu-id="4eceb-330">Requirement</span></span> | <span data-ttu-id="4eceb-331">Значение</span><span class="sxs-lookup"><span data-stu-id="4eceb-331">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eceb-332">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4eceb-332">Minimum supported client</span></span><br/> | <span data-ttu-id="4eceb-333">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4eceb-333">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4eceb-334">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4eceb-334">Minimum supported server</span></span><br/> | <span data-ttu-id="4eceb-335">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4eceb-335">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4eceb-336">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4eceb-336">Namespace</span></span><br/>                | <span data-ttu-id="4eceb-337">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4eceb-337">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4eceb-338">MOF</span><span class="sxs-lookup"><span data-stu-id="4eceb-338">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4eceb-339"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4eceb-339"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4eceb-340">DLL</span><span class="sxs-lookup"><span data-stu-id="4eceb-340">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4eceb-341"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4eceb-341"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


---
description: Содержит сведения о синтетических трехмерных графических процессорах (GPU), доступных в главной системе.
ms.assetid: 771A42C3-4888-49DF-A389-161A2D0E3DBD
title: Класс Msvm_Synth3dVideoPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool
- Msvm_Synth3dVideoPool.InstanceID
- Msvm_Synth3dVideoPool.Caption
- Msvm_Synth3dVideoPool.Description
- Msvm_Synth3dVideoPool.ElementName
- Msvm_Synth3dVideoPool.InstallDate
- Msvm_Synth3dVideoPool.Name
- Msvm_Synth3dVideoPool.OperationalStatus
- Msvm_Synth3dVideoPool.StatusDescriptions
- Msvm_Synth3dVideoPool.Status
- Msvm_Synth3dVideoPool.HealthState
- Msvm_Synth3dVideoPool.CommunicationStatus
- Msvm_Synth3dVideoPool.DetailedStatus
- Msvm_Synth3dVideoPool.OperatingStatus
- Msvm_Synth3dVideoPool.PrimaryStatus
- Msvm_Synth3dVideoPool.PoolID
- Msvm_Synth3dVideoPool.Primordial
- Msvm_Synth3dVideoPool.Capacity
- Msvm_Synth3dVideoPool.Reserved
- Msvm_Synth3dVideoPool.ResourceType
- Msvm_Synth3dVideoPool.OtherResourceType
- Msvm_Synth3dVideoPool.ResourceSubType
- Msvm_Synth3dVideoPool.AllocationUnits
- Msvm_Synth3dVideoPool.ConsumedResourceUnits
- Msvm_Synth3dVideoPool.CurrentlyConsumedResource
- Msvm_Synth3dVideoPool.MaxConsumableResource
- Msvm_Synth3dVideoPool.Is3dVideoSupported
- Msvm_Synth3dVideoPool.IsSLATCapable
- Msvm_Synth3dVideoPool.IsGPUCapable
- Msvm_Synth3dVideoPool.DirectXVersion
- Msvm_Synth3dVideoPool.RequiredMinimumDirectXVersion
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1afad0f1b2e80a747bb518cb3eafc75d494de62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991586"
---
# <a name="msvm_synth3dvideopool-class"></a><span data-ttu-id="83ac9-103">\_Класс мсвм Synth3dVideoPool</span><span class="sxs-lookup"><span data-stu-id="83ac9-103">Msvm\_Synth3dVideoPool class</span></span>

<span data-ttu-id="83ac9-104">Содержит сведения о синтетических трехмерных графических процессорах (GPU), доступных в главной системе.</span><span class="sxs-lookup"><span data-stu-id="83ac9-104">Contains information about the synthetic 3-D video graphics processing units (GPUs) available on the host system.</span></span> <span data-ttu-id="83ac9-105">Этот класс используется только с системами узлов, поддерживающими RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="83ac9-105">This class is only used with host systems that support RemoteFX.</span></span>

<span data-ttu-id="83ac9-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="83ac9-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="83ac9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83ac9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synth3dVideoPool : CIM_ResourcePool
{
  string   InstanceID;
  string   Caption = "3D Display Controller Resource Pool";
  string   Description = "Resource pool used to allocate synthetic 3D video controller resources to a virtual machine.";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = {"OK"};
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   PoolID;
  boolean  Primordial = True;
  uint64   Capacity;
  uint64   Reserved = 0;
  uint16   ResourceType;
  string   OtherResourceType;
  string   ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
  string   AllocationUnits = "count";
  string   ConsumedResourceUnits = "count";
  uint64   CurrentlyConsumedResource;
  uint64   MaxConsumableResource;
  boolean  Is3dVideoSupported;
  boolean  IsSLATCapable;
  boolean  IsGPUCapable;
  string   DirectXVersion;
  string   RequiredMinimumDirectXVersion;
};
```

## <a name="members"></a><span data-ttu-id="83ac9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="83ac9-108">Members</span></span>

<span data-ttu-id="83ac9-109">Класс **мсвм \_ Synth3dVideoPool** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="83ac9-109">The **Msvm\_Synth3dVideoPool** class has these types of members:</span></span>

-   [<span data-ttu-id="83ac9-110">Методы</span><span class="sxs-lookup"><span data-stu-id="83ac9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="83ac9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="83ac9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="83ac9-112">Методы</span><span class="sxs-lookup"><span data-stu-id="83ac9-112">Methods</span></span>

<span data-ttu-id="83ac9-113">Класс **мсвм \_ Synth3dVideoPool** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="83ac9-113">The **Msvm\_Synth3dVideoPool** class has these methods.</span></span>



| <span data-ttu-id="83ac9-114">Метод</span><span class="sxs-lookup"><span data-stu-id="83ac9-114">Method</span></span>                                                                                             | <span data-ttu-id="83ac9-115">Описание</span><span class="sxs-lookup"><span data-stu-id="83ac9-115">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83ac9-116">**калкулатевидеомеморирекуирементс**</span><span class="sxs-lookup"><span data-stu-id="83ac9-116">**CalculateVideoMemoryRequirements**</span></span>](msvm-synth3dvideopool-calculatevideomemoryrequirements.md) | <span data-ttu-id="83ac9-117">Вычисляет объем видеопамяти, необходимый для виртуальной машины RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="83ac9-117">Calculates the amount of video memory required for a RemoteFX virtual machine.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="83ac9-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="83ac9-118">Properties</span></span>

<span data-ttu-id="83ac9-119">Класс **мсвм \_ Synth3dVideoPool** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="83ac9-119">The **Msvm\_Synth3dVideoPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83ac9-120">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="83ac9-120">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="83ac9-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-123">Единицы распределения, используемые пулом ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83ac9-123">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="83ac9-124">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="83ac9-124">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-125">**Производительность**</span><span class="sxs-lookup"><span data-stu-id="83ac9-125">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-126">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83ac9-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-128">Максимальный объем активных резервирований (в единицах **аллокатионунитс**), который может поддерживать пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83ac9-128">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="83ac9-129">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="83ac9-129">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-130">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="83ac9-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="83ac9-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-133">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="83ac9-133">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-134">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="83ac9-134">A short description of the object.</span></span> <span data-ttu-id="83ac9-135">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ac9-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-136">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="83ac9-136">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-137">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83ac9-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-139">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="83ac9-139">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="83ac9-140">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="83ac9-140">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="83ac9-141">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="83ac9-141">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="83ac9-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="83ac9-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="83ac9-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-144"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="83ac9-144"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-145"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="83ac9-145"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-146"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="83ac9-146"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-147"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="83ac9-147"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-148"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="83ac9-148"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="83ac9-149">)</span><span class="sxs-lookup"><span data-stu-id="83ac9-149">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="83ac9-150">**консумедресаурцеунитс**</span><span class="sxs-lookup"><span data-stu-id="83ac9-150">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="83ac9-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-153">Указывает единицы для свойств **максконсумаблересаурце** и **куррентликонсумедресаурце** .</span><span class="sxs-lookup"><span data-stu-id="83ac9-153">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span> <span data-ttu-id="83ac9-154">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="83ac9-154">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-155">**куррентликонсумедресаурце**</span><span class="sxs-lookup"><span data-stu-id="83ac9-155">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-156">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83ac9-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-158">Указывает объем ресурсов, которые в настоящее время предоставляет пул ресурсов для потребителей.</span><span class="sxs-lookup"><span data-stu-id="83ac9-158">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="83ac9-159">Это свойство отличается от **зарезервированного** свойства тем, что оно описывает представление ресурса "потребители", а **зарезервированное** свойство описывает представление "производители" ресурса.</span><span class="sxs-lookup"><span data-stu-id="83ac9-159">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span> <span data-ttu-id="83ac9-160">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="83ac9-160">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-161">**Описание**</span><span class="sxs-lookup"><span data-stu-id="83ac9-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="83ac9-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-164">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="83ac9-164">A description of the object.</span></span> <span data-ttu-id="83ac9-165">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ac9-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="83ac9-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-167">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83ac9-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-169">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="83ac9-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="83ac9-170">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="83ac9-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="83ac9-171">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="83ac9-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="83ac9-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="83ac9-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="83ac9-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="83ac9-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="83ac9-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="83ac9-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="83ac9-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="83ac9-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="83ac9-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="83ac9-180">)</span><span class="sxs-lookup"><span data-stu-id="83ac9-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="83ac9-181">**директксверсион**</span><span class="sxs-lookup"><span data-stu-id="83ac9-181">**DirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="83ac9-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-184">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="83ac9-184">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-185">Указывает самую раннюю версию DirectX, поддерживаемую картами в пуле ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83ac9-185">Specifies the lowest version of DirectX that is supported by the cards within the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-186">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="83ac9-186">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="83ac9-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-189">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="83ac9-189">A display name for the object.</span></span> <span data-ttu-id="83ac9-190">Это свойство позволяет каждому экземпляру определить отображаемое имя в дополнение к его ключевым свойствам, идентификационным данным и сведениям о описании.</span><span class="sxs-lookup"><span data-stu-id="83ac9-190">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="83ac9-191">Свойство [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) класса **CIM \_ манажедсистемелемент** также определяется как отображаемое имя, но часто этот класс является ключом.</span><span class="sxs-lookup"><span data-stu-id="83ac9-191">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name, but it is often subclassed to be a Key.</span></span> <span data-ttu-id="83ac9-192">Не целесообразно, что одно и то же свойство может передать как удостоверение, так и отображаемое имя без несогласованности.</span><span class="sxs-lookup"><span data-stu-id="83ac9-192">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="83ac9-193">Если [**имя**](msvm-keyboard.md) существует и не является ключом (например, для экземпляров класса с ключом), то одни и те же данные могут присутствовать в свойствах **Name** и **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="83ac9-193">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="83ac9-194">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ac9-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-195">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="83ac9-195">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-196">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83ac9-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-198">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="83ac9-198">The current health of the element.</span></span> <span data-ttu-id="83ac9-199">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="83ac9-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-200">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="83ac9-200">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-201">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="83ac9-201">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-203">Дата и время создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="83ac9-203">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="83ac9-204">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="83ac9-204">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-205">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="83ac9-205">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-206">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="83ac9-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-208">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="83ac9-208">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-209">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="83ac9-209">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="83ac9-210">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="83ac9-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-211">**Is3dVideoSupported**</span><span class="sxs-lookup"><span data-stu-id="83ac9-211">**Is3dVideoSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-212">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="83ac9-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-214">Указывает, поддерживается ли трехмерное видео системой узла.</span><span class="sxs-lookup"><span data-stu-id="83ac9-214">Specifies whether 3-D video is supported by the host system.</span></span> <span data-ttu-id="83ac9-215">Содержит ненулевое значение, если поддерживается трехмерное видео или в противном случае — ноль.</span><span class="sxs-lookup"><span data-stu-id="83ac9-215">Contains a nonzero value if 3-D video is supported, or zero otherwise.</span></span> <span data-ttu-id="83ac9-216">Для поддержки трехмерного видео узел RemoteFX должен иметь возможности преобразования адресов второго уровня (SLAT) и иметь по крайней мере один физический GPU, поддерживающий RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="83ac9-216">To support 3-D video, the RemoteFX host must have second level address translation (SLAT) capabilities and have at least one physical GPU that supports RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-217">**исгпукапабле**</span><span class="sxs-lookup"><span data-stu-id="83ac9-217">**IsGPUCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-218">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="83ac9-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-220">Указывает, имеют ли узлы GPU, поддерживающие RemoteFX, и соответствуют ли их версии DirectX минимальным требованиям.</span><span class="sxs-lookup"><span data-stu-id="83ac9-220">Specifies whether the host has GPUs that support RemoteFX and whether their DirectX versions meet the minimum requirement.</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-221">**исслаткапабле**</span><span class="sxs-lookup"><span data-stu-id="83ac9-221">**IsSLATCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-222">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="83ac9-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-224">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения")</span><span class="sxs-lookup"><span data-stu-id="83ac9-224">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-225">Указывает, имеет ли узел ЦП с поддержкой преобразования адресов второго уровня (SLAT).</span><span class="sxs-lookup"><span data-stu-id="83ac9-225">Specifies whether the host has a second level address translation (SLAT) capable CPU.</span></span>

> [!Note]  
> <span data-ttu-id="83ac9-226">Не рекомендуется в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="83ac9-226">Deprecated in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="83ac9-227">**максконсумаблересаурце**</span><span class="sxs-lookup"><span data-stu-id="83ac9-227">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-228">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83ac9-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-230">Указывает максимальный объем потребляемого пула ресурсов, который может предоставляться потребителям.</span><span class="sxs-lookup"><span data-stu-id="83ac9-230">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="83ac9-231">Это свойство отличается от свойства **Capacity** в том, что оно описывает представление ресурса "потребители", а свойство **Capacity** описывает представление "производители" ресурса.</span><span class="sxs-lookup"><span data-stu-id="83ac9-231">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span> <span data-ttu-id="83ac9-232">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="83ac9-232">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-233">**Name**</span><span class="sxs-lookup"><span data-stu-id="83ac9-233">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-234">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="83ac9-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-236">Квалификаторы: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="83ac9-236">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-237">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="83ac9-237">The label by which the object is known.</span></span> <span data-ttu-id="83ac9-238">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="83ac9-238">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="83ac9-239">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="83ac9-239">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-240">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="83ac9-240">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-241">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83ac9-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-243">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="83ac9-243">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="83ac9-244">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="83ac9-244">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="83ac9-245">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="83ac9-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="83ac9-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="83ac9-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-247"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="83ac9-247"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-248"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="83ac9-248"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-249"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="83ac9-249"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-250"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="83ac9-250"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-251"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="83ac9-251"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-252"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="83ac9-252"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-253"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="83ac9-253"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-254"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="83ac9-254"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-255"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="83ac9-255"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-256"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="83ac9-256"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-257"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="83ac9-257"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-258"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="83ac9-258"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-259"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="83ac9-259"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-260"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="83ac9-260"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-261"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="83ac9-261"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-262"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="83ac9-262"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="83ac9-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="83ac9-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="83ac9-265">)</span><span class="sxs-lookup"><span data-stu-id="83ac9-265">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="83ac9-266">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="83ac9-266">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-267">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="83ac9-267">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-269">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="83ac9-269">The current status of the element.</span></span> <span data-ttu-id="83ac9-270">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="83ac9-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span> <span data-ttu-id="83ac9-271">Hyper-V будет использовать только первый элемент этого массива.</span><span class="sxs-lookup"><span data-stu-id="83ac9-271">Hyper-V will only ever use the first element of this array.</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-272">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="83ac9-272">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-273">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="83ac9-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-275">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а [**ResourceType**](msvm-processorpool.md) имеет значение 0 ("Other").</span><span class="sxs-lookup"><span data-stu-id="83ac9-275">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorpool.md) is set to 0 ("Other").</span></span> <span data-ttu-id="83ac9-276">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="83ac9-276">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-277">**пулид**</span><span class="sxs-lookup"><span data-stu-id="83ac9-277">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-278">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="83ac9-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-280">На это значение ссылаются экземпляры [**\_ ресаурцеаллокатионсеттингдата CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , которые были выделены из этого пула.</span><span class="sxs-lookup"><span data-stu-id="83ac9-280">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="83ac9-281">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))и всегда имеет значение "Microsoft:*GUID* \\ root".</span><span class="sxs-lookup"><span data-stu-id="83ac9-281">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-282">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="83ac9-282">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-283">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83ac9-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-285">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="83ac9-285">Provides high level status information.</span></span> <span data-ttu-id="83ac9-286">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="83ac9-286">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="83ac9-287">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="83ac9-287">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="83ac9-288">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="83ac9-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="83ac9-289"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="83ac9-289"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-290"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="83ac9-290"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-291"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="83ac9-291"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-292"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="83ac9-292"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-293"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="83ac9-293"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-294"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="83ac9-294"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="83ac9-295">)</span><span class="sxs-lookup"><span data-stu-id="83ac9-295">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="83ac9-296">**Исходный пул**</span><span class="sxs-lookup"><span data-stu-id="83ac9-296">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-297">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="83ac9-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-299">**Значение true** , если этот пул ресурсов является базовым, из которого ресурсы рисуются и возвращаются в действии управления ресурсами. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="83ac9-299">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="83ac9-300">Является первичным, это означает, что этот пул ресурсов не может быть создан или удален потребителями этой модели.</span><span class="sxs-lookup"><span data-stu-id="83ac9-300">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="83ac9-301">Однако другие действия, смоделированные или не связанные с, могут повлиять на характеристики или размер первичных пулов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83ac9-301">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="83ac9-302">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="83ac9-302">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-303">**рекуиредминимумдиректксверсион**</span><span class="sxs-lookup"><span data-stu-id="83ac9-303">**RequiredMinimumDirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="83ac9-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-306">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="83ac9-306">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-307">Указывает самую раннюю версию DirectX, необходимую для карточек в пуле ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83ac9-307">Specifies the lowest version of DirectX that is required by the cards within the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-308">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="83ac9-308">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-309">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83ac9-309">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-311">Текущие резервирования (в единицах **аллокатионунитс**) распределяются по всем активным выделениям из этого пула.</span><span class="sxs-lookup"><span data-stu-id="83ac9-311">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="83ac9-312">В иерархической конфигурации этот параметр представляет сумму всех текущих резервирований пула ресурсов-потомков.</span><span class="sxs-lookup"><span data-stu-id="83ac9-312">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="83ac9-313">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="83ac9-313">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-314">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="83ac9-314">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-315">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="83ac9-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-317">Строка, описывающая конкретный подтип реализации для этого пула.</span><span class="sxs-lookup"><span data-stu-id="83ac9-317">A string that describes an implementation specific subtype for this pool.</span></span> <span data-ttu-id="83ac9-318">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83ac9-318">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="83ac9-319">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="83ac9-319">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-320">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="83ac9-320">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-321">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83ac9-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-323">Тип ресурса, который может выделить этот пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83ac9-323">The type of resource this resource pool can allocate.</span></span> <span data-ttu-id="83ac9-324">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))и всегда имеет значение 4 ("Memory").</span><span class="sxs-lookup"><span data-stu-id="83ac9-324">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-325">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="83ac9-325">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-326">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="83ac9-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-328">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="83ac9-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="83ac9-329">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="83ac9-329">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83ac9-330">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="83ac9-330">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="83ac9-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="83ac9-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83ac9-332">Строки, описывающие различные значения массива [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="83ac9-332">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="83ac9-333">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="83ac9-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span> <span data-ttu-id="83ac9-334">Hyper-V будет использовать только первый элемент этого массива.</span><span class="sxs-lookup"><span data-stu-id="83ac9-334">Hyper-V will only ever use the first element of this array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83ac9-335">Требования</span><span class="sxs-lookup"><span data-stu-id="83ac9-335">Requirements</span></span>



| <span data-ttu-id="83ac9-336">Требование</span><span class="sxs-lookup"><span data-stu-id="83ac9-336">Requirement</span></span> | <span data-ttu-id="83ac9-337">Значение</span><span class="sxs-lookup"><span data-stu-id="83ac9-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83ac9-338">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83ac9-338">Minimum supported client</span></span><br/> | <span data-ttu-id="83ac9-339">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="83ac9-339">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="83ac9-340">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83ac9-340">Minimum supported server</span></span><br/> | <span data-ttu-id="83ac9-341">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="83ac9-341">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="83ac9-342">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="83ac9-342">Namespace</span></span><br/>                | <span data-ttu-id="83ac9-343">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="83ac9-343">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="83ac9-344">MOF</span><span class="sxs-lookup"><span data-stu-id="83ac9-344">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83ac9-345"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83ac9-345"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="83ac9-346">DLL</span><span class="sxs-lookup"><span data-stu-id="83ac9-346">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83ac9-347"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="83ac9-347"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="83ac9-348">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83ac9-348">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83ac9-349">**\_RESOURCEPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="83ac9-349">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> </dl>

 


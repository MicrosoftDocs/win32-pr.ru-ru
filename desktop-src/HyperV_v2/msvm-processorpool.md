---
description: Статистическая обработка ресурсов процессора, которые могут быть выделены виртуальной машине.
ms.assetid: 73424568-fa6c-4ed8-9640-a67a6d2829f0
title: Класс Msvm_ProcessorPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool
- Msvm_ProcessorPool.InstanceID
- Msvm_ProcessorPool.Caption
- Msvm_ProcessorPool.Description
- Msvm_ProcessorPool.ElementName
- Msvm_ProcessorPool.InstallDate
- Msvm_ProcessorPool.Name
- Msvm_ProcessorPool.OperationalStatus
- Msvm_ProcessorPool.StatusDescriptions
- Msvm_ProcessorPool.Status
- Msvm_ProcessorPool.HealthState
- Msvm_ProcessorPool.CommunicationStatus
- Msvm_ProcessorPool.DetailedStatus
- Msvm_ProcessorPool.OperatingStatus
- Msvm_ProcessorPool.PrimaryStatus
- Msvm_ProcessorPool.PoolID
- Msvm_ProcessorPool.Primordial
- Msvm_ProcessorPool.Capacity
- Msvm_ProcessorPool.Reserved
- Msvm_ProcessorPool.ResourceType
- Msvm_ProcessorPool.OtherResourceType
- Msvm_ProcessorPool.ResourceSubType
- Msvm_ProcessorPool.AllocationUnits
- Msvm_ProcessorPool.ConsumedResourceUnits
- Msvm_ProcessorPool.CurrentlyConsumedResource
- Msvm_ProcessorPool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 93927483c23147fd387e24cdc5a550a1771457cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683545"
---
# <a name="msvm_processorpool-class"></a><span data-ttu-id="8517f-103">\_Класс мсвм процессорпул</span><span class="sxs-lookup"><span data-stu-id="8517f-103">Msvm\_ProcessorPool class</span></span>

<span data-ttu-id="8517f-104">Статистическая обработка ресурсов процессора, которые могут быть выделены виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="8517f-104">Aggregates the processor resources that may be allocated to a virtual machine.</span></span>

<span data-ttu-id="8517f-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="8517f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8517f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8517f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProcessorPool : CIM_ResourcePool
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
  string   PoolID = "Microsoft:GUID\Root";
  boolean  Primordial = False;
  uint64   Capacity;
  uint64   Reserved;
  uint16   ResourceType = 4;
  string   OtherResourceType;
  string   ResourceSubType;
  string   AllocationUnits = "Megabyte";
  string   ConsumedResourceUnits = "count";
  uint64   CurrentlyConsumedResource;
  uint64   MaxConsumableResource;
};
```

## <a name="members"></a><span data-ttu-id="8517f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="8517f-107">Members</span></span>

<span data-ttu-id="8517f-108">Класс **мсвм \_ процессорпул** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8517f-108">The **Msvm\_ProcessorPool** class has these types of members:</span></span>

-   [<span data-ttu-id="8517f-109">Методы</span><span class="sxs-lookup"><span data-stu-id="8517f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="8517f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="8517f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8517f-111">Методы</span><span class="sxs-lookup"><span data-stu-id="8517f-111">Methods</span></span>

<span data-ttu-id="8517f-112">Класс **мсвм \_ процессорпул** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8517f-112">The **Msvm\_ProcessorPool** class has these methods.</span></span>



| <span data-ttu-id="8517f-113">Метод</span><span class="sxs-lookup"><span data-stu-id="8517f-113">Method</span></span>                                                                          | <span data-ttu-id="8517f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8517f-114">Description</span></span>                                           |
|:--------------------------------------------------------------------------------|:------------------------------------------------------|
| [<span data-ttu-id="8517f-115">**калкулатепоссиблересерве**</span><span class="sxs-lookup"><span data-stu-id="8517f-115">**CalculatePossibleReserve**</span></span>](calculatepossiblereserve-msvm-processorpool.md) | <span data-ttu-id="8517f-116">Используется для поиска действительного резерва процессора.</span><span class="sxs-lookup"><span data-stu-id="8517f-116">Used to find the actual processor reserve.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8517f-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="8517f-117">Properties</span></span>

<span data-ttu-id="8517f-118">Класс **мсвм \_ процессорпул** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8517f-118">The **Msvm\_ProcessorPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8517f-119">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="8517f-119">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8517f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-122">Единицы распределения, используемые пулом ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8517f-122">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="8517f-123">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))и имеет значение "мегабайт".</span><span class="sxs-lookup"><span data-stu-id="8517f-123">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to "Megabyte".</span></span>

</dd> <dt>

<span data-ttu-id="8517f-124">**Производительность**</span><span class="sxs-lookup"><span data-stu-id="8517f-124">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-125">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8517f-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-127">Максимальный объем активных резервирований (в единицах **аллокатионунитс**), который может поддерживать пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8517f-127">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="8517f-128">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8517f-128">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8517f-129">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="8517f-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8517f-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-132">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8517f-132">A short description of the object.</span></span> <span data-ttu-id="8517f-133">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8517f-133">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8517f-134">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="8517f-134">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-135">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8517f-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-137">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="8517f-137">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8517f-138">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8517f-138">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8517f-139">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8517f-139">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8517f-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="8517f-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-141"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="8517f-141"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-142"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="8517f-142"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-143"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="8517f-143"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-144"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="8517f-144"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-145"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="8517f-145"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-146"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8517f-146"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8517f-147">)</span><span class="sxs-lookup"><span data-stu-id="8517f-147">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8517f-148">**консумедресаурцеунитс**</span><span class="sxs-lookup"><span data-stu-id="8517f-148">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8517f-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-151">Указывает единицы для свойств **максконсумаблересаурце** и **куррентликонсумедресаурце** .</span><span class="sxs-lookup"><span data-stu-id="8517f-151">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span> <span data-ttu-id="8517f-152">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8517f-152">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8517f-153">**куррентликонсумедресаурце**</span><span class="sxs-lookup"><span data-stu-id="8517f-153">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-154">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8517f-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-156">Указывает объем ресурсов, которые в настоящее время предоставляет пул ресурсов для потребителей.</span><span class="sxs-lookup"><span data-stu-id="8517f-156">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="8517f-157">Это свойство отличается от **зарезервированного** свойства тем, что оно описывает представление ресурса "потребители", а **зарезервированное** свойство описывает представление "производители" ресурса.</span><span class="sxs-lookup"><span data-stu-id="8517f-157">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span> <span data-ttu-id="8517f-158">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8517f-158">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8517f-159">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8517f-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8517f-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-162">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8517f-162">A description of the object.</span></span> <span data-ttu-id="8517f-163">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8517f-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8517f-164">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8517f-164">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-165">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8517f-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-167">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="8517f-167">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8517f-168">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8517f-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8517f-169">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8517f-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8517f-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="8517f-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="8517f-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="8517f-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="8517f-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="8517f-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="8517f-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="8517f-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8517f-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8517f-178">)</span><span class="sxs-lookup"><span data-stu-id="8517f-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8517f-179">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8517f-179">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8517f-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-182">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="8517f-182">A display name for the object.</span></span> <span data-ttu-id="8517f-183">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8517f-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8517f-184">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8517f-184">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-185">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8517f-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-187">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="8517f-187">The current health of the element.</span></span> <span data-ttu-id="8517f-188">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8517f-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8517f-189">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8517f-189">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-190">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8517f-190">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-192">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="8517f-192">The date and time when the object was installed.</span></span> <span data-ttu-id="8517f-193">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="8517f-193">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="8517f-194">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8517f-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8517f-195">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8517f-195">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-196">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8517f-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8517f-198">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="8517f-198">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8517f-199">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="8517f-199">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8517f-200">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8517f-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8517f-201">**максконсумаблересаурце**</span><span class="sxs-lookup"><span data-stu-id="8517f-201">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-202">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8517f-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-204">Указывает максимальный объем потребляемого пула ресурсов, который может предоставляться потребителям.</span><span class="sxs-lookup"><span data-stu-id="8517f-204">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="8517f-205">Это свойство отличается от свойства **Capacity** в том, что оно описывает представление ресурса "потребители", а свойство **Capacity** описывает представление "производители" ресурса.</span><span class="sxs-lookup"><span data-stu-id="8517f-205">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span> <span data-ttu-id="8517f-206">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8517f-206">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8517f-207">**Name**</span><span class="sxs-lookup"><span data-stu-id="8517f-207">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8517f-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-210">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="8517f-210">The label by which the object is known.</span></span> <span data-ttu-id="8517f-211">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8517f-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8517f-212">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="8517f-212">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-213">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8517f-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-215">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="8517f-215">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8517f-216">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8517f-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8517f-217">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8517f-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8517f-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="8517f-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="8517f-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-220"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="8517f-220"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-221"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="8517f-221"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-222"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="8517f-222"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-223"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="8517f-223"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-224"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="8517f-224"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-225"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="8517f-225"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-226"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="8517f-226"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-227"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="8517f-227"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-228"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="8517f-228"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-229"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="8517f-229"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-230"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="8517f-230"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-231"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="8517f-231"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-232"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="8517f-232"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-233"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="8517f-233"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-234"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="8517f-234"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-235"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="8517f-235"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-236"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8517f-236"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8517f-237">)</span><span class="sxs-lookup"><span data-stu-id="8517f-237">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8517f-238">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8517f-238">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-239">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8517f-239">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8517f-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-241">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="8517f-241">The current statuses of the object.</span></span> <span data-ttu-id="8517f-242">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8517f-242">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8517f-243">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="8517f-243">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-244">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8517f-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-246">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а **ResourceType** имеет значение 0 ("Other").</span><span class="sxs-lookup"><span data-stu-id="8517f-246">A string that describes the resource type when a well-defined value is not available and **ResourceType** is set to 0 ("Other").</span></span> <span data-ttu-id="8517f-247">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="8517f-247">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8517f-248">**пулид**</span><span class="sxs-lookup"><span data-stu-id="8517f-248">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8517f-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-251">На это значение ссылаются экземпляры [**\_ ресаурцеаллокатионсеттингдата CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , которые были выделены из этого пула.</span><span class="sxs-lookup"><span data-stu-id="8517f-251">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="8517f-252">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))и всегда имеет значение "Microsoft:*GUID* \\ root".</span><span class="sxs-lookup"><span data-stu-id="8517f-252">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="8517f-253">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="8517f-253">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-254">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8517f-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-255">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-256">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="8517f-256">Provides high level status information.</span></span> <span data-ttu-id="8517f-257">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="8517f-257">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="8517f-258">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="8517f-258">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8517f-259">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8517f-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8517f-260"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="8517f-260"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-261"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="8517f-261"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-262"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="8517f-262"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-263"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="8517f-263"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="8517f-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8517f-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8517f-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8517f-266">)</span><span class="sxs-lookup"><span data-stu-id="8517f-266">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8517f-267">**Исходный пул**</span><span class="sxs-lookup"><span data-stu-id="8517f-267">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-268">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8517f-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-270">**Значение true** , если этот пул ресурсов является базовым, из которого ресурсы рисуются и возвращаются в действии управления ресурсами. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="8517f-270">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="8517f-271">Является первичным, это означает, что этот пул ресурсов не может быть создан или удален потребителями этой модели.</span><span class="sxs-lookup"><span data-stu-id="8517f-271">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="8517f-272">Однако другие действия, смоделированные или не связанные с, могут повлиять на характеристики или размер первичных пулов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8517f-272">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="8517f-273">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8517f-273">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8517f-274">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="8517f-274">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-275">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8517f-275">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-277">Текущие резервирования (в единицах **аллокатионунитс**) распределяются по всем активным выделениям из этого пула.</span><span class="sxs-lookup"><span data-stu-id="8517f-277">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="8517f-278">В иерархической конфигурации этот параметр представляет сумму всех текущих резервирований пула ресурсов-потомков.</span><span class="sxs-lookup"><span data-stu-id="8517f-278">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="8517f-279">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8517f-279">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8517f-280">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="8517f-280">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-281">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8517f-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-283">Строка, описывающая конкретный подтип реализации для этого пула.</span><span class="sxs-lookup"><span data-stu-id="8517f-283">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="8517f-284">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8517f-284">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="8517f-285">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8517f-285">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8517f-286">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="8517f-286">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-287">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8517f-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-289">Тип ресурса, который может выделить этот пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8517f-289">The type of resource this resource pool may allocate.</span></span> <span data-ttu-id="8517f-290">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))и имеет значение 4 ("Memory").</span><span class="sxs-lookup"><span data-stu-id="8517f-290">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="8517f-291">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="8517f-291">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-292">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8517f-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8517f-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-294">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="8517f-294">The current status of the object.</span></span> <span data-ttu-id="8517f-295">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="8517f-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8517f-296">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="8517f-296">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8517f-297">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8517f-297">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8517f-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8517f-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8517f-299">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="8517f-299">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="8517f-300">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8517f-300">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8517f-301">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8517f-301">Remarks</span></span>

<span data-ttu-id="8517f-302">Доступ к классу **\_ процессорпул мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="8517f-302">Access to the **Msvm\_ProcessorPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8517f-303">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8517f-303">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="8517f-304">Требования</span><span class="sxs-lookup"><span data-stu-id="8517f-304">Requirements</span></span>



| <span data-ttu-id="8517f-305">Требование</span><span class="sxs-lookup"><span data-stu-id="8517f-305">Requirement</span></span> | <span data-ttu-id="8517f-306">Значение</span><span class="sxs-lookup"><span data-stu-id="8517f-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8517f-307">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8517f-307">Minimum supported client</span></span><br/> | <span data-ttu-id="8517f-308">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8517f-308">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8517f-309">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8517f-309">Minimum supported server</span></span><br/> | <span data-ttu-id="8517f-310">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8517f-310">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8517f-311">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8517f-311">Namespace</span></span><br/>                | <span data-ttu-id="8517f-312">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="8517f-312">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8517f-313">MOF</span><span class="sxs-lookup"><span data-stu-id="8517f-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8517f-314"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8517f-314"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8517f-315">DLL</span><span class="sxs-lookup"><span data-stu-id="8517f-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8517f-316"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8517f-316"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8517f-317">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8517f-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8517f-318">**\_RESOURCEPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="8517f-318">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> <dt>

<span data-ttu-id="8517f-319">[**\_RESOURCEPOOL CIM**](/previous-versions//cc136903(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8517f-319">[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8517f-320">Классы процессоров</span><span class="sxs-lookup"><span data-stu-id="8517f-320">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 


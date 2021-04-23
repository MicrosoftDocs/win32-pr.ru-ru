---
description: Описание типа виртуального ресурса, доступного для использования в виртуальных машинах.
ms.assetid: A93D990E-D921-4113-8D88-218D0F84EFA0
title: Класс Msvm_ResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePool
- Msvm_ResourcePool.InstanceID
- Msvm_ResourcePool.Caption
- Msvm_ResourcePool.Description
- Msvm_ResourcePool.ElementName
- Msvm_ResourcePool.InstallDate
- Msvm_ResourcePool.Name
- Msvm_ResourcePool.OperationalStatus
- Msvm_ResourcePool.StatusDescriptions
- Msvm_ResourcePool.Status
- Msvm_ResourcePool.HealthState
- Msvm_ResourcePool.CommunicationStatus
- Msvm_ResourcePool.DetailedStatus
- Msvm_ResourcePool.OperatingStatus
- Msvm_ResourcePool.PrimaryStatus
- Msvm_ResourcePool.PoolID
- Msvm_ResourcePool.Primordial
- Msvm_ResourcePool.Capacity
- Msvm_ResourcePool.Reserved
- Msvm_ResourcePool.ResourceType
- Msvm_ResourcePool.OtherResourceType
- Msvm_ResourcePool.ResourceSubType
- Msvm_ResourcePool.AllocationUnits
- Msvm_ResourcePool.ConsumedResourceUnits
- Msvm_ResourcePool.CurrentlyConsumedResource
- Msvm_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c45f67a3e1b7c2b4b5291b24beddcdd4cf5e964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265053"
---
# <a name="msvm_resourcepool-class"></a><span data-ttu-id="a0265-103">\_Класс мсвм ResourcePool</span><span class="sxs-lookup"><span data-stu-id="a0265-103">Msvm\_ResourcePool class</span></span>

<span data-ttu-id="a0265-104">Описание типа виртуального ресурса, доступного для использования в виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="a0265-104">Describes a type of virtual resource available for use in virtual machines.</span></span> <span data-ttu-id="a0265-105">Пул ресурсов объединяет физические ресурсы и используется для выделения ресурсов виртуальным машинам.</span><span class="sxs-lookup"><span data-stu-id="a0265-105">The resource pool aggregates physical resources and is used to allocate resources to virtual machines.</span></span> <span data-ttu-id="a0265-106">В Hyper-V все пулы ресурсов являются первичными, и существует ровно один пул для каждого конкретного типа ресурсов, которые могут быть выделены виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a0265-106">In Hyper-V, all resource pools are primordial, and there is exactly one pool for each specific type of resource which may be allocated to a virtual machine.</span></span>

<span data-ttu-id="a0265-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a0265-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0265-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0265-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourcePool : CIM_ResourcePool
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

## <a name="members"></a><span data-ttu-id="a0265-109">Члены</span><span class="sxs-lookup"><span data-stu-id="a0265-109">Members</span></span>

<span data-ttu-id="a0265-110">Класс **мсвм \_ ResourcePool** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a0265-110">The **Msvm\_ResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="a0265-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a0265-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a0265-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="a0265-112">Properties</span></span>

<span data-ttu-id="a0265-113">Класс **мсвм \_ ResourcePool** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a0265-113">The **Msvm\_ResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0265-114">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="a0265-114">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0265-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-117">Единицы распределения, используемые пулом ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a0265-117">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="a0265-118">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))и имеет значение "мегабайт".</span><span class="sxs-lookup"><span data-stu-id="a0265-118">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to "Megabyte".</span></span>

</dd> <dt>

<span data-ttu-id="a0265-119">**Производительность**</span><span class="sxs-lookup"><span data-stu-id="a0265-119">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-120">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a0265-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-122">Максимальный объем активных резервирований (в единицах **аллокатионунитс**), который может поддерживать пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a0265-122">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="a0265-123">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0265-123">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a0265-124">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="a0265-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0265-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-127">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a0265-127">A short description of the object.</span></span> <span data-ttu-id="a0265-128">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a0265-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0265-129">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="a0265-129">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-130">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0265-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-132">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="a0265-132">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a0265-133">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="a0265-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a0265-134">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0265-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a0265-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a0265-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="a0265-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="a0265-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="a0265-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="a0265-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="a0265-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a0265-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a0265-142">)</span><span class="sxs-lookup"><span data-stu-id="a0265-142">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0265-143">**консумедресаурцеунитс**</span><span class="sxs-lookup"><span data-stu-id="a0265-143">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0265-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-146">Указывает единицы для свойств **максконсумаблересаурце** и **куррентликонсумедресаурце** .</span><span class="sxs-lookup"><span data-stu-id="a0265-146">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span>

</dd> <dt>

<span data-ttu-id="a0265-147">**куррентликонсумедресаурце**</span><span class="sxs-lookup"><span data-stu-id="a0265-147">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-148">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a0265-148">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-150">Указывает объем ресурсов, которые в настоящее время предоставляет пул ресурсов для потребителей.</span><span class="sxs-lookup"><span data-stu-id="a0265-150">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="a0265-151">Это свойство отличается от **зарезервированного** свойства тем, что оно описывает представление ресурса "потребители", а **зарезервированное** свойство описывает представление "производители" ресурса.</span><span class="sxs-lookup"><span data-stu-id="a0265-151">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a0265-152">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a0265-152">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0265-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-155">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a0265-155">A description of the object.</span></span> <span data-ttu-id="a0265-156">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a0265-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0265-157">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a0265-157">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-158">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0265-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-160">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="a0265-160">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a0265-161">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="a0265-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a0265-162">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0265-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a0265-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="a0265-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="a0265-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="a0265-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="a0265-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="a0265-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="a0265-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="a0265-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a0265-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a0265-171">)</span><span class="sxs-lookup"><span data-stu-id="a0265-171">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0265-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a0265-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0265-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-175">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="a0265-175">A display name for the object.</span></span> <span data-ttu-id="a0265-176">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a0265-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0265-177">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a0265-177">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-178">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0265-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-180">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="a0265-180">The current health of the element.</span></span> <span data-ttu-id="a0265-181">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0265-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0265-182">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a0265-182">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-183">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a0265-183">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-185">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="a0265-185">The date and time when the object was installed.</span></span> <span data-ttu-id="a0265-186">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="a0265-186">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="a0265-187">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0265-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0265-188">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a0265-188">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0265-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0265-191">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="a0265-191">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a0265-192">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="a0265-192">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a0265-193">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a0265-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0265-194">**максконсумаблересаурце**</span><span class="sxs-lookup"><span data-stu-id="a0265-194">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-195">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a0265-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-197">Указывает максимальный объем потребляемого пула ресурсов, который может предоставляться потребителям.</span><span class="sxs-lookup"><span data-stu-id="a0265-197">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="a0265-198">Это свойство отличается от свойства **Capacity** в том, что оно описывает представление ресурса "потребители", а свойство **Capacity** описывает представление "производители" ресурса.</span><span class="sxs-lookup"><span data-stu-id="a0265-198">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a0265-199">**Name**</span><span class="sxs-lookup"><span data-stu-id="a0265-199">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-200">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0265-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-202">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="a0265-202">The label by which the object is known.</span></span> <span data-ttu-id="a0265-203">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0265-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0265-204">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="a0265-204">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-205">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0265-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-207">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="a0265-207">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a0265-208">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="a0265-208">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a0265-209">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0265-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a0265-210"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a0265-210"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-211"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="a0265-211"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-212"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="a0265-212"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-213"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="a0265-213"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-214"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="a0265-214"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-215"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="a0265-215"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-216"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="a0265-216"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-217"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="a0265-217"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-218"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="a0265-218"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-219"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="a0265-219"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-220"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="a0265-220"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-221"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="a0265-221"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-222"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="a0265-222"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-223"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="a0265-223"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-224"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="a0265-224"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-225"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="a0265-225"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-226"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="a0265-226"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="a0265-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a0265-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a0265-229">)</span><span class="sxs-lookup"><span data-stu-id="a0265-229">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0265-230">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a0265-230">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-231">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a0265-231">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a0265-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0265-233">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="a0265-233">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a0265-234">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="a0265-234">The current statuses of the object.</span></span> <span data-ttu-id="a0265-235">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0265-235">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="a0265-236">Если условия, связанные с QoS, не обнаружены, основное состояние (OperationalStatus \[ 0 \] ) установлено в значение ОК (2).</span><span class="sxs-lookup"><span data-stu-id="a0265-236">If no QoS related conditions have been detected, the primary status (OperationalStatus\[0\]) is set to OK (2).</span></span> <span data-ttu-id="a0265-237">В противном случае в качестве основного состояния устанавливается пониженная работоспособность (3), а в массиве заполняется одно или несколько вторичных значений состояния, начиная с индекса 1, который сообщает о более конкретных условиях в соответствии с этой таблицей.</span><span class="sxs-lookup"><span data-stu-id="a0265-237">Otherwise, the primary status is set to Degraded (3), and one or more secondary status values is filled in the array, starting at index 1, which report more specific conditions, according to this table.</span></span>



| <span data-ttu-id="a0265-238">Значение</span><span class="sxs-lookup"><span data-stu-id="a0265-238">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="a0265-239">Описание</span><span class="sxs-lookup"><span data-stu-id="a0265-239">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0265-240"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Недостаточная пропускная способность (32788)</span><span class="sxs-lookup"><span data-stu-id="a0265-240"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Insufficient Throughput  (32788)</span></span><br/> | <span data-ttu-id="a0265-241">По крайней мере один из виртуальных дисков, выделенных из пула, в настоящее время сообщает о недостаточной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="a0265-241">At least one of the virtual disks allocated from the pool is currently reporting an  Insufficient Throughput  status.</span></span><br/> |



 

<span data-ttu-id="a0265-242">Поставщик WMI Hyper-V создает событие [**мсвм \_ сторажеалерт**](msvm-storagealert.md) каждый раз при изменении класса OperationalStatus **мсвм \_ ResourcePool** .</span><span class="sxs-lookup"><span data-stu-id="a0265-242">The Hyper-V WMI provider raises an [**Msvm\_StorageAlert**](msvm-storagealert.md) event each time the OperationalStatus of the **Msvm\_ResourcePool** class changes.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a0265-243">**ОК** (2)</span><span class="sxs-lookup"><span data-stu-id="a0265-243">**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a0265-244">**Снижение работоспособности** (3)</span><span class="sxs-lookup"><span data-stu-id="a0265-244">**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="a0265-245">**Неустранимая ошибка** (7)</span><span class="sxs-lookup"><span data-stu-id="a0265-245">**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a0265-246">**Нет контакта** (12)</span><span class="sxs-lookup"><span data-stu-id="a0265-246">**No Contact** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="a0265-247">**Потеря связи** (13)</span><span class="sxs-lookup"><span data-stu-id="a0265-247">**Lost Communication** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="a0265-248">**Несоответствие протоколов** (32775)</span><span class="sxs-lookup"><span data-stu-id="a0265-248">**Protocol Mismatch** (32775)</span></span>


</dt> <dd></dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span data-ttu-id="a0265-249">**Недостаточная пропускная способность** (32788)</span><span class="sxs-lookup"><span data-stu-id="a0265-249">**Insufficient Throughput** (32788)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a0265-250">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="a0265-250">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-251">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0265-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-253">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а [**ResourceType**](msvm-processorpool.md) имеет значение 0 ("Other").</span><span class="sxs-lookup"><span data-stu-id="a0265-253">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorpool.md) is set to 0 ("Other").</span></span> <span data-ttu-id="a0265-254">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)) и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a0265-254">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)) and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a0265-255">**пулид**</span><span class="sxs-lookup"><span data-stu-id="a0265-255">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-256">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0265-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-258">На это значение ссылаются экземпляры [**\_ ресаурцеаллокатионсеттингдата CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , которые были выделены из этого пула.</span><span class="sxs-lookup"><span data-stu-id="a0265-258">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="a0265-259">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))и всегда имеет значение "Microsoft:*GUID* \\ root".</span><span class="sxs-lookup"><span data-stu-id="a0265-259">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="a0265-260">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="a0265-260">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-261">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0265-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-263">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="a0265-263">Provides high level status information.</span></span> <span data-ttu-id="a0265-264">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="a0265-264">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="a0265-265">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="a0265-265">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a0265-266">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0265-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a0265-267"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a0265-267"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-268"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="a0265-268"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-269"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="a0265-269"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="a0265-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-271"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="a0265-271"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a0265-272"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a0265-272"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a0265-273">)</span><span class="sxs-lookup"><span data-stu-id="a0265-273">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0265-274">**Исходный пул**</span><span class="sxs-lookup"><span data-stu-id="a0265-274">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-275">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a0265-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-277">**Значение true** , если этот пул ресурсов является базовым, из которого ресурсы рисуются и возвращаются в действии управления ресурсами. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a0265-277">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="a0265-278">Является первичным, это означает, что этот пул ресурсов не может быть создан или удален потребителями этой модели.</span><span class="sxs-lookup"><span data-stu-id="a0265-278">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="a0265-279">Однако другие действия, смоделированные или не связанные с, могут повлиять на характеристики или размер первичных пулов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a0265-279">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="a0265-280">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0265-280">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a0265-281">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="a0265-281">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-282">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a0265-282">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-284">Текущие резервирования (в единицах **аллокатионунитс**) распределяются по всем активным выделениям из этого пула.</span><span class="sxs-lookup"><span data-stu-id="a0265-284">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="a0265-285">В иерархической конфигурации этот параметр представляет сумму всех текущих резервирований пула ресурсов-потомков.</span><span class="sxs-lookup"><span data-stu-id="a0265-285">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="a0265-286">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0265-286">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a0265-287">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="a0265-287">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0265-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-290">Строка, описывающая конкретный подтип реализации для этого пула.</span><span class="sxs-lookup"><span data-stu-id="a0265-290">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="a0265-291">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a0265-291">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="a0265-292">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0265-292">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a0265-293">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="a0265-293">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-294">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0265-294">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-296">Тип ресурса, который может выделить этот пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a0265-296">The type of resource this resource pool may allocate.</span></span> <span data-ttu-id="a0265-297">Это свойство наследуется от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))и имеет значение 4 ("Memory").</span><span class="sxs-lookup"><span data-stu-id="a0265-297">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="a0265-298">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="a0265-298">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-299">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a0265-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0265-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-301">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="a0265-301">The current status of the object.</span></span> <span data-ttu-id="a0265-302">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="a0265-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0265-303">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="a0265-303">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0265-304">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="a0265-304">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a0265-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0265-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0265-306">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="a0265-306">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a0265-307">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0265-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0265-308">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0265-308">Remarks</span></span>

<span data-ttu-id="a0265-309">Доступ к классу **\_ ResourcePool мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="a0265-309">Access to the **Msvm\_ResourcePool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a0265-310">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a0265-310">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0265-311">Требования</span><span class="sxs-lookup"><span data-stu-id="a0265-311">Requirements</span></span>



| <span data-ttu-id="a0265-312">Требование</span><span class="sxs-lookup"><span data-stu-id="a0265-312">Requirement</span></span> | <span data-ttu-id="a0265-313">Значение</span><span class="sxs-lookup"><span data-stu-id="a0265-313">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0265-314">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0265-314">Minimum supported client</span></span><br/> | <span data-ttu-id="a0265-315">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a0265-315">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a0265-316">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0265-316">Minimum supported server</span></span><br/> | <span data-ttu-id="a0265-317">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a0265-317">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a0265-318">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a0265-318">Namespace</span></span><br/>                | <span data-ttu-id="a0265-319">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a0265-319">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a0265-320">MOF</span><span class="sxs-lookup"><span data-stu-id="a0265-320">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0265-321"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0265-321"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0265-322">DLL</span><span class="sxs-lookup"><span data-stu-id="a0265-322">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0265-323"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a0265-323"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a0265-324">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0265-324">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0265-325">**\_RESOURCEPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="a0265-325">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> <dt>

<span data-ttu-id="a0265-326">[**\_RESOURCEPOOL CIM**](/previous-versions//cc136903(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a0265-326">[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a0265-327">**Мсвм \_ ResourcePool (v1)**</span><span class="sxs-lookup"><span data-stu-id="a0265-327">**Msvm\_ResourcePool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourcepool)
</dt> <dt>

[<span data-ttu-id="a0265-328">**Мсвм \_ сторажеалерт**</span><span class="sxs-lookup"><span data-stu-id="a0265-328">**Msvm\_StorageAlert**</span></span>](msvm-storagealert.md)
</dt> <dt>

[<span data-ttu-id="a0265-329">Классы управления ресурсами</span><span class="sxs-lookup"><span data-stu-id="a0265-329">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 


---
description: Определяет средства, с помощью которых клиент может обнаружить допустимый диапазон параметров по умолчанию для виртуального ресурса.
ms.assetid: AC516723-7CD2-4F10-B8BF-EF9D458D3E5B
title: Класс Msvm_AllocationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AllocationCapabilities
- Msvm_AllocationCapabilities.InstanceID
- Msvm_AllocationCapabilities.Caption
- Msvm_AllocationCapabilities.Description
- Msvm_AllocationCapabilities.ElementName
- Msvm_AllocationCapabilities.ResourceType
- Msvm_AllocationCapabilities.OtherResourceType
- Msvm_AllocationCapabilities.ResourceSubType
- Msvm_AllocationCapabilities.RequestTypesSupported
- Msvm_AllocationCapabilities.SharingMode
- Msvm_AllocationCapabilities.SupportedAddStates
- Msvm_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7642d1b590affcb3704f7d854d65edb5481c2285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684360"
---
# <a name="msvm_allocationcapabilities-class"></a><span data-ttu-id="dbd7a-103">\_Класс мсвм аллокатионкапабилитиес</span><span class="sxs-lookup"><span data-stu-id="dbd7a-103">Msvm\_AllocationCapabilities class</span></span>

<span data-ttu-id="dbd7a-104">Определяет средства, с помощью которых клиент может обнаружить допустимый диапазон параметров по умолчанию для виртуального ресурса.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-104">Defines the means by which a client can discover the valid range of default settings for a virtual resource.</span></span> <span data-ttu-id="dbd7a-105">Объект **\_ аллокатионкапабилитиес мсвм** связан с каждым пулом ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-105">A **Msvm\_AllocationCapabilities** object is associated with each resource pool.</span></span> <span data-ttu-id="dbd7a-106">Четыре объекта [**мсвм \_ ресаурцеаллокатионсеттингдата**](msvm-resourceallocationsettingdata.md) связаны с объектом **мсвм \_ аллокатионкапабилитиес** для описания минимального, максимального, по умолчанию и добавочных значений для выделения данного ресурса.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-106">Four [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) objects are associated with the **Msvm\_AllocationCapabilities** object to describe the minimum, maximum, default, and incremental values for the given resource's allocation.</span></span> <span data-ttu-id="dbd7a-107">Вместе эти классы описывают общий диапазон поддерживаемых возможностей.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-107">Together, these classes describe the overall range of supported capabilities.</span></span>

<span data-ttu-id="dbd7a-108">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbd7a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbd7a-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AllocationCapabilities : CIM_AllocationCapabilities
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a><span data-ttu-id="dbd7a-110">Члены</span><span class="sxs-lookup"><span data-stu-id="dbd7a-110">Members</span></span>

<span data-ttu-id="dbd7a-111">Класс **мсвм \_ аллокатионкапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dbd7a-111">The **Msvm\_AllocationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="dbd7a-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="dbd7a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbd7a-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="dbd7a-113">Properties</span></span>

<span data-ttu-id="dbd7a-114">Класс **мсвм \_ аллокатионкапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-114">The **Msvm\_AllocationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbd7a-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd7a-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbd7a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-118">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-118">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="dbd7a-119">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-119">A short description of the object.</span></span> <span data-ttu-id="dbd7a-120">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dbd7a-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dbd7a-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd7a-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbd7a-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbd7a-124">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-124">A description of the object.</span></span> <span data-ttu-id="dbd7a-125">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dbd7a-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dbd7a-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd7a-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbd7a-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbd7a-129">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-129">A display name for the object.</span></span> <span data-ttu-id="dbd7a-130">Это свойство позволяет каждому экземпляру определить отображаемое имя в дополнение к его ключевым свойствам, идентификационным данным и сведениям о описании.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-130">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="dbd7a-131">Свойство [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) класса **CIM \_ манажедсистемелемент** также определяется как отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-131">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="dbd7a-132">Но часто этот класс является ключом.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-132">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="dbd7a-133">Не целесообразно, что одно и то же свойство может передать как удостоверение, так и отображаемое имя без несогласованности.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-133">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="dbd7a-134">Если [**имя**](msvm-keyboard.md) существует и не является ключом (например, для экземпляров логического устройства), то одни и те же сведения могут присутствовать в свойствах **Name** и **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="dbd7a-134">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of a logical device), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="dbd7a-135">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dbd7a-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dbd7a-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd7a-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbd7a-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbd7a-139">Уникальный идентификатор для этого пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-139">A unique identifier for this resource pool.</span></span> <span data-ttu-id="dbd7a-140">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dbd7a-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dbd7a-141">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-141">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd7a-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbd7a-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbd7a-144">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а **ResourceType** имеет значение other.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-144">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="dbd7a-145">Это свойство наследуется от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="dbd7a-145">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="dbd7a-146">**рекуесттипессуппортед**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-146">**RequestTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd7a-147">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbd7a-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbd7a-149">Указывает, поддерживается ли запрос определенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-149">Indicates whether requesting a specific resource is supported.</span></span> <span data-ttu-id="dbd7a-150">Это свойство наследуется от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="dbd7a-150">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>



| <span data-ttu-id="dbd7a-151">Значение</span><span class="sxs-lookup"><span data-stu-id="dbd7a-151">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="dbd7a-152">Значение</span><span class="sxs-lookup"><span data-stu-id="dbd7a-152">Meaning</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="dbd7a-153"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dbd7a-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="dbd7a-154">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="dbd7a-154">Unknown</span></span><br/>                                                         |
| <span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span><dl> <span data-ttu-id="dbd7a-155"><dt>**Конкретное**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dbd7a-155"><dt>**Specific**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="dbd7a-156">Запрос может включать запрос определенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-156">The request can include a request for a specific resource.</span></span><br/>      |
| <span id="General"></span><span id="general"></span><span id="GENERAL"></span><dl> <span data-ttu-id="dbd7a-157"><dt>**Общее**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="dbd7a-157"><dt>**General**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="dbd7a-158">Запрос не включает запрос определенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-158">The request does not include a request for a specific resource.</span></span><br/> |
| <span id="Both"></span><span id="both"></span><span id="BOTH"></span><dl> <span data-ttu-id="dbd7a-159"><dt>**Оба**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="dbd7a-159"><dt>**Both**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="dbd7a-160">Поддерживаются как конкретные, так и общие запросы.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-160">Both specific and general requests are supported.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="dbd7a-161">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-161">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd7a-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbd7a-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbd7a-164">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-164">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="dbd7a-165">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-165">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="dbd7a-166">Это свойство наследуется от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="dbd7a-166">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="dbd7a-167">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-167">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd7a-168">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbd7a-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbd7a-170">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-170">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="dbd7a-171">Это свойство наследуется от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="dbd7a-171">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="dbd7a-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-173"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Компьютерная система** (2)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-173"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-174"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Процессор** (3)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-174"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-175"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Память** (4)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-175"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-176"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-контроллер** (5)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-176"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-177"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Параллельный SCSI HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-177"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-178"><span id="FC_HBA"></span><span id="fc_hba"></span>**Адаптер шины FC** (7)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-178"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-179"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**адаптер шины iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-179"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-180"><span id="IB_HCA"></span><span id="ib_hca"></span>**Геохка** (9)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-180"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-181"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-адаптер** (10)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-181"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-182"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Другой сетевой адаптер** (11)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-182"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-183"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Разъем ввода-вывода** (12)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-183"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-184"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Устройство ввода-вывода** (13)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-184"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-185"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>Дисковод **гибких дисков** (14)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-185"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-186"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Дисковод компакт-дисков** (15)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-186"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-187"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-дисковод** (16)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-187"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-188"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Диск** (17)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-188"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-189"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Ленточный накопитель** (18)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-189"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-190"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Область хранения** (19)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-190"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-191"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Другое запоминающее устройство** (20)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-191"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-192"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Последовательный порт** (21)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-192"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-193"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Параллельный порт** (22)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-193"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-194"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Контроллер USB** (23)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-194"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-195"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Графический контроллер** (24)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-195"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-196"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Контроллер IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-196"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-197"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Единица секционирования** (26)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-197"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-198"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Базовая единица секционирования** (27)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-198"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-199"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Мощность** (28)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-199"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-200"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Емкость системы охлаждения** (29)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-200"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Cooling Capacity** (29)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-201"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Порт коммутатора Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-201"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-202"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Логический диск** (31)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-202"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-203"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Том хранилища** (32)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-203"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-204"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet-подключение** (33)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-204"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet Connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-205"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-205"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-206"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="dbd7a-206"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dbd7a-207">**шарингмоде**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-207">**SharingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd7a-208">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbd7a-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbd7a-210">Указывает, как предоставляется доступ к базовому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-210">Indicates how access to an underlying resource is granted.</span></span> <span data-ttu-id="dbd7a-211">Это свойство наследуется от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="dbd7a-211">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>



| <span data-ttu-id="dbd7a-212">Значение</span><span class="sxs-lookup"><span data-stu-id="dbd7a-212">Value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="dbd7a-213">Значение</span><span class="sxs-lookup"><span data-stu-id="dbd7a-213">Meaning</span></span>                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="dbd7a-214"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dbd7a-214"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="dbd7a-215">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="dbd7a-215">Unknown</span></span><br/>                                     |
| <span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span><dl> <span data-ttu-id="dbd7a-216"><dt>**Выделенный**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dbd7a-216"><dt>**Dedicated**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="dbd7a-217">Монопольный доступ к базовому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-217">Exclusive access to an underlying resource.</span></span><br/> |
| <span id="Shared"></span><span id="shared"></span><span id="SHARED"></span><dl> <span data-ttu-id="dbd7a-218"><dt>**Общее**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="dbd7a-218"><dt>**Shared**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="dbd7a-219">Общее использование базового ресурса.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-219">Shared use of an underlying resource.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="dbd7a-220">**суппортедаддстатес**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-220">**SupportedAddStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd7a-221">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dbd7a-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbd7a-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbd7a-223">Указывает состояния, в которых система, с которой будет связан ресурс, может входить в систему при создании нового ресурса.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-223">Indicates the states that the system to which the resource will be associated can be in when a new resource is created.</span></span> <span data-ttu-id="dbd7a-224">Это свойство наследуется от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="dbd7a-224">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="dbd7a-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-228"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-228"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-229"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-229"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-230"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Включено, но отключено** (6)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-230"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-231"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (7)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-231"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-232"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Отложено** (8)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-232"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-233"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-233"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (10)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-235"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (11)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-235"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (11)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-236"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Приостановлено** (12)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-236"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (12)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="dbd7a-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dbd7a-239">**суппортедремовестатес**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-239">**SupportedRemoveStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd7a-240">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dbd7a-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbd7a-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbd7a-242">Указывает состояния, в которых система, с которой связан ресурс, может находиться в случае удаления ресурса.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-242">Indicates the states that the system to which the resource is associated can be in when the resource is removed.</span></span> <span data-ttu-id="dbd7a-243">Это свойство наследуется от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="dbd7a-243">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="dbd7a-244"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-244"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-245"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-245"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-246"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-246"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-247"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-247"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-248"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-248"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-249"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Включено, но отключено** (6)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-249"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-250"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (7)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-250"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-251"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Отложено** (8)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-251"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-252"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-252"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-253"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (10)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-253"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-254"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (11)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-254"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (11)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-255"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Приостановлено** (12)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-255"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (12)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-256"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="dbd7a-256"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dbd7a-257"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="dbd7a-257"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbd7a-258">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbd7a-258">Remarks</span></span>

<span data-ttu-id="dbd7a-259">Доступ к классу **\_ аллокатионкапабилитиес мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-259">Access to the **Msvm\_AllocationCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dbd7a-260">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="dbd7a-260">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbd7a-261">Требования</span><span class="sxs-lookup"><span data-stu-id="dbd7a-261">Requirements</span></span>



| <span data-ttu-id="dbd7a-262">Требование</span><span class="sxs-lookup"><span data-stu-id="dbd7a-262">Requirement</span></span> | <span data-ttu-id="dbd7a-263">Значение</span><span class="sxs-lookup"><span data-stu-id="dbd7a-263">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbd7a-264">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbd7a-264">Minimum supported client</span></span><br/> | <span data-ttu-id="dbd7a-265">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dbd7a-265">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dbd7a-266">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbd7a-266">Minimum supported server</span></span><br/> | <span data-ttu-id="dbd7a-267">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dbd7a-267">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dbd7a-268">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dbd7a-268">Namespace</span></span><br/>                | <span data-ttu-id="dbd7a-269">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="dbd7a-269">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dbd7a-270">MOF</span><span class="sxs-lookup"><span data-stu-id="dbd7a-270">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbd7a-271"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbd7a-271"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbd7a-272">DLL</span><span class="sxs-lookup"><span data-stu-id="dbd7a-272">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbd7a-273"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dbd7a-273"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dbd7a-274">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbd7a-274">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbd7a-275">**\_АЛЛОКАТИОНКАПАБИЛИТИЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-275">**CIM\_AllocationCapabilities**</span></span>](cim-allocationcapabilities.md)
</dt> <dt>

[<span data-ttu-id="dbd7a-276">**\_АЛЛОКАТИОНКАПАБИЛИТИЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-276">**CIM\_AllocationCapabilities**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)
</dt> <dt>

[<span data-ttu-id="dbd7a-277">**Мсвм \_ аллокатионкапабилитиес (v1)**</span><span class="sxs-lookup"><span data-stu-id="dbd7a-277">**Msvm\_AllocationCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-allocationcapabilities)
</dt> <dt>

[<span data-ttu-id="dbd7a-278">Классы управления ресурсами</span><span class="sxs-lookup"><span data-stu-id="dbd7a-278">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 


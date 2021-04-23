---
description: Представляет параметры \_ экземпляра ResourcePool мсвм, не связанные с выделением.
ms.assetid: 32e0066c-7e14-454c-8aa9-06e093ef8072
title: Класс Msvm_ResourcePoolSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolSettingData
- Msvm_ResourcePoolSettingData.InstanceID
- Msvm_ResourcePoolSettingData.Caption
- Msvm_ResourcePoolSettingData.Description
- Msvm_ResourcePoolSettingData.ElementName
- Msvm_ResourcePoolSettingData.PoolID
- Msvm_ResourcePoolSettingData.ResourceType
- Msvm_ResourcePoolSettingData.OtherResourceType
- Msvm_ResourcePoolSettingData.ResourceSubType
- Msvm_ResourcePoolSettingData.LoadBalancingBehavior
- Msvm_ResourcePoolSettingData.MappingBehavior
- Msvm_ResourcePoolSettingData.MappingOrder
- Msvm_ResourcePoolSettingData.Notes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37ec7dc6600dbc536ac50a2042e7d53ff8043242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650824"
---
# <a name="msvm_resourcepoolsettingdata-class"></a><span data-ttu-id="6f99e-103">\_Класс мсвм ресаурцепулсеттингдата</span><span class="sxs-lookup"><span data-stu-id="6f99e-103">Msvm\_ResourcePoolSettingData class</span></span>

<span data-ttu-id="6f99e-104">Представляет параметры экземпляра [**\_ ResourcePool мсвм**](msvm-resourcepool.md) , не связанные с выделением.</span><span class="sxs-lookup"><span data-stu-id="6f99e-104">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span>

<span data-ttu-id="6f99e-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6f99e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f99e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f99e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourcePoolSettingData : Msvm_AbstractResourcePoolSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string PoolID;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 LoadBalancingBehavior;
  uint16 MappingBehavior;
  string MappingOrder[];
  string Notes;
};
```

## <a name="members"></a><span data-ttu-id="6f99e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6f99e-107">Members</span></span>

<span data-ttu-id="6f99e-108">Класс **мсвм \_ ресаурцепулсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6f99e-108">The **Msvm\_ResourcePoolSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="6f99e-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="6f99e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f99e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="6f99e-110">Properties</span></span>

<span data-ttu-id="6f99e-111">Класс **мсвм \_ ресаурцепулсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6f99e-111">The **Msvm\_ResourcePoolSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f99e-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="6f99e-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f99e-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f99e-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f99e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f99e-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6f99e-115">A short description of the object.</span></span> <span data-ttu-id="6f99e-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6f99e-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f99e-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6f99e-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f99e-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f99e-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f99e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f99e-120">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6f99e-120">A description of the object.</span></span> <span data-ttu-id="6f99e-121">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6f99e-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f99e-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6f99e-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f99e-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f99e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f99e-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f99e-125">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="6f99e-125">A display name for the object.</span></span> <span data-ttu-id="6f99e-126">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6f99e-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f99e-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6f99e-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f99e-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f99e-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f99e-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-130">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="6f99e-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6f99e-131">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="6f99e-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6f99e-132">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6f99e-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6f99e-133">**лоадбаланЦингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="6f99e-133">**LoadBalancingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f99e-134">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f99e-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f99e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f99e-136">Указывает стратегию распределения, используемую пулом ресурсов для балансировки использования ресурсов в совокупных ресурсах.</span><span class="sxs-lookup"><span data-stu-id="6f99e-136">Specifies the allocation strategy to be used by the resource pool to balance resource usage across its aggregated resources.</span></span> <span data-ttu-id="6f99e-137">Это свойство наследуется от [**мсвм \_ абстрактресаурцепулсеттингдата**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="6f99e-137">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="6f99e-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="6f99e-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (2)</span><span class="sxs-lookup"><span data-stu-id="6f99e-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Нет** (3)</span><span class="sxs-lookup"><span data-stu-id="6f99e-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-141"><span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>**Распределено** (4)</span><span class="sxs-lookup"><span data-stu-id="6f99e-141"><span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>**Distributed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-142"><span id="Consolidated_"></span><span id="consolidated_"></span><span id="CONSOLIDATED_"></span>**Консолидировано** (5)</span><span class="sxs-lookup"><span data-stu-id="6f99e-142"><span id="Consolidated_"></span><span id="consolidated_"></span><span id="CONSOLIDATED_"></span>**Consolidated** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6f99e-143">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="6f99e-143">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f99e-144">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f99e-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f99e-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f99e-146">Указывает, может ли пул ресурсов попытаться использовать другие ресурсы узла для удовлетворения запроса на выделение, если не удается выделить нужные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="6f99e-146">Specifies whether the resource pool can attempt to use other host resources to satisfy the allocation request if the desired resources cannot be allocated.</span></span> <span data-ttu-id="6f99e-147">Это свойство наследуется от [**мсвм \_ абстрактресаурцепулсеттингдата**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="6f99e-147">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="6f99e-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="6f99e-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-149"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (2)</span><span class="sxs-lookup"><span data-stu-id="6f99e-149"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-150"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (3)</span><span class="sxs-lookup"><span data-stu-id="6f99e-150"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-151"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Мягкое сходство** (4)</span><span class="sxs-lookup"><span data-stu-id="6f99e-151"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Soft Affinity** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-152"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Жесткое сходство** (5)</span><span class="sxs-lookup"><span data-stu-id="6f99e-152"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Hard Affinity** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="6f99e-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Зарезервировано поставщиком** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6f99e-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32767..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6f99e-155">**маппингордер**</span><span class="sxs-lookup"><span data-stu-id="6f99e-155">**MappingOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f99e-156">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="6f99e-156">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f99e-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f99e-158">Указывает порядок, в котором ресурсы узла, доступные через этот пул, будут выбраны при попытке удовлетворить запрос на выделение, а запрошенный ресурс узла недоступен или не указан ресурс узла.</span><span class="sxs-lookup"><span data-stu-id="6f99e-158">Specifies the order in which host resources available through this pool will be selected when attempting to satisfy an allocation request, and the requested host resource is not available or no host resource is specified.</span></span> <span data-ttu-id="6f99e-159">Это свойство наследуется от [**мсвм \_ абстрактресаурцепулсеттингдата**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="6f99e-159">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f99e-160">**Примечания**</span><span class="sxs-lookup"><span data-stu-id="6f99e-160">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f99e-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f99e-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f99e-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f99e-163">Заметки конечного пользователя, связанные с этим пулом ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f99e-163">End-user supplied notes that are related to this resource pool.</span></span> <span data-ttu-id="6f99e-164">Это свойство наследуется от [**мсвм \_ абстрактресаурцепулсеттингдата**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="6f99e-164">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f99e-165">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="6f99e-165">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f99e-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f99e-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f99e-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f99e-168">Строка, описывающая тип ресурса, когда хорошо определенное значение недоступно, а **ResourceType** имеет значение 0 (другое).</span><span class="sxs-lookup"><span data-stu-id="6f99e-168">A string that describes the resource type when a well defined value is not available and **ResourceType** is set to 0 (Other).</span></span> <span data-ttu-id="6f99e-169">Это свойство наследуется от [**мсвм \_ абстрактресаурцепулсеттингдата**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="6f99e-169">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f99e-170">**пулид**</span><span class="sxs-lookup"><span data-stu-id="6f99e-170">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f99e-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f99e-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f99e-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f99e-173">Идентификатор пула.</span><span class="sxs-lookup"><span data-stu-id="6f99e-173">An identifier for the pool.</span></span> <span data-ttu-id="6f99e-174">Это свойство используется для обеспечения корреляции между сохранением и восстановлением данных конфигурации в базовое постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="6f99e-174">This property is used to provide correlation across save and restore of configuration data to underlying persistent storage.</span></span> <span data-ttu-id="6f99e-175">Это свойство наследуется от [**мсвм \_ абстрактресаурцепулсеттингдата**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="6f99e-175">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f99e-176">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="6f99e-176">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f99e-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f99e-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f99e-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f99e-179">Строка, описывающая подтип для этого пула, зависящий от реализации.</span><span class="sxs-lookup"><span data-stu-id="6f99e-179">A string that describes an implementation-specific subtype for this pool.</span></span> <span data-ttu-id="6f99e-180">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f99e-180">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="6f99e-181">Это свойство наследуется от [**мсвм \_ абстрактресаурцепулсеттингдата**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="6f99e-181">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f99e-182">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="6f99e-182">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f99e-183">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f99e-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f99e-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f99e-185">Тип ресурса, который может выделить этот пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f99e-185">The type of resource this resource pool can allocate.</span></span> <span data-ttu-id="6f99e-186">Это свойство наследуется от [**мсвм \_ абстрактресаурцепулсеттингдата**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="6f99e-186">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="6f99e-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="6f99e-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-188"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Компьютерная система** (2)</span><span class="sxs-lookup"><span data-stu-id="6f99e-188"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-189"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Процессор** (3)</span><span class="sxs-lookup"><span data-stu-id="6f99e-189"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-190"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Память** (4)</span><span class="sxs-lookup"><span data-stu-id="6f99e-190"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-191"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-контроллер** (5)</span><span class="sxs-lookup"><span data-stu-id="6f99e-191"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-192"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Параллельный SCSI HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="6f99e-192"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-193"><span id="FC_HBA"></span><span id="fc_hba"></span>**Адаптер шины FC** (7)</span><span class="sxs-lookup"><span data-stu-id="6f99e-193"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-194"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**адаптер шины iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="6f99e-194"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-195"><span id="IB_HCA"></span><span id="ib_hca"></span>**Геохка** (9)</span><span class="sxs-lookup"><span data-stu-id="6f99e-195"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-196"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-адаптер** (10)</span><span class="sxs-lookup"><span data-stu-id="6f99e-196"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-197"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Другой сетевой адаптер** (11)</span><span class="sxs-lookup"><span data-stu-id="6f99e-197"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-198"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Разъем ввода-вывода** (12)</span><span class="sxs-lookup"><span data-stu-id="6f99e-198"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-199"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Устройство ввода-вывода** (13)</span><span class="sxs-lookup"><span data-stu-id="6f99e-199"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-200"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>Дисковод **гибких дисков** (14)</span><span class="sxs-lookup"><span data-stu-id="6f99e-200"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-201"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Дисковод компакт-дисков** (15)</span><span class="sxs-lookup"><span data-stu-id="6f99e-201"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-202"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-дисковод** (16)</span><span class="sxs-lookup"><span data-stu-id="6f99e-202"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-203"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Диск** (17)</span><span class="sxs-lookup"><span data-stu-id="6f99e-203"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-204"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Ленточный накопитель** (18)</span><span class="sxs-lookup"><span data-stu-id="6f99e-204"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-205"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Область хранения** (19)</span><span class="sxs-lookup"><span data-stu-id="6f99e-205"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-206"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Другое запоминающее устройство** (20)</span><span class="sxs-lookup"><span data-stu-id="6f99e-206"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-207"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Последовательный порт** (21)</span><span class="sxs-lookup"><span data-stu-id="6f99e-207"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-208"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Параллельный порт** (22)</span><span class="sxs-lookup"><span data-stu-id="6f99e-208"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-209"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Контроллер USB** (23)</span><span class="sxs-lookup"><span data-stu-id="6f99e-209"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-210"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Графический контроллер** (24)</span><span class="sxs-lookup"><span data-stu-id="6f99e-210"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-211"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Контроллер IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="6f99e-211"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-212"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Единица секционирования** (26)</span><span class="sxs-lookup"><span data-stu-id="6f99e-212"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-213"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Базовая единица секционирования** (27)</span><span class="sxs-lookup"><span data-stu-id="6f99e-213"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-214"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Мощность** (28)</span><span class="sxs-lookup"><span data-stu-id="6f99e-214"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-215"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Емкость системы охлаждения** (29)</span><span class="sxs-lookup"><span data-stu-id="6f99e-215"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Cooling Capacity** (29)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-216"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Порт коммутатора Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="6f99e-216"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-217"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Логический диск** (31)</span><span class="sxs-lookup"><span data-stu-id="6f99e-217"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-218"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Том хранилища** (32)</span><span class="sxs-lookup"><span data-stu-id="6f99e-218"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-219"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet-подключение** (33)</span><span class="sxs-lookup"><span data-stu-id="6f99e-219"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet Connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-220"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="6f99e-220"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6f99e-221"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="6f99e-221"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f99e-222">Требования</span><span class="sxs-lookup"><span data-stu-id="6f99e-222">Requirements</span></span>



| <span data-ttu-id="6f99e-223">Требование</span><span class="sxs-lookup"><span data-stu-id="6f99e-223">Requirement</span></span> | <span data-ttu-id="6f99e-224">Значение</span><span class="sxs-lookup"><span data-stu-id="6f99e-224">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f99e-225">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f99e-225">Minimum supported client</span></span><br/> | <span data-ttu-id="6f99e-226">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6f99e-226">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6f99e-227">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f99e-227">Minimum supported server</span></span><br/> | <span data-ttu-id="6f99e-228">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6f99e-228">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f99e-229">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6f99e-229">Namespace</span></span><br/>                | <span data-ttu-id="6f99e-230">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6f99e-230">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6f99e-231">MOF</span><span class="sxs-lookup"><span data-stu-id="6f99e-231">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f99e-232"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f99e-232"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f99e-233">DLL</span><span class="sxs-lookup"><span data-stu-id="6f99e-233">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f99e-234"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f99e-234"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


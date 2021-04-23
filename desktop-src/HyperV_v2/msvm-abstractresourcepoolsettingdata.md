---
description: Представляет параметры \_ экземпляра ResourcePool мсвм, не связанные с выделением.
ms.assetid: c5954a92-8942-4b45-aae2-6936328dab1a
title: Класс Msvm_AbstractResourcePoolSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AbstractResourcePoolSettingData
- Msvm_AbstractResourcePoolSettingData.InstanceID
- Msvm_AbstractResourcePoolSettingData.Caption
- Msvm_AbstractResourcePoolSettingData.Description
- Msvm_AbstractResourcePoolSettingData.ElementName
- Msvm_AbstractResourcePoolSettingData.PoolID
- Msvm_AbstractResourcePoolSettingData.ResourceType
- Msvm_AbstractResourcePoolSettingData.OtherResourceType
- Msvm_AbstractResourcePoolSettingData.ResourceSubType
- Msvm_AbstractResourcePoolSettingData.LoadBalancingBehavior
- Msvm_AbstractResourcePoolSettingData.MappingBehavior
- Msvm_AbstractResourcePoolSettingData.MappingOrder
- Msvm_AbstractResourcePoolSettingData.Notes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9109bd428797c8c4f1073577e015bf4b9eddcc07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998832"
---
# <a name="msvm_abstractresourcepoolsettingdata-class"></a><span data-ttu-id="618c8-103">\_Класс мсвм абстрактресаурцепулсеттингдата</span><span class="sxs-lookup"><span data-stu-id="618c8-103">Msvm\_AbstractResourcePoolSettingData class</span></span>

<span data-ttu-id="618c8-104">Представляет параметры экземпляра [**\_ ResourcePool мсвм**](msvm-resourcepool.md) , не связанные с выделением.</span><span class="sxs-lookup"><span data-stu-id="618c8-104">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span>

<span data-ttu-id="618c8-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="618c8-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="618c8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="618c8-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Msvm_AbstractResourcePoolSettingData : CIM_SettingData
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

## <a name="members"></a><span data-ttu-id="618c8-107">Члены</span><span class="sxs-lookup"><span data-stu-id="618c8-107">Members</span></span>

<span data-ttu-id="618c8-108">Класс **мсвм \_ абстрактресаурцепулсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="618c8-108">The **Msvm\_AbstractResourcePoolSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="618c8-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="618c8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="618c8-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="618c8-110">Properties</span></span>

<span data-ttu-id="618c8-111">Класс **мсвм \_ абстрактресаурцепулсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="618c8-111">The **Msvm\_AbstractResourcePoolSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="618c8-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="618c8-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="618c8-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="618c8-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="618c8-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="618c8-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="618c8-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="618c8-115">A short description of the object.</span></span> <span data-ttu-id="618c8-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="618c8-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="618c8-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="618c8-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="618c8-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="618c8-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="618c8-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="618c8-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="618c8-120">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="618c8-120">A description of the object.</span></span> <span data-ttu-id="618c8-121">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="618c8-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="618c8-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="618c8-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="618c8-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="618c8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="618c8-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="618c8-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="618c8-125">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="618c8-125">A display name for the object.</span></span> <span data-ttu-id="618c8-126">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="618c8-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="618c8-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="618c8-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="618c8-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="618c8-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="618c8-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="618c8-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="618c8-130">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="618c8-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="618c8-131">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="618c8-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="618c8-132">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="618c8-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="618c8-133">**лоадбаланЦингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="618c8-133">**LoadBalancingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="618c8-134">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="618c8-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="618c8-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="618c8-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="618c8-136">Указывает стратегию распределения, используемую пулом ресурсов для балансировки использования ресурсов в совокупных ресурсах.</span><span class="sxs-lookup"><span data-stu-id="618c8-136">Specifies the allocation strategy to be used by the resource pool to balance resource usage across its aggregated resources.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="618c8-137">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="618c8-137">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="618c8-138">**Не поддерживается** (2)</span><span class="sxs-lookup"><span data-stu-id="618c8-138">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="618c8-139">**Нет** (3)</span><span class="sxs-lookup"><span data-stu-id="618c8-139">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>

<span data-ttu-id="618c8-140">**Распределено** (4)</span><span class="sxs-lookup"><span data-stu-id="618c8-140">**Distributed** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Consolidated"></span><span id="consolidated"></span><span id="CONSOLIDATED"></span>

<span data-ttu-id="618c8-141">**Консолидировано** (5)</span><span class="sxs-lookup"><span data-stu-id="618c8-141">**Consolidated** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="618c8-142">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="618c8-142">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="618c8-143">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="618c8-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="618c8-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="618c8-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="618c8-145">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md).**Маппингбехавиор**")</span><span class="sxs-lookup"><span data-stu-id="618c8-145">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="618c8-146">Указывает, может ли пул ресурсов попытаться использовать другие ресурсы узла для удовлетворения запроса на выделение, если не удается выделить нужные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="618c8-146">Specifies whether the resource pool can attempt to use other host resources to satisfy the allocation request if the desired resources cannot be allocated.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="618c8-147">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="618c8-147">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="618c8-148">**Не поддерживается** (2)</span><span class="sxs-lookup"><span data-stu-id="618c8-148">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="618c8-149">**Выделенный** (3)</span><span class="sxs-lookup"><span data-stu-id="618c8-149">**Dedicated** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

<span data-ttu-id="618c8-150">**Мягкое сходство** (4)</span><span class="sxs-lookup"><span data-stu-id="618c8-150">**Soft Affinity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

<span data-ttu-id="618c8-151">**Жесткое сходство** (5)</span><span class="sxs-lookup"><span data-stu-id="618c8-151">**Hard Affinity** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="618c8-152">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="618c8-152">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="618c8-153">**Зарезервировано поставщиком** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="618c8-153">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="618c8-154">**маппингордер**</span><span class="sxs-lookup"><span data-stu-id="618c8-154">**MappingOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="618c8-155">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="618c8-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="618c8-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="618c8-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="618c8-157">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**мсвм \_ ресаурцепулсеттингдата**](msvm-resourcepoolsettingdata.md).**Маппингбехавиор**")</span><span class="sxs-lookup"><span data-stu-id="618c8-157">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="618c8-158">Указывает порядок, в котором ресурсы узла, доступные через этот пул, будут выбраны при попытке удовлетворить запрос на выделение, а запрошенный ресурс узла недоступен или не указан ресурс узла.</span><span class="sxs-lookup"><span data-stu-id="618c8-158">Specifies the order in which host resources available through this pool will be selected when attempting to satisfy an allocation request, and the requested host resource is not available or no host resource is specified.</span></span>

</dd> <dt>

<span data-ttu-id="618c8-159">**Примечания**</span><span class="sxs-lookup"><span data-stu-id="618c8-159">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="618c8-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="618c8-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="618c8-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="618c8-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="618c8-162">Заметки конечного пользователя, связанные с этим пулом ресурсов.</span><span class="sxs-lookup"><span data-stu-id="618c8-162">End-user supplied notes that are related to this resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="618c8-163">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="618c8-163">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="618c8-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="618c8-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="618c8-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="618c8-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="618c8-166">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**Осерресаурцетипе**")</span><span class="sxs-lookup"><span data-stu-id="618c8-166">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**OtherResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="618c8-167">Строка, описывающая тип ресурса, когда хорошо определенное значение недоступно, а **ResourceType** имеет значение 0 (другое).</span><span class="sxs-lookup"><span data-stu-id="618c8-167">A string that describes the resource type when a well defined value is not available and **ResourceType** is set to 0 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="618c8-168">**пулид**</span><span class="sxs-lookup"><span data-stu-id="618c8-168">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="618c8-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="618c8-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="618c8-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="618c8-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="618c8-171">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**Пулид**")</span><span class="sxs-lookup"><span data-stu-id="618c8-171">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**PoolID**")</span></span>
</dt> </dl>

<span data-ttu-id="618c8-172">Идентификатор пула.</span><span class="sxs-lookup"><span data-stu-id="618c8-172">An identifier for the pool.</span></span> <span data-ttu-id="618c8-173">Это свойство используется для обеспечения корреляции между сохранением и восстановлением данных конфигурации в базовое постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="618c8-173">This property is used to provide correlation across save and restore of configuration data to underlying persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="618c8-174">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="618c8-174">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="618c8-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="618c8-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="618c8-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="618c8-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="618c8-177">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**Ресаурцесубтипе**")</span><span class="sxs-lookup"><span data-stu-id="618c8-177">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="618c8-178">Строка, описывающая конкретный подтип реализации для этого пула.</span><span class="sxs-lookup"><span data-stu-id="618c8-178">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="618c8-179">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="618c8-179">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="618c8-180">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="618c8-180">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="618c8-181">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="618c8-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="618c8-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="618c8-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="618c8-183">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="618c8-183">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="618c8-184">Тип ресурса, который может выделить этот пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="618c8-184">The type of resource this resource pool can allocate.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="618c8-185">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="618c8-185">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="618c8-186">**Компьютерная система** (2)</span><span class="sxs-lookup"><span data-stu-id="618c8-186">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="618c8-187">**Процессор** (3)</span><span class="sxs-lookup"><span data-stu-id="618c8-187">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="618c8-188">**Память** (4)</span><span class="sxs-lookup"><span data-stu-id="618c8-188">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="618c8-189">**IDE-контроллер** (5)</span><span class="sxs-lookup"><span data-stu-id="618c8-189">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="618c8-190">**Параллельный SCSI HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="618c8-190">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="618c8-191">**Адаптер шины FC** (7)</span><span class="sxs-lookup"><span data-stu-id="618c8-191">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="618c8-192">**адаптер шины iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="618c8-192">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="618c8-193">**Геохка** (9)</span><span class="sxs-lookup"><span data-stu-id="618c8-193">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="618c8-194">**Ethernet-адаптер** (10)</span><span class="sxs-lookup"><span data-stu-id="618c8-194">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="618c8-195">**Другой сетевой адаптер** (11)</span><span class="sxs-lookup"><span data-stu-id="618c8-195">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="618c8-196">**Разъем ввода-вывода** (12)</span><span class="sxs-lookup"><span data-stu-id="618c8-196">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="618c8-197">**Устройство ввода-вывода** (13)</span><span class="sxs-lookup"><span data-stu-id="618c8-197">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="618c8-198">Дисковод **гибких дисков** (14)</span><span class="sxs-lookup"><span data-stu-id="618c8-198">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="618c8-199">**Дисковод компакт-дисков** (15)</span><span class="sxs-lookup"><span data-stu-id="618c8-199">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="618c8-200">**DVD-дисковод** (16)</span><span class="sxs-lookup"><span data-stu-id="618c8-200">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="618c8-201">**Диск** (17)</span><span class="sxs-lookup"><span data-stu-id="618c8-201">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="618c8-202">**Ленточный накопитель** (18)</span><span class="sxs-lookup"><span data-stu-id="618c8-202">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="618c8-203">**Область хранения** (19)</span><span class="sxs-lookup"><span data-stu-id="618c8-203">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="618c8-204">**Другое запоминающее устройство** (20)</span><span class="sxs-lookup"><span data-stu-id="618c8-204">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="618c8-205">**Последовательный порт** (21)</span><span class="sxs-lookup"><span data-stu-id="618c8-205">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="618c8-206">**Параллельный порт** (22)</span><span class="sxs-lookup"><span data-stu-id="618c8-206">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="618c8-207">**Контроллер USB** (23)</span><span class="sxs-lookup"><span data-stu-id="618c8-207">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="618c8-208">**Графический контроллер** (24)</span><span class="sxs-lookup"><span data-stu-id="618c8-208">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="618c8-209">**Контроллер IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="618c8-209">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="618c8-210">**Единица секционирования** (26)</span><span class="sxs-lookup"><span data-stu-id="618c8-210">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="618c8-211">**Базовая единица секционирования** (27)</span><span class="sxs-lookup"><span data-stu-id="618c8-211">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="618c8-212">**Мощность** (28)</span><span class="sxs-lookup"><span data-stu-id="618c8-212">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="618c8-213">**Емкость системы охлаждения** (29)</span><span class="sxs-lookup"><span data-stu-id="618c8-213">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="618c8-214">**Порт коммутатора Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="618c8-214">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="618c8-215">**Логический диск** (31)</span><span class="sxs-lookup"><span data-stu-id="618c8-215">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="618c8-216">**Том хранилища** (32)</span><span class="sxs-lookup"><span data-stu-id="618c8-216">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="618c8-217">**Ethernet-подключение** (33)</span><span class="sxs-lookup"><span data-stu-id="618c8-217">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="618c8-218">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="618c8-218">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="618c8-219">**Поставщик зарезервирован** (0x8000.. 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="618c8-219">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="618c8-220"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="618c8-220"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="618c8-221">Требования</span><span class="sxs-lookup"><span data-stu-id="618c8-221">Requirements</span></span>



| <span data-ttu-id="618c8-222">Требование</span><span class="sxs-lookup"><span data-stu-id="618c8-222">Requirement</span></span> | <span data-ttu-id="618c8-223">Значение</span><span class="sxs-lookup"><span data-stu-id="618c8-223">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="618c8-224">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="618c8-224">Minimum supported client</span></span><br/> | <span data-ttu-id="618c8-225">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="618c8-225">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="618c8-226">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="618c8-226">Minimum supported server</span></span><br/> | <span data-ttu-id="618c8-227">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="618c8-227">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="618c8-228">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="618c8-228">Namespace</span></span><br/>                | <span data-ttu-id="618c8-229">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="618c8-229">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="618c8-230">MOF</span><span class="sxs-lookup"><span data-stu-id="618c8-230">MOF</span></span><br/>                      | <dl> <span data-ttu-id="618c8-231"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="618c8-231"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="618c8-232">DLL</span><span class="sxs-lookup"><span data-stu-id="618c8-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="618c8-233"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="618c8-233"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


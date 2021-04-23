---
description: Представляет ассоциацию, в которой \_ объект CIM басеметрикдефинитион определяет метрики для управляемого элемента.
ms.assetid: 10905038-fc23-4018-bae8-f336e4f001e7
title: Класс CIM_MetricDefForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricDefForME
- CIM_MetricDefForME.Antecedent
- CIM_MetricDefForME.Dependent
- CIM_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d0bcc115bdb5d501567223a307dd30e62f624214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911036"
---
# <a name="cim_metricdefforme-class"></a><span data-ttu-id="6759c-103">\_Класс CIM метрикдефформе</span><span class="sxs-lookup"><span data-stu-id="6759c-103">CIM\_MetricDefForME class</span></span>

<span data-ttu-id="6759c-104">Представляет ассоциацию, в которой объект [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) определяет метрики для управляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="6759c-104">Represents an association in which a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object defines metrics for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="6759c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6759c-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricDefForME : CIM_Dependency
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a><span data-ttu-id="6759c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="6759c-106">Members</span></span>

<span data-ttu-id="6759c-107">Класс **CIM \_ метрикдефформе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6759c-107">The **CIM\_MetricDefForME** class has these types of members:</span></span>

-   [<span data-ttu-id="6759c-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="6759c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6759c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="6759c-109">Properties</span></span>

<span data-ttu-id="6759c-110">Класс **CIM \_ метрикдефформе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6759c-110">The **CIM\_MetricDefForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6759c-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="6759c-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6759c-112">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="6759c-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="6759c-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6759c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6759c-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="6759c-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6759c-115">Управляемый элемент, связанный с определением метрики.</span><span class="sxs-lookup"><span data-stu-id="6759c-115">The managed element that is associated with the metric definition.</span></span>

</dd> <dt>

<span data-ttu-id="6759c-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="6759c-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6759c-117">Тип данных: **CIM \_ басеметрикдефинитион**</span><span class="sxs-lookup"><span data-stu-id="6759c-117">Data type: **CIM\_BaseMetricDefinition**</span></span>
</dt> <dt>

<span data-ttu-id="6759c-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6759c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6759c-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="6759c-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6759c-120">Определение метрики, связанное с управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="6759c-120">The metric definition that is associated with the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="6759c-121">**метрикколлектионенаблед**</span><span class="sxs-lookup"><span data-stu-id="6759c-121">**MetricCollectionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6759c-122">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6759c-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6759c-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6759c-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6759c-124">Указывает, собирается ли метрика для управляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="6759c-124">Indicates whether the metric is being collected for the managed element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6759c-125">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="6759c-125">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6759c-126">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="6759c-126">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="6759c-127">**Зарезервировано** (4)</span><span class="sxs-lookup"><span data-stu-id="6759c-127">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6759c-128">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="6759c-128">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="6759c-129">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6759c-129">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="6759c-130"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6759c-130"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="6759c-131">Требования</span><span class="sxs-lookup"><span data-stu-id="6759c-131">Requirements</span></span>



| <span data-ttu-id="6759c-132">Требование</span><span class="sxs-lookup"><span data-stu-id="6759c-132">Requirement</span></span> | <span data-ttu-id="6759c-133">Значение</span><span class="sxs-lookup"><span data-stu-id="6759c-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6759c-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6759c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6759c-135">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6759c-135">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6759c-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6759c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6759c-137">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6759c-137">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6759c-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6759c-138">Namespace</span></span><br/>                | <span data-ttu-id="6759c-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6759c-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6759c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6759c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6759c-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6759c-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6759c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6759c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6759c-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6759c-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6759c-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6759c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6759c-145">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="6759c-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


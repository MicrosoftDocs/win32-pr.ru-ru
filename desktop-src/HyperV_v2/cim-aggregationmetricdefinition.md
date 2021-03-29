---
description: Представляет определение метрики, которая является производной от другого значения метрики. Объект CIM \_ аггрегатионметрикдефинитион должен быть связан с \_ объектами CIM манажеделемент, к которым он применяется.
ms.assetid: 0059bfd6-ecf3-41f0-be6b-0ce46dfbbb18
title: Класс CIM_AggregationMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricDefinition
- CIM_AggregationMetricDefinition.ChangeType
- CIM_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9a84eed5a725ebff3b39ca92bab530ef90cfca58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812736"
---
# <a name="cim_aggregationmetricdefinition-class"></a><span data-ttu-id="12d9a-104">\_Класс CIM аггрегатионметрикдефинитион</span><span class="sxs-lookup"><span data-stu-id="12d9a-104">CIM\_AggregationMetricDefinition class</span></span>

<span data-ttu-id="12d9a-105">Представляет определение метрики, которая является производной от другого значения метрики.</span><span class="sxs-lookup"><span data-stu-id="12d9a-105">Represents the definition of a metric that is derived from another metric value.</span></span> <span data-ttu-id="12d9a-106">Объект **CIM \_ аггрегатионметрикдефинитион** должен быть связан с объектами **CIM \_ манажеделемент** , к которым он применяется.</span><span class="sxs-lookup"><span data-stu-id="12d9a-106">A **CIM\_AggregationMetricDefinition** object should be associated with the **CIM\_ManagedElement** objects to which it applies.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d9a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12d9a-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricDefinition : CIM_BaseMetricDefinition
{
  uint16 ChangeType = 5;
  uint16 SimpleFunction;
};
```

## <a name="members"></a><span data-ttu-id="12d9a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="12d9a-108">Members</span></span>

<span data-ttu-id="12d9a-109">Класс **CIM \_ аггрегатионметрикдефинитион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="12d9a-109">The **CIM\_AggregationMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="12d9a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="12d9a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="12d9a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="12d9a-111">Properties</span></span>

<span data-ttu-id="12d9a-112">Класс **CIM \_ аггрегатионметрикдефинитион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="12d9a-112">The **CIM\_AggregationMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12d9a-113">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="12d9a-113">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d9a-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12d9a-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12d9a-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="12d9a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12d9a-116">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ChangeType"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ аггрегатионметрикдефинитион**.**Continuous**»)</span><span class="sxs-lookup"><span data-stu-id="12d9a-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ChangeType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricDefinition**.**IsContinuous**")</span></span>
</dt> </dl>

<span data-ttu-id="12d9a-117">Указывает, как изменяется значение метрики с помощью общих атрибутов, таких как изменение направления, минимальное и максимальное значения, а также семантика упаковки.</span><span class="sxs-lookup"><span data-stu-id="12d9a-117">Indicates how the metric value changes using common attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span>

<dt>

<span id="Simple_Function"></span><span id="simple_function"></span><span id="SIMPLE_FUNCTION"></span>

<span data-ttu-id="12d9a-118">**Простая функция** (5)</span><span class="sxs-lookup"><span data-stu-id="12d9a-118">**Simple Function** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="12d9a-119">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="12d9a-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="12d9a-120">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="12d9a-120">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12d9a-121">**симплефунктион**</span><span class="sxs-lookup"><span data-stu-id="12d9a-121">**SimpleFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d9a-122">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12d9a-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12d9a-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="12d9a-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12d9a-124">Базовые вычисления, выполняемые с базовой метрикой, которые поступают на значение этой производной метрики.</span><span class="sxs-lookup"><span data-stu-id="12d9a-124">The basic computation performed on an underlying metric to arrive at the value of this derived metric.</span></span> <span data-ttu-id="12d9a-125">Это свойство имеет значение **null** , если свойство **ChangeType** имеет значение, отличное от "5" (простая функция).</span><span class="sxs-lookup"><span data-stu-id="12d9a-125">This property is **NULL** when the **ChangeType** property has a value other than "5" (Simple Function).</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="12d9a-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="12d9a-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="12d9a-127"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Минимум** (2)</span><span class="sxs-lookup"><span data-stu-id="12d9a-127"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (2)</span></span>


</dt> <dd>

<span data-ttu-id="12d9a-128">Метрика сообщает наименьшее значение, обнаруженное для связанной отслеживаемой сущности.</span><span class="sxs-lookup"><span data-stu-id="12d9a-128">The metric reports the lowest value detected for the associated monitored entity.</span></span> <span data-ttu-id="12d9a-129">Это также называется нижнего предела.</span><span class="sxs-lookup"><span data-stu-id="12d9a-129">This is also known as a low watermark.</span></span>

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="12d9a-130"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Максимум** (3)</span><span class="sxs-lookup"><span data-stu-id="12d9a-130"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)</span></span>


</dt> <dd>

<span data-ttu-id="12d9a-131">Метрика сообщает максимальное значение, обнаруженное для связанной отслеживаемой сущности.</span><span class="sxs-lookup"><span data-stu-id="12d9a-131">The metric reports the maximum value detected for the associated monitored entity.</span></span> <span data-ttu-id="12d9a-132">Это также называется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="12d9a-132">This is also known as a high watermark.</span></span>

</dd> <dt>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>

<span data-ttu-id="12d9a-133"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Среднее значение** (4)</span><span class="sxs-lookup"><span data-stu-id="12d9a-133"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Average** (4)</span></span>


</dt> <dd>

<span data-ttu-id="12d9a-134">Метрика Возвращает среднее значение базовых значений метрики.</span><span class="sxs-lookup"><span data-stu-id="12d9a-134">The metric reports the average value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>

<span data-ttu-id="12d9a-135"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Медиана** (5)</span><span class="sxs-lookup"><span data-stu-id="12d9a-135"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Median** (5)</span></span>


</dt> <dd>

<span data-ttu-id="12d9a-136">Метрика сообщает медиану значений базовых метрик.</span><span class="sxs-lookup"><span data-stu-id="12d9a-136">The metric reports the median value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>

<span data-ttu-id="12d9a-137"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Режим** (6)</span><span class="sxs-lookup"><span data-stu-id="12d9a-137"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode** (6)</span></span>


</dt> <dd>

<span data-ttu-id="12d9a-138">Метрика сообщает об модальном значении базовых значений метрики.</span><span class="sxs-lookup"><span data-stu-id="12d9a-138">the metric reports the modal value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="12d9a-139"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="12d9a-139"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="12d9a-140"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="12d9a-140"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="12d9a-141">Требования</span><span class="sxs-lookup"><span data-stu-id="12d9a-141">Requirements</span></span>



| <span data-ttu-id="12d9a-142">Требование</span><span class="sxs-lookup"><span data-stu-id="12d9a-142">Requirement</span></span> | <span data-ttu-id="12d9a-143">Значение</span><span class="sxs-lookup"><span data-stu-id="12d9a-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12d9a-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12d9a-144">Minimum supported client</span></span><br/> | <span data-ttu-id="12d9a-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="12d9a-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="12d9a-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12d9a-146">Minimum supported server</span></span><br/> | <span data-ttu-id="12d9a-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="12d9a-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="12d9a-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="12d9a-148">Namespace</span></span><br/>                | <span data-ttu-id="12d9a-149">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="12d9a-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="12d9a-150">MOF</span><span class="sxs-lookup"><span data-stu-id="12d9a-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12d9a-151"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12d9a-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="12d9a-152">DLL</span><span class="sxs-lookup"><span data-stu-id="12d9a-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12d9a-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="12d9a-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="12d9a-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12d9a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d9a-155">**\_БАСЕМЕТРИКДЕФИНИТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="12d9a-155">**CIM\_BaseMetricDefinition**</span></span>](cim-basemetricdefinition.md)
</dt> </dl>

 


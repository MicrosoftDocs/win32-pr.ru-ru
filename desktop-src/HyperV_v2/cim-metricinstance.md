---
description: Представляет связь между экземпляром значения метрики и определением метрики.
ms.assetid: 4c620a7a-8b15-49ad-ae84-246e2fca175d
title: Класс CIM_MetricInstance
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricInstance
- CIM_MetricInstance.Antecedent
- CIM_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: defba85f46e037c226a96cfaa8ffac44b99244f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663593"
---
# <a name="cim_metricinstance-class"></a><span data-ttu-id="38379-103">\_Класс CIM метриЦинстанце</span><span class="sxs-lookup"><span data-stu-id="38379-103">CIM\_MetricInstance class</span></span>

<span data-ttu-id="38379-104">Представляет связь между экземпляром значения метрики и определением метрики.</span><span class="sxs-lookup"><span data-stu-id="38379-104">Represents an association between an instance of a metric value and a metric definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="38379-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38379-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricInstance : CIM_Dependency
{
  CIM_BaseMetricDefinition REF Antecedent;
  CIM_BaseMetricValue      REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="38379-106">Члены</span><span class="sxs-lookup"><span data-stu-id="38379-106">Members</span></span>

<span data-ttu-id="38379-107">Класс **CIM \_ метриЦинстанце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="38379-107">The **CIM\_MetricInstance** class has these types of members:</span></span>

-   [<span data-ttu-id="38379-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="38379-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38379-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="38379-109">Properties</span></span>

<span data-ttu-id="38379-110">Класс **CIM \_ метриЦинстанце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="38379-110">The **CIM\_MetricInstance** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38379-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="38379-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38379-112">Тип данных: **CIM \_ басеметрикдефинитион**</span><span class="sxs-lookup"><span data-stu-id="38379-112">Data type: **CIM\_BaseMetricDefinition**</span></span>
</dt> <dt>

<span data-ttu-id="38379-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38379-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38379-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="38379-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="38379-115">Определение значения метрики.</span><span class="sxs-lookup"><span data-stu-id="38379-115">The definition of the metric value.</span></span>

</dd> <dt>

<span data-ttu-id="38379-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="38379-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38379-117">Тип данных: **CIM \_ басеметриквалуе**</span><span class="sxs-lookup"><span data-stu-id="38379-117">Data type: **CIM\_BaseMetricValue**</span></span>
</dt> <dt>

<span data-ttu-id="38379-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38379-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38379-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="38379-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="38379-120">Значение метрики, связанное с определением метрики.</span><span class="sxs-lookup"><span data-stu-id="38379-120">The metric value that is associated with the metric definition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38379-121">Требования</span><span class="sxs-lookup"><span data-stu-id="38379-121">Requirements</span></span>



| <span data-ttu-id="38379-122">Требование</span><span class="sxs-lookup"><span data-stu-id="38379-122">Requirement</span></span> | <span data-ttu-id="38379-123">Значение</span><span class="sxs-lookup"><span data-stu-id="38379-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38379-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38379-124">Minimum supported client</span></span><br/> | <span data-ttu-id="38379-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="38379-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="38379-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38379-126">Minimum supported server</span></span><br/> | <span data-ttu-id="38379-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38379-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="38379-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="38379-128">Namespace</span></span><br/>                | <span data-ttu-id="38379-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="38379-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="38379-130">MOF</span><span class="sxs-lookup"><span data-stu-id="38379-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38379-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38379-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="38379-132">DLL</span><span class="sxs-lookup"><span data-stu-id="38379-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38379-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="38379-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="38379-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38379-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38379-135">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="38379-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


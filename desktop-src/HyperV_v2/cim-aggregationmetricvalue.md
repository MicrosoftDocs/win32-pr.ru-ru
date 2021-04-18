---
description: Представляет значение экземпляра метрики, определенной экземпляром CIM \_ аггрегатионметрикдефинитион.
ms.assetid: 663ef18a-0238-416f-9682-8809b271b4fc
title: Класс CIM_AggregationMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricValue
- CIM_AggregationMetricValue.AggregationTimeStamp
- CIM_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0af264b66838e7c039ef3f99a4f365ebab55c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662823"
---
# <a name="cim_aggregationmetricvalue-class"></a><span data-ttu-id="11767-103">\_Класс CIM аггрегатионметриквалуе</span><span class="sxs-lookup"><span data-stu-id="11767-103">CIM\_AggregationMetricValue class</span></span>

<span data-ttu-id="11767-104">Представляет значение экземпляра метрики, определенной экземпляром **CIM \_ аггрегатионметрикдефинитион**.</span><span class="sxs-lookup"><span data-stu-id="11767-104">Represents the instance value of a metric defined by an instance of **CIM\_AggregationMetricDefinition**.</span></span>

## <a name="syntax"></a><span data-ttu-id="11767-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11767-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricValue : CIM_BaseMetricValue
{
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a><span data-ttu-id="11767-106">Члены</span><span class="sxs-lookup"><span data-stu-id="11767-106">Members</span></span>

<span data-ttu-id="11767-107">Класс **CIM \_ аггрегатионметриквалуе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="11767-107">The **CIM\_AggregationMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="11767-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="11767-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11767-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="11767-109">Properties</span></span>

<span data-ttu-id="11767-110">Класс **CIM \_ аггрегатионметриквалуе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="11767-110">The **CIM\_AggregationMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11767-111">**аггрегатиондуратион**</span><span class="sxs-lookup"><span data-stu-id="11767-111">**AggregationDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11767-112">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="11767-112">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="11767-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11767-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11767-114">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ аггрегатионметриквалуе**.**Аггрегатионтиместамп**")</span><span class="sxs-lookup"><span data-stu-id="11767-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricValue**.**AggregationTimeStamp**")</span></span>
</dt> </dl>

<span data-ttu-id="11767-115">Представляет период времени, в течение которого Вычисление агрегата было выполнено.</span><span class="sxs-lookup"><span data-stu-id="11767-115">Represents the time duration over which the aggregation was computed.</span></span> <span data-ttu-id="11767-116">Начало интервала мониторинга, по отношению к которому применяется статистическая функция, определяется путем вычитания значения **аггрегатиондуратион** из значения **аггрегатионтиместамп** .</span><span class="sxs-lookup"><span data-stu-id="11767-116">The start of a monitoring interval over which the aggregation function is applied is determined by subtracting the **AggregationDuration** value from the **AggregationTimestamp** value.</span></span>

</dd> <dt>

<span data-ttu-id="11767-117">**аггрегатионтиместамп**</span><span class="sxs-lookup"><span data-stu-id="11767-117">**AggregationTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11767-118">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="11767-118">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="11767-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11767-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11767-120">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ аггрегатионметриквалуе**.**Duration (длительность**))</span><span class="sxs-lookup"><span data-stu-id="11767-120">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="11767-121">Время, когда статистическая функция была применена для определения значения экземпляра метрики.</span><span class="sxs-lookup"><span data-stu-id="11767-121">The time when the aggregation function was applied to determine the value of the metric instance.</span></span> <span data-ttu-id="11767-122">Это отличается от времени создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="11767-122">This is different from the time when the instance is created.</span></span> <span data-ttu-id="11767-123">Значение **аггрегатионтиместамп** изменяется каждый раз, когда статистическая функция применяется для вычисления значения.</span><span class="sxs-lookup"><span data-stu-id="11767-123">The **AggregationTimeStamp** value changes whenever the aggregation function is applied to calculate the value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11767-124">Требования</span><span class="sxs-lookup"><span data-stu-id="11767-124">Requirements</span></span>



| <span data-ttu-id="11767-125">Требование</span><span class="sxs-lookup"><span data-stu-id="11767-125">Requirement</span></span> | <span data-ttu-id="11767-126">Значение</span><span class="sxs-lookup"><span data-stu-id="11767-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11767-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11767-127">Minimum supported client</span></span><br/> | <span data-ttu-id="11767-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="11767-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="11767-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11767-129">Minimum supported server</span></span><br/> | <span data-ttu-id="11767-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11767-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="11767-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="11767-131">Namespace</span></span><br/>                | <span data-ttu-id="11767-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="11767-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="11767-133">MOF</span><span class="sxs-lookup"><span data-stu-id="11767-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11767-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11767-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="11767-135">DLL</span><span class="sxs-lookup"><span data-stu-id="11767-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11767-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="11767-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="11767-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11767-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11767-138">**\_БАСЕМЕТРИКВАЛУЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="11767-138">**CIM\_BaseMetricValue**</span></span>](cim-basemetricvalue.md)
</dt> </dl>

 


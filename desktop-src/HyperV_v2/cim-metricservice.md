---
description: Управляет метриками для управляемых элементов.
ms.assetid: df249d0c-960b-47d6-9590-f0fd08ddec18
title: Класс CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 41c4ab5e947fe22434e38006c5169711701915a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663473"
---
# <a name="cim_metricservice-class"></a><span data-ttu-id="36c4c-103">\_Класс CIM метриксервице</span><span class="sxs-lookup"><span data-stu-id="36c4c-103">CIM\_MetricService class</span></span>

<span data-ttu-id="36c4c-104">Управляет метриками для управляемых элементов.</span><span class="sxs-lookup"><span data-stu-id="36c4c-104">Manages metrics for managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="36c4c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36c4c-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="36c4c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="36c4c-106">Members</span></span>

<span data-ttu-id="36c4c-107">Класс **CIM \_ метриксервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="36c4c-107">The **CIM\_MetricService** class has these types of members:</span></span>

-   [<span data-ttu-id="36c4c-108">Методы</span><span class="sxs-lookup"><span data-stu-id="36c4c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="36c4c-109">Методы</span><span class="sxs-lookup"><span data-stu-id="36c4c-109">Methods</span></span>

<span data-ttu-id="36c4c-110">Класс **CIM \_ метриксервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="36c4c-110">The **CIM\_MetricService** class has these methods.</span></span>



| <span data-ttu-id="36c4c-111">Метод</span><span class="sxs-lookup"><span data-stu-id="36c4c-111">Method</span></span>                                                                   | <span data-ttu-id="36c4c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="36c4c-112">Description</span></span>                                                                                                                                                                         |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36c4c-113">**контролметрикс**</span><span class="sxs-lookup"><span data-stu-id="36c4c-113">**ControlMetrics**</span></span>](cim-metricservice-controlmetrics.md)               | <span data-ttu-id="36c4c-114">Включает и отключает сбор метрик.</span><span class="sxs-lookup"><span data-stu-id="36c4c-114">Enables and disables the collection of metrics.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="36c4c-115">**контролметриксбикласс**</span><span class="sxs-lookup"><span data-stu-id="36c4c-115">**ControlMetricsByClass**</span></span>](cim-metricservice-controlmetricsbyclass.md) | <span data-ttu-id="36c4c-116">Включает и отключает сбор метрик для класса.</span><span class="sxs-lookup"><span data-stu-id="36c4c-116">Enables and disables the collection of metrics for a class.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="36c4c-117">**контролсамплетимес**</span><span class="sxs-lookup"><span data-stu-id="36c4c-117">**ControlSampleTimes**</span></span>](cim-metricservice-controlsampletimes.md)       | <span data-ttu-id="36c4c-118">Указывает, когда собираются метрики.</span><span class="sxs-lookup"><span data-stu-id="36c4c-118">Specifies when metrics are gathered.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="36c4c-119">**жетметриквалуес**</span><span class="sxs-lookup"><span data-stu-id="36c4c-119">**GetMetricValues**</span></span>](cim-metricservice-getmetricvalues.md)             | <span data-ttu-id="36c4c-120">Извлекает отфильтрованный список значений метрик.</span><span class="sxs-lookup"><span data-stu-id="36c4c-120">Retrieves a filtered list of metric values.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="36c4c-121">**шовметрикс**</span><span class="sxs-lookup"><span data-stu-id="36c4c-121">**ShowMetrics**</span></span>](cim-metricservice-showmetrics.md)                     | <span data-ttu-id="36c4c-122">Указывает, включена ли коллекция метрик для указанных управляемых элементов, и указывает метрики, доступные для коллекции для каждого управляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="36c4c-122">Indicates whether metric collection is enabled for the specified managed elements, and indicates the metrics that are available for collection for each managed element.</span></span><br/> |
| [<span data-ttu-id="36c4c-123">**шовметриксбикласс**</span><span class="sxs-lookup"><span data-stu-id="36c4c-123">**ShowMetricsByClass**</span></span>](cim-metricservice-showmetricsbyclass.md)       | <span data-ttu-id="36c4c-124">Указывает, какие метрики доступны для коллекции для всех экземпляров класса CIM.</span><span class="sxs-lookup"><span data-stu-id="36c4c-124">Indicates which metrics are available for collection for all instances of a CIM class.</span></span><br/>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="36c4c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="36c4c-125">Requirements</span></span>



| <span data-ttu-id="36c4c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="36c4c-126">Requirement</span></span> | <span data-ttu-id="36c4c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="36c4c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36c4c-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36c4c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="36c4c-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="36c4c-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="36c4c-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36c4c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="36c4c-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36c4c-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="36c4c-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="36c4c-132">Namespace</span></span><br/>                | <span data-ttu-id="36c4c-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="36c4c-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="36c4c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="36c4c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36c4c-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36c4c-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="36c4c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="36c4c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36c4c-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="36c4c-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="36c4c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36c4c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36c4c-139">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="36c4c-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 





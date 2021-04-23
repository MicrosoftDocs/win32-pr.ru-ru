---
description: Представляет ассоциацию, в которой собираются значения метрик для управляемого элемента.
ms.assetid: 00752751-bc27-463b-a4ac-4db8e5040077
title: Класс CIM_MetricForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricForME
- CIM_MetricForME.Antecedent
- CIM_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89c119ad622b778d0402100a64ff15befe623685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683762"
---
# <a name="cim_metricforme-class"></a><span data-ttu-id="bb9cf-103">\_Класс CIM метрикформе</span><span class="sxs-lookup"><span data-stu-id="bb9cf-103">CIM\_MetricForME class</span></span>

<span data-ttu-id="bb9cf-104">Представляет ассоциацию, в которой собираются значения метрик для управляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="bb9cf-104">Represents an association in which a metric values are collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb9cf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb9cf-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricForME : CIM_Dependency
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="bb9cf-106">Члены</span><span class="sxs-lookup"><span data-stu-id="bb9cf-106">Members</span></span>

<span data-ttu-id="bb9cf-107">Класс **CIM \_ метрикформе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bb9cf-107">The **CIM\_MetricForME** class has these types of members:</span></span>

-   [<span data-ttu-id="bb9cf-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="bb9cf-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb9cf-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="bb9cf-109">Properties</span></span>

<span data-ttu-id="bb9cf-110">Класс **CIM \_ метрикформе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bb9cf-110">The **CIM\_MetricForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb9cf-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="bb9cf-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9cf-112">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="bb9cf-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="bb9cf-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb9cf-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9cf-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="bb9cf-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="bb9cf-115">Управляемый элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="bb9cf-115">The managed element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="bb9cf-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="bb9cf-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9cf-117">Тип данных: **CIM \_ басеметриквалуе**</span><span class="sxs-lookup"><span data-stu-id="bb9cf-117">Data type: **CIM\_BaseMetricValue**</span></span>
</dt> <dt>

<span data-ttu-id="bb9cf-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb9cf-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9cf-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="bb9cf-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="bb9cf-120">Значение метрики в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="bb9cf-120">The metric value in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb9cf-121">Требования</span><span class="sxs-lookup"><span data-stu-id="bb9cf-121">Requirements</span></span>



| <span data-ttu-id="bb9cf-122">Требование</span><span class="sxs-lookup"><span data-stu-id="bb9cf-122">Requirement</span></span> | <span data-ttu-id="bb9cf-123">Значение</span><span class="sxs-lookup"><span data-stu-id="bb9cf-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb9cf-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb9cf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bb9cf-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bb9cf-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="bb9cf-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb9cf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bb9cf-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bb9cf-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="bb9cf-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bb9cf-128">Namespace</span></span><br/>                | <span data-ttu-id="bb9cf-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="bb9cf-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bb9cf-130">MOF</span><span class="sxs-lookup"><span data-stu-id="bb9cf-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb9cf-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb9cf-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb9cf-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bb9cf-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb9cf-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb9cf-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bb9cf-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb9cf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb9cf-135">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="bb9cf-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


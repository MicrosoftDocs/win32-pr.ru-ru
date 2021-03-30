---
description: 'Выводит следующие сведения: метрики, доступные для сбора для управляемого элемента, управляемые элементы, для которых метрика, определенная экземпляром CIM \_ басеметрикдефинитион, доступна для сбора, а также сведения о том, собирается ли определенная метрика для управляемого элемента в данный момент.'
ms.assetid: 5af430d2-9ab3-4bee-ad51-d9045b51172a
title: Метод Шовметрикс класса CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1e0e062adaefd6c6d9bdabe6f168bd64e789acc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156594"
---
# <a name="showmetrics-method-of-the-cim_metricservice-class"></a><span data-ttu-id="029cd-103">Метод Шовметрикс \_ класса CIM метриксервице</span><span class="sxs-lookup"><span data-stu-id="029cd-103">ShowMetrics method of the CIM\_MetricService class</span></span>

<span data-ttu-id="029cd-104">Выводит следующие сведения: метрики, доступные для сбора для управляемого элемента, управляемые элементы, для которых метрика, определенная экземпляром [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , доступна для сбора, а также сведения о том, собирается ли определенная метрика для управляемого элемента в данный момент.</span><span class="sxs-lookup"><span data-stu-id="029cd-104">Reports the following: the metrics available to be collected for a managed element, the managed elements for which a metric defined by an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) is available to be collected, and whether or not a particular metric is currently being collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="029cd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="029cd-105">Syntax</span></span>


```mof
uint32 ShowMetrics(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_ManagedElement       REF ManagedElements[],
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="029cd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="029cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="029cd-107">*Тема* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="029cd-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="029cd-108">Определяет экземпляр [**CIM \_ манажеделемент**](cim-managedelement.md) , для которого метод возвращает ссылки на экземпляры [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, которые фиксируются для **CIM \_ манажеделемент**.</span><span class="sxs-lookup"><span data-stu-id="029cd-108">Identifies an instance of [**CIM\_ManagedElement**](cim-managedelement.md) for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are being captured for the **CIM\_ManagedElement**.</span></span>

</dd> <dt>

<span data-ttu-id="029cd-109">*Определение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="029cd-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="029cd-110">Идентифицирует экземпляр [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="029cd-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="029cd-111">Метод возвращает ссылки на экземпляры [**CIM \_ манажеделемент**](cim-managedelement.md) , для которых можно собирать метрики, определенные экземпляром **CIM \_ басеметрикдефинитион** .</span><span class="sxs-lookup"><span data-stu-id="029cd-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="029cd-112">*Манажеделементс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="029cd-112">*ManagedElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="029cd-113">При успешном выполнении может содержать ссылки на объекты [**CIM \_ манажеделемент**](cim-managedelement.md) , для которых метрика, определяемая параметром *определения* , доступна для коллекции.</span><span class="sxs-lookup"><span data-stu-id="029cd-113">On success, may contain references to [**CIM\_ManagedElement**](cim-managedelement.md) objects for which the metric identified by the *Definition* parameter is available for collection.</span></span>

</dd> <dt>

<span data-ttu-id="029cd-114">*Дефинитионлист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="029cd-114">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="029cd-115">При успешном выполнении может содержать ссылки на экземпляры объектов [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, доступные для сбора [**для \_ манажеделемент CIM**](cim-managedelement.md) , идентифицируемые параметром *subject* .</span><span class="sxs-lookup"><span data-stu-id="029cd-115">On success, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) objects that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="029cd-116">*MetricNames* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="029cd-116">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="029cd-117">При успешном выполнении каждый индекс массива должен содержать значение свойства **Name** для экземпляра [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , на который ссылается соответствующий индекс массива параметра *дефинитионлист* .</span><span class="sxs-lookup"><span data-stu-id="029cd-117">On success, each array index shall contain the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="029cd-118">*Метрикколлектионенаблед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="029cd-118">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="029cd-119">Указывает, собирается ли метрика для управляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="029cd-119">Indicates whether a metric is being collected for a managed element.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="029cd-120">**Включить** (2)</span><span class="sxs-lookup"><span data-stu-id="029cd-120">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="029cd-121">**Отключить** (3)</span><span class="sxs-lookup"><span data-stu-id="029cd-121">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="029cd-122">**Зарезервировано** (4)</span><span class="sxs-lookup"><span data-stu-id="029cd-122">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="029cd-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="029cd-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="029cd-124">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="029cd-124">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="029cd-125"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="029cd-125"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="029cd-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="029cd-126">Return value</span></span>

<span data-ttu-id="029cd-127">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="029cd-127">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="029cd-128">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="029cd-128">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="029cd-129">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="029cd-129">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="029cd-130">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="029cd-130">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="029cd-131">**Метод зарезервирован** (..)</span><span class="sxs-lookup"><span data-stu-id="029cd-131">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="029cd-132">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="029cd-132">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="029cd-133">Требования</span><span class="sxs-lookup"><span data-stu-id="029cd-133">Requirements</span></span>



| <span data-ttu-id="029cd-134">Требование</span><span class="sxs-lookup"><span data-stu-id="029cd-134">Requirement</span></span> | <span data-ttu-id="029cd-135">Значение</span><span class="sxs-lookup"><span data-stu-id="029cd-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="029cd-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="029cd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="029cd-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="029cd-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="029cd-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="029cd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="029cd-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="029cd-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="029cd-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="029cd-140">Namespace</span></span><br/>                | <span data-ttu-id="029cd-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="029cd-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="029cd-142">MOF</span><span class="sxs-lookup"><span data-stu-id="029cd-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="029cd-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="029cd-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="029cd-144">DLL</span><span class="sxs-lookup"><span data-stu-id="029cd-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="029cd-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="029cd-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="029cd-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="029cd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="029cd-147">**\_МЕТРИКСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="029cd-147">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 





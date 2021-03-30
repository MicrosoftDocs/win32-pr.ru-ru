---
description: 'Сообщает следующее: метрики, доступные для сбора для всех экземпляров класса CIM, классы CIM, для которых метрика, определенная экземпляром CIM \_ басеметрикдефинитион, доступна для сбора, а также сведения о том, собирается ли определенная метрика для управляемого элемента в данный момент.'
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: Метод Шовметриксбикласс класса CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f843c835e6c92e39c4ac1f9628d0479b94a691bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910159"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a><span data-ttu-id="d2715-103">Метод Шовметриксбикласс \_ класса CIM метриксервице</span><span class="sxs-lookup"><span data-stu-id="d2715-103">ShowMetricsByClass method of the CIM\_MetricService class</span></span>

<span data-ttu-id="d2715-104">Сообщает следующее: метрики, доступные для сбора для всех экземпляров класса CIM, классы CIM, для которых метрика, определенная экземпляром [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , доступна для сбора, а также сведения о том, собирается ли определенная метрика для управляемого элемента в данный момент.</span><span class="sxs-lookup"><span data-stu-id="d2715-104">Reports the following: the metrics available to be collected for all instances of a CIM class, The CIM classes for which a metric defined by an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) is available to be collected, and whether or not a particular metric is currently being collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2715-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2715-105">Syntax</span></span>


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="d2715-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2715-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2715-107">*Тема* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2715-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2715-108">Определяет класс CIM, для которого метод возвращает ссылки на экземпляры [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, доступные для записи во всех экземплярах класса.</span><span class="sxs-lookup"><span data-stu-id="d2715-108">Identifies a CIM class for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are available to be captured for all instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="d2715-109">*Определение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2715-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2715-110">Идентифицирует экземпляр [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="d2715-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="d2715-111">Метод возвращает ссылки на экземпляры [**CIM \_ манажеделемент**](cim-managedelement.md) , для которых можно собирать метрики, определенные экземпляром **CIM \_ басеметрикдефинитион** .</span><span class="sxs-lookup"><span data-stu-id="d2715-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="d2715-112">*Дефинитионлист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d2715-112">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2715-113">При успешном выполнении может содержать ссылки на экземпляры объектов [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, доступные для сбора [**для \_ манажеделемент CIM**](cim-managedelement.md) , идентифицируемые параметром *subject* .</span><span class="sxs-lookup"><span data-stu-id="d2715-113">On success, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) objects that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d2715-114">*MetricNames* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d2715-114">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2715-115">При успешном выполнении каждый индекс массива должен содержать значение свойства **Name** для экземпляра [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , на который ссылается соответствующий индекс массива параметра *дефинитионлист* .</span><span class="sxs-lookup"><span data-stu-id="d2715-115">On success, each array index shall contain the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d2715-116">*Метрикколлектионенаблед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d2715-116">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2715-117">Указывает, собирается ли метрика для всех экземпляров класса управляемых элементов.</span><span class="sxs-lookup"><span data-stu-id="d2715-117">Indicates whether a metric is being collected for all instances of a class of managed elements.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d2715-118">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="d2715-118">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d2715-119">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="d2715-119">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="d2715-120">**Зарезервировано** (4)</span><span class="sxs-lookup"><span data-stu-id="d2715-120">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d2715-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="d2715-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="d2715-122">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="d2715-122">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="d2715-123"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d2715-123"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="d2715-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2715-124">Return value</span></span>

<span data-ttu-id="d2715-125">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d2715-125">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="d2715-126">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="d2715-126">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2715-127">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="d2715-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2715-128">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="d2715-128">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2715-129">**Метод зарезервирован** (..)</span><span class="sxs-lookup"><span data-stu-id="d2715-129">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2715-130">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="d2715-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d2715-131">Требования</span><span class="sxs-lookup"><span data-stu-id="d2715-131">Requirements</span></span>



| <span data-ttu-id="d2715-132">Требование</span><span class="sxs-lookup"><span data-stu-id="d2715-132">Requirement</span></span> | <span data-ttu-id="d2715-133">Значение</span><span class="sxs-lookup"><span data-stu-id="d2715-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2715-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2715-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d2715-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d2715-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d2715-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2715-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d2715-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d2715-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d2715-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d2715-138">Namespace</span></span><br/>                | <span data-ttu-id="d2715-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d2715-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d2715-140">MOF</span><span class="sxs-lookup"><span data-stu-id="d2715-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2715-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2715-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2715-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d2715-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2715-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d2715-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d2715-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2715-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2715-145">**\_МЕТРИКСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="d2715-145">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 





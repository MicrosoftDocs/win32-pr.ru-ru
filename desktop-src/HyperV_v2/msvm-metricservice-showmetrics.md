---
description: Показывает указанные метрики.
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: Метод Шовметрикс класса Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9823ea61864b0d87245ebe8b171195a2fd3c411a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913124"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="6b25c-103">Метод Шовметрикс \_ класса Метриксервице мсвм</span><span class="sxs-lookup"><span data-stu-id="6b25c-103">ShowMetrics method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="6b25c-104">Показывает указанные метрики.</span><span class="sxs-lookup"><span data-stu-id="6b25c-104">Shows the specified metrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b25c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b25c-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="6b25c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b25c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b25c-107">*Тема* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b25c-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b25c-108">Параметр Subject определяет экземпляр [**CIM \_ манажеделемент**](cim-managedelement.md) , для которого метод возвращает ссылки на экземпляры [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, которые фиксируются для **CIM \_ манажеделемент**.</span><span class="sxs-lookup"><span data-stu-id="6b25c-108">The Subject parameter identifies an instance of [**CIM\_ManagedElement**](cim-managedelement.md) for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are being captured for the **CIM\_ManagedElement**.</span></span>

</dd> <dt>

<span data-ttu-id="6b25c-109">*Определение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b25c-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b25c-110">Параметр определения определяет экземпляр [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="6b25c-110">The Definition parameter identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="6b25c-111">Метод возвращает ссылки на экземпляры [**CIM \_ манажеделемент**](cim-managedelement.md) , для которых можно собирать метрики, определенные экземпляром **CIM \_ басеметрикдефинитион** .</span><span class="sxs-lookup"><span data-stu-id="6b25c-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="6b25c-112">*Манажеделементс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6b25c-112">*ManagedElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b25c-113">После успешного завершения метода параметр *манажеделементс* \[ \] может содержать ссылки на [**CIM \_ манажеделемент**](cim-managedelement.md) , для которых метрика, идентифицируемая параметром *определения* , доступна для коллекции.</span><span class="sxs-lookup"><span data-stu-id="6b25c-113">Upon successful completion of the method, the *ManagedElements*\[\] parameter may contain references to [**CIM\_ManagedElement**](cim-managedelement.md) for which the metric identified by *Definition* parameter is available for collection.</span></span>

</dd> <dt>

<span data-ttu-id="6b25c-114">*Дефинитионлист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6b25c-114">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b25c-115">После успешного завершения метода параметр *дефинитионлист* может содержать ссылки на экземпляры [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, доступные для сбора для [**CIM \_ манажеделемент**](cim-managedelement.md) , определяемого параметром *subject* .</span><span class="sxs-lookup"><span data-stu-id="6b25c-115">Upon successful completion of the method, the *DefinitionList* parameter may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6b25c-116">*MetricNames* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6b25c-116">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b25c-117">После успешного завершения метода каждый индекс массива параметра *MetricNames* должен содержать значение свойства Name для экземпляра [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , на который ссылается соответствующий индекс массива параметра *дефинитионлист* .</span><span class="sxs-lookup"><span data-stu-id="6b25c-117">Upon successful completion of the method, each array index of the *MetricNames* parameter shall contain the value of the Name property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6b25c-118">*Метрикколлектионенаблед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6b25c-118">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b25c-119">Параметр *метрикколлектионенаблед* указывает, собирается ли метрика для управляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="6b25c-119">The *MetricCollectionEnabled* parameter indicates whether a metric is being collected for a managed element.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="6b25c-120">**Включить** (2)</span><span class="sxs-lookup"><span data-stu-id="6b25c-120">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="6b25c-121">**Отключить** (3)</span><span class="sxs-lookup"><span data-stu-id="6b25c-121">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="6b25c-122">**Зарезервировано** (4)</span><span class="sxs-lookup"><span data-stu-id="6b25c-122">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6b25c-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="6b25c-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="6b25c-124">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6b25c-124">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="6b25c-125"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6b25c-125"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="6b25c-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b25c-126">Return value</span></span>

<span data-ttu-id="6b25c-127">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6b25c-127">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6b25c-128">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="6b25c-128">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6b25c-129">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="6b25c-129">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6b25c-130">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="6b25c-130">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6b25c-131">**Метод зарезервирован** (..)</span><span class="sxs-lookup"><span data-stu-id="6b25c-131">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6b25c-132">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="6b25c-132">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6b25c-133">Требования</span><span class="sxs-lookup"><span data-stu-id="6b25c-133">Requirements</span></span>



| <span data-ttu-id="6b25c-134">Требование</span><span class="sxs-lookup"><span data-stu-id="6b25c-134">Requirement</span></span> | <span data-ttu-id="6b25c-135">Значение</span><span class="sxs-lookup"><span data-stu-id="6b25c-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b25c-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b25c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6b25c-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6b25c-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6b25c-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b25c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6b25c-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6b25c-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6b25c-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6b25c-140">Namespace</span></span><br/>                | <span data-ttu-id="6b25c-141">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6b25c-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6b25c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6b25c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b25c-143"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b25c-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b25c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6b25c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b25c-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6b25c-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6b25c-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b25c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b25c-147">**Мсвм \_ метриксервице**</span><span class="sxs-lookup"><span data-stu-id="6b25c-147">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 





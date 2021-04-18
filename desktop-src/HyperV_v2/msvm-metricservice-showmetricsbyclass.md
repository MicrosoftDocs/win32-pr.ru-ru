---
description: Показывает метрики по классу.
ms.assetid: a08c0749-b60b-4b8a-996f-b3bbaf1fb2d3
title: Метод Шовметриксбикласс класса Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93f132b24c6c20826b1551e979c128b1aa38c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663071"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="4073b-103">Метод Шовметриксбикласс \_ класса Метриксервице мсвм</span><span class="sxs-lookup"><span data-stu-id="4073b-103">ShowMetricsByClass method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="4073b-104">Показывает метрики по классу.</span><span class="sxs-lookup"><span data-stu-id="4073b-104">Shows metrics by class.</span></span>

## <a name="syntax"></a><span data-ttu-id="4073b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4073b-105">Syntax</span></span>


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="4073b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4073b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4073b-107">*Тема* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4073b-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4073b-108">Определяет класс CIM, для которого метод возвращает ссылки на экземпляры [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, доступные для записи во всех экземплярах класса.</span><span class="sxs-lookup"><span data-stu-id="4073b-108">Identifies a CIM class for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are available to be captured for all instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="4073b-109">*Определение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4073b-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4073b-110">Идентифицирует экземпляр [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="4073b-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="4073b-111">Метод возвращает ссылки на экземпляры [**CIM \_ манажеделемент**](cim-managedelement.md) , для которых можно собирать метрики, определенные экземпляром **CIM \_ басеметрикдефинитион** .</span><span class="sxs-lookup"><span data-stu-id="4073b-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="4073b-112">*Дефинитионлист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4073b-112">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4073b-113">После успешного завершения метода может содержать ссылки на экземпляры [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, доступные для сбора для [**\_ манажеделемент CIM**](cim-managedelement.md) , идентифицируемые параметром *subject* .</span><span class="sxs-lookup"><span data-stu-id="4073b-113">Upon successful completion of the method, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4073b-114">*MetricNames* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4073b-114">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4073b-115">После успешного завершения метода каждый индекс массива содержит значение свойства **Name** для экземпляра [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , на который ссылается соответствующий индекс массива параметра *дефинитионлист* .</span><span class="sxs-lookup"><span data-stu-id="4073b-115">Upon successful completion of the method, each array index contains the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4073b-116">*Метрикколлектионенаблед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4073b-116">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4073b-117">Указывает, собирается ли метрика для всех экземпляров класса управляемых элементов.</span><span class="sxs-lookup"><span data-stu-id="4073b-117">Indicates whether a metric is being collected for all instances of a class of managed elements.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4073b-118">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="4073b-118">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4073b-119">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="4073b-119">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="4073b-120">**Зарезервировано** (4)</span><span class="sxs-lookup"><span data-stu-id="4073b-120">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4073b-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="4073b-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="4073b-122">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="4073b-122">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="4073b-123"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4073b-123"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="4073b-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4073b-124">Return value</span></span>

<span data-ttu-id="4073b-125">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4073b-125">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="4073b-126">**Успешно** ()</span><span class="sxs-lookup"><span data-stu-id="4073b-126">**Success** ()</span></span>
</dt> <dt>

<span data-ttu-id="4073b-127">**Не поддерживается** ()</span><span class="sxs-lookup"><span data-stu-id="4073b-127">**Not Supported** ()</span></span>
</dt> <dt>

<span data-ttu-id="4073b-128">**Сбой** ()</span><span class="sxs-lookup"><span data-stu-id="4073b-128">**Failed** ()</span></span>
</dt> <dt>

<span data-ttu-id="4073b-129">**Метод зарезервирован** ()</span><span class="sxs-lookup"><span data-stu-id="4073b-129">**Method Reserved** ()</span></span>
</dt> <dt>

<span data-ttu-id="4073b-130">**Зависит от поставщика** ()</span><span class="sxs-lookup"><span data-stu-id="4073b-130">**Vendor Specific** ()</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4073b-131">Требования</span><span class="sxs-lookup"><span data-stu-id="4073b-131">Requirements</span></span>



| <span data-ttu-id="4073b-132">Требование</span><span class="sxs-lookup"><span data-stu-id="4073b-132">Requirement</span></span> | <span data-ttu-id="4073b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4073b-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4073b-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4073b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4073b-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4073b-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4073b-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4073b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4073b-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4073b-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4073b-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4073b-138">Namespace</span></span><br/>                | <span data-ttu-id="4073b-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4073b-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4073b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="4073b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4073b-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4073b-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4073b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4073b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4073b-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4073b-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4073b-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4073b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4073b-145">**Мсвм \_ метриксервице**</span><span class="sxs-lookup"><span data-stu-id="4073b-145">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 





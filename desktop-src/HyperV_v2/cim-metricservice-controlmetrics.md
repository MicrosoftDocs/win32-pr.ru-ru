---
description: Метод Контролметрикс класса CIM_MetricService — включает и отключает сбор метрик.
ms.assetid: afb90863-e70a-46e5-b1b7-d959dcacc306
title: Метод Контролметрикс класса CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 19e732e50f8c367463e7f528a520a736117999b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090872"
---
# <a name="controlmetrics-method-of-the-cim_metricservice-class"></a><span data-ttu-id="f2583-103">Метод Контролметрикс \_ класса CIM метриксервице</span><span class="sxs-lookup"><span data-stu-id="f2583-103">ControlMetrics method of the CIM\_MetricService class</span></span>

<span data-ttu-id="f2583-104">Включает и отключает сбор метрик. **Контролметрикс** используется для управления сбором каждого типа метрики для [**CIM \_ манажеделемент**](cim-managedelement.md), коллекции заданного типа метрики для всех управляемых элементов или коллекции определенной метрики для конкретного управляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="f2583-104">Enables and disables the collection of metrics.**ControlMetrics** is used to control the collection of each type of metric for a [**CIM\_ManagedElement**](cim-managedelement.md), the collection of a given type of metric for all managed elements, or the collection of a specific metric for a specific managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2583-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2583-105">Syntax</span></span>


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="f2583-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2583-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2583-107">*Тема* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2583-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2583-108">[**\_ Манажеделемент CIM**](cim-managedelement.md) , определяющий управляемые элементы, для которых будут контролироваться метрики.</span><span class="sxs-lookup"><span data-stu-id="f2583-108">A [**CIM\_ManagedElement**](cim-managedelement.md) that identifies managed element(s) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="f2583-109">*Определение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2583-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2583-110">Определяет [**CIM- \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , для которой будут контролироваться метрики.</span><span class="sxs-lookup"><span data-stu-id="f2583-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="f2583-111">*Метрикколлектионенаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2583-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2583-112">Указывает требуемую операцию для метрик.</span><span class="sxs-lookup"><span data-stu-id="f2583-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="f2583-113">**Включить** (2)</span><span class="sxs-lookup"><span data-stu-id="f2583-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="f2583-114">**Отключить** (3)</span><span class="sxs-lookup"><span data-stu-id="f2583-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="f2583-115">**Сброс** (4)</span><span class="sxs-lookup"><span data-stu-id="f2583-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f2583-116">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="f2583-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f2583-117">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="f2583-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="f2583-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f2583-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="f2583-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2583-119">Return value</span></span>

<span data-ttu-id="f2583-120">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f2583-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f2583-121">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="f2583-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f2583-122">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="f2583-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f2583-123">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="f2583-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f2583-124">**Метод зарезервирован** (..)</span><span class="sxs-lookup"><span data-stu-id="f2583-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f2583-125">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="f2583-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f2583-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f2583-126">Requirements</span></span>



| <span data-ttu-id="f2583-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f2583-127">Requirement</span></span> | <span data-ttu-id="f2583-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f2583-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2583-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2583-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f2583-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f2583-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f2583-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2583-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f2583-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f2583-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f2583-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f2583-133">Namespace</span></span><br/>                | <span data-ttu-id="f2583-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f2583-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f2583-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f2583-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2583-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2583-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2583-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f2583-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2583-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f2583-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f2583-139">См. также</span><span class="sxs-lookup"><span data-stu-id="f2583-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2583-140">**\_МЕТРИКСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="f2583-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 





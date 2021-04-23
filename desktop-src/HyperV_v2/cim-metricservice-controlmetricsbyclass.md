---
description: Включает и отключает сбор метрик.
ms.assetid: 1a53c7a7-c0fc-49d7-ad1b-d185d776ede5
title: Метод Контролметриксбикласс класса CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 46e961b298c212a7635599818fb1f7079805372d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663475"
---
# <a name="controlmetricsbyclass-method-of-the-cim_metricservice-class"></a><span data-ttu-id="cbdbf-103">Метод Контролметриксбикласс \_ класса CIM метриксервице</span><span class="sxs-lookup"><span data-stu-id="cbdbf-103">ControlMetricsByClass method of the CIM\_MetricService class</span></span>

<span data-ttu-id="cbdbf-104">Включает и отключает сбор метрик. **Контролметриксбикласс** используется для управления сбором каждого типа метрики для всех экземпляров класса или коллекции определенной метрики для всех экземпляров класса.</span><span class="sxs-lookup"><span data-stu-id="cbdbf-104">Enables and disables the collection of metrics.**ControlMetricsByClass** is used to control the collection of each type of metric for all instances of a class or the collection of a specific metric for all instances of a class.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbdbf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbdbf-105">Syntax</span></span>


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="cbdbf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbdbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbdbf-107">*Тема* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbdbf-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbdbf-108">Идентифицирует класс [**CIM \_ манажеделемент**](cim-managedelement.md) , для которого будут контролироваться метрики.</span><span class="sxs-lookup"><span data-stu-id="cbdbf-108">Identifies the [**CIM\_ManagedElement**](cim-managedelement.md) class for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="cbdbf-109">*Определение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbdbf-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbdbf-110">Определяет [**CIM- \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , для которой будут контролироваться метрики.</span><span class="sxs-lookup"><span data-stu-id="cbdbf-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="cbdbf-111">*Метрикколлектионенаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbdbf-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbdbf-112">Указывает требуемую операцию для метрик.</span><span class="sxs-lookup"><span data-stu-id="cbdbf-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="cbdbf-113">**Включить** (2)</span><span class="sxs-lookup"><span data-stu-id="cbdbf-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="cbdbf-114">**Отключить** (3)</span><span class="sxs-lookup"><span data-stu-id="cbdbf-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="cbdbf-115">**Сброс** (4)</span><span class="sxs-lookup"><span data-stu-id="cbdbf-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cbdbf-116">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="cbdbf-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="cbdbf-117">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="cbdbf-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="cbdbf-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cbdbf-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="cbdbf-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbdbf-119">Return value</span></span>

<span data-ttu-id="cbdbf-120">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="cbdbf-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="cbdbf-121">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="cbdbf-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cbdbf-122">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="cbdbf-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cbdbf-123">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="cbdbf-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cbdbf-124">**Метод зарезервирован** (..)</span><span class="sxs-lookup"><span data-stu-id="cbdbf-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cbdbf-125">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="cbdbf-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cbdbf-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cbdbf-126">Requirements</span></span>



| <span data-ttu-id="cbdbf-127">Требование</span><span class="sxs-lookup"><span data-stu-id="cbdbf-127">Requirement</span></span> | <span data-ttu-id="cbdbf-128">Значение</span><span class="sxs-lookup"><span data-stu-id="cbdbf-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbdbf-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cbdbf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cbdbf-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cbdbf-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="cbdbf-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cbdbf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cbdbf-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="cbdbf-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="cbdbf-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cbdbf-133">Namespace</span></span><br/>                | <span data-ttu-id="cbdbf-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="cbdbf-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cbdbf-135">MOF</span><span class="sxs-lookup"><span data-stu-id="cbdbf-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbdbf-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cbdbf-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbdbf-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cbdbf-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbdbf-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cbdbf-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cbdbf-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbdbf-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbdbf-140">**\_МЕТРИКСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="cbdbf-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 





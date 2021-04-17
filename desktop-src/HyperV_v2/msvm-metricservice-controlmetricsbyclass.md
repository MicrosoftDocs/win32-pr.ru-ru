---
description: Управляет метриками по классу.
ms.assetid: f848fdec-561b-4be0-b1e9-a59e15196d1d
title: Метод Контролметриксбикласс класса Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4149da6327edf774afda20e64f34ae0958f7c3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684472"
---
# <a name="controlmetricsbyclass-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="cfbb9-103">Метод Контролметриксбикласс \_ класса Метриксервице мсвм</span><span class="sxs-lookup"><span data-stu-id="cfbb9-103">ControlMetricsByClass method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="cfbb9-104">Управляет метриками по классу.</span><span class="sxs-lookup"><span data-stu-id="cfbb9-104">Controls metrics by class.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfbb9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfbb9-105">Syntax</span></span>


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="cfbb9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfbb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfbb9-107">*Тема* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cfbb9-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfbb9-108">Определяет класс CIM, для которого будут контролироваться метрики.</span><span class="sxs-lookup"><span data-stu-id="cfbb9-108">Identifies the CIM class for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="cfbb9-109">*Определение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cfbb9-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfbb9-110">Определяет [**CIM- \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , для которой будут контролироваться метрики.</span><span class="sxs-lookup"><span data-stu-id="cfbb9-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="cfbb9-111">*Метрикколлектионенаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cfbb9-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfbb9-112">Указывает требуемую операцию для метрик.</span><span class="sxs-lookup"><span data-stu-id="cfbb9-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="cfbb9-113">**Включить** (2)</span><span class="sxs-lookup"><span data-stu-id="cfbb9-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="cfbb9-114">**Отключить** (3)</span><span class="sxs-lookup"><span data-stu-id="cfbb9-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="cfbb9-115">**Сброс** (4)</span><span class="sxs-lookup"><span data-stu-id="cfbb9-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cfbb9-116">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="cfbb9-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="cfbb9-117">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="cfbb9-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="cfbb9-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cfbb9-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="cfbb9-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cfbb9-119">Return value</span></span>

<span data-ttu-id="cfbb9-120">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="cfbb9-120">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="cfbb9-121">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="cfbb9-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cfbb9-122">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="cfbb9-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cfbb9-123">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="cfbb9-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cfbb9-124">**Метод зарезервирован** (..)</span><span class="sxs-lookup"><span data-stu-id="cfbb9-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cfbb9-125">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="cfbb9-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cfbb9-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cfbb9-126">Requirements</span></span>



| <span data-ttu-id="cfbb9-127">Требование</span><span class="sxs-lookup"><span data-stu-id="cfbb9-127">Requirement</span></span> | <span data-ttu-id="cfbb9-128">Значение</span><span class="sxs-lookup"><span data-stu-id="cfbb9-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbb9-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cfbb9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cfbb9-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cfbb9-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="cfbb9-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cfbb9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cfbb9-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="cfbb9-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="cfbb9-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cfbb9-133">Namespace</span></span><br/>                | <span data-ttu-id="cfbb9-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="cfbb9-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cfbb9-135">MOF</span><span class="sxs-lookup"><span data-stu-id="cfbb9-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfbb9-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cfbb9-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfbb9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cfbb9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfbb9-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cfbb9-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cfbb9-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cfbb9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfbb9-140">**Мсвм \_ метриксервице**</span><span class="sxs-lookup"><span data-stu-id="cfbb9-140">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 





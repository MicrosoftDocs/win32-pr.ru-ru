---
title: Каунтеритем. метод Statistics
description: Возвращает среднее, максимальное и минимальное значения счетчика.
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
keywords:
- Метод Сисмон
- Метод Сисмон, класс Каунтеритем
- Каунтеритем Class Сисмон, метод Statistics
topic_type:
- apiref
api_name:
- CounterItem.GetStatistics
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c993ed8b9bb39a4d8bb3ff18663f2d884ece156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988783"
---
# <a name="counteritemgetstatistics-method"></a><span data-ttu-id="5f8e0-106">Каунтеритем. метод Statistics</span><span class="sxs-lookup"><span data-stu-id="5f8e0-106">CounterItem.GetStatistics method</span></span>

<span data-ttu-id="5f8e0-107">Возвращает среднее, максимальное и минимальное значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-107">Retrieves the average, maximum, and minimum values for the counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f8e0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f8e0-108">Syntax</span></span>


```VB
CounterItem.GetStatistics( _
  ByRef max As Double, _
  ByRef min As Double, _
  ByRef average As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="5f8e0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f8e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f8e0-110">*Максимальное число* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5f8e0-110">*max* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8e0-111">Максимальное значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-111">Maximum value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e0-112">*минимальное* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5f8e0-112">*min* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8e0-113">Минимальное значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-113">Minimum value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e0-114">*среднее значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5f8e0-114">*average* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8e0-115">Среднее значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-115">Average value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e0-116">*состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5f8e0-116">*status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8e0-117">Указывает, являются ли значения допустимыми.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-117">Indicates if the values are valid.</span></span>



| <span data-ttu-id="5f8e0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5f8e0-118">Value</span></span>                                                                                              | <span data-ttu-id="5f8e0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5f8e0-119">Meaning</span></span>                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="5f8e0-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5f8e0-120"><dt>0</dt></span></span> </dl>                       | <span data-ttu-id="5f8e0-121">Допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-121">The values are valid.</span></span><br/>     |
| <dl> <span data-ttu-id="5f8e0-122"><dt>0xC0000BBA (3221228474)</dt></span><span class="sxs-lookup"><span data-stu-id="5f8e0-122"><dt>0xC0000BBA (3221228474)</dt></span></span> </dl> | <span data-ttu-id="5f8e0-123">Недопустимые значения.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-123">The values are not valid.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f8e0-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f8e0-124">Return value</span></span>

<span data-ttu-id="5f8e0-125">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-125">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f8e0-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f8e0-126">Remarks</span></span>

<span data-ttu-id="5f8e0-127">Для вычисления статистических значений используются только те значения счетчика, которые видны в окне графа.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-127">Only those counter values that are visible in the graph window are used to calculate the statistical values.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f8e0-128">Требования</span><span class="sxs-lookup"><span data-stu-id="5f8e0-128">Requirements</span></span>



| <span data-ttu-id="5f8e0-129">Требование</span><span class="sxs-lookup"><span data-stu-id="5f8e0-129">Requirement</span></span> | <span data-ttu-id="5f8e0-130">Значение</span><span class="sxs-lookup"><span data-stu-id="5f8e0-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f8e0-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f8e0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5f8e0-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5f8e0-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5f8e0-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f8e0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5f8e0-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5f8e0-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f8e0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5f8e0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f8e0-136"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5f8e0-136"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f8e0-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f8e0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f8e0-138">**каунтеритем**</span><span class="sxs-lookup"><span data-stu-id="5f8e0-138">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="5f8e0-139">**Каунтеритем. Жетдатаат**</span><span class="sxs-lookup"><span data-stu-id="5f8e0-139">**CounterItem.GetDataAt**</span></span>](counteritem-getdataat.md)
</dt> <dt>

[<span data-ttu-id="5f8e0-140">**Каунтеритем. GetValue**</span><span class="sxs-lookup"><span data-stu-id="5f8e0-140">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 






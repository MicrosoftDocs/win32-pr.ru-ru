---
title: Метод Counters. Remove
description: Удаляет экземпляр Каунтеритем из коллекции.
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- Удалить метод Сисмон
- Remove Method Сисмон, класс Counters
- Counters Class Сисмон, Remove, метод
topic_type:
- apiref
api_name:
- Counters.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa82a1a988be3554c265c097ba2a582035547391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988524"
---
# <a name="countersremove-method"></a><span data-ttu-id="e7cf1-106">Метод Counters. Remove</span><span class="sxs-lookup"><span data-stu-id="e7cf1-106">Counters.Remove method</span></span>

<span data-ttu-id="e7cf1-107">Удаляет экземпляр [**каунтеритем**](counteritem.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="e7cf1-107">Removes a [**CounterItem**](counteritem.md) instance from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7cf1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7cf1-108">Syntax</span></span>


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="e7cf1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7cf1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7cf1-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e7cf1-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7cf1-111">Индекс объекта [**каунтеритем**](counteritem.md) , который необходимо удалить из коллекции.</span><span class="sxs-lookup"><span data-stu-id="e7cf1-111">Index of the [**CounterItem**](counteritem.md) object to remove from the collection.</span></span> <span data-ttu-id="e7cf1-112">Индекс основан на единицах.</span><span class="sxs-lookup"><span data-stu-id="e7cf1-112">The index is one-based.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7cf1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7cf1-113">Return value</span></span>

<span data-ttu-id="e7cf1-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e7cf1-114">This method does not return a value.</span></span>

## <a name="exceptions"></a><span data-ttu-id="e7cf1-115">Исключения</span><span class="sxs-lookup"><span data-stu-id="e7cf1-115">Exceptions</span></span>



| <span data-ttu-id="e7cf1-116">Тип исключения</span><span class="sxs-lookup"><span data-stu-id="e7cf1-116">Exception type</span></span>                                  | <span data-ttu-id="e7cf1-117">Условие</span><span class="sxs-lookup"><span data-stu-id="e7cf1-117">Condition</span></span>                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="e7cf1-118">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="e7cf1-118">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="e7cf1-119">Указан недопустимый индекс.</span><span class="sxs-lookup"><span data-stu-id="e7cf1-119">The specified index is not valid.</span></span> <span data-ttu-id="e7cf1-120">Значение Err. Number —???.</span><span class="sxs-lookup"><span data-stu-id="e7cf1-120">The Err.Number value is ???.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e7cf1-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7cf1-121">Remarks</span></span>

<span data-ttu-id="e7cf1-122">Чтобы удалить все счетчики из коллекции, можно вызвать [**системмонитор. Reset**](systemmonitor-reset.md).</span><span class="sxs-lookup"><span data-stu-id="e7cf1-122">To remove all counters from the collection, you can call [**SystemMonitor.Reset**](systemmonitor-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7cf1-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e7cf1-123">Requirements</span></span>



| <span data-ttu-id="e7cf1-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e7cf1-124">Requirement</span></span> | <span data-ttu-id="e7cf1-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e7cf1-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7cf1-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7cf1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e7cf1-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e7cf1-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e7cf1-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7cf1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e7cf1-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e7cf1-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7cf1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e7cf1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7cf1-131"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e7cf1-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7cf1-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7cf1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7cf1-133">**Счетчики**</span><span class="sxs-lookup"><span data-stu-id="e7cf1-133">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="e7cf1-134">**Системмонитор. Reset**</span><span class="sxs-lookup"><span data-stu-id="e7cf1-134">**SystemMonitor.Reset**</span></span>](systemmonitor-reset.md)
</dt> </dl>

 

 






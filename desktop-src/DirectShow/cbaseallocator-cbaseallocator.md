---
description: Метод конструктора.
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: Конструктор Кбасеаллокатор. Кбасеаллокатор (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98a1ba1163058f92fba666177d0ff82331dd528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656838"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a><span data-ttu-id="773cb-103">Кбасеаллокатор. Кбасеаллокатор, конструктор</span><span class="sxs-lookup"><span data-stu-id="773cb-103">CBaseAllocator.CBaseAllocator constructor</span></span>

<span data-ttu-id="773cb-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="773cb-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="773cb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="773cb-105">Syntax</span></span>


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="773cb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="773cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="773cb-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="773cb-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="773cb-108">Указатель на строку, содержащую имя отладки распределителя.</span><span class="sxs-lookup"><span data-stu-id="773cb-108">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="773cb-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="773cb-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="773cb-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="773cb-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="773cb-111">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="773cb-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="773cb-112">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="773cb-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="773cb-113">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="773cb-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="773cb-114">*фр*</span><span class="sxs-lookup"><span data-stu-id="773cb-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="773cb-115">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="773cb-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="773cb-116">Перед созданием объекта задайте для него значение " \_ ОК".</span><span class="sxs-lookup"><span data-stu-id="773cb-116">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="773cb-117">Если конструктор завершается неудачно, ему присваивается значение кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="773cb-117">If the constructor fails, the value is set to an error code.</span></span>

</dd> <dt>

<span data-ttu-id="773cb-118">*перевентиляционное отверстие*</span><span class="sxs-lookup"><span data-stu-id="773cb-118">*bEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="773cb-119">Логическое значение, указывающее, следует ли создать семафор.</span><span class="sxs-lookup"><span data-stu-id="773cb-119">Boolean value indicating whether to create a semaphore.</span></span> <span data-ttu-id="773cb-120">Если **значение — true**, распределитель создает семафор ([**кбасеаллокатор:: m \_ хсем**](cbaseallocator-m-hsem.md)), который сигнализирует, когда станет доступным образец.</span><span class="sxs-lookup"><span data-stu-id="773cb-120">If **TRUE**, the allocator creates a semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)), which is signaled whenever a sample becomes available.</span></span> <span data-ttu-id="773cb-121">Если реализуется производный класс, для которого не требуется семафор, установите значение **false** .</span><span class="sxs-lookup"><span data-stu-id="773cb-121">Set the value to **FALSE** if you are implementing a derived class that does not require a semaphore.</span></span>

</dd> <dt>

<span data-ttu-id="773cb-122">*фенаблерелеасекаллбакк*</span><span class="sxs-lookup"><span data-stu-id="773cb-122">*fEnableReleaseCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="773cb-123">Логическое значение, указывающее, включен ли механизм обратного вызова выпуска.</span><span class="sxs-lookup"><span data-stu-id="773cb-123">Boolean value indicating whether the release callback mechanism is enabled.</span></span> <span data-ttu-id="773cb-124">Задайте значение **true** , если требуется предоставить интерфейс обратного вызова, который вызывается при освобождении буферов.</span><span class="sxs-lookup"><span data-stu-id="773cb-124">Set the value to **TRUE** if you want to supply a callback interface, which is called when buffers are released.</span></span> <span data-ttu-id="773cb-125">Укажите обратный вызов, вызвав метод [**кбасеаллокатор:: сетнотифи**](cbaseallocator-setnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="773cb-125">Specify the callback by calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="773cb-126">Требования</span><span class="sxs-lookup"><span data-stu-id="773cb-126">Requirements</span></span>



| <span data-ttu-id="773cb-127">Требование</span><span class="sxs-lookup"><span data-stu-id="773cb-127">Requirement</span></span> | <span data-ttu-id="773cb-128">Значение</span><span class="sxs-lookup"><span data-stu-id="773cb-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="773cb-129">Header</span><span class="sxs-lookup"><span data-stu-id="773cb-129">Header</span></span><br/>  | <dl> <span data-ttu-id="773cb-130"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="773cb-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="773cb-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="773cb-131">Library</span></span><br/> | <dl> <span data-ttu-id="773cb-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="773cb-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="773cb-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="773cb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="773cb-134">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="773cb-134">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 





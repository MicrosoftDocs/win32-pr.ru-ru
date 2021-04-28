---
description: Метод конструктора Цимажеаллокатор. Цимажеаллокатор.
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: Конструктор Цимажеаллокатор. Цимажеаллокатор (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f17ae78b668f6cc35e454c5e4e83d38727077ef7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085762"
---
# <a name="cimageallocatorcimageallocator-constructor"></a><span data-ttu-id="5ce10-103">Цимажеаллокатор. Цимажеаллокатор, конструктор</span><span class="sxs-lookup"><span data-stu-id="5ce10-103">CImageAllocator.CImageAllocator constructor</span></span>

<span data-ttu-id="5ce10-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="5ce10-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ce10-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ce10-105">Syntax</span></span>


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="5ce10-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ce10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ce10-107">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="5ce10-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="5ce10-108">Указатель на фильтр-владелец.</span><span class="sxs-lookup"><span data-stu-id="5ce10-108">Pointer to the owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="5ce10-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="5ce10-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="5ce10-110">Указатель на строку, содержащую имя отладки распределителя.</span><span class="sxs-lookup"><span data-stu-id="5ce10-110">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="5ce10-111">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="5ce10-111">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ce10-112">*фр*</span><span class="sxs-lookup"><span data-stu-id="5ce10-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="5ce10-113">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5ce10-113">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="5ce10-114">Перед созданием объекта задайте для него значение " \_ ОК".</span><span class="sxs-lookup"><span data-stu-id="5ce10-114">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="5ce10-115">Если конструктор завершается неудачно, ему присваивается значение кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="5ce10-115">If the constructor fails, the value is set to an error code.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ce10-116">Требования</span><span class="sxs-lookup"><span data-stu-id="5ce10-116">Requirements</span></span>



| <span data-ttu-id="5ce10-117">Требование</span><span class="sxs-lookup"><span data-stu-id="5ce10-117">Requirement</span></span> | <span data-ttu-id="5ce10-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5ce10-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ce10-119">Header</span><span class="sxs-lookup"><span data-stu-id="5ce10-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5ce10-120"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ce10-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5ce10-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5ce10-121">Library</span></span><br/> | <dl> <span data-ttu-id="5ce10-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5ce10-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ce10-123">См. также</span><span class="sxs-lookup"><span data-stu-id="5ce10-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ce10-124">**Класс Цимажеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="5ce10-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 





---
description: Метод конструктора.
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
ms.openlocfilehash: a5f6873e8cc073e0b716f94c980ecceba8f4512f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657543"
---
# <a name="cimageallocatorcimageallocator-constructor"></a><span data-ttu-id="6f022-103">Цимажеаллокатор. Цимажеаллокатор, конструктор</span><span class="sxs-lookup"><span data-stu-id="6f022-103">CImageAllocator.CImageAllocator constructor</span></span>

<span data-ttu-id="6f022-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="6f022-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f022-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f022-105">Syntax</span></span>


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="6f022-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f022-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f022-107">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="6f022-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="6f022-108">Указатель на фильтр-владелец.</span><span class="sxs-lookup"><span data-stu-id="6f022-108">Pointer to the owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="6f022-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="6f022-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="6f022-110">Указатель на строку, содержащую имя отладки распределителя.</span><span class="sxs-lookup"><span data-stu-id="6f022-110">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="6f022-111">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="6f022-111">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f022-112">*фр*</span><span class="sxs-lookup"><span data-stu-id="6f022-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="6f022-113">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6f022-113">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="6f022-114">Перед созданием объекта задайте для него значение " \_ ОК".</span><span class="sxs-lookup"><span data-stu-id="6f022-114">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="6f022-115">Если конструктор завершается неудачно, ему присваивается значение кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="6f022-115">If the constructor fails, the value is set to an error code.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f022-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6f022-116">Requirements</span></span>



| <span data-ttu-id="6f022-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6f022-117">Requirement</span></span> | <span data-ttu-id="6f022-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6f022-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f022-119">Header</span><span class="sxs-lookup"><span data-stu-id="6f022-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6f022-120"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f022-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6f022-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6f022-121">Library</span></span><br/> | <dl> <span data-ttu-id="6f022-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6f022-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f022-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f022-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f022-124">**Класс Цимажеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="6f022-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 





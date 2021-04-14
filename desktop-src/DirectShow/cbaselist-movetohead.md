---
description: Метод Моветохеад разделяет список и вставляет фрагмент хвоста в заголовок другого списка.
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: Кбаселист. Моветохеад, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80adec6c8e2f6d42b5cf2cabd3a83a4c3aededa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668598"
---
# <a name="cbaselistmovetohead-method"></a><span data-ttu-id="6c55d-103">Кбаселист. Моветохеад, метод</span><span class="sxs-lookup"><span data-stu-id="6c55d-103">CBaseList.MoveToHead method</span></span>

<span data-ttu-id="6c55d-104">`MoveToHead`Метод разделяет список и вставляет фрагмент хвоста в начало другого списка.</span><span class="sxs-lookup"><span data-stu-id="6c55d-104">The `MoveToHead` method splits the list and inserts the tail portion at the head of another list.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c55d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c55d-105">Syntax</span></span>


```C++
BOOL MoveToHead(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="6c55d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c55d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c55d-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="6c55d-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="6c55d-108">Индикатор положения, помечающий разбиение в списке.</span><span class="sxs-lookup"><span data-stu-id="6c55d-108">Position indicator that marks the split in the list.</span></span>

</dd> <dt>

<span data-ttu-id="6c55d-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="6c55d-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="6c55d-110">Указатель на другой список.</span><span class="sxs-lookup"><span data-stu-id="6c55d-110">Pointer to another list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c55d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c55d-111">Return value</span></span>

<span data-ttu-id="6c55d-112">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6c55d-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c55d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c55d-113">Remarks</span></span>

<span data-ttu-id="6c55d-114">Этот метод разделяет список перед позицией, заданной параметром *POS* .</span><span class="sxs-lookup"><span data-stu-id="6c55d-114">This method splits the list before the position specified by the *pos* parameter.</span></span> <span data-ttu-id="6c55d-115">Главная часть остается в списке.</span><span class="sxs-lookup"><span data-stu-id="6c55d-115">The head portion remains in the list.</span></span> <span data-ttu-id="6c55d-116">Заключительная часть вставляется в заголовок другого списка.</span><span class="sxs-lookup"><span data-stu-id="6c55d-116">The tail portion is inserted at the head of the other list.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c55d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6c55d-117">Requirements</span></span>



| <span data-ttu-id="6c55d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6c55d-118">Requirement</span></span> | <span data-ttu-id="6c55d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6c55d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c55d-120">Header</span><span class="sxs-lookup"><span data-stu-id="6c55d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6c55d-121"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c55d-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6c55d-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6c55d-122">Library</span></span><br/> | <dl> <span data-ttu-id="6c55d-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6c55d-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c55d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c55d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c55d-125">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="6c55d-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





---
description: Метод Моветотаил разделяет список и добавляет его в конец другого списка.
ms.assetid: f5cefe7c-075c-433b-9ece-aa10217344fa
title: Кбаселист. Моветотаил, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c28e1051c08884e70e56b25b0fb2707ccd55ed1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657388"
---
# <a name="cbaselistmovetotail-method"></a><span data-ttu-id="85a7d-103">Кбаселист. Моветотаил, метод</span><span class="sxs-lookup"><span data-stu-id="85a7d-103">CBaseList.MoveToTail method</span></span>

<span data-ttu-id="85a7d-104">`MoveToTail`Метод разбивает список и добавляет его в конец другого списка.</span><span class="sxs-lookup"><span data-stu-id="85a7d-104">The `MoveToTail` method splits the list and appends the head portion to the tail of another list.</span></span>

## <a name="syntax"></a><span data-ttu-id="85a7d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85a7d-105">Syntax</span></span>


```C++
BOOL MoveToTail(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="85a7d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85a7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85a7d-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="85a7d-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="85a7d-108">Индикатор положения, помечающий разбиение в списке.</span><span class="sxs-lookup"><span data-stu-id="85a7d-108">Position indicator that marks the split in the list.</span></span>

</dd> <dt>

<span data-ttu-id="85a7d-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="85a7d-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="85a7d-110">Указатель на другой список.</span><span class="sxs-lookup"><span data-stu-id="85a7d-110">Pointer to another list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85a7d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85a7d-111">Return value</span></span>

<span data-ttu-id="85a7d-112">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="85a7d-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="85a7d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85a7d-113">Remarks</span></span>

<span data-ttu-id="85a7d-114">Этот метод разделяет список после того, как позиция задается параметром *POS* .</span><span class="sxs-lookup"><span data-stu-id="85a7d-114">This method splits the list after the position specified by the *pos* parameter.</span></span> <span data-ttu-id="85a7d-115">Заключительная часть остается в списке.</span><span class="sxs-lookup"><span data-stu-id="85a7d-115">The tail portion remains in the list.</span></span> <span data-ttu-id="85a7d-116">Главная часть добавляется в конец другого списка.</span><span class="sxs-lookup"><span data-stu-id="85a7d-116">The head portion is appended to the tail of the other list.</span></span>

## <a name="requirements"></a><span data-ttu-id="85a7d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="85a7d-117">Requirements</span></span>



| <span data-ttu-id="85a7d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="85a7d-118">Requirement</span></span> | <span data-ttu-id="85a7d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="85a7d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85a7d-120">Header</span><span class="sxs-lookup"><span data-stu-id="85a7d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="85a7d-121"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85a7d-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="85a7d-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="85a7d-122">Library</span></span><br/> | <dl> <span data-ttu-id="85a7d-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="85a7d-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85a7d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85a7d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85a7d-125">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="85a7d-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





---
description: Метод AddTail добавляет еще один список в конец этого списка.
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: Кбаселист. AddTail, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36d42f0b80703457032e5dde37f6d1549da089c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668610"
---
# <a name="cbaselistaddtail-method"></a><span data-ttu-id="87dca-103">Кбаселист. AddTail, метод</span><span class="sxs-lookup"><span data-stu-id="87dca-103">CBaseList.AddTail method</span></span>

<span data-ttu-id="87dca-104">`AddTail`Метод добавляет еще один список в конец этого списка.</span><span class="sxs-lookup"><span data-stu-id="87dca-104">The `AddTail` method appends another list to the end of this list.</span></span>

## <a name="syntax"></a><span data-ttu-id="87dca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87dca-105">Syntax</span></span>


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="87dca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87dca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87dca-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="87dca-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="87dca-108">Указатель на добавляемый список.</span><span class="sxs-lookup"><span data-stu-id="87dca-108">Pointer to the list to append.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87dca-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87dca-109">Return value</span></span>

<span data-ttu-id="87dca-110">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="87dca-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="87dca-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87dca-111">Remarks</span></span>

<span data-ttu-id="87dca-112">В случае сбоя метода некоторые элементы могут быть добавлены в список.</span><span class="sxs-lookup"><span data-stu-id="87dca-112">If the method fails, some items may have been added to the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="87dca-113">Требования</span><span class="sxs-lookup"><span data-stu-id="87dca-113">Requirements</span></span>



| <span data-ttu-id="87dca-114">Требование</span><span class="sxs-lookup"><span data-stu-id="87dca-114">Requirement</span></span> | <span data-ttu-id="87dca-115">Значение</span><span class="sxs-lookup"><span data-stu-id="87dca-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87dca-116">Header</span><span class="sxs-lookup"><span data-stu-id="87dca-116">Header</span></span><br/>  | <dl> <span data-ttu-id="87dca-117"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87dca-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="87dca-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="87dca-118">Library</span></span><br/> | <dl> <span data-ttu-id="87dca-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="87dca-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87dca-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87dca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87dca-121">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="87dca-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





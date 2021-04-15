---
description: Метод Аддхеади добавляет элемент в начало списка.
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: Кбаселист. Аддхеади, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6104b6acae0f22c028f3bad050567f4da34ff0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668611"
---
# <a name="cbaselistaddheadi-method"></a><span data-ttu-id="5633e-103">Кбаселист. Аддхеади, метод</span><span class="sxs-lookup"><span data-stu-id="5633e-103">CBaseList.AddHeadI method</span></span>

<span data-ttu-id="5633e-104">`AddHeadI`Метод добавляет элемент в начало списка.</span><span class="sxs-lookup"><span data-stu-id="5633e-104">The `AddHeadI` method adds an item to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="5633e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5633e-105">Syntax</span></span>


```C++
POSITION AddHeadI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="5633e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5633e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5633e-107">*побж*</span><span class="sxs-lookup"><span data-stu-id="5633e-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="5633e-108">Указатель на элемент.</span><span class="sxs-lookup"><span data-stu-id="5633e-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5633e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5633e-109">Return value</span></span>

<span data-ttu-id="5633e-110">Возвращает значение расположения, указывающее новую головную точку.</span><span class="sxs-lookup"><span data-stu-id="5633e-110">Returns a POSITION value indicating the new head position.</span></span>

## <a name="remarks"></a><span data-ttu-id="5633e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5633e-111">Remarks</span></span>

<span data-ttu-id="5633e-112">Если метод завершается ошибкой, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="5633e-112">If the method fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5633e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5633e-113">Requirements</span></span>



| <span data-ttu-id="5633e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5633e-114">Requirement</span></span> | <span data-ttu-id="5633e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5633e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5633e-116">Header</span><span class="sxs-lookup"><span data-stu-id="5633e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5633e-117"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5633e-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5633e-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5633e-118">Library</span></span><br/> | <dl> <span data-ttu-id="5633e-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5633e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5633e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5633e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5633e-121">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="5633e-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





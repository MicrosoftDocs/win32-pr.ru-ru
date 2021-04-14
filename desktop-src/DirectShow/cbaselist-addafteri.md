---
description: Метод Аддафтери вставляет элемент после указанной позиции.
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: Кбаселист. Аддафтери, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfterI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 760c0bea3a213d7126ea795e9575b3897117f7a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668619"
---
# <a name="cbaselistaddafteri-method"></a><span data-ttu-id="4c414-103">Кбаселист. Аддафтери, метод</span><span class="sxs-lookup"><span data-stu-id="4c414-103">CBaseList.AddAfterI method</span></span>

<span data-ttu-id="4c414-104">`AddAfterI`Метод вставляет элемент после указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="4c414-104">The `AddAfterI` method inserts an item after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c414-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c414-105">Syntax</span></span>


```C++
POSITION AddAfterI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="4c414-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c414-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c414-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="4c414-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="4c414-108">Позиция, после которой нужно добавить элемент.</span><span class="sxs-lookup"><span data-stu-id="4c414-108">Position after which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="4c414-109">*побж*</span><span class="sxs-lookup"><span data-stu-id="4c414-109">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="4c414-110">Указатель на добавляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="4c414-110">Pointer to the item to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c414-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c414-111">Return value</span></span>

<span data-ttu-id="4c414-112">Возвращает индикатор позиции вставленного элемента.</span><span class="sxs-lookup"><span data-stu-id="4c414-112">Returns the position indicator of the inserted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c414-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c414-113">Remarks</span></span>

<span data-ttu-id="4c414-114">Если *POS* имеет **значение NULL**, этот метод добавляет элемент в заголовок списка (эквивалентно вызову метода [**кбаселист:: аддхеади**](cbaselist-addheadi.md) ).</span><span class="sxs-lookup"><span data-stu-id="4c414-114">If *pos* is **NULL**, this method adds the item to the head of the list (equivalent to calling the [**CBaseList::AddHeadI**](cbaselist-addheadi.md) method).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c414-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4c414-115">Requirements</span></span>



| <span data-ttu-id="4c414-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4c414-116">Requirement</span></span> | <span data-ttu-id="4c414-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4c414-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c414-118">Header</span><span class="sxs-lookup"><span data-stu-id="4c414-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4c414-119"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c414-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4c414-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4c414-120">Library</span></span><br/> | <dl> <span data-ttu-id="4c414-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4c414-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c414-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c414-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c414-123">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="4c414-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





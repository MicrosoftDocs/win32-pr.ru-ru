---
description: Метод Аддафтер вставляет список после указанной позицией.
ms.assetid: c2a2e599-0a83-4eb0-aceb-c483f153ba7e
title: Кбаселист. Аддафтер, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fdab54a124986b462e0ef592bba888e27c09b53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657402"
---
# <a name="cbaselistaddafter-method"></a><span data-ttu-id="35e73-103">Кбаселист. Аддафтер, метод</span><span class="sxs-lookup"><span data-stu-id="35e73-103">CBaseList.AddAfter method</span></span>

<span data-ttu-id="35e73-104">`AddAfter`Метод вставляет список после указанной позицией.</span><span class="sxs-lookup"><span data-stu-id="35e73-104">The `AddAfter` method inserts a list after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e73-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35e73-105">Syntax</span></span>


```C++
BOOL AddAfter(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="35e73-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="35e73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35e73-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="35e73-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="35e73-108">Расположение, после которого необходимо вставить список.</span><span class="sxs-lookup"><span data-stu-id="35e73-108">Position after which to insert the list.</span></span>

</dd> <dt>

<span data-ttu-id="35e73-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="35e73-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="35e73-110">Указатель на список для вставки.</span><span class="sxs-lookup"><span data-stu-id="35e73-110">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35e73-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35e73-111">Return value</span></span>

<span data-ttu-id="35e73-112">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="35e73-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="35e73-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35e73-113">Remarks</span></span>

<span data-ttu-id="35e73-114">Существующие индикаторы позиционирования, включая указанные в параметре *POS* , остаются действительными.</span><span class="sxs-lookup"><span data-stu-id="35e73-114">Existing position indicators, including the one specified in the *pos* parameter, remain valid.</span></span> <span data-ttu-id="35e73-115">В случае сбоя метода некоторые элементы могли быть добавлены.</span><span class="sxs-lookup"><span data-stu-id="35e73-115">If the method fails, some of the items might have been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="35e73-116">Требования</span><span class="sxs-lookup"><span data-stu-id="35e73-116">Requirements</span></span>



| <span data-ttu-id="35e73-117">Требование</span><span class="sxs-lookup"><span data-stu-id="35e73-117">Requirement</span></span> | <span data-ttu-id="35e73-118">Значение</span><span class="sxs-lookup"><span data-stu-id="35e73-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35e73-119">Header</span><span class="sxs-lookup"><span data-stu-id="35e73-119">Header</span></span><br/>  | <dl> <span data-ttu-id="35e73-120"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35e73-120"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="35e73-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="35e73-121">Library</span></span><br/> | <dl> <span data-ttu-id="35e73-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="35e73-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35e73-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35e73-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35e73-124">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="35e73-124">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





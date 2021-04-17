---
description: Метод Аддбефоре вставляет список перед указанной позицией.
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: Кбаселист. Аддбефоре, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3c25b2dd545b3e6698404bf00f82d1086bfb81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657401"
---
# <a name="cbaselistaddbefore-method"></a><span data-ttu-id="32eea-103">Кбаселист. Аддбефоре, метод</span><span class="sxs-lookup"><span data-stu-id="32eea-103">CBaseList.AddBefore method</span></span>

<span data-ttu-id="32eea-104">`AddBefore`Метод вставляет список перед указанной позицией.</span><span class="sxs-lookup"><span data-stu-id="32eea-104">The `AddBefore` method inserts a list before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="32eea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32eea-105">Syntax</span></span>


```C++
BOOL AddBefore(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="32eea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="32eea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32eea-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="32eea-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="32eea-108">Расположение, до которого необходимо вставить список.</span><span class="sxs-lookup"><span data-stu-id="32eea-108">Position before which to insert the list.</span></span>

</dd> <dt>

<span data-ttu-id="32eea-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="32eea-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="32eea-110">Указатель на список для вставки.</span><span class="sxs-lookup"><span data-stu-id="32eea-110">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32eea-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32eea-111">Return value</span></span>

<span data-ttu-id="32eea-112">Возвращает **значение true** в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="32eea-112">Returns **TRUE** if successful.</span></span> <span data-ttu-id="32eea-113">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="32eea-113">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="32eea-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32eea-114">Remarks</span></span>

<span data-ttu-id="32eea-115">Существующие индикаторы позиционирования, включая указанные в параметре *POS* , остаются действительными.</span><span class="sxs-lookup"><span data-stu-id="32eea-115">Existing position indicators, including the one specified in the *pos* parameter, remain valid.</span></span> <span data-ttu-id="32eea-116">В случае сбоя метода некоторые элементы могли быть добавлены.</span><span class="sxs-lookup"><span data-stu-id="32eea-116">If the method fails, some of the items might have been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="32eea-117">Требования</span><span class="sxs-lookup"><span data-stu-id="32eea-117">Requirements</span></span>



| <span data-ttu-id="32eea-118">Требование</span><span class="sxs-lookup"><span data-stu-id="32eea-118">Requirement</span></span> | <span data-ttu-id="32eea-119">Значение</span><span class="sxs-lookup"><span data-stu-id="32eea-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32eea-120">Header</span><span class="sxs-lookup"><span data-stu-id="32eea-120">Header</span></span><br/>  | <dl> <span data-ttu-id="32eea-121"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32eea-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="32eea-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="32eea-122">Library</span></span><br/> | <dl> <span data-ttu-id="32eea-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="32eea-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32eea-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32eea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32eea-125">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="32eea-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





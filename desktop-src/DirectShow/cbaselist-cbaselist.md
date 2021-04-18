---
description: Метод конструктора.
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: Конструктор Кбаселист. Кбаселист (TCHAR *, INT) (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c947c8ffa6b61f919d03470b386ffa82945f3b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668609"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a><span data-ttu-id="711c3-103">Конструктор Кбаселист. Кбаселист (TCHAR \* , int)</span><span class="sxs-lookup"><span data-stu-id="711c3-103">CBaseList.CBaseList(TCHAR\*, INT) constructor</span></span>

<span data-ttu-id="711c3-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="711c3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="711c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="711c3-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a><span data-ttu-id="711c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="711c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711c3-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="711c3-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="711c3-108">Указатель на имя списка.</span><span class="sxs-lookup"><span data-stu-id="711c3-108">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="711c3-109">*иитемс*</span><span class="sxs-lookup"><span data-stu-id="711c3-109">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="711c3-110">Размер кэша узлов.</span><span class="sxs-lookup"><span data-stu-id="711c3-110">Size of the node cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="711c3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="711c3-111">Remarks</span></span>

<span data-ttu-id="711c3-112">Для повышения эффективности `CBaseList` класс поддерживает кэш узлов списка.</span><span class="sxs-lookup"><span data-stu-id="711c3-112">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="711c3-113">Если вы понимаете, сколько элементов будет храниться в списке, используйте эту версию конструктора.</span><span class="sxs-lookup"><span data-stu-id="711c3-113">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="711c3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="711c3-114">Requirements</span></span>



| <span data-ttu-id="711c3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="711c3-115">Requirement</span></span> | <span data-ttu-id="711c3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="711c3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="711c3-117">Header</span><span class="sxs-lookup"><span data-stu-id="711c3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="711c3-118"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="711c3-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="711c3-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="711c3-119">Library</span></span><br/> | <dl> <span data-ttu-id="711c3-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="711c3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="711c3-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="711c3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="711c3-122">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="711c3-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





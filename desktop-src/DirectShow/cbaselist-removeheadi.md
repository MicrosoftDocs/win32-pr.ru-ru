---
description: Метод Ремовехеади удаляет первый элемент из списка.
ms.assetid: 7e448e32-ea31-4015-9219-1f990bf8763d
title: Кбаселист. Ремовехеади, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d9b99dbac1d99587145aa2eba293ffa7ace959c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668897"
---
# <a name="cbaselistremoveheadi-method"></a><span data-ttu-id="97b8a-103">Кбаселист. Ремовехеади, метод</span><span class="sxs-lookup"><span data-stu-id="97b8a-103">CBaseList.RemoveHeadI method</span></span>

<span data-ttu-id="97b8a-104">`RemoveHeadI`Метод удаляет первый элемент из списка.</span><span class="sxs-lookup"><span data-stu-id="97b8a-104">The `RemoveHeadI` method removes the first item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="97b8a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97b8a-105">Syntax</span></span>


```C++
void* RemoveHeadI();
```



## <a name="parameters"></a><span data-ttu-id="97b8a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="97b8a-106">Parameters</span></span>

<span data-ttu-id="97b8a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="97b8a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="97b8a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97b8a-108">Return value</span></span>

<span data-ttu-id="97b8a-109">Возвращает указатель на элемент или **значение NULL** , если список пуст.</span><span class="sxs-lookup"><span data-stu-id="97b8a-109">Returns a pointer to the item, or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="97b8a-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97b8a-110">Remarks</span></span>

<span data-ttu-id="97b8a-111">Этот метод удаляет узел списка, но не элемент, содержащийся в узле.</span><span class="sxs-lookup"><span data-stu-id="97b8a-111">This method deletes the list node, but not the item that the node contains.</span></span>

## <a name="requirements"></a><span data-ttu-id="97b8a-112">Требования</span><span class="sxs-lookup"><span data-stu-id="97b8a-112">Requirements</span></span>



| <span data-ttu-id="97b8a-113">Требование</span><span class="sxs-lookup"><span data-stu-id="97b8a-113">Requirement</span></span> | <span data-ttu-id="97b8a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="97b8a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97b8a-115">Header</span><span class="sxs-lookup"><span data-stu-id="97b8a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="97b8a-116"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97b8a-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="97b8a-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="97b8a-117">Library</span></span><br/> | <dl> <span data-ttu-id="97b8a-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="97b8a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97b8a-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97b8a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97b8a-120">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="97b8a-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





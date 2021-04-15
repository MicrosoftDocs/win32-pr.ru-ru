---
description: Метод Ремоветаили удаляет последний элемент в списке.
ms.assetid: 3e9f88a5-a681-4494-8977-d9a6ec62a849
title: Кбаселист. Ремоветаили, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17c4e151426b54667ea3b9e4cb88be9526e2054b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668996"
---
# <a name="cbaselistremovetaili-method"></a><span data-ttu-id="cfcdb-103">Кбаселист. Ремоветаили, метод</span><span class="sxs-lookup"><span data-stu-id="cfcdb-103">CBaseList.RemoveTailI method</span></span>

<span data-ttu-id="cfcdb-104">`RemoveTailI`Метод удаляет последний элемент в списке.</span><span class="sxs-lookup"><span data-stu-id="cfcdb-104">The `RemoveTailI` method removes the last item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfcdb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfcdb-105">Syntax</span></span>


```C++
void* RemoveTailI();
```



## <a name="parameters"></a><span data-ttu-id="cfcdb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfcdb-106">Parameters</span></span>

<span data-ttu-id="cfcdb-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cfcdb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cfcdb-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cfcdb-108">Return value</span></span>

<span data-ttu-id="cfcdb-109">Возвращает указатель на элемент или **значение NULL** , если список пуст.</span><span class="sxs-lookup"><span data-stu-id="cfcdb-109">Returns a pointer to the item, or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfcdb-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cfcdb-110">Remarks</span></span>

<span data-ttu-id="cfcdb-111">Этот метод удаляет узел списка, но не элемент, содержащийся в узле.</span><span class="sxs-lookup"><span data-stu-id="cfcdb-111">This method deletes the list node, but not the item that is contained in the node.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfcdb-112">Требования</span><span class="sxs-lookup"><span data-stu-id="cfcdb-112">Requirements</span></span>



| <span data-ttu-id="cfcdb-113">Требование</span><span class="sxs-lookup"><span data-stu-id="cfcdb-113">Requirement</span></span> | <span data-ttu-id="cfcdb-114">Значение</span><span class="sxs-lookup"><span data-stu-id="cfcdb-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfcdb-115">Header</span><span class="sxs-lookup"><span data-stu-id="cfcdb-115">Header</span></span><br/>  | <dl> <span data-ttu-id="cfcdb-116"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cfcdb-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="cfcdb-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cfcdb-117">Library</span></span><br/> | <dl> <span data-ttu-id="cfcdb-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cfcdb-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfcdb-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cfcdb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfcdb-120">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="cfcdb-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





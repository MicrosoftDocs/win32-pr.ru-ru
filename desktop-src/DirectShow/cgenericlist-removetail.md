---
description: Метод Ремоветаил удаляет последний элемент в списке.
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: Кженериклист. Ремоветаил, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7b98187c663f643acdce28b4f12ebc37b1d4c25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657556"
---
# <a name="cgenericlistremovetail-method"></a><span data-ttu-id="c78fa-103">Кженериклист. Ремоветаил, метод</span><span class="sxs-lookup"><span data-stu-id="c78fa-103">CGenericList.RemoveTail method</span></span>

<span data-ttu-id="c78fa-104">`RemoveTail`Метод удаляет последний элемент в списке.</span><span class="sxs-lookup"><span data-stu-id="c78fa-104">The `RemoveTail` method removes the last item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c78fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c78fa-105">Syntax</span></span>


```C++
OBJECT* RemoveTail();
```



## <a name="parameters"></a><span data-ttu-id="c78fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c78fa-106">Parameters</span></span>

<span data-ttu-id="c78fa-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c78fa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c78fa-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c78fa-108">Return value</span></span>

<span data-ttu-id="c78fa-109">Возвращает указатель на объект типа **Object** (тип шаблона) или **значение NULL** , если список пуст.</span><span class="sxs-lookup"><span data-stu-id="c78fa-109">Returns a pointer to an object of type **OBJECT** (the template type), or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="c78fa-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c78fa-110">Remarks</span></span>

<span data-ttu-id="c78fa-111">Этот метод удаляет узел списка, но не элемент, содержащийся в узле.</span><span class="sxs-lookup"><span data-stu-id="c78fa-111">This method deletes the list node, but not the item that is contained in the node.</span></span>

## <a name="requirements"></a><span data-ttu-id="c78fa-112">Требования</span><span class="sxs-lookup"><span data-stu-id="c78fa-112">Requirements</span></span>



| <span data-ttu-id="c78fa-113">Требование</span><span class="sxs-lookup"><span data-stu-id="c78fa-113">Requirement</span></span> | <span data-ttu-id="c78fa-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c78fa-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c78fa-115">Header</span><span class="sxs-lookup"><span data-stu-id="c78fa-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c78fa-116"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c78fa-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c78fa-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c78fa-117">Library</span></span><br/> | <dl> <span data-ttu-id="c78fa-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c78fa-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c78fa-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c78fa-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c78fa-120">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="c78fa-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





---
description: Метод Аддхеад добавляет элемент в начало списка.
ms.assetid: 8f0012b7-bbc2-407c-ae5a-9843c2f692dc
title: Кженериклист. Аддхеад, метод (Вкслист. h) — параметр Побж
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62a32eb177c80d10a876a4b163c8a1609104fbea
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104081962"
---
# <a name="cgenericlistaddhead-method-wxlisth---pobj-parameter"></a><span data-ttu-id="ef13e-103">Кженериклист. Аддхеад, метод (Вкслист. h) — параметр Побж</span><span class="sxs-lookup"><span data-stu-id="ef13e-103">CGenericList.AddHead method (Wxlist.h) - pObj parameter</span></span>

<span data-ttu-id="ef13e-104">`AddHead`Метод добавляет элемент в начало списка.</span><span class="sxs-lookup"><span data-stu-id="ef13e-104">The `AddHead` method adds an item to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef13e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef13e-105">Syntax</span></span>


```C++
POSITION AddHead(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="ef13e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef13e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef13e-107">*побж*</span><span class="sxs-lookup"><span data-stu-id="ef13e-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="ef13e-108">Указатель на объект типа **Object** (тип шаблона).</span><span class="sxs-lookup"><span data-stu-id="ef13e-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef13e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef13e-109">Return value</span></span>

<span data-ttu-id="ef13e-110">Возвращает значение расположения, указывающее новую головную точку.</span><span class="sxs-lookup"><span data-stu-id="ef13e-110">Returns a POSITION value indicating the new head position.</span></span> <span data-ttu-id="ef13e-111">Если метод завершается ошибкой, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ef13e-111">If the method fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef13e-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ef13e-112">Requirements</span></span>

| <span data-ttu-id="ef13e-113">Требование</span><span class="sxs-lookup"><span data-stu-id="ef13e-113">Requirement</span></span> | <span data-ttu-id="ef13e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ef13e-114">Value</span></span> |
|-|-|
| <span data-ttu-id="ef13e-115">Header</span><span class="sxs-lookup"><span data-stu-id="ef13e-115">Header</span></span> | <span data-ttu-id="ef13e-116">Вкслист. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="ef13e-116">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="ef13e-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ef13e-117">Library</span></span>| <span data-ttu-id="ef13e-118">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="ef13e-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ef13e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef13e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef13e-120">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="ef13e-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





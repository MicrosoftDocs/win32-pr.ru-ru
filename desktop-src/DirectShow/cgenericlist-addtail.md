---
description: Метод AddTail добавляет элемент в конец списка.
ms.assetid: e365a23e-7447-42ec-b836-21dd68962db1
title: Кженериклист. AddTail, метод (Вкслист. h) — параметр Побж
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1e7cd3d8758107b9529114a75b3a90527937c6
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105665013"
---
# <a name="cgenericlistaddtail-method-wxlisth---pobj-parameter"></a><span data-ttu-id="044a2-103">Кженериклист. AddTail, метод (Вкслист. h) — параметр Побж</span><span class="sxs-lookup"><span data-stu-id="044a2-103">CGenericList.AddTail method (Wxlist.h) - pObj parameter</span></span>

<span data-ttu-id="044a2-104">`AddTail`Метод добавляет элемент в конец списка.</span><span class="sxs-lookup"><span data-stu-id="044a2-104">The `AddTail` method appends an item to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="044a2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="044a2-105">Syntax</span></span>


```C++
POSITION AddTail(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="044a2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="044a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="044a2-107">*побж*</span><span class="sxs-lookup"><span data-stu-id="044a2-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="044a2-108">Указатель на объект типа **Object** (тип шаблона).</span><span class="sxs-lookup"><span data-stu-id="044a2-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="044a2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="044a2-109">Return value</span></span>

<span data-ttu-id="044a2-110">Возвращает значение позиции для новой позиции хвоста.</span><span class="sxs-lookup"><span data-stu-id="044a2-110">Returns a POSITION value for the new tail position.</span></span> <span data-ttu-id="044a2-111">Если метод завершается с ошибкой, возвращается **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="044a2-111">If the method fails, it returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="044a2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="044a2-112">Requirements</span></span>

| <span data-ttu-id="044a2-113">Требование</span><span class="sxs-lookup"><span data-stu-id="044a2-113">Requirement</span></span> | <span data-ttu-id="044a2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="044a2-114">Value</span></span> |
|-|-|
| <span data-ttu-id="044a2-115">Header</span><span class="sxs-lookup"><span data-stu-id="044a2-115">Header</span></span> | <span data-ttu-id="044a2-116">Вкслист. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="044a2-116">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="044a2-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="044a2-117">Library</span></span>| <span data-ttu-id="044a2-118">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="044a2-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="044a2-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="044a2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="044a2-120">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="044a2-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





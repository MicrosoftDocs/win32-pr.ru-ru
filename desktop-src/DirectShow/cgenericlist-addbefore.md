---
description: Метод Аддбефоре вставляет элемент перед указанной позицией. Этот метод использует параметры "p" и "Побж".
ms.assetid: ec10fd08-6bb9-4357-830c-78b3d3a32e03
title: Кженериклист. Аддбефоре, метод (Вкслист. h) — p, параметры Побж
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a79c0edb8938e3d3d5a89b4a84a418846b9f1986
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104000546"
---
# <a name="cgenericlistaddbefore-method-wxlisth---p-pobj-parameters"></a><span data-ttu-id="c48ec-104">Кженериклист. Аддбефоре, метод (Вкслист. h) — p, параметры Побж</span><span class="sxs-lookup"><span data-stu-id="c48ec-104">CGenericList.AddBefore method (Wxlist.h) - p, pObj parameters</span></span>

<span data-ttu-id="c48ec-105">`AddBefore`Метод вставляет элемент перед указанной позицией.</span><span class="sxs-lookup"><span data-stu-id="c48ec-105">The `AddBefore` method inserts an item before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="c48ec-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c48ec-106">Syntax</span></span>


```C++
POSITION AddBefore(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="c48ec-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c48ec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c48ec-108">*ш*</span><span class="sxs-lookup"><span data-stu-id="c48ec-108">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="c48ec-109">Расположение, до которого необходимо вставить список.</span><span class="sxs-lookup"><span data-stu-id="c48ec-109">Position before which to insert the list.</span></span> <span data-ttu-id="c48ec-110">Если значение *p* равно **null**, этот метод добавляет элемент в конец списка.</span><span class="sxs-lookup"><span data-stu-id="c48ec-110">If *p* is **NULL**, this method adds the item to the tail of the list.</span></span>

</dd> <dt>

<span data-ttu-id="c48ec-111">*побж*</span><span class="sxs-lookup"><span data-stu-id="c48ec-111">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="c48ec-112">Указатель на объект типа **Object** (тип шаблона).</span><span class="sxs-lookup"><span data-stu-id="c48ec-112">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c48ec-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c48ec-113">Return value</span></span>

<span data-ttu-id="c48ec-114">Возвращает индикатор позиции для вставленного элемента.</span><span class="sxs-lookup"><span data-stu-id="c48ec-114">Returns the position indicator for the inserted item.</span></span>

## <a name="requirements"></a><span data-ttu-id="c48ec-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c48ec-115">Requirements</span></span>

| <span data-ttu-id="c48ec-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c48ec-116">Requirement</span></span> | <span data-ttu-id="c48ec-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c48ec-117">Value</span></span> |
|-|-|
| <span data-ttu-id="c48ec-118">Header</span><span class="sxs-lookup"><span data-stu-id="c48ec-118">Header</span></span> | <span data-ttu-id="c48ec-119">Вкслист. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="c48ec-119">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="c48ec-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c48ec-120">Library</span></span>| <span data-ttu-id="c48ec-121">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="c48ec-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c48ec-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c48ec-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c48ec-123">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="c48ec-123">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





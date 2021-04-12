---
description: Метод Аддафтер вставляет элемент после указанной позиции и использует параметры "p" и "Побж".
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: Кженериклист. Аддафтер, метод (Вкслист. h) — p, параметры Побж
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fbb9553310a8ba817f90464d90226eb36371505e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356153"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a><span data-ttu-id="f7720-103">Кженериклист. Аддафтер, метод (Вкслист. h) — p, параметры Побж</span><span class="sxs-lookup"><span data-stu-id="f7720-103">CGenericList.AddAfter method (Wxlist.h) - p, pObj parameters</span></span>

<span data-ttu-id="f7720-104">`AddAfter`Метод вставляет элемент после указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="f7720-104">The `AddAfter` method inserts an item after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7720-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7720-105">Syntax</span></span>


```C++
POSITION AddAfter(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="f7720-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7720-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7720-107">*ш*</span><span class="sxs-lookup"><span data-stu-id="f7720-107">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="f7720-108">Позиция, после которой нужно добавить элемент.</span><span class="sxs-lookup"><span data-stu-id="f7720-108">Position after which to add the item.</span></span> <span data-ttu-id="f7720-109">Если значение *p* равно **null**, метод добавляет элемент в заголовок списка.</span><span class="sxs-lookup"><span data-stu-id="f7720-109">If *p* is **NULL**, the method adds the item to the head of the list.</span></span>

</dd> <dt>

<span data-ttu-id="f7720-110">*побж*</span><span class="sxs-lookup"><span data-stu-id="f7720-110">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="f7720-111">Указатель на объект типа **Object** (тип шаблона).</span><span class="sxs-lookup"><span data-stu-id="f7720-111">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7720-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7720-112">Return value</span></span>

<span data-ttu-id="f7720-113">Возвращает индикатор позиции вставленного элемента.</span><span class="sxs-lookup"><span data-stu-id="f7720-113">Returns the position indicator of the inserted item.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7720-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f7720-114">Requirements</span></span>

| <span data-ttu-id="f7720-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f7720-115">Requirement</span></span> | <span data-ttu-id="f7720-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f7720-116">Value</span></span> |
|-|-|
| <span data-ttu-id="f7720-117">Header</span><span class="sxs-lookup"><span data-stu-id="f7720-117">Header</span></span> | <span data-ttu-id="f7720-118">Вкслист. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="f7720-118">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="f7720-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f7720-119">Library</span></span>| <span data-ttu-id="f7720-120">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="f7720-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="f7720-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7720-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7720-122">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="f7720-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





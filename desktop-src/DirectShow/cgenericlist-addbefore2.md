---
description: Метод Аддбефоре вставляет список перед указанной позицией. Этот метод использует параметры "POS" и "pList".
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: Кженериклист. Аддбефоре, метод (Вкслист. h) — параметры POS, pList
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
ms.openlocfilehash: b6aa6aa71b1738a815beee9cdc7c0f47118eb27f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "103821588"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a><span data-ttu-id="4baa3-104">Кженериклист. Аддбефоре, метод (Вкслист. h) — параметры POS, pList</span><span class="sxs-lookup"><span data-stu-id="4baa3-104">CGenericList.AddBefore method (Wxlist.h) - pos, pList parameters</span></span>

<span data-ttu-id="4baa3-105">`AddBefore`Метод вставляет список перед указанной позицией.</span><span class="sxs-lookup"><span data-stu-id="4baa3-105">The `AddBefore` method inserts a list before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="4baa3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4baa3-106">Syntax</span></span>


```C++
BOOL AddBefore(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="4baa3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4baa3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4baa3-108">*pos*</span><span class="sxs-lookup"><span data-stu-id="4baa3-108">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="4baa3-109">Расположение для вставки списка.</span><span class="sxs-lookup"><span data-stu-id="4baa3-109">Position to insert the list.</span></span> <span data-ttu-id="4baa3-110">Список вставляется перед этой позицией.</span><span class="sxs-lookup"><span data-stu-id="4baa3-110">The list is inserted before this position.</span></span>

</dd> <dt>

<span data-ttu-id="4baa3-111">*pList*</span><span class="sxs-lookup"><span data-stu-id="4baa3-111">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="4baa3-112">Указатель на список для вставки.</span><span class="sxs-lookup"><span data-stu-id="4baa3-112">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4baa3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4baa3-113">Return value</span></span>

<span data-ttu-id="4baa3-114">Возвращает **значение true** в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="4baa3-114">Returns **TRUE** if successful.</span></span> <span data-ttu-id="4baa3-115">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="4baa3-115">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4baa3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4baa3-116">Requirements</span></span>

| <span data-ttu-id="4baa3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4baa3-117">Requirement</span></span> | <span data-ttu-id="4baa3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4baa3-118">Value</span></span> |
|-|-|
| <span data-ttu-id="4baa3-119">Header</span><span class="sxs-lookup"><span data-stu-id="4baa3-119">Header</span></span> | <span data-ttu-id="4baa3-120">Вкслист. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="4baa3-120">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="4baa3-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4baa3-121">Library</span></span>| <span data-ttu-id="4baa3-122">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="4baa3-122">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="4baa3-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4baa3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4baa3-124">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="4baa3-124">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





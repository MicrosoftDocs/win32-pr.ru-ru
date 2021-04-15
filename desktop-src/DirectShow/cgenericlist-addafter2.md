---
description: Метод Аддафтер вставляет список после указанной должности и использует параметры "POS" и "plist".
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: Кженериклист. Аддафтер, метод (Вкслист. h) — параметры POS, plist
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
ms.openlocfilehash: c6bbe26e98acc999f067a7b0e96c3716e7e0c0c0
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104548167"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a><span data-ttu-id="43ee6-103">Кженериклист. Аддафтер, метод (Вкслист. h) — параметры POS, plist</span><span class="sxs-lookup"><span data-stu-id="43ee6-103">CGenericList.AddAfter method (Wxlist.h) - pos, plist parameters</span></span>

<span data-ttu-id="43ee6-104">`AddAfter`Метод вставляет список после указанной позицией.</span><span class="sxs-lookup"><span data-stu-id="43ee6-104">The `AddAfter` method inserts a list after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="43ee6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43ee6-105">Syntax</span></span>


```C++
BOOL AddAfter(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="43ee6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43ee6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43ee6-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="43ee6-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="43ee6-108">Расположение для вставки списка.</span><span class="sxs-lookup"><span data-stu-id="43ee6-108">Position to insert the list.</span></span> <span data-ttu-id="43ee6-109">Список вставляется после этой должности.</span><span class="sxs-lookup"><span data-stu-id="43ee6-109">The list is inserted after this position.</span></span>

</dd> <dt>

<span data-ttu-id="43ee6-110">*pList*</span><span class="sxs-lookup"><span data-stu-id="43ee6-110">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="43ee6-111">Указатель на список для вставки.</span><span class="sxs-lookup"><span data-stu-id="43ee6-111">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43ee6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43ee6-112">Return value</span></span>

<span data-ttu-id="43ee6-113">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="43ee6-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="43ee6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="43ee6-114">Requirements</span></span>

| <span data-ttu-id="43ee6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="43ee6-115">Requirement</span></span> | <span data-ttu-id="43ee6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="43ee6-116">Value</span></span> |
|-|-|
| <span data-ttu-id="43ee6-117">Header</span><span class="sxs-lookup"><span data-stu-id="43ee6-117">Header</span></span> | <span data-ttu-id="43ee6-118">Вкслист. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="43ee6-118">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="43ee6-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43ee6-119">Library</span></span>| <span data-ttu-id="43ee6-120">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="43ee6-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="43ee6-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43ee6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43ee6-122">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="43ee6-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





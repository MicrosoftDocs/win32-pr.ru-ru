---
description: Сведения о методе конструктора для Кженериклист. Кженериклист (Вкслист. h). Этот метод использует параметры "pName" и "Иитемс".
ms.assetid: 2258ecd6-7594-4ff8-961b-9e5e1ae9ff82
title: Конструктор Кженериклист. Кженериклист (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77a3dd932872b9d96c754ac5b1db184dcf99cf03
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356200"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-iitems-parameters"></a><span data-ttu-id="f21d5-104">Конструктор Кженериклист. Кженериклист (Вкслист. h) — pName, параметры Иитемс</span><span class="sxs-lookup"><span data-stu-id="f21d5-104">CGenericList.CGenericList constructor (Wxlist.h) - pName, iItems parameters</span></span>

<span data-ttu-id="f21d5-105">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="f21d5-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f21d5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f21d5-106">Syntax</span></span>


```C++
CGenericList(
   TCHAR *pName,
   INT   iItems,
   BOOL  bLock,
   BOOL  bAlert
);
```



## <a name="parameters"></a><span data-ttu-id="f21d5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f21d5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f21d5-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="f21d5-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f21d5-109">Указатель на имя списка.</span><span class="sxs-lookup"><span data-stu-id="f21d5-109">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="f21d5-110">*иитемс*</span><span class="sxs-lookup"><span data-stu-id="f21d5-110">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="f21d5-111">Размер кэша узлов.</span><span class="sxs-lookup"><span data-stu-id="f21d5-111">Size of the node cache.</span></span>

</dd> <dt>

<span data-ttu-id="f21d5-112">*Блок*</span><span class="sxs-lookup"><span data-stu-id="f21d5-112">*bLock*</span></span> 
</dt> <dd>

<span data-ttu-id="f21d5-113">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f21d5-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f21d5-114">*балерт*</span><span class="sxs-lookup"><span data-stu-id="f21d5-114">*bAlert*</span></span> 
</dt> <dd>

<span data-ttu-id="f21d5-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f21d5-115">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f21d5-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f21d5-116">Remarks</span></span>

<span data-ttu-id="f21d5-117">Для повышения эффективности `CGenericList` класс поддерживает кэш узлов списка.</span><span class="sxs-lookup"><span data-stu-id="f21d5-117">For efficiency, the `CGenericList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="f21d5-118">Если вы понимаете, сколько элементов будет храниться в списке, используйте эту версию конструктора.</span><span class="sxs-lookup"><span data-stu-id="f21d5-118">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="f21d5-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f21d5-119">Requirements</span></span>

| <span data-ttu-id="f21d5-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f21d5-120">Requirement</span></span> | <span data-ttu-id="f21d5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f21d5-121">Value</span></span> |
|-|-|
| <span data-ttu-id="f21d5-122">Header</span><span class="sxs-lookup"><span data-stu-id="f21d5-122">Header</span></span> | <span data-ttu-id="f21d5-123">Вкслист. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="f21d5-123">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="f21d5-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f21d5-124">Library</span></span>| <span data-ttu-id="f21d5-125">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="f21d5-125">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="f21d5-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f21d5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f21d5-127">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="f21d5-127">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





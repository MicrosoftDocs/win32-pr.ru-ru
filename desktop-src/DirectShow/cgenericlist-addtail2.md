---
description: Метод AddTail добавляет список в конец списка.
ms.assetid: 006cccc5-4fb2-4e3f-9481-5d10c090d24e
title: Кженериклист. AddTail, метод (Вкслист. h) — параметр pList
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
ms.openlocfilehash: 6695df796e54e85ba32dcd63cce2940e00a0199c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105656827"
---
# <a name="cgenericlistaddtail-method-wxlisth---plist-parameter"></a><span data-ttu-id="c9cf2-103">Кженериклист. AddTail, метод (Вкслист. h) — параметр pList</span><span class="sxs-lookup"><span data-stu-id="c9cf2-103">CGenericList.AddTail method (Wxlist.h) - pList parameter</span></span>

<span data-ttu-id="c9cf2-104">`AddTail`Метод добавляет список в конец списка.</span><span class="sxs-lookup"><span data-stu-id="c9cf2-104">The `AddTail` method appends a list to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9cf2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9cf2-105">Syntax</span></span>


```C++
BOOL AddTail(
   CGenericList<OBJECT> pList
);
```



## <a name="parameters"></a><span data-ttu-id="c9cf2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9cf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9cf2-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="c9cf2-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="c9cf2-108">Указатель на добавляемый список.</span><span class="sxs-lookup"><span data-stu-id="c9cf2-108">Pointer to the list to append.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9cf2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9cf2-109">Return value</span></span>

<span data-ttu-id="c9cf2-110">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c9cf2-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9cf2-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c9cf2-111">Requirements</span></span>

| <span data-ttu-id="c9cf2-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c9cf2-112">Requirement</span></span> | <span data-ttu-id="c9cf2-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c9cf2-113">Value</span></span> |
|-|-|
| <span data-ttu-id="c9cf2-114">Header</span><span class="sxs-lookup"><span data-stu-id="c9cf2-114">Header</span></span> | <span data-ttu-id="c9cf2-115">Вкслист. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="c9cf2-115">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="c9cf2-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9cf2-116">Library</span></span>| <span data-ttu-id="c9cf2-117">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="c9cf2-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c9cf2-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9cf2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9cf2-119">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="c9cf2-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





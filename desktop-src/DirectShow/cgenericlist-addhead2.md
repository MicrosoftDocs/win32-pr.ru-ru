---
description: Метод Аддхеад добавляет список в начало списка.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: Кженериклист. Аддхеад, метод (Вкслист. h) — параметр pList
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
ms.openlocfilehash: 0039566f111033062bca080cb24924c7ea4324ac
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105665015"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a><span data-ttu-id="4f91b-103">Кженериклист. Аддхеад, метод (Вкслист. h) — параметр pList</span><span class="sxs-lookup"><span data-stu-id="4f91b-103">CGenericList.AddHead method (Wxlist.h) - pList parameter</span></span>

<span data-ttu-id="4f91b-104">`AddHead`Метод добавляет список в начало списка.</span><span class="sxs-lookup"><span data-stu-id="4f91b-104">The `AddHead` method adds a list to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f91b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f91b-105">Syntax</span></span>


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="4f91b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f91b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f91b-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="4f91b-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="4f91b-108">Указатель на список элементов для добавления.</span><span class="sxs-lookup"><span data-stu-id="4f91b-108">Pointer to the list of items to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f91b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f91b-109">Return value</span></span>

<span data-ttu-id="4f91b-110">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4f91b-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f91b-111">Требования</span><span class="sxs-lookup"><span data-stu-id="4f91b-111">Requirements</span></span>

| <span data-ttu-id="4f91b-112">Требование</span><span class="sxs-lookup"><span data-stu-id="4f91b-112">Requirement</span></span> | <span data-ttu-id="4f91b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4f91b-113">Value</span></span> |
|-|-|
| <span data-ttu-id="4f91b-114">Header</span><span class="sxs-lookup"><span data-stu-id="4f91b-114">Header</span></span> | <span data-ttu-id="4f91b-115">Вкслист. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="4f91b-115">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="4f91b-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4f91b-116">Library</span></span>| <span data-ttu-id="4f91b-117">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="4f91b-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="4f91b-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f91b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f91b-119">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="4f91b-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





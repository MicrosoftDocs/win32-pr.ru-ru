---
description: Метод Жети извлекает элемент в указанной позиции.
ms.assetid: fc775230-491a-49b6-b631-e7d5b8c82d8c
title: Кбаселист. Жети, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2473401aeaee201456b4eede39ffb492f40ee2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657393"
---
# <a name="cbaselistgeti-method"></a><span data-ttu-id="931cf-103">Кбаселист. Жети, метод</span><span class="sxs-lookup"><span data-stu-id="931cf-103">CBaseList.GetI method</span></span>

<span data-ttu-id="931cf-104">`GetI`Метод извлекает элемент в указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="931cf-104">The `GetI` method retrieves the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="931cf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="931cf-105">Syntax</span></span>


```C++
void* GetI(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="931cf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="931cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="931cf-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="931cf-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="931cf-108">Индикатор позиции для извлекаемого элемента.</span><span class="sxs-lookup"><span data-stu-id="931cf-108">Position indicator for the item to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="931cf-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="931cf-109">Return value</span></span>

<span data-ttu-id="931cf-110">Возвращает указатель на элемент.</span><span class="sxs-lookup"><span data-stu-id="931cf-110">Returns a pointer to the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="931cf-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="931cf-111">Remarks</span></span>

<span data-ttu-id="931cf-112">Если *POS* имеет **значение NULL**, метод возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="931cf-112">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="931cf-113">Требования</span><span class="sxs-lookup"><span data-stu-id="931cf-113">Requirements</span></span>



| <span data-ttu-id="931cf-114">Требование</span><span class="sxs-lookup"><span data-stu-id="931cf-114">Requirement</span></span> | <span data-ttu-id="931cf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="931cf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="931cf-116">Header</span><span class="sxs-lookup"><span data-stu-id="931cf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="931cf-117"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="931cf-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="931cf-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="931cf-118">Library</span></span><br/> | <dl> <span data-ttu-id="931cf-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="931cf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="931cf-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="931cf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="931cf-121">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="931cf-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





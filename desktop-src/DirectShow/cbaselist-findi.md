---
description: Метод Финди извлекает первую позицию, содержащую указанный элемент.
ms.assetid: a95fac19-0f93-4bb4-8e76-0da82745a1d2
title: Кбаселист. Финди, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.FindI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2366f8c4c117b8550d91c84bffafb03393801088
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668608"
---
# <a name="cbaselistfindi-method"></a><span data-ttu-id="f4074-103">Кбаселист. Финди, метод</span><span class="sxs-lookup"><span data-stu-id="f4074-103">CBaseList.FindI method</span></span>

<span data-ttu-id="f4074-104">`FindI`Метод извлекает первую позицию, содержащую указанный элемент.</span><span class="sxs-lookup"><span data-stu-id="f4074-104">The `FindI` method retrieves the first position that holds the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4074-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4074-105">Syntax</span></span>


```C++
POSITION FindI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="f4074-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4074-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4074-107">*побж*</span><span class="sxs-lookup"><span data-stu-id="f4074-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="f4074-108">Указатель на элемент.</span><span class="sxs-lookup"><span data-stu-id="f4074-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4074-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4074-109">Return value</span></span>

<span data-ttu-id="f4074-110">Возвращает значение позиции или **значение NULL** , если элемент отсутствует в списке.</span><span class="sxs-lookup"><span data-stu-id="f4074-110">Returns a POSITION value, or **NULL** if the item is not in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4074-111">Требования</span><span class="sxs-lookup"><span data-stu-id="f4074-111">Requirements</span></span>



| <span data-ttu-id="f4074-112">Требование</span><span class="sxs-lookup"><span data-stu-id="f4074-112">Requirement</span></span> | <span data-ttu-id="f4074-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f4074-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4074-114">Header</span><span class="sxs-lookup"><span data-stu-id="f4074-114">Header</span></span><br/>  | <dl> <span data-ttu-id="f4074-115"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4074-115"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f4074-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f4074-116">Library</span></span><br/> | <dl> <span data-ttu-id="f4074-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f4074-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4074-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4074-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4074-119">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="f4074-119">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





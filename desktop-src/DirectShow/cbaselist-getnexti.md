---
description: Метод Жетнексти извлекает элемент в указанной позиции и перемещает позицию.
ms.assetid: 3ec217ec-b0f9-4ff4-bdb7-ac204df99010
title: Кбаселист. Жетнексти, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetNextI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f96be8d8cdf286a4017e56af7050970d45e8a56e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668603"
---
# <a name="cbaselistgetnexti-method"></a><span data-ttu-id="831f0-103">Кбаселист. Жетнексти, метод</span><span class="sxs-lookup"><span data-stu-id="831f0-103">CBaseList.GetNextI method</span></span>

<span data-ttu-id="831f0-104">`GetNextI`Метод получает элемент в указанной позиции и перемещает позицию.</span><span class="sxs-lookup"><span data-stu-id="831f0-104">The `GetNextI` method retrieves the item at the specified position, and advances the position.</span></span>

## <a name="syntax"></a><span data-ttu-id="831f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="831f0-105">Syntax</span></span>


```C++
void* GetNextI(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a><span data-ttu-id="831f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="831f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="831f0-107">*RP* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="831f0-107">*rp* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="831f0-108">Ссылка на значение должности.</span><span class="sxs-lookup"><span data-stu-id="831f0-108">Reference to a POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="831f0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="831f0-109">Return value</span></span>

<span data-ttu-id="831f0-110">Возвращает указатель на элемент.</span><span class="sxs-lookup"><span data-stu-id="831f0-110">Returns a pointer to the item.</span></span> <span data-ttu-id="831f0-111">Если значение *RP* равно **null**, метод возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="831f0-111">If *rp* is **NULL**, the method returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="831f0-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="831f0-112">Remarks</span></span>

<span data-ttu-id="831f0-113">Этот метод перемещает индикатор положения на следующую позицию.</span><span class="sxs-lookup"><span data-stu-id="831f0-113">This method advances the position indicator to the next position.</span></span> <span data-ttu-id="831f0-114">Если индикатор позиции перемещается за концом списка, метод присваивает ему **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="831f0-114">If the position indicator moves past the end of the list, the method sets it to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="831f0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="831f0-115">Requirements</span></span>



| <span data-ttu-id="831f0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="831f0-116">Requirement</span></span> | <span data-ttu-id="831f0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="831f0-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="831f0-118">Header</span><span class="sxs-lookup"><span data-stu-id="831f0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="831f0-119"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="831f0-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="831f0-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="831f0-120">Library</span></span><br/> | <dl> <span data-ttu-id="831f0-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="831f0-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="831f0-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="831f0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="831f0-123">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="831f0-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





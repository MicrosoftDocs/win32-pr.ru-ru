---
description: Метод GetNext извлекает элемент в указанной позиции и перемещает позицию.
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: Метод Кженериклист. GetNext (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.GetNext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9491e58d817ce2c9dc4fb59fafa9bf96812a013a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668808"
---
# <a name="cgenericlistgetnext-method"></a><span data-ttu-id="e0469-103">Кженериклист. GetNext, метод</span><span class="sxs-lookup"><span data-stu-id="e0469-103">CGenericList.GetNext method</span></span>

<span data-ttu-id="e0469-104">`GetNext`Метод получает элемент в указанной позиции и перемещает позицию.</span><span class="sxs-lookup"><span data-stu-id="e0469-104">The `GetNext` method retrieves the item at the specified position, and advances the position.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0469-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0469-105">Syntax</span></span>


```C++
OBJECT* GetNext(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a><span data-ttu-id="e0469-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0469-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0469-107">*RP* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="e0469-107">*rp* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e0469-108">Ссылка на значение должности.</span><span class="sxs-lookup"><span data-stu-id="e0469-108">Reference to a POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0469-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0469-109">Return value</span></span>

<span data-ttu-id="e0469-110">Возвращает указатель на объект типа **Object** (тип шаблона).</span><span class="sxs-lookup"><span data-stu-id="e0469-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="e0469-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0469-111">Remarks</span></span>

<span data-ttu-id="e0469-112">Этот метод перемещает индикатор положения на следующую позицию.</span><span class="sxs-lookup"><span data-stu-id="e0469-112">This method advances the position indicator to the next position.</span></span> <span data-ttu-id="e0469-113">Если индикатор позиции перемещается за концом списка, метод присваивает ему **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e0469-113">If the position indicator moves past the end of the list, the method sets it to **NULL**.</span></span>

<span data-ttu-id="e0469-114">Если значение *RP* равно **null**, метод возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e0469-114">If *rp* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0469-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e0469-115">Requirements</span></span>



| <span data-ttu-id="e0469-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e0469-116">Requirement</span></span> | <span data-ttu-id="e0469-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e0469-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0469-118">Header</span><span class="sxs-lookup"><span data-stu-id="e0469-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e0469-119"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0469-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e0469-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e0469-120">Library</span></span><br/> | <dl> <span data-ttu-id="e0469-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e0469-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0469-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0469-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0469-123">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="e0469-123">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





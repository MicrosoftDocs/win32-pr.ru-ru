---
description: Метод Рекордфрамелатенесс записывает, как своевременно выполнялась визуализация, и собирает статистику для страницы свойств.
ms.assetid: 9d4b90d7-b529-40cc-a0fd-6635163fb7dd
title: Кбасевидеорендерер. Рекордфрамелатенесс, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.RecordFrameLateness
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10ae7069ceedbe43f9614ea3fd1c7c901d7023cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675007"
---
# <a name="cbasevideorendererrecordframelateness-method"></a><span data-ttu-id="89c4d-103">Кбасевидеорендерер. Рекордфрамелатенесс, метод</span><span class="sxs-lookup"><span data-stu-id="89c4d-103">CBaseVideoRenderer.RecordFrameLateness method</span></span>

<span data-ttu-id="89c4d-104">`RecordFrameLateness`Метод записывает, как своевременно выполнялась визуализация, и собирает статистику для страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="89c4d-104">The `RecordFrameLateness` method records how timely the rendering occurred and gathers statistics for the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="89c4d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89c4d-105">Syntax</span></span>


```C++
virtual void RecordFrameLateness(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a><span data-ttu-id="89c4d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="89c4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89c4d-107">*трлате*</span><span class="sxs-lookup"><span data-stu-id="89c4d-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="89c4d-108">Значение, указывающее, насколько поздно образец превысил время его выполнения в ссылочных единицах времени.</span><span class="sxs-lookup"><span data-stu-id="89c4d-108">Value indicating how late the sample was beyond its due time, in reference time units.</span></span>

</dd> <dt>

<span data-ttu-id="89c4d-109">*трфраме*</span><span class="sxs-lookup"><span data-stu-id="89c4d-109">*trFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="89c4d-110">Время между кадрами, в ссылочных единицах времени.</span><span class="sxs-lookup"><span data-stu-id="89c4d-110">Interframe time, in reference time units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89c4d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89c4d-111">Return value</span></span>

<span data-ttu-id="89c4d-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="89c4d-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="89c4d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="89c4d-113">Requirements</span></span>



| <span data-ttu-id="89c4d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="89c4d-114">Requirement</span></span> | <span data-ttu-id="89c4d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="89c4d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c4d-116">Header</span><span class="sxs-lookup"><span data-stu-id="89c4d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="89c4d-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89c4d-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="89c4d-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="89c4d-118">Library</span></span><br/> | <dl> <span data-ttu-id="89c4d-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="89c4d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89c4d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89c4d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89c4d-121">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="89c4d-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 





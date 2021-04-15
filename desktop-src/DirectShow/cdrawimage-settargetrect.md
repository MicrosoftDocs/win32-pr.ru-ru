---
description: Метод Сеттаржетрект задает целевой прямоугольник.
ms.assetid: 033f8bae-e63d-4be0-8dd0-715cc1229392
title: Кдравимаже. Сеттаржетрект, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4513b6aeda16d19476769290a6139f91b2fd1f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665473"
---
# <a name="cdrawimagesettargetrect-method"></a><span data-ttu-id="cc4d9-103">Кдравимаже. Сеттаржетрект, метод</span><span class="sxs-lookup"><span data-stu-id="cc4d9-103">CDrawImage.SetTargetRect method</span></span>

<span data-ttu-id="cc4d9-104">`SetTargetRect`Метод задает целевой прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-104">The `SetTargetRect` method sets the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc4d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc4d9-105">Syntax</span></span>


```C++
void SetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="cc4d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc4d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc4d9-107">*птаржетрект*</span><span class="sxs-lookup"><span data-stu-id="cc4d9-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="cc4d9-108">Указатель на структуру **Rect** , определяющую новый целевой прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-108">Pointer to a **RECT** structure that defines the new target rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc4d9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc4d9-109">Return value</span></span>

<span data-ttu-id="cc4d9-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc4d9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc4d9-111">Remarks</span></span>

<span data-ttu-id="cc4d9-112">Фильтр-владелец должен вызывать этот метод, если исходный прямоугольник изменяется; Например, в ответ на вызов [**ибасиквидео:: сетдестинатионпоситион**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) .</span><span class="sxs-lookup"><span data-stu-id="cc4d9-112">The owning filter should call this method if the source rectangle changes; for example, in response to an [**IBasicVideo::SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) call.</span></span>

<span data-ttu-id="cc4d9-113">Перед вызовом этого метода проверьте прямоугольник, заданный в *птаржетрект*, относительно окна видео.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-113">Before calling this method, validate the rectangle given in *pTargetRect*, relative to the video window.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc4d9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cc4d9-114">Requirements</span></span>



| <span data-ttu-id="cc4d9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cc4d9-115">Requirement</span></span> | <span data-ttu-id="cc4d9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cc4d9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc4d9-117">Header</span><span class="sxs-lookup"><span data-stu-id="cc4d9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="cc4d9-118"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc4d9-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cc4d9-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cc4d9-119">Library</span></span><br/> | <dl> <span data-ttu-id="cc4d9-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cc4d9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc4d9-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc4d9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc4d9-122">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="cc4d9-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 





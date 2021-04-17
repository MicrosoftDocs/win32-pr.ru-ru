---
description: Метод DrawImage рисует кадр видео в окне видео.
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: Метод Кдравимаже. DrawImage (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d219eb82ab2cf1929605eee4045c2f278022ad98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657180"
---
# <a name="cdrawimagedrawimage-method"></a><span data-ttu-id="aa11f-103">Кдравимаже. DrawImage, метод</span><span class="sxs-lookup"><span data-stu-id="aa11f-103">CDrawImage.DrawImage method</span></span>

<span data-ttu-id="aa11f-104">`DrawImage`Метод рисует кадр видео в окне видео.</span><span class="sxs-lookup"><span data-stu-id="aa11f-104">The `DrawImage` method draws a video frame on the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa11f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa11f-105">Syntax</span></span>


```C++
BOOL DrawImage(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="aa11f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa11f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa11f-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="aa11f-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="aa11f-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца, который содержит изображение.</span><span class="sxs-lookup"><span data-stu-id="aa11f-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa11f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa11f-109">Return value</span></span>

<span data-ttu-id="aa11f-110">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="aa11f-110">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa11f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa11f-111">Remarks</span></span>

<span data-ttu-id="aa11f-112">Этот метод делегирует [**кдравимаже:: фастрендер**](cdrawimage-fastrender.md) или [**Кдравимаже:: словрендер**](cdrawimage-slowrender.md)в зависимости от того, владеет ли фильтр распределителем, который предоставил пример.</span><span class="sxs-lookup"><span data-stu-id="aa11f-112">This method delegates to [**CDrawImage::FastRender**](cdrawimage-fastrender.md) or [**CDrawImage::SlowRender**](cdrawimage-slowrender.md), depending on whether the filter owns the allocator that provided the sample.</span></span> <span data-ttu-id="aa11f-113">Если фильтр владеет распределителем, пример гарантированно будет объектом [**Цимажесампле**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="aa11f-113">If the filter does own the allocator, the sample is guaranteed to be a [**CImageSample**](cimagesample.md) object.</span></span> <span data-ttu-id="aa11f-114">В этом случае в примере используется общая память, выделенная GDI, а изображение можно изобразить с помощью **BitBlt** или **стретчблт**.</span><span class="sxs-lookup"><span data-stu-id="aa11f-114">In that case, the sample uses shared memory allocated by GDI, and the image can be drawn using either **BitBlt** or **StretchBlt**.</span></span> <span data-ttu-id="aa11f-115">В противном случае изображения должны быть выведены с помощью медленных функций **сетдибитстодевице** или **стретчдибитс** .</span><span class="sxs-lookup"><span data-stu-id="aa11f-115">Otherwise, the images must be drawn using the slower **SetDIBitsToDevice** or **StretchDIBits** functions.</span></span>

<span data-ttu-id="aa11f-116">В отладочных сборках этот метод вызывает **дисплайсамплетимес** , чтобы нарисовать отметки времени образца на изображении видео.</span><span class="sxs-lookup"><span data-stu-id="aa11f-116">In debug builds, this method calls **DisplaySampleTimes** to draw the sample's time stamps over the video image.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa11f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="aa11f-117">Requirements</span></span>



| <span data-ttu-id="aa11f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="aa11f-118">Requirement</span></span> | <span data-ttu-id="aa11f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="aa11f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa11f-120">Header</span><span class="sxs-lookup"><span data-stu-id="aa11f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="aa11f-121"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa11f-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aa11f-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="aa11f-122">Library</span></span><br/> | <dl> <span data-ttu-id="aa11f-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="aa11f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa11f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa11f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa11f-125">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="aa11f-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="aa11f-126">**Кдравимаже:: Усингимажеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="aa11f-126">**CDrawImage::UsingImageAllocator**</span></span>](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 





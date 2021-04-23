---
description: Метод Словрендер рисует изображение видео с помощью функций Сетдибитстодевице или Стретчдибитс.
ms.assetid: e1d8b189-b588-48eb-988a-3e5dedb38dbd
title: Кдравимаже. Словрендер, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SlowRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b736bf6c44d4ada6e0a28408c449c9f8b2f1e1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657176"
---
# <a name="cdrawimageslowrender-method"></a><span data-ttu-id="26bf6-103">Кдравимаже. Словрендер, метод</span><span class="sxs-lookup"><span data-stu-id="26bf6-103">CDrawImage.SlowRender method</span></span>

<span data-ttu-id="26bf6-104">`SlowRender`Метод рисует изображение видео с помощью функций **Сетдибитстодевице** или **стретчдибитс** .</span><span class="sxs-lookup"><span data-stu-id="26bf6-104">The `SlowRender` method draws the video image using the **SetDIBitsToDevice** or **StretchDIBits** functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="26bf6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26bf6-105">Syntax</span></span>


```C++
void SlowRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="26bf6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="26bf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26bf6-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="26bf6-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="26bf6-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца, который содержит изображение.</span><span class="sxs-lookup"><span data-stu-id="26bf6-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26bf6-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26bf6-109">Return value</span></span>

<span data-ttu-id="26bf6-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="26bf6-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="26bf6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26bf6-111">Remarks</span></span>

<span data-ttu-id="26bf6-112">Если [**кдравимаже:: усингимажеаллокатор**](cdrawimage-usingimageallocator.md) возвращает **значение false**, то метод [**кдравимаже::D равимаже**](cdrawimage-drawimage.md) использует `SlowRender` для рисования видеоизображения.</span><span class="sxs-lookup"><span data-stu-id="26bf6-112">If [**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md) returns **FALSE**, the [**CDrawImage::DrawImage**](cdrawimage-drawimage.md) method uses `SlowRender` to draw the video image.</span></span> <span data-ttu-id="26bf6-113">В противном случае DrawImage использует метод **фастрендер** .</span><span class="sxs-lookup"><span data-stu-id="26bf6-113">Otherwise, DrawImage uses the **FastRender** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="26bf6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="26bf6-114">Requirements</span></span>



| <span data-ttu-id="26bf6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="26bf6-115">Requirement</span></span> | <span data-ttu-id="26bf6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="26bf6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26bf6-117">Header</span><span class="sxs-lookup"><span data-stu-id="26bf6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="26bf6-118"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26bf6-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="26bf6-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="26bf6-119">Library</span></span><br/> | <dl> <span data-ttu-id="26bf6-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="26bf6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26bf6-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26bf6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26bf6-122">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="26bf6-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="26bf6-123">**Кдравимаже:: Фастрендер**</span><span class="sxs-lookup"><span data-stu-id="26bf6-123">**CDrawImage::FastRender**</span></span>](cdrawimage-fastrender.md)
</dt> </dl>

 

 





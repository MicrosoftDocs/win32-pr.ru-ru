---
description: Метод Фастрендер рисует изображение видео с помощью функций BitBlt или Стретчблт.
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: Кдравимаже. Фастрендер, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.FastRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 823583beed6696d40803ccc098410dac053b8948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665474"
---
# <a name="cdrawimagefastrender-method"></a><span data-ttu-id="2565f-103">Кдравимаже. Фастрендер, метод</span><span class="sxs-lookup"><span data-stu-id="2565f-103">CDrawImage.FastRender method</span></span>

<span data-ttu-id="2565f-104">`FastRender`Метод рисует изображение видео с помощью функций **BitBlt** или **стретчблт** .</span><span class="sxs-lookup"><span data-stu-id="2565f-104">The `FastRender` method draws the video image using the **BitBlt** or **StretchBlt** functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="2565f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2565f-105">Syntax</span></span>


```C++
void FastRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="2565f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2565f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2565f-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="2565f-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="2565f-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца, который содержит изображение.</span><span class="sxs-lookup"><span data-stu-id="2565f-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2565f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2565f-109">Return value</span></span>

<span data-ttu-id="2565f-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2565f-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2565f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2565f-111">Remarks</span></span>

<span data-ttu-id="2565f-112">Метод [**кдравимаже::D равимаже**](cdrawimage-drawimage.md) вызывает этот метод, но только в том случае, если распределитель для соединения является объектом [**Цимажеаллокатор**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="2565f-112">The [**CDrawImage::DrawImage**](cdrawimage-drawimage.md) method calls this method, but only if the allocator for the connection is a [**CImageAllocator**](cimageallocator.md) object.</span></span> <span data-ttu-id="2565f-113">В этом случае пример носителя гарантированно будет объектом [**Цимажесампле**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="2565f-113">In that case, the media sample is guaranteed to be a [**CImageSample**](cimagesample.md) object.</span></span> <span data-ttu-id="2565f-114">Объект **Цимажесампле** использует функцию **креатедибсектион** для выделения общей памяти для точечного рисунка, что дает возможность рисовать изображение с помощью **BitBlt** или **стретчблт**.</span><span class="sxs-lookup"><span data-stu-id="2565f-114">The **CImageSample** object uses the **CreateDIBSection** function to allocate shared memory for the bitmap, which makes it possible to draw the image using either **BitBlt** or **StretchBlt**.</span></span>

<span data-ttu-id="2565f-115">Этот метод вызывает **BitBlt** , если прямоугольники источника и недопустимая точно совпадают, или **стретчблт** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2565f-115">This method calls **BitBlt** if the source and targer rectangles exactly match, or **StretchBlt** otherwise.</span></span>

<span data-ttu-id="2565f-116">Если фильтр не владеет распределителем, метод **DrawImage** использует [**Кдравимаже:: словрендер**](cdrawimage-slowrender.md) для рисования изображения.</span><span class="sxs-lookup"><span data-stu-id="2565f-116">If the filter does not own the allocator, the **DrawImage** method uses [**CDrawImage::SlowRender**](cdrawimage-slowrender.md) to draw the image.</span></span>

## <a name="requirements"></a><span data-ttu-id="2565f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2565f-117">Requirements</span></span>



| <span data-ttu-id="2565f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2565f-118">Requirement</span></span> | <span data-ttu-id="2565f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2565f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2565f-120">Header</span><span class="sxs-lookup"><span data-stu-id="2565f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2565f-121"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2565f-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2565f-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2565f-122">Library</span></span><br/> | <dl> <span data-ttu-id="2565f-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2565f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2565f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2565f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2565f-125">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="2565f-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 





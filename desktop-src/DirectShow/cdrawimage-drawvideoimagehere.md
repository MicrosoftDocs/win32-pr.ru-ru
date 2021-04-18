---
description: Метод Драввидеоимажехере рисует изображение из примера носителя в заданном контексте устройства.
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: Кдравимаже. Драввидеоимажехере, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawVideoImageHere
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 599dd82e282f2d14ac7e974363a62695e209c080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657179"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a><span data-ttu-id="e017e-103">Кдравимаже. Драввидеоимажехере, метод</span><span class="sxs-lookup"><span data-stu-id="e017e-103">CDrawImage.DrawVideoImageHere method</span></span>

<span data-ttu-id="e017e-104">`DrawVideoImageHere`Метод выводит изображение из примера носителя в указанный контекст устройства.</span><span class="sxs-lookup"><span data-stu-id="e017e-104">The `DrawVideoImageHere` method draws an image from a media sample to a specified device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="e017e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e017e-105">Syntax</span></span>


```C++
BOOL DrawVideoImageHere(
   HDC          hdc,
   IMediaSample *pMediaSample,
   RECT         *lprcSrc,
   RECT         *lprcDst
);
```



## <a name="parameters"></a><span data-ttu-id="e017e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e017e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e017e-107">*HDC*</span><span class="sxs-lookup"><span data-stu-id="e017e-107">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="e017e-108">Обработайте с контекстом устройства, где будет выполняться рисование.</span><span class="sxs-lookup"><span data-stu-id="e017e-108">Handle to a device context, where the drawing will occur.</span></span>

</dd> <dt>

<span data-ttu-id="e017e-109">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="e017e-109">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e017e-110">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца, который содержит изображение.</span><span class="sxs-lookup"><span data-stu-id="e017e-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> <dt>

<span data-ttu-id="e017e-111">*лпрксрк*</span><span class="sxs-lookup"><span data-stu-id="e017e-111">*lprcSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="e017e-112">Указатель на исходный прямоугольник, используемый для рисования.</span><span class="sxs-lookup"><span data-stu-id="e017e-112">Pointer to a source rectangle to use for drawing.</span></span> <span data-ttu-id="e017e-113">Если **значение равно NULL**, используется прямоугольник в [**кдравимаже:: m \_ саурцерект**](cdrawimage-m-sourcerect.md) .</span><span class="sxs-lookup"><span data-stu-id="e017e-113">If **NULL**, the rectangle in [**CDrawImage::m\_SourceRect**](cdrawimage-m-sourcerect.md) is used.</span></span>

</dd> <dt>

<span data-ttu-id="e017e-114">*лпркдст*</span><span class="sxs-lookup"><span data-stu-id="e017e-114">*lprcDst*</span></span> 
</dt> <dd>

<span data-ttu-id="e017e-115">Указатель на целевой прямоугольник, используемый для рисования.</span><span class="sxs-lookup"><span data-stu-id="e017e-115">Pointer to a target rectangle to use for drawing.</span></span> <span data-ttu-id="e017e-116">Если **значение равно NULL**, используется прямоугольник в [**кдравимаже:: m \_ таржетрект**](cdrawimage-m-targetrect.md) .</span><span class="sxs-lookup"><span data-stu-id="e017e-116">If **NULL**, the rectangle in [**CDrawImage::m\_TargetRect**](cdrawimage-m-targetrect.md) is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e017e-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e017e-117">Return value</span></span>

<span data-ttu-id="e017e-118">Возвращает **значение true** в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="e017e-118">Returns **TRUE** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="e017e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e017e-119">Requirements</span></span>



| <span data-ttu-id="e017e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e017e-120">Requirement</span></span> | <span data-ttu-id="e017e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e017e-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e017e-122">Header</span><span class="sxs-lookup"><span data-stu-id="e017e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e017e-123"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e017e-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e017e-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e017e-124">Library</span></span><br/> | <dl> <span data-ttu-id="e017e-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e017e-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e017e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e017e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e017e-127">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="e017e-127">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 





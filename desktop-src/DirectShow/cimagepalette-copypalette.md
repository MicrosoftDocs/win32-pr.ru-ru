---
description: Метод Копипалетте копирует палитру из любой структуры ВИДЕОИНФО в любую палеттизед ВИДЕОИНФО структуру.
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: Цимажепалетте. Копипалетте, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CopyPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b429c5fd4d3d0e0e28cd0662fbee0a1ac926ddc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669213"
---
# <a name="cimagepalettecopypalette-method"></a><span data-ttu-id="7ccf4-103">Цимажепалетте. Копипалетте, метод</span><span class="sxs-lookup"><span data-stu-id="7ccf4-103">CImagePalette.CopyPalette method</span></span>

<span data-ttu-id="7ccf4-104">`CopyPalette`Метод копирует палитру из любой структуры [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) в любую структуру палеттизед **видеоинфо** .</span><span class="sxs-lookup"><span data-stu-id="7ccf4-104">The `CopyPalette` method copies the palette from any [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure to any palettized **VIDEOINFO** structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ccf4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ccf4-105">Syntax</span></span>


```C++
HRESULT CopyPalette(
   const CMediaType *pSrc,
   const CMediaType *pDest
);
```



## <a name="parameters"></a><span data-ttu-id="7ccf4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ccf4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ccf4-107">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="7ccf4-107">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="7ccf4-108">Указатель на исходный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="7ccf4-108">Pointer to the source media type.</span></span>

</dd> <dt>

<span data-ttu-id="7ccf4-109">*pDest*</span><span class="sxs-lookup"><span data-stu-id="7ccf4-109">*pDest*</span></span> 
</dt> <dd>

<span data-ttu-id="7ccf4-110">Указатель на тип носителя назначения.</span><span class="sxs-lookup"><span data-stu-id="7ccf4-110">Pointer to the destination media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ccf4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ccf4-111">Return value</span></span>

<span data-ttu-id="7ccf4-112">Возвращает значение \_ ОК, если палитра скопирована.</span><span class="sxs-lookup"><span data-stu-id="7ccf4-112">Returns S\_OK if the palette was copied.</span></span> <span data-ttu-id="7ccf4-113">Возвращает \_ значение false, если исходный или конечный тип носителя не имеет палитры.</span><span class="sxs-lookup"><span data-stu-id="7ccf4-113">Returns S\_FALSE if either the source or destination media type does not have a palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ccf4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ccf4-114">Remarks</span></span>

<span data-ttu-id="7ccf4-115">Тип носителя *пдест* должен быть форматом палеттизед с глубиной цвета 8 бит или меньше.</span><span class="sxs-lookup"><span data-stu-id="7ccf4-115">The *pDest* media type must be a palettized format with a color depth of 8 bits or less.</span></span> <span data-ttu-id="7ccf4-116">Тип носителя *pSrc* может быть любым типом [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) с палитрой, включая форматы YUV и True-Color с записями палитры.</span><span class="sxs-lookup"><span data-stu-id="7ccf4-116">The *pSrc* media type can be any [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) type with a palette, including YUV and true-color formats with palette entries.</span></span> <span data-ttu-id="7ccf4-117">Метод копирует записи палитры из *pSrc* в новую палитру и прикрепляет новую палитру к *пдест*.</span><span class="sxs-lookup"><span data-stu-id="7ccf4-117">The method copies the palette entries from *pSrc* into a new palette, and attaches the new palette to *pDest*.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ccf4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7ccf4-118">Requirements</span></span>



| <span data-ttu-id="7ccf4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7ccf4-119">Requirement</span></span> | <span data-ttu-id="7ccf4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7ccf4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ccf4-121">Header</span><span class="sxs-lookup"><span data-stu-id="7ccf4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7ccf4-122"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ccf4-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7ccf4-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7ccf4-123">Library</span></span><br/> | <dl> <span data-ttu-id="7ccf4-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7ccf4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ccf4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ccf4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ccf4-126">**Класс Цимажепалетте**</span><span class="sxs-lookup"><span data-stu-id="7ccf4-126">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 





---
description: Метод Макепалетте создает логическую палитру из таблицы цветов в видеоформате.
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: Цимажепалетте. Макепалетте, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20c4484b2666b25b5d713ede450a9a5a99f93348
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674943"
---
# <a name="cimagepalettemakepalette-method"></a><span data-ttu-id="d2424-103">Цимажепалетте. Макепалетте, метод</span><span class="sxs-lookup"><span data-stu-id="d2424-103">CImagePalette.MakePalette method</span></span>

<span data-ttu-id="d2424-104">`MakePalette`Метод создает логическую палитру из таблицы цветов в видеоформате.</span><span class="sxs-lookup"><span data-stu-id="d2424-104">The `MakePalette` method creates a logical palette from the color table in a video format.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2424-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2424-105">Syntax</span></span>


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="d2424-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2424-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2424-107">*пвидеоинфо*</span><span class="sxs-lookup"><span data-stu-id="d2424-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="d2424-108">Указатель на структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , содержащую таблицу цветов.</span><span class="sxs-lookup"><span data-stu-id="d2424-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure that contains the color table.</span></span>

</dd> <dt>

<span data-ttu-id="d2424-109">*сздевице*</span><span class="sxs-lookup"><span data-stu-id="d2424-109">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="d2424-110">Указатель на строку, содержащую имя устройства вывода, которое возвращается функцией GDI **енумдисплайдевицес** .</span><span class="sxs-lookup"><span data-stu-id="d2424-110">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="d2424-111">Чтобы использовать основное устройство вывода, присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d2424-111">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2424-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2424-112">Return value</span></span>

<span data-ttu-id="d2424-113">В случае успеха возвращает маркер для палитры.</span><span class="sxs-lookup"><span data-stu-id="d2424-113">If successful, returns a handle to the palette.</span></span> <span data-ttu-id="d2424-114">В противном случае возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d2424-114">Otherwise, returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2424-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d2424-115">Requirements</span></span>



| <span data-ttu-id="d2424-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d2424-116">Requirement</span></span> | <span data-ttu-id="d2424-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d2424-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2424-118">Header</span><span class="sxs-lookup"><span data-stu-id="d2424-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d2424-119"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2424-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d2424-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d2424-120">Library</span></span><br/> | <dl> <span data-ttu-id="d2424-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d2424-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2424-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2424-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2424-123">**Класс Цимажепалетте**</span><span class="sxs-lookup"><span data-stu-id="d2424-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 





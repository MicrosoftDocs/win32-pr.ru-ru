---
description: Метод Жетимажесизе извлекает сведения о размере изображения видео.
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: Кбасеконтролвидео. Жетимажесизе, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed7795e3998bc101e907bce87c9981e86f51fcb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689521"
---
# <a name="cbasecontrolvideogetimagesize-method"></a><span data-ttu-id="caff5-103">Кбасеконтролвидео. Жетимажесизе, метод</span><span class="sxs-lookup"><span data-stu-id="caff5-103">CBaseControlVideo.GetImageSize method</span></span>

<span data-ttu-id="caff5-104">`GetImageSize`Метод получает сведения о размере изображения видео.</span><span class="sxs-lookup"><span data-stu-id="caff5-104">The `GetImageSize` method retrieves video image size information.</span></span>

## <a name="syntax"></a><span data-ttu-id="caff5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="caff5-105">Syntax</span></span>


```C++
HRESULT GetImageSize(
   VIDEOINFOHEADER *pVideoInfo,
   long            *pBufferSize,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="caff5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="caff5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caff5-107">*пвидеоинфо*</span><span class="sxs-lookup"><span data-stu-id="caff5-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="caff5-108">Указатель на структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) для заполнения.</span><span class="sxs-lookup"><span data-stu-id="caff5-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure to be filled in.</span></span>

</dd> <dt>

<span data-ttu-id="caff5-109">*пбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="caff5-109">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="caff5-110">Указатель на размер буфера видео.</span><span class="sxs-lookup"><span data-stu-id="caff5-110">Pointer to the size of the video buffer.</span></span>

</dd> <dt>

<span data-ttu-id="caff5-111">*псаурцерект*</span><span class="sxs-lookup"><span data-stu-id="caff5-111">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="caff5-112">Указатель на размеры прямоугольника исходного видео.</span><span class="sxs-lookup"><span data-stu-id="caff5-112">Pointer to the rectangle dimensions of the source video.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caff5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="caff5-113">Return value</span></span>

<span data-ttu-id="caff5-114">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="caff5-114">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="caff5-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="caff5-115">Return code</span></span>                                                                                  | <span data-ttu-id="caff5-116">Описание</span><span class="sxs-lookup"><span data-stu-id="caff5-116">Description</span></span>                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="caff5-117"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="caff5-117"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="caff5-118">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="caff5-118">Failure.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="caff5-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="caff5-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="caff5-120">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="caff5-120">Invalid argument.</span></span> <span data-ttu-id="caff5-121">Формат данных несовместим.</span><span class="sxs-lookup"><span data-stu-id="caff5-121">The data format is not compatible.</span></span><br/>           |
| <dl> <span data-ttu-id="caff5-122"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="caff5-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="caff5-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="caff5-123">Unexpected error occurred.</span></span> <span data-ttu-id="caff5-124">Один или несколько аргументов имеют **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="caff5-124">One or more arguments are **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="caff5-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="caff5-125"><dt>**NOERROR**</dt></span></span> </dl>       | <span data-ttu-id="caff5-126">Успешно.</span><span class="sxs-lookup"><span data-stu-id="caff5-126">Success.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="caff5-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="caff5-127">Remarks</span></span>

<span data-ttu-id="caff5-128">Эта функция-член является вспомогательной функцией, используемой для создания изображений изображений DIB.</span><span class="sxs-lookup"><span data-stu-id="caff5-128">This member function is a helper function used for creating memory image renderings of DIB images.</span></span> <span data-ttu-id="caff5-129">Он вызывается из реализации базового класса [**кбасеконтролвидео:: жеткуррентимаже**](cbasecontrolvideo-getcurrentimage.md) , когда в эту функцию-член передается параметр _пвидеоимаже_ **null**.</span><span class="sxs-lookup"><span data-stu-id="caff5-129">It is called from the base class implementation of [**CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) when a **NULL**_pVideoImage_ parameter is passed to that member function.</span></span> <span data-ttu-id="caff5-130">В результате эта функция-член конструирует и возвращает структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , используя сведения в *пбуфферсизе* и *псаурцерект*.</span><span class="sxs-lookup"><span data-stu-id="caff5-130">As a result, this member function constructs and returns a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, using the information in *pBufferSize* and *pSourceRect*.</span></span>

## <a name="requirements"></a><span data-ttu-id="caff5-131">Требования</span><span class="sxs-lookup"><span data-stu-id="caff5-131">Requirements</span></span>



| <span data-ttu-id="caff5-132">Требование</span><span class="sxs-lookup"><span data-stu-id="caff5-132">Requirement</span></span> | <span data-ttu-id="caff5-133">Значение</span><span class="sxs-lookup"><span data-stu-id="caff5-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caff5-134">Header</span><span class="sxs-lookup"><span data-stu-id="caff5-134">Header</span></span><br/>  | <dl> <span data-ttu-id="caff5-135"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="caff5-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="caff5-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="caff5-136">Library</span></span><br/> | <dl> <span data-ttu-id="caff5-137"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="caff5-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caff5-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="caff5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caff5-139">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="caff5-139">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





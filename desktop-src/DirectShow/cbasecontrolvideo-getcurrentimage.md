---
description: Метод Жеткуррентимаже извлекает копию текущего изображения в модуле подготовки отчетов.
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: Кбасеконтролвидео. Жеткуррентимаже, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetCurrentImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d44e6930d0d7e179162939c13a54f2953c5ab965
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689522"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a><span data-ttu-id="85690-103">Кбасеконтролвидео. Жеткуррентимаже, метод</span><span class="sxs-lookup"><span data-stu-id="85690-103">CBaseControlVideo.GetCurrentImage method</span></span>

<span data-ttu-id="85690-104">`GetCurrentImage`Метод извлекает копию текущего изображения в модуле подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="85690-104">The `GetCurrentImage` method retrieves a copy of the current image at the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="85690-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85690-105">Syntax</span></span>


```C++
HRESULT GetCurrentImage(
   long *pBufferSize,
   long *pVideoImage
);
```



## <a name="parameters"></a><span data-ttu-id="85690-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85690-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85690-107">*пбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="85690-107">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="85690-108">Указатель на размер выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="85690-108">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="85690-109">*пвидеоимаже*</span><span class="sxs-lookup"><span data-stu-id="85690-109">*pVideoImage*</span></span> 
</dt> <dd>

<span data-ttu-id="85690-110">Указатель на выходной буфер для изображения.</span><span class="sxs-lookup"><span data-stu-id="85690-110">Pointer to the output buffer for the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85690-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85690-111">Return value</span></span>

<span data-ttu-id="85690-112">Возвращает значение **HRESULT** , которое зависит от реализации. может принимать одно из следующих значений или другие значения, отсутствующие в списке.</span><span class="sxs-lookup"><span data-stu-id="85690-112">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="85690-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="85690-113">Return code</span></span>                                                                                        | <span data-ttu-id="85690-114">Описание</span><span class="sxs-lookup"><span data-stu-id="85690-114">Description</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85690-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="85690-115"><dt>**E\_FAIL**</dt></span></span> </dl>             | <span data-ttu-id="85690-116">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="85690-116">Failure.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="85690-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="85690-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>       | <span data-ttu-id="85690-118">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="85690-118">Invalid argument.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="85690-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="85690-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>      | <span data-ttu-id="85690-120">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="85690-120">Out of memory.</span></span> <span data-ttu-id="85690-121">Возвращается, если параметр *пвидеоинфо* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="85690-121">Returned when the *pVideoInfo* parameter is **NULL**.</span></span><br/>   |
| <dl> <span data-ttu-id="85690-122"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="85690-122"><dt>**NOERROR**</dt></span></span> </dl>             | <span data-ttu-id="85690-123">Успешно.</span><span class="sxs-lookup"><span data-stu-id="85690-123">Success.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="85690-124"><dt>**VFW \_ E \_ не \_ приостановлен**</dt></span><span class="sxs-lookup"><span data-stu-id="85690-124"><dt>**VFW\_E\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="85690-125">Не удалось выполнить операцию, поскольку фильтр не приостановлен.</span><span class="sxs-lookup"><span data-stu-id="85690-125">The operation could not be performed because the filter is not paused.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="85690-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85690-126">Remarks</span></span>

<span data-ttu-id="85690-127">Эта функция члена извлекает изображение из примера и копирует его в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="85690-127">This member function retrieves the image from the sample and copies it into the output buffer.</span></span> <span data-ttu-id="85690-128">Раздел видео, скопированный в выходной буфер, отражает исходный прямоугольник, заданный через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="85690-128">The section of video copied into the output buffer reflects the source rectangle set through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="85690-129">Он не отражает конечный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="85690-129">It does not reflect the destination rectangle.</span></span>

## <a name="requirements"></a><span data-ttu-id="85690-130">Требования</span><span class="sxs-lookup"><span data-stu-id="85690-130">Requirements</span></span>



| <span data-ttu-id="85690-131">Требование</span><span class="sxs-lookup"><span data-stu-id="85690-131">Requirement</span></span> | <span data-ttu-id="85690-132">Значение</span><span class="sxs-lookup"><span data-stu-id="85690-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85690-133">Header</span><span class="sxs-lookup"><span data-stu-id="85690-133">Header</span></span><br/>  | <dl> <span data-ttu-id="85690-134"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85690-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="85690-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="85690-135">Library</span></span><br/> | <dl> <span data-ttu-id="85690-136"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="85690-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85690-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85690-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85690-138">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="85690-138">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





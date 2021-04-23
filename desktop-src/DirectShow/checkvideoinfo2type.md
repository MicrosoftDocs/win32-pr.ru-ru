---
description: Функция CheckVideoInfo2Type проверяет тип носителя, содержащий структуру формата VIDEOINFOHEADER2, для некоторых распространенных ошибок, которые могут привести к переполнению буфера или переполнению целочисленных значений.
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: Функция CheckVideoInfo2Type (Чеккбми. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfo2Type
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 5ec092bdea1e3dd00de36893d1816f70ca6d7945
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675830"
---
# <a name="checkvideoinfo2type-function"></a><span data-ttu-id="d5d3e-103">Функция CheckVideoInfo2Type</span><span class="sxs-lookup"><span data-stu-id="d5d3e-103">CheckVideoInfo2Type function</span></span>

<span data-ttu-id="d5d3e-104">`CheckVideoInfo2Type`Функция проверяет тип мультимедиа, содержащий структуру формата [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) для некоторых распространенных ошибок, которые могут привести к переполнению буфера или переполнению целочисленных значений.</span><span class="sxs-lookup"><span data-stu-id="d5d3e-104">The `CheckVideoInfo2Type` function checks a media type that contains a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="d5d3e-105">Эта функция не гарантирует, что тип носителя является допустимым или что код, использующий структуру, является безопасным.</span><span class="sxs-lookup"><span data-stu-id="d5d3e-105">This function does not guarantee that the media type is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d5d3e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5d3e-106">Syntax</span></span>


```C++
HRESULT CheckVideoInfo2Type(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="d5d3e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5d3e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5d3e-108">*состоит*</span><span class="sxs-lookup"><span data-stu-id="d5d3e-108">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="d5d3e-109">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) для проверки.</span><span class="sxs-lookup"><span data-stu-id="d5d3e-109">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to validate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5d3e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5d3e-110">Return value</span></span>

<span data-ttu-id="d5d3e-111">Возвращает одно из следующих значений **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d5d3e-111">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="d5d3e-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d5d3e-112">Return code</span></span>                                                                                                | <span data-ttu-id="d5d3e-113">Описание</span><span class="sxs-lookup"><span data-stu-id="d5d3e-113">Description</span></span>                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="d5d3e-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d5d3e-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="d5d3e-115">Успешно</span><span class="sxs-lookup"><span data-stu-id="d5d3e-115">Success</span></span><br/>                |
| <dl> <span data-ttu-id="d5d3e-116"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="d5d3e-116"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="d5d3e-117">Значение указателя **null**</span><span class="sxs-lookup"><span data-stu-id="d5d3e-117">**NULL** pointer value</span></span><br/> |
| <dl> <span data-ttu-id="d5d3e-118"><dt>**\_тип VFW \_ E \_ не \_ принят**</dt></span><span class="sxs-lookup"><span data-stu-id="d5d3e-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="d5d3e-119">Недопустимый тип носителя</span><span class="sxs-lookup"><span data-stu-id="d5d3e-119">Invalid media type</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="d5d3e-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5d3e-120">Remarks</span></span>

<span data-ttu-id="d5d3e-121">Эта функция вызывает [**валидатебитмапинфохеадер**](validatebitmapinfoheader.md) для проверки структуры [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) в типе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d5d3e-121">This function calls [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) to validate the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the media type.</span></span> <span data-ttu-id="d5d3e-122">Если тип формата отличается от **Format \_ VideoInfo2**, функция возвращает **\_ тип VFW E \_ \_ не \_ принято**.</span><span class="sxs-lookup"><span data-stu-id="d5d3e-122">If the format type is not **FORMAT\_VideoInfo2**, the function returns **VFW\_E\_TYPE\_NOT\_ACCEPTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5d3e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d5d3e-123">Requirements</span></span>



| <span data-ttu-id="d5d3e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d5d3e-124">Requirement</span></span> | <span data-ttu-id="d5d3e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d5d3e-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d3e-126">Header</span><span class="sxs-lookup"><span data-stu-id="d5d3e-126">Header</span></span><br/> | <dl> <span data-ttu-id="d5d3e-127"><dt>Чеккбми. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5d3e-127"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5d3e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5d3e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d3e-129">Функции видео и изображений</span><span class="sxs-lookup"><span data-stu-id="d5d3e-129">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 





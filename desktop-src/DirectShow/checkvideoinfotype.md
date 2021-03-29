---
description: Функция Чекквидеоинфотипе проверяет тип носителя, содержащий структуру формата ВИДЕОИНФОХЕАДЕР, для некоторых распространенных ошибок, которые могут привести к переполнению буфера или переполнению целочисленных значений.
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: Функция Чекквидеоинфотипе (Чеккбми. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfoType
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 7c3a3c9603f974458ed3012dc651815abd432645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657546"
---
# <a name="checkvideoinfotype-function"></a><span data-ttu-id="54fd8-103">Функция Чекквидеоинфотипе</span><span class="sxs-lookup"><span data-stu-id="54fd8-103">CheckVideoInfoType function</span></span>

<span data-ttu-id="54fd8-104">`CheckVideoInfoType`Функция проверяет тип мультимедиа, содержащий структуру формата [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) для некоторых распространенных ошибок, которые могут привести к переполнению буфера или переполнению целочисленных значений.</span><span class="sxs-lookup"><span data-stu-id="54fd8-104">The `CheckVideoInfoType` function checks a media type that contains a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="54fd8-105">Эта функция не гарантирует, что тип носителя является допустимым или что код, использующий структуру, является безопасным.</span><span class="sxs-lookup"><span data-stu-id="54fd8-105">This function does not guarantee that the media type is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="54fd8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54fd8-106">Syntax</span></span>


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="54fd8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="54fd8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54fd8-108">*состоит*</span><span class="sxs-lookup"><span data-stu-id="54fd8-108">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="54fd8-109">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) для проверки</span><span class="sxs-lookup"><span data-stu-id="54fd8-109">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to validate</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54fd8-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54fd8-110">Return value</span></span>

<span data-ttu-id="54fd8-111">Возвращает одно из следующих значений **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="54fd8-111">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="54fd8-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="54fd8-112">Return code</span></span>                                                                                                | <span data-ttu-id="54fd8-113">Описание</span><span class="sxs-lookup"><span data-stu-id="54fd8-113">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="54fd8-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="54fd8-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="54fd8-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="54fd8-115">Success.</span></span><br/>                |
| <dl> <span data-ttu-id="54fd8-116"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="54fd8-116"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="54fd8-117">Значение указателя **null** .</span><span class="sxs-lookup"><span data-stu-id="54fd8-117">**NULL** pointer value.</span></span><br/> |
| <dl> <span data-ttu-id="54fd8-118"><dt>**\_тип VFW \_ E \_ не \_ принят**</dt></span><span class="sxs-lookup"><span data-stu-id="54fd8-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="54fd8-119">Недопустимый тип носителя.</span><span class="sxs-lookup"><span data-stu-id="54fd8-119">Invalid media type.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="54fd8-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54fd8-120">Remarks</span></span>

<span data-ttu-id="54fd8-121">Эта функция вызывает [**валидатебитмапинфохеадер**](validatebitmapinfoheader.md) для проверки структуры [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) в типе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="54fd8-121">This function calls [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) to validate the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the media type.</span></span> <span data-ttu-id="54fd8-122">Если тип формата отличается от FORMAT \_ видеоинфо, функция возвращает \_ тип VFW E \_ \_ не \_ принято.</span><span class="sxs-lookup"><span data-stu-id="54fd8-122">If the format type is not FORMAT\_VideoInfo, the function returns VFW\_E\_TYPE\_NOT\_ACCEPTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="54fd8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="54fd8-123">Requirements</span></span>



| <span data-ttu-id="54fd8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="54fd8-124">Requirement</span></span> | <span data-ttu-id="54fd8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="54fd8-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54fd8-126">Header</span><span class="sxs-lookup"><span data-stu-id="54fd8-126">Header</span></span><br/> | <dl> <span data-ttu-id="54fd8-127"><dt>Чеккбми. h</dt></span><span class="sxs-lookup"><span data-stu-id="54fd8-127"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54fd8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54fd8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54fd8-129">Функции видео и изображений</span><span class="sxs-lookup"><span data-stu-id="54fd8-129">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 





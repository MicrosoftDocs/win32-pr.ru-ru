---
description: Функция ConvertVideoInfoToVideoInfo2 преобразует тип мультимедиа, который использует ВИДЕОИНФОХЕАДЕР, в тот, который использует VIDEOINFOHEADER2.
ms.assetid: d938bfc0-a5ae-475b-b183-56ff39b4bae1
title: Функция ConvertVideoInfoToVideoInfo2 (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertVideoInfoToVideoInfo2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54611c83c30ad65a806a077dc51c933a9f881636
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674785"
---
# <a name="convertvideoinfotovideoinfo2-function"></a><span data-ttu-id="cc8c9-103">Функция ConvertVideoInfoToVideoInfo2</span><span class="sxs-lookup"><span data-stu-id="cc8c9-103">ConvertVideoInfoToVideoInfo2 function</span></span>

<span data-ttu-id="cc8c9-104">`ConvertVideoInfoToVideoInfo2`Функция преобразует тип мультимедиа, который использует [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , в один, использующий [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="cc8c9-104">The `ConvertVideoInfoToVideoInfo2` function converts a media type that uses [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) to one that uses [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc8c9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc8c9-105">Syntax</span></span>


```C++
HRESULT STDAPI ConvertVideoInfoToVideoInfo2(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="cc8c9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc8c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc8c9-107">*состоит*</span><span class="sxs-lookup"><span data-stu-id="cc8c9-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="cc8c9-108">Указатель на преобразуемую структуру [**\_ \_ типа файлов мультимедиа**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="cc8c9-108">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to convert.</span></span> <span data-ttu-id="cc8c9-109">Структура должна иметь формат типа Format \_ видеоинфо.</span><span class="sxs-lookup"><span data-stu-id="cc8c9-109">The structure must have format type FORMAT\_VideoInfo.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc8c9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc8c9-110">Return value</span></span>

<span data-ttu-id="cc8c9-111">Возвращает S \_ OK или E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cc8c9-111">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc8c9-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc8c9-112">Remarks</span></span>

<span data-ttu-id="cc8c9-113">Эта функция выделяет новую структуру **VIDEOINFOHEADER2** , копирует члены структуры **видеоинфохеадер** в нее и заменяет старую структуру новой структурой в блоке формата типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cc8c9-113">This function allocates a new **VIDEOINFOHEADER2** structure, copies the members of the **VIDEOINFOHEADER** structure into it, and replaces the old structure with the new structure in the format block of the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc8c9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cc8c9-114">Requirements</span></span>



| <span data-ttu-id="cc8c9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cc8c9-115">Requirement</span></span> | <span data-ttu-id="cc8c9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cc8c9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc8c9-117">Header</span><span class="sxs-lookup"><span data-stu-id="cc8c9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="cc8c9-118"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc8c9-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cc8c9-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cc8c9-119">Library</span></span><br/> | <dl> <span data-ttu-id="cc8c9-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cc8c9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc8c9-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc8c9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc8c9-122">Функции видео и изображений</span><span class="sxs-lookup"><span data-stu-id="cc8c9-122">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 





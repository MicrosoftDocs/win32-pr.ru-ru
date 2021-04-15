---
description: Функция Контаинспалетте определяет, содержит ли указанная структура ВИДЕОИНФОХЕАДЕР палитру.
ms.assetid: e87ab1af-a822-45d8-9326-08b450e11279
title: Функция Контаинспалетте (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContainsPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9417d9dd39f958e4a4caf68ef368d231a2097de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675823"
---
# <a name="containspalette-function"></a><span data-ttu-id="25417-103">Функция Контаинспалетте</span><span class="sxs-lookup"><span data-stu-id="25417-103">ContainsPalette function</span></span>

<span data-ttu-id="25417-104">Функция **контаинспалетте** определяет, содержит ли указанная структура [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) палитру.</span><span class="sxs-lookup"><span data-stu-id="25417-104">The **ContainsPalette** function determines whether a specified [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure contains a palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="25417-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25417-105">Syntax</span></span>


```C++
BOOL ContainsPalette(
   const VIDEOINFOHEADER *pVideoInfo

);
```



## <a name="parameters"></a><span data-ttu-id="25417-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="25417-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25417-107">*пвидеоинфо*</span><span class="sxs-lookup"><span data-stu-id="25417-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="25417-108">Указатель на структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="25417-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25417-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25417-109">Return value</span></span>

<span data-ttu-id="25417-110">Возвращает **значение true** , если значение битдепс равно 8 или меньше (**бмихеадер. бибиткаунт**), или количество цветовых индексов больше нуля (**бмихеадер. биклрусед**).</span><span class="sxs-lookup"><span data-stu-id="25417-110">Returns **TRUE** if the bitdepth is 8 or less (**bmiHeader.biBitCount**), or the number of color indexes is more than zero (**bmiHeader.biClrUsed**).</span></span> <span data-ttu-id="25417-111">В противном случае возвращает **false** .</span><span class="sxs-lookup"><span data-stu-id="25417-111">Returns **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="25417-112">Требования</span><span class="sxs-lookup"><span data-stu-id="25417-112">Requirements</span></span>



| <span data-ttu-id="25417-113">Требование</span><span class="sxs-lookup"><span data-stu-id="25417-113">Requirement</span></span> | <span data-ttu-id="25417-114">Значение</span><span class="sxs-lookup"><span data-stu-id="25417-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25417-115">Header</span><span class="sxs-lookup"><span data-stu-id="25417-115">Header</span></span><br/>  | <dl> <span data-ttu-id="25417-116"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25417-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="25417-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="25417-117">Library</span></span><br/> | <dl> <span data-ttu-id="25417-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="25417-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25417-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25417-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25417-120">Функции видео и изображений</span><span class="sxs-lookup"><span data-stu-id="25417-120">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 





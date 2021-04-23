---
description: Функция Жеттруеколортипе извлекает удобное для восприятия имя подтипа видео.
ms.assetid: 479a020c-b55c-44ec-9096-5528113a4b74
title: Функция Жеттруеколортипе (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTrueColorType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c262031045eed3755fe2d19d3bd703a347e6117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651908"
---
# <a name="gettruecolortype-function"></a><span data-ttu-id="f6f4d-103">Функция Жеттруеколортипе</span><span class="sxs-lookup"><span data-stu-id="f6f4d-103">GetTrueColorType function</span></span>

<span data-ttu-id="f6f4d-104">Функция **жеттруеколортипе** извлекает удобное для восприятия имя подтипа видео.</span><span class="sxs-lookup"><span data-stu-id="f6f4d-104">The **GetTrueColorType** function retrieves the human-readable name of a video subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6f4d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6f4d-105">Syntax</span></span>


```C++
const GUID GetTrueColorType(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="f6f4d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6f4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6f4d-107">*феадер*</span><span class="sxs-lookup"><span data-stu-id="f6f4d-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="f6f4d-108">Указатель на структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , определяющую точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="f6f4d-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure that defines the bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6f4d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6f4d-109">Return value</span></span>

<span data-ttu-id="f6f4d-110">Возвращает МЕДИАСУБТИПЕ \_ RGB555 или медиасубтипе \_ RGB565.</span><span class="sxs-lookup"><span data-stu-id="f6f4d-110">Returns MEDIASUBTYPE\_RGB555 or MEDIASUBTYPE\_RGB565.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6f4d-111">Требования</span><span class="sxs-lookup"><span data-stu-id="f6f4d-111">Requirements</span></span>



| <span data-ttu-id="f6f4d-112">Требование</span><span class="sxs-lookup"><span data-stu-id="f6f4d-112">Requirement</span></span> | <span data-ttu-id="f6f4d-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f6f4d-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f4d-114">Header</span><span class="sxs-lookup"><span data-stu-id="f6f4d-114">Header</span></span><br/>  | <dl> <span data-ttu-id="f6f4d-115"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6f4d-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f6f4d-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f6f4d-116">Library</span></span><br/> | <dl> <span data-ttu-id="f6f4d-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f6f4d-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6f4d-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6f4d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6f4d-119">Функции видео и изображений</span><span class="sxs-lookup"><span data-stu-id="f6f4d-119">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 





---
description: Функция Жетбитмаппалетте возвращает первую запись Palette в структуре ВИДЕОИНФОХЕАДЕР.
ms.assetid: 7c620f81-31d9-408f-954d-aeff39f93956
title: Функция Жетбитмаппалетте (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa4139c7aaece3e92a26fbf69fc02b8759f1613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675530"
---
# <a name="getbitmappalette-function"></a><span data-ttu-id="47f94-103">Функция Жетбитмаппалетте</span><span class="sxs-lookup"><span data-stu-id="47f94-103">GetBitmapPalette function</span></span>

<span data-ttu-id="47f94-104">`GetBitmapPalette`Функция возвращает первую запись Palette в структуре [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="47f94-104">The `GetBitmapPalette` function returns the first palette entry in a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f94-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47f94-105">Syntax</span></span>


```C++
const RGBQUAD* GetBitmapPalette(
   const VIDEOINFOHEADER *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="47f94-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="47f94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47f94-107">*пвидеоинфо*</span><span class="sxs-lookup"><span data-stu-id="47f94-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="47f94-108">Указатель на структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="47f94-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47f94-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47f94-109">Return value</span></span>

<span data-ttu-id="47f94-110">Возвращает указатель на первую запись в палитре.</span><span class="sxs-lookup"><span data-stu-id="47f94-110">Returns a pointer to the first palette entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="47f94-111">Требования</span><span class="sxs-lookup"><span data-stu-id="47f94-111">Requirements</span></span>



| <span data-ttu-id="47f94-112">Требование</span><span class="sxs-lookup"><span data-stu-id="47f94-112">Requirement</span></span> | <span data-ttu-id="47f94-113">Значение</span><span class="sxs-lookup"><span data-stu-id="47f94-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f94-114">Header</span><span class="sxs-lookup"><span data-stu-id="47f94-114">Header</span></span><br/>  | <dl> <span data-ttu-id="47f94-115"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47f94-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="47f94-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="47f94-116">Library</span></span><br/> | <dl> <span data-ttu-id="47f94-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="47f94-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





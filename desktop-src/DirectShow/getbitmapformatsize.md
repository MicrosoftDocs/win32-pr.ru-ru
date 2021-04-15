---
description: Функция Жетбитмапформатсизе вычисляет размер, необходимый для структуры ВИДЕОИНФО, которая может содержать указанную структуру БИТМАПИНФОХЕАДЕР.
ms.assetid: a559415a-070f-4674-be12-a65a46025809
title: Функция Жетбитмапформатсизе (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapFormatSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39a64f6d975e403de6c177906b23ef7e09f29ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651934"
---
# <a name="getbitmapformatsize-function"></a><span data-ttu-id="2313f-103">Функция Жетбитмапформатсизе</span><span class="sxs-lookup"><span data-stu-id="2313f-103">GetBitmapFormatSize function</span></span>

<span data-ttu-id="2313f-104">`GetBitmapFormatSize`Функция вычисляет размер, необходимый для структуры [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) , которая может содержать указанную структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="2313f-104">The `GetBitmapFormatSize` function calculates the size needed for a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure that can hold a specified [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2313f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2313f-105">Syntax</span></span>


```C++
LONG GetBitmapFormatSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="2313f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2313f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2313f-107">*феадер*</span><span class="sxs-lookup"><span data-stu-id="2313f-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="2313f-108">Указатель на структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="2313f-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2313f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2313f-109">Return value</span></span>

<span data-ttu-id="2313f-110">Возвращает размер в байтах.</span><span class="sxs-lookup"><span data-stu-id="2313f-110">Returns the size, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="2313f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2313f-111">Remarks</span></span>

<span data-ttu-id="2313f-112">За структурой [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) могут следовать цветные маски или записи палитры, поэтому может быть трудно определить число байтов, необходимое для создания структуры [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) из существующей структуры **битмапинфохеадер** .</span><span class="sxs-lookup"><span data-stu-id="2313f-112">A [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure might be followed by color masks or palette entries, so it can be difficult to determine the number of bytes required to construct a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure from an existing **BITMAPINFOHEADER** structure.</span></span>

<span data-ttu-id="2313f-113">Чтобы скопировать структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) в структуру [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) , используйте макрос [**Header**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) , который вычисляет правильное смещение.</span><span class="sxs-lookup"><span data-stu-id="2313f-113">To copy a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure into a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure, use the [**HEADER**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) macro, which calculates the correct offset.</span></span>

## <a name="examples"></a><span data-ttu-id="2313f-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="2313f-114">Examples</span></span>


```
LONG size = GetBitmapFormatSize(&bmi);

VIDEOINFO *pVi = static_cast<VIDEOINFO*>(CoTaskMemAlloc(size));

if (pVi != NULL)
{
    CopyMemory(HEADER(pVi), &bmi, sizeof(BITMAPINFOHEADER));
}
```



## <a name="requirements"></a><span data-ttu-id="2313f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2313f-115">Requirements</span></span>



| <span data-ttu-id="2313f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2313f-116">Requirement</span></span> | <span data-ttu-id="2313f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2313f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2313f-118">Header</span><span class="sxs-lookup"><span data-stu-id="2313f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2313f-119"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2313f-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2313f-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2313f-120">Library</span></span><br/> | <dl> <span data-ttu-id="2313f-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2313f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2313f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2313f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2313f-123">Функции видео и изображений</span><span class="sxs-lookup"><span data-stu-id="2313f-123">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 





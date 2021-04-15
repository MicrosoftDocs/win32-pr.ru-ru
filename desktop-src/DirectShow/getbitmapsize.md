---
description: Функция Жетбитмапсизе вычисляет число байтов, необходимых для аппаратно-независимого точечного рисунка (DIB). Эта функция просто вызывает макрос ДИБСИЗЕ.
ms.assetid: ce23cdf2-9804-4d2e-b9ef-16e54b2d571e
title: Функция Жетбитмапсизе (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 004201cf3ff839aa1301dcfff0240a73a9128e50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651933"
---
# <a name="getbitmapsize-function"></a><span data-ttu-id="dd0aa-104">Функция Жетбитмапсизе</span><span class="sxs-lookup"><span data-stu-id="dd0aa-104">GetBitmapSize function</span></span>

<span data-ttu-id="dd0aa-105">`GetBitmapSize`Функция вычисляет число байтов, необходимых для аппаратно-независимого точечного рисунка (DIB).</span><span class="sxs-lookup"><span data-stu-id="dd0aa-105">The `GetBitmapSize` function calculates the number of bytes required by a device-independent bitmap (DIB).</span></span> <span data-ttu-id="dd0aa-106">Эта функция просто вызывает макрос [**дибсизе**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) .</span><span class="sxs-lookup"><span data-stu-id="dd0aa-106">This function simply calls the [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) macro.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd0aa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd0aa-107">Syntax</span></span>


```C++
DWORD GetBitmapSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="dd0aa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd0aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd0aa-109">*феадер*</span><span class="sxs-lookup"><span data-stu-id="dd0aa-109">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="dd0aa-110">Указатель на структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="dd0aa-110">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd0aa-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd0aa-111">Return value</span></span>

<span data-ttu-id="dd0aa-112">Возвращает размер в байтах.</span><span class="sxs-lookup"><span data-stu-id="dd0aa-112">Returns the size in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd0aa-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dd0aa-113">Requirements</span></span>



| <span data-ttu-id="dd0aa-114">Требование</span><span class="sxs-lookup"><span data-stu-id="dd0aa-114">Requirement</span></span> | <span data-ttu-id="dd0aa-115">Значение</span><span class="sxs-lookup"><span data-stu-id="dd0aa-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0aa-116">Header</span><span class="sxs-lookup"><span data-stu-id="dd0aa-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dd0aa-117"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd0aa-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="dd0aa-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dd0aa-118">Library</span></span><br/> | <dl> <span data-ttu-id="dd0aa-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="dd0aa-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd0aa-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd0aa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd0aa-121">Функции видео и изображений</span><span class="sxs-lookup"><span data-stu-id="dd0aa-121">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 





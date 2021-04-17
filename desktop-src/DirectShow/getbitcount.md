---
description: Функция Жетбиткаунт возвращает число бит на пиксель, используемых указанным подтипом видео. Эта функция допустима только для несжатых подтипов RGB.
ms.assetid: 876b91c8-50ba-4217-b79c-7f7ec1c22b83
title: Функция Жетбиткаунт (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fed9b24ebf2e95b2408de30a407904e6bd3c1c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675531"
---
# <a name="getbitcount-function"></a><span data-ttu-id="9c3b5-104">Функция Жетбиткаунт</span><span class="sxs-lookup"><span data-stu-id="9c3b5-104">GetBitCount function</span></span>

<span data-ttu-id="9c3b5-105">`GetBitCount`Функция возвращает число бит на пиксель, используемых указанным подтипом видео.</span><span class="sxs-lookup"><span data-stu-id="9c3b5-105">The `GetBitCount` function returns the number of bits per pixel used by a specified video subtype.</span></span> <span data-ttu-id="9c3b5-106">Эта функция допустима только для несжатых подтипов RGB.</span><span class="sxs-lookup"><span data-stu-id="9c3b5-106">This function is valid for uncompressed RGB subtypes only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c3b5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c3b5-107">Syntax</span></span>


```C++
WORD GetBitCount(
   const GUID *pSubtype
);
```



## <a name="parameters"></a><span data-ttu-id="9c3b5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c3b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c3b5-109">*псубтипе*</span><span class="sxs-lookup"><span data-stu-id="9c3b5-109">*pSubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="9c3b5-110">Указатель на **GUID** подтипа видео.</span><span class="sxs-lookup"><span data-stu-id="9c3b5-110">Pointer to a video subtype **GUID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c3b5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c3b5-111">Return value</span></span>

<span data-ttu-id="9c3b5-112">Возвращает число битов на пиксель для этого подтипа или значение **ушрт \_ Max** , если подтип не распознан.</span><span class="sxs-lookup"><span data-stu-id="9c3b5-112">Returns the number of bits per pixel for this subtype, or the value **USHRT\_MAX** if the subtype is not recognized.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c3b5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9c3b5-113">Requirements</span></span>



| <span data-ttu-id="9c3b5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9c3b5-114">Requirement</span></span> | <span data-ttu-id="9c3b5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9c3b5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c3b5-116">Header</span><span class="sxs-lookup"><span data-stu-id="9c3b5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9c3b5-117"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c3b5-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9c3b5-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9c3b5-118">Library</span></span><br/> | <dl> <span data-ttu-id="9c3b5-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9c3b5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c3b5-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c3b5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c3b5-121">Функции видео и изображений</span><span class="sxs-lookup"><span data-stu-id="9c3b5-121">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 





---
description: Функция Дисплайтипе отправляет сведения о типе мультимедиа в расположение выходных данных отладки. Игнорируется в розничных сборках.
ms.assetid: 63a88508-dff8-4869-97e5-0f75f4a9dca0
title: Функция Дисплайтипе (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DisplayType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3d83bbe7a24463fc4cfaed4ace3adec9d6fcf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675583"
---
# <a name="displaytype-function"></a><span data-ttu-id="545a5-104">Функция Дисплайтипе</span><span class="sxs-lookup"><span data-stu-id="545a5-104">DisplayType function</span></span>

<span data-ttu-id="545a5-105">`DisplayType`Функция отправляет сведения о типе мультимедиа в расположение выходных данных отладки.</span><span class="sxs-lookup"><span data-stu-id="545a5-105">The `DisplayType` function sends information about a media type to the debug output location.</span></span> <span data-ttu-id="545a5-106">Игнорируется в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="545a5-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="545a5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="545a5-107">Syntax</span></span>


```C++
void DisplayType(
         LPTSTR        label,
   const AM_MEDIA_TYPE *pmtIn
);
```



## <a name="parameters"></a><span data-ttu-id="545a5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="545a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="545a5-109">*label*</span><span class="sxs-lookup"><span data-stu-id="545a5-109">*label*</span></span> 
</dt> <dd>

<span data-ttu-id="545a5-110">Строка, содержащая сообщение, отображаемое со сведениями о типе носителя.</span><span class="sxs-lookup"><span data-stu-id="545a5-110">String that contains a message to display with the media type information.</span></span>

</dd> <dt>

<span data-ttu-id="545a5-111">*пмтин*</span><span class="sxs-lookup"><span data-stu-id="545a5-111">*pmtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="545a5-112">оинтер к структуре [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , которая содержит тип носителя.</span><span class="sxs-lookup"><span data-stu-id="545a5-112">ointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="545a5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="545a5-113">Return value</span></span>

<span data-ttu-id="545a5-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="545a5-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="545a5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="545a5-115">Remarks</span></span>

<span data-ttu-id="545a5-116">Эта функция создает несколько \_ сообщений трассировки журнала.</span><span class="sxs-lookup"><span data-stu-id="545a5-116">This function generates several LOG\_TRACE messages.</span></span> <span data-ttu-id="545a5-117">При уровне ведения журнала 2 или выше функция отображает основной тип, подтип и тип формата, а также данные из блока формата.</span><span class="sxs-lookup"><span data-stu-id="545a5-117">At logging level 2 or higher, the function displays the major type, subtype, and format type, and data from the format block.</span></span> <span data-ttu-id="545a5-118">При уровне ведения журнала 5 или выше функция отображает дополнительные сведения, такие как исходный и целевой прямоугольники для типов видео.</span><span class="sxs-lookup"><span data-stu-id="545a5-118">At logging level 5 or higher, the function displays additional information, such as the source and target rectangles for video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="545a5-119">Требования</span><span class="sxs-lookup"><span data-stu-id="545a5-119">Requirements</span></span>



| <span data-ttu-id="545a5-120">Требование</span><span class="sxs-lookup"><span data-stu-id="545a5-120">Requirement</span></span> | <span data-ttu-id="545a5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="545a5-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="545a5-122">Header</span><span class="sxs-lookup"><span data-stu-id="545a5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="545a5-123"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="545a5-123"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="545a5-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="545a5-124">Library</span></span><br/> | <dl> <span data-ttu-id="545a5-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="545a5-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="545a5-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="545a5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="545a5-127">Выходные функции отладки</span><span class="sxs-lookup"><span data-stu-id="545a5-127">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 





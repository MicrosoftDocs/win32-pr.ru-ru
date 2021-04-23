---
description: Функция Креатеаудиомедиатипе инициализирует тип мультимедиа из структуры ВАВЕФОРМАТЕКС.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: Функция Креатеаудиомедиатипе (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateAudioMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef4e525762d4b6928e6a9095fad34f3f4f2e96fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679678"
---
# <a name="createaudiomediatype-function"></a><span data-ttu-id="000b5-103">Функция Креатеаудиомедиатипе</span><span class="sxs-lookup"><span data-stu-id="000b5-103">CreateAudioMediaType function</span></span>

<span data-ttu-id="000b5-104">Функция **креатеаудиомедиатипе** инициализирует тип мультимедиа из структуры [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="000b5-104">The **CreateAudioMediaType** function initializes a media type from a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="000b5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="000b5-105">Syntax</span></span>


```C++
HRESULT STDAPI CreateAudioMediaType(
   const WAVEFORMATEX  *pwfx,
         AM_MEDIA_TYPE *pmt,
         BOOL          bSetFormat
);
```



## <a name="parameters"></a><span data-ttu-id="000b5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="000b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="000b5-107">*пвфкс*</span><span class="sxs-lookup"><span data-stu-id="000b5-107">*pwfx*</span></span> 
</dt> <dd>

<span data-ttu-id="000b5-108">Указатель на переданную структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="000b5-108">Pointer to the supplied [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="000b5-109">*состоит*</span><span class="sxs-lookup"><span data-stu-id="000b5-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="000b5-110">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) для инициализации.</span><span class="sxs-lookup"><span data-stu-id="000b5-110">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to initialize.</span></span>

</dd> <dt>

<span data-ttu-id="000b5-111">*бсетформат*</span><span class="sxs-lookup"><span data-stu-id="000b5-111">*bSetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="000b5-112">Флаг, указывающий, инициализировать ли блок формата.</span><span class="sxs-lookup"><span data-stu-id="000b5-112">Flag indicating whether to initialize the format block.</span></span> <span data-ttu-id="000b5-113">Укажите **значение true** , чтобы инициализировать его, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="000b5-113">Specify **TRUE** to initialize it, or **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="000b5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="000b5-114">Return value</span></span>

<span data-ttu-id="000b5-115">Возвращает значение E \_ OUTOFMEMORY, если память не может быть выделена для данных формата. \_ОК в противном случае.</span><span class="sxs-lookup"><span data-stu-id="000b5-115">Returns E\_OUTOFMEMORY if memory could not be allocated for the format data; S\_OK otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="000b5-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="000b5-116">Remarks</span></span>

<span data-ttu-id="000b5-117">Если параметр *бсетформат* имеет **значение true**, метод выделяет память для блока Format.</span><span class="sxs-lookup"><span data-stu-id="000b5-117">If the *bSetFormat* parameter is **TRUE**, the method allocates the memory for the format block.</span></span> <span data-ttu-id="000b5-118">Если параметр *ПЛТ* уже содержит выделенный блок формата, произойдет утечка памяти.</span><span class="sxs-lookup"><span data-stu-id="000b5-118">If the *pmt* parameter already contains an allocated format block, a memory leak will occur.</span></span> <span data-ttu-id="000b5-119">Чтобы избежать утечки памяти, вызовите [**фримедиатипе**](freemediatype.md) перед вызовом этой функции.</span><span class="sxs-lookup"><span data-stu-id="000b5-119">To avoid a memory leak, call [**FreeMediaType**](freemediatype.md) before calling this function.</span></span> <span data-ttu-id="000b5-120">После возврата метода вызовите **фримедиатипе** еще раз, чтобы освободить блок формата.</span><span class="sxs-lookup"><span data-stu-id="000b5-120">After the method returns, call **FreeMediaType** again to free the format block.</span></span>

## <a name="requirements"></a><span data-ttu-id="000b5-121">Требования</span><span class="sxs-lookup"><span data-stu-id="000b5-121">Requirements</span></span>



| <span data-ttu-id="000b5-122">Требование</span><span class="sxs-lookup"><span data-stu-id="000b5-122">Requirement</span></span> | <span data-ttu-id="000b5-123">Значение</span><span class="sxs-lookup"><span data-stu-id="000b5-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="000b5-124">Header</span><span class="sxs-lookup"><span data-stu-id="000b5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="000b5-125"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="000b5-125"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="000b5-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="000b5-126">Library</span></span><br/> | <dl> <span data-ttu-id="000b5-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="000b5-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="000b5-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="000b5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="000b5-129">**Функции типа мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="000b5-129">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 


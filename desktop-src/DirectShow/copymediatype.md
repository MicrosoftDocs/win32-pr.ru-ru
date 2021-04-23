---
description: Функция Копимедиатипе копирует \_ \_ в другую структуру структуру типа мультимедиа am, включая блок Format
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: Функция Копимедиатипе (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CopyMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e37f277244ae9b82c395d7901917e1fc1e78b35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675899"
---
# <a name="copymediatype-function"></a><span data-ttu-id="bfb8f-103">Функция Копимедиатипе</span><span class="sxs-lookup"><span data-stu-id="bfb8f-103">CopyMediaType function</span></span>

<span data-ttu-id="bfb8f-104">Функция **копимедиатипе** копирует в другую структуру структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , включая блок Format</span><span class="sxs-lookup"><span data-stu-id="bfb8f-104">The **CopyMediaType** function copies an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure into another structure, including the format block</span></span>

## <a name="syntax"></a><span data-ttu-id="bfb8f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfb8f-105">Syntax</span></span>


```C++
HRESULT WINAPI CopyMediaType(
         AM_MEDIA_TYPE *pmtTarget,
   const AM_MEDIA_TYPE *pmtSource
);
```



## <a name="parameters"></a><span data-ttu-id="bfb8f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfb8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfb8f-107">*пмттаржет*</span><span class="sxs-lookup"><span data-stu-id="bfb8f-107">*pmtTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="bfb8f-108">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="bfb8f-108">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="bfb8f-109">Метод копирует тип мультимедиа в эту структуру.</span><span class="sxs-lookup"><span data-stu-id="bfb8f-109">The method copies the media type into this structure.</span></span>

</dd> <dt>

<span data-ttu-id="bfb8f-110">*пмтсаурце*</span><span class="sxs-lookup"><span data-stu-id="bfb8f-110">*pmtSource*</span></span> 
</dt> <dd>

<span data-ttu-id="bfb8f-111">Указатель на источник — [**Структура \_ \_ типа мультимедиа**](/windows/win32/api/strmif/ns-strmif-am_media_type) для копирования.</span><span class="sxs-lookup"><span data-stu-id="bfb8f-111">Pointer to a source [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfb8f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bfb8f-112">Return value</span></span>

<span data-ttu-id="bfb8f-113">Возвращает S \_ OK или E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bfb8f-113">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfb8f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bfb8f-114">Remarks</span></span>

<span data-ttu-id="bfb8f-115">Эта функция выделяет память для блока Format.</span><span class="sxs-lookup"><span data-stu-id="bfb8f-115">This function allocates the memory for the format block.</span></span> <span data-ttu-id="bfb8f-116">Если параметр *пмттаржет* уже содержит выделенный блок формата, произойдет утечка памяти.</span><span class="sxs-lookup"><span data-stu-id="bfb8f-116">If the *pmtTarget* parameter already contains an allocated format block, a memory leak will occur.</span></span> <span data-ttu-id="bfb8f-117">Чтобы избежать утечки памяти, вызовите [**фримедиатипе**](freemediatype.md) перед вызовом этой функции.</span><span class="sxs-lookup"><span data-stu-id="bfb8f-117">To avoid a memory leak, call [**FreeMediaType**](freemediatype.md) before calling this function.</span></span>

<span data-ttu-id="bfb8f-118">После возврата метода вызовите [**фримедиатипе**](freemediatype.md) для *пмттаржет* , чтобы освободить блок формата.</span><span class="sxs-lookup"><span data-stu-id="bfb8f-118">After the method returns, call [**FreeMediaType**](freemediatype.md) on *pmtTarget* to free the format block.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfb8f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="bfb8f-119">Requirements</span></span>



| <span data-ttu-id="bfb8f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="bfb8f-120">Requirement</span></span> | <span data-ttu-id="bfb8f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="bfb8f-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfb8f-122">Header</span><span class="sxs-lookup"><span data-stu-id="bfb8f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bfb8f-123"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfb8f-123"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="bfb8f-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bfb8f-124">Library</span></span><br/> | <dl> <span data-ttu-id="bfb8f-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bfb8f-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfb8f-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bfb8f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfb8f-127">**Функции типа мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="bfb8f-127">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 





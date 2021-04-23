---
description: Создает копию изображения в памяти.
ms.assetid: 83a980bc-1298-439f-8dfc-49534591977f
title: Кбасеконтролвидео. Копимаже, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CopyImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23ada87e77d3c3441f489abed2e7af86a2a556ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657250"
---
# <a name="cbasecontrolvideocopyimage-method"></a><span data-ttu-id="83965-103">Кбасеконтролвидео. Копимаже, метод</span><span class="sxs-lookup"><span data-stu-id="83965-103">CBaseControlVideo.CopyImage method</span></span>

<span data-ttu-id="83965-104">Создает копию изображения в памяти.</span><span class="sxs-lookup"><span data-stu-id="83965-104">Creates a memory copy of an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="83965-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83965-105">Syntax</span></span>


```C++
HRESULT CopyImage(
   IMediaSample    *pMediaSample,
   VIDEOINFOHEADER *pVideoInfo,
   LONG            *pBufferSize,
   BYTE            *pVideoImage,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="83965-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="83965-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83965-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="83965-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="83965-108">Указатель на образец, содержащий изображение видео.</span><span class="sxs-lookup"><span data-stu-id="83965-108">Pointer to the sample containing the video image.</span></span>

</dd> <dt>

<span data-ttu-id="83965-109">*пвидеоинфо*</span><span class="sxs-lookup"><span data-stu-id="83965-109">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="83965-110">Указатель на формат, представляющий изображение видео.</span><span class="sxs-lookup"><span data-stu-id="83965-110">Pointer to the format representing the video image.</span></span>

</dd> <dt>

<span data-ttu-id="83965-111">*пбуфферсизе*</span><span class="sxs-lookup"><span data-stu-id="83965-111">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="83965-112">Указатель на размер выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="83965-112">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="83965-113">*пвидеоимаже*</span><span class="sxs-lookup"><span data-stu-id="83965-113">*pVideoImage*</span></span> 
</dt> <dd>

<span data-ttu-id="83965-114">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="83965-114">Pointer to the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="83965-115">*псаурцерект*</span><span class="sxs-lookup"><span data-stu-id="83965-115">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="83965-116">Указатель на исходный прямоугольник видео.</span><span class="sxs-lookup"><span data-stu-id="83965-116">Pointer to the source video rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83965-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83965-117">Return value</span></span>

<span data-ttu-id="83965-118">Если параметр *пвидеоимаже* имеет **значение NULL**, параметр *пбуфферсизе* заполняется числом байтов, необходимых выходному буферу для хранения изображения.</span><span class="sxs-lookup"><span data-stu-id="83965-118">If the *pVideoImage* parameter is **NULL**, the *pBufferSize* parameter is filled in with the number of bytes the output buffer requires to store the image.</span></span> <span data-ttu-id="83965-119">Если переданный буфер слишком мал или функция-член не может выделить достаточно памяти, функция-член возвращает E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="83965-119">If the buffer passed in is too small or the member function fails to allocate sufficient memory, the member function returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="83965-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83965-120">Remarks</span></span>

<span data-ttu-id="83965-121">Функция члена получает изображение из примера и копирует его в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="83965-121">The member function retrieves the image from the sample and copies it into the output buffer.</span></span> <span data-ttu-id="83965-122">Раздел видео, скопированный в выходной буфер, отражает исходный прямоугольник, заданный через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) (хотя он не отражает конечный прямоугольник).</span><span class="sxs-lookup"><span data-stu-id="83965-122">The section of video copied into the output buffer reflects the source rectangle that is set through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface (although it does not reflect the destination rectangle).</span></span>

## <a name="requirements"></a><span data-ttu-id="83965-123">Требования</span><span class="sxs-lookup"><span data-stu-id="83965-123">Requirements</span></span>



| <span data-ttu-id="83965-124">Требование</span><span class="sxs-lookup"><span data-stu-id="83965-124">Requirement</span></span> | <span data-ttu-id="83965-125">Значение</span><span class="sxs-lookup"><span data-stu-id="83965-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83965-126">Header</span><span class="sxs-lookup"><span data-stu-id="83965-126">Header</span></span><br/>  | <dl> <span data-ttu-id="83965-127"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83965-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="83965-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="83965-128">Library</span></span><br/> | <dl> <span data-ttu-id="83965-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="83965-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83965-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83965-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83965-131">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="83965-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





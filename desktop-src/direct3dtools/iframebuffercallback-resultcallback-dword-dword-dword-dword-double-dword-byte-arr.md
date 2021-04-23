---
description: Обратный вызов, уведомляющий узел о буфера кадров данных, возвращаемых связанным запросом.
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ифрамебуфферкаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F0276125-2DA9-45BC-A295-BD67C21EE601
api_name:
- IFrameBufferCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5433c7bbf5fe67455b60fd754eecb2c2877c5d6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140063"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span data-ttu-id="19657-103"><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>Метод Ифрамебуфферкаллбакк:: Ресулткаллбакк</span><span class="sxs-lookup"><span data-stu-id="19657-103"><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>IFrameBufferCallback::ResultCallback method</span></span>

<span data-ttu-id="19657-104">Обратный вызов, уведомляющий узел о буфера кадров данных, возвращаемых связанным запросом.</span><span class="sxs-lookup"><span data-stu-id="19657-104">A callback that notifies the host of framebuffer information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="19657-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19657-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD   frameNumber,
   DWORD   width,
   DWORD   height,
   DWORD   renderTargetPtr,
   double  frameDuraction,
   DWORD   size,
   BYTE [] count5_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="19657-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="19657-106">Parameters</span></span>

<span data-ttu-id="19657-107">*фраменумбер* </span><span class="sxs-lookup"><span data-stu-id="19657-107">*frameNumber* </span></span>  
<span data-ttu-id="19657-108">Номер кадра.</span><span class="sxs-lookup"><span data-stu-id="19657-108">The frame number.</span></span>

<span data-ttu-id="19657-109">*Ширина* </span><span class="sxs-lookup"><span data-stu-id="19657-109">*width* </span></span>  
<span data-ttu-id="19657-110">Ширина рамки.</span><span class="sxs-lookup"><span data-stu-id="19657-110">The width of the frame.</span></span>

<span data-ttu-id="19657-111">*равно* </span><span class="sxs-lookup"><span data-stu-id="19657-111">*height* </span></span>  
<span data-ttu-id="19657-112">Высота рамки.</span><span class="sxs-lookup"><span data-stu-id="19657-112">The height of the frame.</span></span>

<span data-ttu-id="19657-113">*рендертаржетптр* </span><span class="sxs-lookup"><span data-stu-id="19657-113">*renderTargetPtr* </span></span>  
<span data-ttu-id="19657-114">Целевой объект отрисовки, из которого берутся результаты.</span><span class="sxs-lookup"><span data-stu-id="19657-114">The render target that the results come from.</span></span> <span data-ttu-id="19657-115">Он всегда является слотом, заданным запросом буфера кадров, или, если не вызовом Draw, первый РТВ баунт в источник вывода.</span><span class="sxs-lookup"><span data-stu-id="19657-115">It is always a slot specified by the frame buffer request, or if not a draw call, then the first RTV bount to the output source.</span></span>

<span data-ttu-id="19657-116">*фрамедурактион* </span><span class="sxs-lookup"><span data-stu-id="19657-116">*frameDuraction* </span></span>  
<span data-ttu-id="19657-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="19657-117">Not used.</span></span>

<span data-ttu-id="19657-118">*изменять* </span><span class="sxs-lookup"><span data-stu-id="19657-118">*size* </span></span>  
<span data-ttu-id="19657-119">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="19657-119">The size of the output buffer in bytes.</span></span>

<span data-ttu-id="19657-120">*\_буфер count5* </span><span class="sxs-lookup"><span data-stu-id="19657-120">*count5\_buffer* </span></span>  
<span data-ttu-id="19657-121">Содержимое целевого объекта отрисовки в формате R8G8B8A8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="19657-121">The contents of the render target in R8G8B8A8\_UNORM format.</span></span>

## <a name="return-value"></a><span data-ttu-id="19657-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19657-122">Return value</span></span>

<span data-ttu-id="19657-123">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="19657-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="19657-124">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="19657-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="19657-125">Требования</span><span class="sxs-lookup"><span data-stu-id="19657-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="19657-126">Header</span><span class="sxs-lookup"><span data-stu-id="19657-126">Header</span></span></p></td><td><span data-ttu-id="19657-127">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="19657-127">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="19657-128"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="19657-128"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="19657-129">**ифрамебуфферкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="19657-129">**IFrameBufferCallback**</span></span>](/windows/desktop/direct3dtools/iframebuffercallback)

 

 

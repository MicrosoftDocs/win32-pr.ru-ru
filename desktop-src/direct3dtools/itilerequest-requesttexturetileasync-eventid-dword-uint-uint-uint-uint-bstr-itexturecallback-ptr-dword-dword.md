---
description: Запросы на получение содержимого мозаичной текстуры в виде. Файл DDS (поверхность DirectDraw).
MS-HAID: vspixengine.ITileRequest\_RequestTextureTileAsync\_EventID\_DWORD\_UINT\_UINT\_UINT\_UINT\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Итилерекуест:: Рекуесттекстуретилеасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E3F4FAC2-E7D9-4FDF-BE64-73D3EA175A8F
api_name:
- ITileRequest.RequestTextureTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e22c3b54c1e04242805d698c37a1d4dd2709fa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140126"
---
# <a name="span-idvspixengineitilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dwordspanitilerequestrequesttexturetileasync-method"></a><span data-ttu-id="5aced-103"><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>Метод Итилерекуест:: Рекуесттекстуретилеасинк</span><span class="sxs-lookup"><span data-stu-id="5aced-103"><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>ITileRequest::RequestTextureTileAsync method</span></span>

<span data-ttu-id="5aced-104">Запросы на получение содержимого мозаичной текстуры в виде. Файл DDS (поверхность DirectDraw).</span><span class="sxs-lookup"><span data-stu-id="5aced-104">Requests to get the contents of a tiled texture as a .DDS (DirectDraw Surface) file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aced-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5aced-105">Syntax</span></span>


```C++
HRESULT RequestTextureTileAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   UINT               tileSubresource,
   UINT               tileX,
   UINT               tileY,
   UINT               tileZ,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="5aced-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5aced-106">Parameters</span></span>

<span data-ttu-id="5aced-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="5aced-107">*eventID* </span></span>  
<span data-ttu-id="5aced-108">Указанное событие для сопоставления содержимого буфера с (например, целевой объект прорисовки может измениться со временем).</span><span class="sxs-lookup"><span data-stu-id="5aced-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="5aced-109">*текстурефилептр* </span><span class="sxs-lookup"><span data-stu-id="5aced-109">*textureFileptr* </span></span>  
<span data-ttu-id="5aced-110">Адрес указанного объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="5aced-110">The address of the specified texture object.</span></span>

<span data-ttu-id="5aced-111">*тилесубресаурце* </span><span class="sxs-lookup"><span data-stu-id="5aced-111">*tileSubresource* </span></span>  
<span data-ttu-id="5aced-112">Указанный подресурс плитки.</span><span class="sxs-lookup"><span data-stu-id="5aced-112">The specified subresource of the tile.</span></span>

<span data-ttu-id="5aced-113">*тилекс* </span><span class="sxs-lookup"><span data-stu-id="5aced-113">*tileX* </span></span>  
<span data-ttu-id="5aced-114">Указанная Координата X плитки.</span><span class="sxs-lookup"><span data-stu-id="5aced-114">The specified tile X position.</span></span>

<span data-ttu-id="5aced-115">*Плитка* </span><span class="sxs-lookup"><span data-stu-id="5aced-115">*tileY* </span></span>  
<span data-ttu-id="5aced-116">Указанная координата плитки Y.</span><span class="sxs-lookup"><span data-stu-id="5aced-116">The specified tile Y position.</span></span>

<span data-ttu-id="5aced-117">*тилез* </span><span class="sxs-lookup"><span data-stu-id="5aced-117">*tileZ* </span></span>  
<span data-ttu-id="5aced-118">Заданная Координата на плитке Z.</span><span class="sxs-lookup"><span data-stu-id="5aced-118">The specified tile Z position.</span></span>

<span data-ttu-id="5aced-119">*ддсфиленаме* </span><span class="sxs-lookup"><span data-stu-id="5aced-119">*ddsFilename* </span></span>  
<span data-ttu-id="5aced-120">Строка COM, содержащая путь к DDS-файлу, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="5aced-120">A COM string that contains the pathname of the .dds file where results are written.</span></span>

<span data-ttu-id="5aced-121">*прекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="5aced-121">*pRequestCallback* </span></span>  
<span data-ttu-id="5aced-122">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="5aced-122">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="5aced-123">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="5aced-123">*requestCookie* </span></span>  
<span data-ttu-id="5aced-124">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="5aced-124">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="5aced-125">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="5aced-125">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="5aced-126">Не используется.</span><span class="sxs-lookup"><span data-stu-id="5aced-126">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="5aced-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5aced-127">Return value</span></span>

<span data-ttu-id="5aced-128">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5aced-128">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5aced-129">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5aced-129">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aced-130">Требования</span><span class="sxs-lookup"><span data-stu-id="5aced-130">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5aced-131">Header</span><span class="sxs-lookup"><span data-stu-id="5aced-131">Header</span></span></p></td><td><span data-ttu-id="5aced-132">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="5aced-132">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5aced-133"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="5aced-133"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5aced-134">**итилерекуест**</span><span class="sxs-lookup"><span data-stu-id="5aced-134">**ITileRequest**</span></span>](/windows/desktop/direct3dtools/itilerequest)

 

 

---
description: Запросы на получение необработанного содержимого плитки.
MS-HAID: vspixengine.ITileRequest_RequestBufferTileAsync_EventID_DWORD_BSTR_UINT_IBufferObjectDataCallback_ptr_DWORD_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Итилерекуест:: Рекуестбуффертилеасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2D68766F-1BED-439E-AC51-790471DA4F70
api_name:
- ITileRequest.RequestBufferTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 83f013b4bc3235ece2850c75324333e4b59d298f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262474"
---
# <a name="span-idvspixengineitilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dwordspanitilerequestrequestbuffertileasync-method"></a><span data-ttu-id="afde2-103"><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>Метод Итилерекуест:: Рекуестбуффертилеасинк</span><span class="sxs-lookup"><span data-stu-id="afde2-103"><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>ITileRequest::RequestBufferTileAsync method</span></span>

<span data-ttu-id="afde2-104">Запросы на получение необработанного содержимого плитки.</span><span class="sxs-lookup"><span data-stu-id="afde2-104">Requests to get the raw contents of a tile.</span></span>

## <a name="syntax"></a><span data-ttu-id="afde2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afde2-105">Syntax</span></span>


```C++
HRESULT RequestBufferTileAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   UINT                        tileIndex,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="afde2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="afde2-106">Parameters</span></span>

<span data-ttu-id="afde2-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="afde2-107">*eventID* </span></span>  
<span data-ttu-id="afde2-108">Указанное событие для сопоставления содержимого плитки с (например, целевой объект прорисовки может измениться со временем).</span><span class="sxs-lookup"><span data-stu-id="afde2-108">The specified event to match the tile's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="afde2-109">*рекуестеддатауид* </span><span class="sxs-lookup"><span data-stu-id="afde2-109">*RequestedDataUID* </span></span>  
<span data-ttu-id="afde2-110">Адрес указанной плитки.</span><span class="sxs-lookup"><span data-stu-id="afde2-110">The address of the specified tile.</span></span>

<span data-ttu-id="afde2-111">*File* </span><span class="sxs-lookup"><span data-stu-id="afde2-111">*File* </span></span>  
<span data-ttu-id="afde2-112">Строка COM, содержащая путь к файлу, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="afde2-112">A COM string that contains the pathname of the file where results are written.</span></span>

<span data-ttu-id="afde2-113">*тилеиндекс* </span><span class="sxs-lookup"><span data-stu-id="afde2-113">*tileIndex* </span></span>  
<span data-ttu-id="afde2-114">Индекс указанной плитки.</span><span class="sxs-lookup"><span data-stu-id="afde2-114">The index of the specified tile.</span></span>

<span data-ttu-id="afde2-115">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="afde2-115">*requestCallback* </span></span>  
<span data-ttu-id="afde2-116">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="afde2-116">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="afde2-117">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="afde2-117">*requestCookie* </span></span>  
<span data-ttu-id="afde2-118">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="afde2-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="afde2-119">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="afde2-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="afde2-120">Не используется.</span><span class="sxs-lookup"><span data-stu-id="afde2-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="afde2-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="afde2-121">Return value</span></span>

<span data-ttu-id="afde2-122">Если этот метод завершается с ошибкой, возвращается **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="afde2-122">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="afde2-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="afde2-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="afde2-124">Требования</span><span class="sxs-lookup"><span data-stu-id="afde2-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="afde2-125">Header</span><span class="sxs-lookup"><span data-stu-id="afde2-125">Header</span></span></p></td><td><span data-ttu-id="afde2-126">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="afde2-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="afde2-127"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="afde2-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="afde2-128">**итилерекуест**</span><span class="sxs-lookup"><span data-stu-id="afde2-128">**ITileRequest**</span></span>](/windows/desktop/direct3dtools/itilerequest)

 

 

---
description: Запросы на получение содержимого текстуры в виде. Файл DDS (поверхность DirectDraw).
MS-HAID: vspixengine.ITextureRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Итекстуререкуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 89A9F230-D296-43CD-A2A6-747057750EED
api_name:
- ITextureRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5abfee1b26fd2145aef8e01239cc0b874ee54e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495678"
---
# <a name="span-idvspixengineitexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dwordspanitexturerequestrequestasync-method"></a><span data-ttu-id="7cb11-103"><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>Метод Итекстуререкуест:: Рекуестасинк</span><span class="sxs-lookup"><span data-stu-id="7cb11-103"><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>ITextureRequest::RequestAsync method</span></span>

<span data-ttu-id="7cb11-104">Запросы на получение содержимого текстуры в виде. Файл DDS (поверхность DirectDraw).</span><span class="sxs-lookup"><span data-stu-id="7cb11-104">Requests to get the contents of a texture as a .DDS (DirectDraw Surface) file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cb11-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cb11-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="7cb11-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cb11-106">Parameters</span></span>

<span data-ttu-id="7cb11-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="7cb11-107">*eventID* </span></span>  
<span data-ttu-id="7cb11-108">Указанное событие для сопоставления содержимого буфера с (например, целевой объект прорисовки может измениться со временем).</span><span class="sxs-lookup"><span data-stu-id="7cb11-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="7cb11-109">*текстурефилептр* </span><span class="sxs-lookup"><span data-stu-id="7cb11-109">*textureFileptr* </span></span>  
<span data-ttu-id="7cb11-110">Адрес объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="7cb11-110">The address of the texture object.</span></span>

<span data-ttu-id="7cb11-111">*ддсфиленаме* </span><span class="sxs-lookup"><span data-stu-id="7cb11-111">*ddsFilename* </span></span>  
<span data-ttu-id="7cb11-112">Строка COM, содержащая путь к DDS-файлу, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="7cb11-112">A COM string that contains the pathname of the .dds file where results are written.</span></span>

<span data-ttu-id="7cb11-113">*прекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="7cb11-113">*pRequestCallback* </span></span>  
<span data-ttu-id="7cb11-114">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="7cb11-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="7cb11-115">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="7cb11-115">*requestCookie* </span></span>  
<span data-ttu-id="7cb11-116">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="7cb11-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="7cb11-117">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="7cb11-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="7cb11-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7cb11-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="7cb11-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cb11-119">Return value</span></span>

<span data-ttu-id="7cb11-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7cb11-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7cb11-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7cb11-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cb11-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7cb11-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7cb11-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7cb11-123">Header</span></span></p></td><td><span data-ttu-id="7cb11-124">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="7cb11-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="7cb11-125"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="7cb11-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="7cb11-126">**итекстуререкуест**</span><span class="sxs-lookup"><span data-stu-id="7cb11-126">**ITextureRequest**</span></span>](/windows/desktop/direct3dtools/itexturerequest)

 

 

---
description: Асинхронный запрос на получение списка кадров, захваченных в журнале графики.
MS-HAID: vspixengine.IFrameListRequest\_RequestAsync\_IFrameListCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ифрамелистрекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 309C28F2-CE01-49E7-9A21-5053E3ED7721
api_name:
- IFrameListRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3627fc5ef3a425ae7607009b4ad382080ea99192
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072177"
---
# <a name="span-idvspixengineiframelistrequest_requestasync_iframelistcallback_ptr_dword_dwordspaniframelistrequestrequestasync-method"></a><span data-ttu-id="cb029-103"><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>Метод Ифрамелистрекуест:: Рекуестасинк</span><span class="sxs-lookup"><span data-stu-id="cb029-103"><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>IFrameListRequest::RequestAsync method</span></span>

<span data-ttu-id="cb029-104">Асинхронный запрос на получение списка кадров, захваченных в журнале графики.</span><span class="sxs-lookup"><span data-stu-id="cb029-104">An asynchronous request to get the list frames captured in the graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb029-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb029-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   IFrameListCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="cb029-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb029-106">Parameters</span></span>

<span data-ttu-id="cb029-107">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="cb029-107">*requestCallback* </span></span>  
<span data-ttu-id="cb029-108">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="cb029-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="cb029-109">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="cb029-109">*requestCookie* </span></span>  
<span data-ttu-id="cb029-110">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="cb029-110">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="cb029-111">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="cb029-111">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="cb029-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="cb029-112">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb029-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb029-113">Return value</span></span>

<span data-ttu-id="cb029-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="cb029-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cb029-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cb029-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb029-116">Требования</span><span class="sxs-lookup"><span data-stu-id="cb029-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="cb029-117">Header</span><span class="sxs-lookup"><span data-stu-id="cb029-117">Header</span></span></p></td><td><span data-ttu-id="cb029-118">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="cb029-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="cb029-119"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="cb029-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="cb029-120">**ифрамелистрекуест**</span><span class="sxs-lookup"><span data-stu-id="cb029-120">**IFrameListRequest**</span></span>](/windows/desktop/direct3dtools/iframelistrequest)

 

 

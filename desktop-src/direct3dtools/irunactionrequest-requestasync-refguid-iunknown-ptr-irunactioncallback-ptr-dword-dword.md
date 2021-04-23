---
description: Асинхронный запрос на инициацию действия (например, запись кадра) в подсистеме.
MS-HAID: vspixengine.IRunActionRequest\_RequestAsync\_REFGUID\_IUnknown\_ptr\_IRunActionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ирунактионрекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4A4DF4BE-383D-4B36-9195-61720C3B4D97
api_name:
- IRunActionRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 179abf44231d122ca82527fc5739b876395c327b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140559"
---
# <a name="span-idvspixengineirunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dwordspanirunactionrequestrequestasync-method"></a><span data-ttu-id="0b498-103"><span id="vspixengine.irunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dword"></span>Метод Ирунактионрекуест:: Рекуестасинк</span><span class="sxs-lookup"><span data-stu-id="0b498-103"><span id="vspixengine.irunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dword"></span>IRunActionRequest::RequestAsync method</span></span>

<span data-ttu-id="0b498-104">Асинхронный запрос на инициацию действия (например, запись кадра) в подсистеме.</span><span class="sxs-lookup"><span data-stu-id="0b498-104">An asynchronous request to initiate an action (for example, capture a frame) in the engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b498-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b498-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   REFGUID              action,
   IUnknown *           actionPayload,
   IRunActionCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="0b498-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b498-106">Parameters</span></span>

<span data-ttu-id="0b498-107">*поддержки* </span><span class="sxs-lookup"><span data-stu-id="0b498-107">*action* </span></span>  
<span data-ttu-id="0b498-108">Указанное действие.</span><span class="sxs-lookup"><span data-stu-id="0b498-108">The specified action.</span></span>

<span data-ttu-id="0b498-109">*актионпайлоад* </span><span class="sxs-lookup"><span data-stu-id="0b498-109">*actionPayload* </span></span>  
<span data-ttu-id="0b498-110">Полезная нагрузка указанного действия.</span><span class="sxs-lookup"><span data-stu-id="0b498-110">The payload of the specified action.</span></span>

<span data-ttu-id="0b498-111">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="0b498-111">*requestCallback* </span></span>  
<span data-ttu-id="0b498-112">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="0b498-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="0b498-113">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="0b498-113">*requestCookie* </span></span>  
<span data-ttu-id="0b498-114">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="0b498-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="0b498-115">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="0b498-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="0b498-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="0b498-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b498-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b498-117">Return value</span></span>

<span data-ttu-id="0b498-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0b498-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0b498-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0b498-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b498-120">Требования</span><span class="sxs-lookup"><span data-stu-id="0b498-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0b498-121">Header</span><span class="sxs-lookup"><span data-stu-id="0b498-121">Header</span></span></p></td><td><span data-ttu-id="0b498-122">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="0b498-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="0b498-123"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="0b498-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="0b498-124">**ирунактионрекуест**</span><span class="sxs-lookup"><span data-stu-id="0b498-124">**IRunActionRequest**</span></span>](/windows/desktop/direct3dtools/irunactionrequest)

 

 

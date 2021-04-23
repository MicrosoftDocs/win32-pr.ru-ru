---
description: Асинхронный запрос для получения адреса RVA стека вызовов (относительных виртуальных адресов) указанного события.
MS-HAID: vspixengine.ICallStackRequest\_RequestAsync\_EventID\_ICallStackCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Икаллстаккрекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1951716F-5382-41EE-90BB-A9053DB38A78
api_name:
- ICallStackRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cad4007a8bc3d0e7b7c9cf1efc7218ce09813a5a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262402"
---
# <a name="span-idvspixengineicallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dwordspanicallstackrequestrequestasync-method"></a><span data-ttu-id="4b252-103"><span id="vspixengine.icallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dword"></span>Метод Икаллстаккрекуест:: Рекуестасинк</span><span class="sxs-lookup"><span data-stu-id="4b252-103"><span id="vspixengine.icallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dword"></span>ICallStackRequest::RequestAsync method</span></span>

<span data-ttu-id="4b252-104">Асинхронный запрос для получения адреса RVA стека вызовов (относительных виртуальных адресов) указанного события.</span><span class="sxs-lookup"><span data-stu-id="4b252-104">An asynchronous request to get the call stack RVAs (relative virtual addresses) of the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b252-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b252-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID              eventID,
   ICallStackCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="4b252-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b252-106">Parameters</span></span>

<span data-ttu-id="4b252-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="4b252-107">*eventID* </span></span>  
<span data-ttu-id="4b252-108">Указанное событие.</span><span class="sxs-lookup"><span data-stu-id="4b252-108">The specified event.</span></span>

<span data-ttu-id="4b252-109">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="4b252-109">*requestCallback* </span></span>  
<span data-ttu-id="4b252-110">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="4b252-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="4b252-111">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="4b252-111">*requestCookie* </span></span>  
<span data-ttu-id="4b252-112">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="4b252-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="4b252-113">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="4b252-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="4b252-114">Не используется.</span><span class="sxs-lookup"><span data-stu-id="4b252-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b252-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b252-115">Return value</span></span>

<span data-ttu-id="4b252-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4b252-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4b252-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4b252-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b252-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4b252-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4b252-119">Header</span><span class="sxs-lookup"><span data-stu-id="4b252-119">Header</span></span></p></td><td><span data-ttu-id="4b252-120">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="4b252-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4b252-121"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="4b252-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4b252-122">**икаллстаккрекуест**</span><span class="sxs-lookup"><span data-stu-id="4b252-122">**ICallStackRequest**</span></span>](/windows/desktop/direct3dtools/icallstackrequest)

 

 

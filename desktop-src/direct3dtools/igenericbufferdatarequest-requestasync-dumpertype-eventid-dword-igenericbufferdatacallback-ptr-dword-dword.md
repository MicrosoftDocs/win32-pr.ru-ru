---
description: Запросы, возвращающие общие данные объекта, описывающие объект в vsglog файле для указанного события и в указанном формате.
MS-HAID: vspixengine.IGenericBufferDataRequest\_RequestAsync\_DumperType\_EventID\_DWORD\_IGenericBufferDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иженерикбуффердатарекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 542E20F9-B91D-4A05-AEE8-9DD2E80B76DB
api_name:
- IGenericBufferDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6d8860b2de7c3dce5c6f8b61467bfe147530ed76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710670"
---
# <a name="span-idvspixengineigenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dwordspanigenericbufferdatarequestrequestasync-method"></a><span data-ttu-id="9ae17-103"><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>Метод Иженерикбуффердатарекуест:: Рекуестасинк</span><span class="sxs-lookup"><span data-stu-id="9ae17-103"><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>IGenericBufferDataRequest::RequestAsync method</span></span>

<span data-ttu-id="9ae17-104">Запросы, возвращающие общие данные объекта, описывающие объект в vsglog файле для указанного события и в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="9ae17-104">Requests to return generic object data that describes an object in the .vsglog file for the specified event and in the specified format.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae17-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ae17-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DumperType                   dumperType,
   EventID                      eventID,
   DWORD                        RequestedDataUID,
   IGenericBufferDataCallback * requestCallback,
   DWORD                        requestCookie,
   DWORD                        progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="9ae17-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ae17-106">Parameters</span></span>

<span data-ttu-id="9ae17-107">*думпертипе* </span><span class="sxs-lookup"><span data-stu-id="9ae17-107">*dumperType* </span></span>  
<span data-ttu-id="9ae17-108">Заданный формат текстового представления объекта (HTML, XML и т. д.)</span><span class="sxs-lookup"><span data-stu-id="9ae17-108">The specified format of the textual representation of the object (HTML, XML, etc.)</span></span>

<span data-ttu-id="9ae17-109">*1008* </span><span class="sxs-lookup"><span data-stu-id="9ae17-109">*eventID* </span></span>  
<span data-ttu-id="9ae17-110">Указанное событие для сопоставления содержимого буфера с (например, целевой объект прорисовки может измениться со временем).</span><span class="sxs-lookup"><span data-stu-id="9ae17-110">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="9ae17-111">*рекуестеддатауид* </span><span class="sxs-lookup"><span data-stu-id="9ae17-111">*RequestedDataUID* </span></span>  
<span data-ttu-id="9ae17-112">Адрес указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="9ae17-112">The address of the specified object.</span></span>

<span data-ttu-id="9ae17-113">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="9ae17-113">*requestCallback* </span></span>  
<span data-ttu-id="9ae17-114">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="9ae17-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="9ae17-115">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="9ae17-115">*requestCookie* </span></span>  
<span data-ttu-id="9ae17-116">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="9ae17-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="9ae17-117">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="9ae17-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="9ae17-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="9ae17-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ae17-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ae17-119">Return value</span></span>

<span data-ttu-id="9ae17-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9ae17-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ae17-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ae17-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ae17-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9ae17-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9ae17-123">Header</span><span class="sxs-lookup"><span data-stu-id="9ae17-123">Header</span></span></p></td><td><span data-ttu-id="9ae17-124">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="9ae17-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9ae17-125"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="9ae17-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9ae17-126">**иженерикбуффердатарекуест**</span><span class="sxs-lookup"><span data-stu-id="9ae17-126">**IGenericBufferDataRequest**</span></span>](/windows/desktop/direct3dtools/igenericbufferdatarequest)

 

 

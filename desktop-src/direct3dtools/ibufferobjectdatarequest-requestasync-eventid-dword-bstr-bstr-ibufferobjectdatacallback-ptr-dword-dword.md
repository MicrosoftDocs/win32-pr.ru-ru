---
description: Запросы на получение необработанного содержимого объекта (буфер, текстура, представление целевого объекта прорисовки и т. д.).
MS-HAID: vspixengine.IBufferObjectDataRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_BSTR\_IBufferObjectDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ибуфферобжектдатарекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 899954DC-6196-4F79-AFB4-5E692DAA03EC
api_name:
- IBufferObjectDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 97d35f656f373f2f0040d49a78a2c0d376bc4266
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139766"
---
# <a name="span-idvspixengineibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dwordspanibufferobjectdatarequestrequestasync-method"></a><span data-ttu-id="71ffd-103"><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>Метод Ибуфферобжектдатарекуест:: Рекуестасинк</span><span class="sxs-lookup"><span data-stu-id="71ffd-103"><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>IBufferObjectDataRequest::RequestAsync method</span></span>

<span data-ttu-id="71ffd-104">Запросы на получение необработанного содержимого объекта (буфер, текстура, представление целевого объекта прорисовки и т. д.)</span><span class="sxs-lookup"><span data-stu-id="71ffd-104">Requests to get the raw contents of an object (buffer, texture, render target view, etc.)</span></span>

## <a name="syntax"></a><span data-ttu-id="71ffd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71ffd-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   BSTR                        Format,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="71ffd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="71ffd-106">Parameters</span></span>

<span data-ttu-id="71ffd-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="71ffd-107">*eventID* </span></span>  
<span data-ttu-id="71ffd-108">Указанное событие для сопоставления содержимого буфера с (например, целевой объект прорисовки может измениться со временем).</span><span class="sxs-lookup"><span data-stu-id="71ffd-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="71ffd-109">*рекуестеддатауид* </span><span class="sxs-lookup"><span data-stu-id="71ffd-109">*RequestedDataUID* </span></span>  
<span data-ttu-id="71ffd-110">Адрес указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="71ffd-110">The address of the specified object.</span></span>

<span data-ttu-id="71ffd-111">*File* </span><span class="sxs-lookup"><span data-stu-id="71ffd-111">*File* </span></span>  
<span data-ttu-id="71ffd-112">Строка COM, содержащая путь к файлу, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="71ffd-112">A COM string that contains the pathname of the file where results are written.</span></span>

<span data-ttu-id="71ffd-113">*Формат* </span><span class="sxs-lookup"><span data-stu-id="71ffd-113">*Format* </span></span>  
<span data-ttu-id="71ffd-114">В настоящий момент не используется.</span><span class="sxs-lookup"><span data-stu-id="71ffd-114">Not currently used.</span></span> <span data-ttu-id="71ffd-115">Строка COM, указывающая формат вывода.</span><span class="sxs-lookup"><span data-stu-id="71ffd-115">A COM string that specifies the output format.</span></span>

<span data-ttu-id="71ffd-116">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="71ffd-116">*requestCallback* </span></span>  
<span data-ttu-id="71ffd-117">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="71ffd-117">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="71ffd-118">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="71ffd-118">*requestCookie* </span></span>  
<span data-ttu-id="71ffd-119">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="71ffd-119">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="71ffd-120">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="71ffd-120">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="71ffd-121">Не используется.</span><span class="sxs-lookup"><span data-stu-id="71ffd-121">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="71ffd-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71ffd-122">Return value</span></span>

<span data-ttu-id="71ffd-123">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="71ffd-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="71ffd-124">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71ffd-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="71ffd-125">Требования</span><span class="sxs-lookup"><span data-stu-id="71ffd-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="71ffd-126">Header</span><span class="sxs-lookup"><span data-stu-id="71ffd-126">Header</span></span></p></td><td><span data-ttu-id="71ffd-127">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="71ffd-127">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="71ffd-128"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="71ffd-128"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="71ffd-129">**ибуфферобжектдатарекуест**</span><span class="sxs-lookup"><span data-stu-id="71ffd-129">**IBufferObjectDataRequest**</span></span>](/windows/desktop/direct3dtools/ibufferobjectdatarequest)

 

 

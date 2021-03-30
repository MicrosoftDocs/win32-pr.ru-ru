---
description: Запрашивает получение указанных сведений из таблицы объектов для указанного события.
MS-HAID: vspixengine.IObjectTableRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IObjectTableCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иобжекттаблерекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: EE40F584-CDDE-465D-B4CB-A98B917DD0EE
api_name:
- IObjectTableRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2c9108708475b27a7a1882051c7f0177e14470f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806196"
---
# <a name="span-idvspixengineiobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dwordspaniobjecttablerequestrequestasync-method"></a><span data-ttu-id="80afa-103"><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>Метод Иобжекттаблерекуест:: Рекуестасинк</span><span class="sxs-lookup"><span data-stu-id="80afa-103"><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>IObjectTableRequest::RequestAsync method</span></span>

<span data-ttu-id="80afa-104">Запрашивает получение указанных сведений из таблицы объектов для указанного события.</span><span class="sxs-lookup"><span data-stu-id="80afa-104">Requests to get specified information from the object table for the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="80afa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80afa-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  eventID,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IObjectTableCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="80afa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80afa-106">Parameters</span></span>

<span data-ttu-id="80afa-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="80afa-107">*eventID* </span></span>  
<span data-ttu-id="80afa-108">Указанное событие.</span><span class="sxs-lookup"><span data-stu-id="80afa-108">The specified event.</span></span>

<span data-ttu-id="80afa-109">*нумколумнс* </span><span class="sxs-lookup"><span data-stu-id="80afa-109">*numColumns* </span></span>  
<span data-ttu-id="80afa-110">Число столбцов (полей) получаемой информации.</span><span class="sxs-lookup"><span data-stu-id="80afa-110">The number of columns (fields) of information to get.</span></span>

<span data-ttu-id="80afa-111">*count1 \_ столбцы* </span><span class="sxs-lookup"><span data-stu-id="80afa-111">*count1\_columns* </span></span>  
<span data-ttu-id="80afa-112">Указанные столбцы (поля).</span><span class="sxs-lookup"><span data-stu-id="80afa-112">The specified columns (fields).</span></span>

<span data-ttu-id="80afa-113">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="80afa-113">*requestCallback* </span></span>  
<span data-ttu-id="80afa-114">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="80afa-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="80afa-115">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="80afa-115">*requestCookie* </span></span>  
<span data-ttu-id="80afa-116">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="80afa-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="80afa-117">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="80afa-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="80afa-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="80afa-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="80afa-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80afa-119">Return value</span></span>

<span data-ttu-id="80afa-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="80afa-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="80afa-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80afa-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="80afa-122">Требования</span><span class="sxs-lookup"><span data-stu-id="80afa-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="80afa-123">Header</span><span class="sxs-lookup"><span data-stu-id="80afa-123">Header</span></span></p></td><td><span data-ttu-id="80afa-124">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="80afa-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="80afa-125"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="80afa-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="80afa-126">**иобжекттаблерекуест**</span><span class="sxs-lookup"><span data-stu-id="80afa-126">**IObjectTableRequest**</span></span>](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 

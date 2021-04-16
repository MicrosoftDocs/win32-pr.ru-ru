---
description: Запросы на получение сведений о столбцах (полях), поддерживаемых типом запроса этой таблицы объектов.
MS-HAID: vspixengine.IObjectTableRequest\_RequestSupportedColumnsAsync\_IObjectTableCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иобжекттаблерекуест:: Рекуестсуппортедколумнсасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0931C81A-65D5-493E-9F54-C7E98FA2FA6F
api_name:
- IObjectTableRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6773a69061e7a17d2271e1a53f89f6f2def1a6c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538213"
---
# <a name="span-idvspixengineiobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dwordspaniobjecttablerequestrequestsupportedcolumnsasync-method"></a><span data-ttu-id="324d2-103"><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>Метод Иобжекттаблерекуест:: Рекуестсуппортедколумнсасинк</span><span class="sxs-lookup"><span data-stu-id="324d2-103"><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>IObjectTableRequest::RequestSupportedColumnsAsync method</span></span>

<span data-ttu-id="324d2-104">Запросы на получение сведений о столбцах (полях), поддерживаемых типом запроса этой таблицы объектов.</span><span class="sxs-lookup"><span data-stu-id="324d2-104">Requests to get information about what columns (fields) this object table request type supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="324d2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="324d2-105">Syntax</span></span>


```C++
HRESULT RequestSupportedColumnsAsync(
   IObjectTableCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="324d2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="324d2-106">Parameters</span></span>

<span data-ttu-id="324d2-107">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="324d2-107">*requestCallback* </span></span>  
<span data-ttu-id="324d2-108">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="324d2-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="324d2-109">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="324d2-109">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="324d2-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="324d2-110">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="324d2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="324d2-111">Return value</span></span>

<span data-ttu-id="324d2-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="324d2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="324d2-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="324d2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="324d2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="324d2-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="324d2-115">Header</span><span class="sxs-lookup"><span data-stu-id="324d2-115">Header</span></span></p></td><td><span data-ttu-id="324d2-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="324d2-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="324d2-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="324d2-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="324d2-118">**иобжекттаблерекуест**</span><span class="sxs-lookup"><span data-stu-id="324d2-118">**IObjectTableRequest**</span></span>](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 

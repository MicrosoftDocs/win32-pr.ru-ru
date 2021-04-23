---
description: Асинхронно передает ресурсы в механизм, например строки для сообщений об ошибках.
MS-HAID: vspixengine.IPixEngine7\_InitEngineAsync\_ResourcePair\_arr\_UINT\_IVersionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine7:: Инитенгинеасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10138B39-88D2-4586-BD51-C618722EFFA0
api_name:
- IPixEngine7.InitEngineAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 21d98a207b0194f281abc2800cd63f9be7de5073
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495726"
---
# <a name="span-idvspixengineipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dwordspanipixengine7initengineasync-method"></a><span data-ttu-id="66a80-103"><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>Метод IPixEngine7:: Инитенгинеасинк</span><span class="sxs-lookup"><span data-stu-id="66a80-103"><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>IPixEngine7::InitEngineAsync method</span></span>

<span data-ttu-id="66a80-104">Асинхронно передает ресурсы в механизм, например строки для сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="66a80-104">Asynchronously passes resources to the engine, such as strings for error messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="66a80-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66a80-105">Syntax</span></span>


```C++
HRESULT InitEngineAsync(
   ResourcePair []   count1_resources,
   UINT              count,
   IVersionCallback* versionCallback,
   DWORD             requestCookie,
   DWORD             progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="66a80-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="66a80-106">Parameters</span></span>

<span data-ttu-id="66a80-107">*\_ресурсы count1* </span><span class="sxs-lookup"><span data-stu-id="66a80-107">*count1\_resources* </span></span>  
<span data-ttu-id="66a80-108">Массив ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66a80-108">An array of resources.</span></span>

<span data-ttu-id="66a80-109">*расчета* </span><span class="sxs-lookup"><span data-stu-id="66a80-109">*count* </span></span>  
<span data-ttu-id="66a80-110">Число ресурсов в count1 \_ Resources</span><span class="sxs-lookup"><span data-stu-id="66a80-110">The number of resources in count1\_resources</span></span>

<span data-ttu-id="66a80-111">*версионкаллбакк* </span><span class="sxs-lookup"><span data-stu-id="66a80-111">*versionCallback* </span></span>  
<span data-ttu-id="66a80-112">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="66a80-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="66a80-113">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="66a80-113">*requestCookie* </span></span>  
<span data-ttu-id="66a80-114">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="66a80-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="66a80-115">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="66a80-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="66a80-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="66a80-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="66a80-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66a80-117">Return value</span></span>

<span data-ttu-id="66a80-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="66a80-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="66a80-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="66a80-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="66a80-120">Требования</span><span class="sxs-lookup"><span data-stu-id="66a80-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="66a80-121">Header</span><span class="sxs-lookup"><span data-stu-id="66a80-121">Header</span></span></p></td><td><span data-ttu-id="66a80-122">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="66a80-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="66a80-123"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="66a80-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="66a80-124">**IPixEngine7**</span><span class="sxs-lookup"><span data-stu-id="66a80-124">**IPixEngine7**</span></span>](/windows/desktop/direct3dtools/ipixengine7)

 

 

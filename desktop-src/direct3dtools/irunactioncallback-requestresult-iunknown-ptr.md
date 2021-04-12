---
description: Функция обратного вызова, используемая для уведомления узла о результатах действия (например, записать кадр), который он запрашивал.
MS-HAID: vspixengine.IRunActionCallback\_RequestResult\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ирунактионкаллбакк:: RequestResult'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5D6B1599-2CF4-46E7-92DB-5D93DD5AD0EE
api_name:
- IRunActionCallback.RequestResult
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8f2d5eea98b167af30bfe0412acb10f83f83d3db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140562"
---
# <a name="span-idvspixengineirunactioncallback_requestresult_iunknown_ptrspanirunactioncallbackrequestresult-method"></a><span data-ttu-id="e829a-103"><span id="vspixengine.irunactioncallback_requestresult_iunknown_ptr"></span>Метод Ирунактионкаллбакк:: RequestResult</span><span class="sxs-lookup"><span data-stu-id="e829a-103"><span id="vspixengine.irunactioncallback_requestresult_iunknown_ptr"></span>IRunActionCallback::RequestResult method</span></span>

<span data-ttu-id="e829a-104">Функция обратного вызова, используемая для уведомления узла о результатах действия (например, записать кадр), который он запрашивал.</span><span class="sxs-lookup"><span data-stu-id="e829a-104">A callback function used to notify the host of results from an action (for example, capture a frame) that it requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="e829a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e829a-105">Syntax</span></span>


```C++
HRESULT RequestResult(
   IUnknown * actionResult
);
```

## <a name="parameters"></a><span data-ttu-id="e829a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e829a-106">Parameters</span></span>

<span data-ttu-id="e829a-107">*actionResult* </span><span class="sxs-lookup"><span data-stu-id="e829a-107">*actionResult* </span></span>  
<span data-ttu-id="e829a-108">Результат действия.</span><span class="sxs-lookup"><span data-stu-id="e829a-108">The result of the action.</span></span>

## <a name="return-value"></a><span data-ttu-id="e829a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e829a-109">Return value</span></span>

<span data-ttu-id="e829a-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e829a-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e829a-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e829a-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e829a-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e829a-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e829a-113">Header</span><span class="sxs-lookup"><span data-stu-id="e829a-113">Header</span></span></p></td><td><span data-ttu-id="e829a-114">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="e829a-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e829a-115"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="e829a-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e829a-116">**ирунактионкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="e829a-116">**IRunActionCallback**</span></span>](/windows/desktop/direct3dtools/irunactioncallback)

 

 

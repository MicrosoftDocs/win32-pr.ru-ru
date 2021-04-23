---
description: Обратный вызов, уведомляющий узел об отмене запроса.
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCallback\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иневфрамескаллбакк:: Канцелусингкаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 291B2F85-1437-4704-8971-4B7C25B693F8
api_name:
- INewFramesCallback.CancelUsingCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 863219cd37078fbde1e7ef8b2da7677a31e12872
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495744"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcallback_iunknown_ptrspaninewframescallbackcancelusingcallback-method"></a><span data-ttu-id="f8530-103"><span id="vspixengine.inewframescallback_cancelusingcallback_iunknown_ptr"></span>Метод Иневфрамескаллбакк:: Канцелусингкаллбакк</span><span class="sxs-lookup"><span data-stu-id="f8530-103"><span id="vspixengine.inewframescallback_cancelusingcallback_iunknown_ptr"></span>INewFramesCallback::CancelUsingCallback method</span></span>

<span data-ttu-id="f8530-104">Обратный вызов, уведомляющий узел об отмене запроса.</span><span class="sxs-lookup"><span data-stu-id="f8530-104">A callback that notifies the host of a canceled request.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8530-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8530-105">Syntax</span></span>


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="f8530-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8530-106">Parameters</span></span>

<span data-ttu-id="f8530-107">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="f8530-107">*requestCallback* </span></span>  
<span data-ttu-id="f8530-108">Адрес отмененного запроса.</span><span class="sxs-lookup"><span data-stu-id="f8530-108">The address of the cancelled request.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8530-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8530-109">Return value</span></span>

<span data-ttu-id="f8530-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f8530-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f8530-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8530-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8530-112">Требования</span><span class="sxs-lookup"><span data-stu-id="f8530-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f8530-113">Header</span><span class="sxs-lookup"><span data-stu-id="f8530-113">Header</span></span></p></td><td><span data-ttu-id="f8530-114">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="f8530-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f8530-115"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="f8530-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f8530-116">**иневфрамескаллбакк**</span><span class="sxs-lookup"><span data-stu-id="f8530-116">**INewFramesCallback**</span></span>](/windows/desktop/direct3dtools/inewframescallback)

 

 

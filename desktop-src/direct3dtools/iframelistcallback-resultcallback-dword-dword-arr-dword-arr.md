---
description: Функция обратного вызова, используемая для уведомления узла о том, какие кадры были захвачены.
MS-HAID: vspixengine.IFrameListCallback\_ResultCallback\_DWORD\_DWORD\_arr\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ифрамелисткаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AEB340C6-74AA-4F8B-86D0-9C0366ECDE70
api_name:
- IFrameListCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 00a991ec2d380d9c052f02ed69bb71d233fd0d93
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495750"
---
# <a name="span-idvspixengineiframelistcallback_resultcallback_dword_dword_arr_dword_arrspaniframelistcallbackresultcallback-method"></a><span data-ttu-id="330ab-103"><span id="vspixengine.iframelistcallback_resultcallback_dword_dword_arr_dword_arr"></span>Метод Ифрамелисткаллбакк:: Ресулткаллбакк</span><span class="sxs-lookup"><span data-stu-id="330ab-103"><span id="vspixengine.iframelistcallback_resultcallback_dword_dword_arr_dword_arr"></span>IFrameListCallback::ResultCallback method</span></span>

<span data-ttu-id="330ab-104">Функция обратного вызова, используемая для уведомления узла о том, какие кадры были захвачены.</span><span class="sxs-lookup"><span data-stu-id="330ab-104">A callback function used to notify the host of which frames were captured.</span></span>

## <a name="syntax"></a><span data-ttu-id="330ab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="330ab-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD    numFrames,
   DWORD [] count0_frameNumbers,
   DWORD [] count0_frameEventIDs
);
```

## <a name="parameters"></a><span data-ttu-id="330ab-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="330ab-106">Parameters</span></span>

<span data-ttu-id="330ab-107">*нумфрамес* </span><span class="sxs-lookup"><span data-stu-id="330ab-107">*numFrames* </span></span>  
<span data-ttu-id="330ab-108">Число захваченных кадров.</span><span class="sxs-lookup"><span data-stu-id="330ab-108">The number of frames captured.</span></span>

<span data-ttu-id="330ab-109">*count0 \_ фраменумберс* </span><span class="sxs-lookup"><span data-stu-id="330ab-109">*count0\_frameNumbers* </span></span>  
<span data-ttu-id="330ab-110">Номера кадров захваченных кадров.</span><span class="sxs-lookup"><span data-stu-id="330ab-110">The frame numbers of the captured frames.</span></span>

<span data-ttu-id="330ab-111">*count0 \_ фрамивентидс* </span><span class="sxs-lookup"><span data-stu-id="330ab-111">*count0\_frameEventIDs* </span></span>  
<span data-ttu-id="330ab-112">Завершающее событие, связанное с каждым кадром.</span><span class="sxs-lookup"><span data-stu-id="330ab-112">The final event associated with each frame.</span></span>

## <a name="return-value"></a><span data-ttu-id="330ab-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="330ab-113">Return value</span></span>

<span data-ttu-id="330ab-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="330ab-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="330ab-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="330ab-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="330ab-116">Требования</span><span class="sxs-lookup"><span data-stu-id="330ab-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="330ab-117">Header</span><span class="sxs-lookup"><span data-stu-id="330ab-117">Header</span></span></p></td><td><span data-ttu-id="330ab-118">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="330ab-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="330ab-119"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="330ab-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="330ab-120">**ифрамелисткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="330ab-120">**IFrameListCallback**</span></span>](/windows/desktop/direct3dtools/iframelistcallback)

 

 

---
description: Функция обратного вызова, используемая для уведомления узла о стеке вызовов.
MS-HAID: vspixengine.ICallStackCallback\_ResultCallback\_DWORD\_CallStackFrame\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Икаллстакккаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9C083298-6FD5-4414-8E0C-625F6A144668
api_name:
- ICallStackCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4bd77ea22fd31b31081d72707b1fd7a2efbda607
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894750"
---
# <a name="span-idvspixengineicallstackcallback_resultcallback_dword_callstackframe_arrspanicallstackcallbackresultcallback-method"></a><span data-ttu-id="b5d9a-103"><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>Метод Икаллстакккаллбакк:: Ресулткаллбакк</span><span class="sxs-lookup"><span data-stu-id="b5d9a-103"><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>ICallStackCallback::ResultCallback method</span></span>

<span data-ttu-id="b5d9a-104">Функция обратного вызова, используемая для уведомления узла о стеке вызовов.</span><span class="sxs-lookup"><span data-stu-id="b5d9a-104">A callback function used to notify the host of call stack information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d9a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5d9a-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD             count,
   CallStackFrame [] count0_callStackFrameBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="b5d9a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5d9a-106">Parameters</span></span>

<span data-ttu-id="b5d9a-107">*расчета* </span><span class="sxs-lookup"><span data-stu-id="b5d9a-107">*count* </span></span>  
<span data-ttu-id="b5d9a-108">Число возвращенных фрамебуфферс вызовов стека.</span><span class="sxs-lookup"><span data-stu-id="b5d9a-108">The number of callstack framebuffers returned.</span></span>

<span data-ttu-id="b5d9a-109">*count0 \_ каллстаккфрамебуффер* </span><span class="sxs-lookup"><span data-stu-id="b5d9a-109">*count0\_callStackFrameBuffer* </span></span>  
<span data-ttu-id="b5d9a-110">Сведения о стеке вызовов.</span><span class="sxs-lookup"><span data-stu-id="b5d9a-110">The callstack information.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5d9a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5d9a-111">Return value</span></span>

<span data-ttu-id="b5d9a-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b5d9a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b5d9a-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b5d9a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5d9a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b5d9a-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b5d9a-115">Header</span><span class="sxs-lookup"><span data-stu-id="b5d9a-115">Header</span></span></p></td><td><span data-ttu-id="b5d9a-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="b5d9a-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b5d9a-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="b5d9a-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b5d9a-118">**икаллстакккаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b5d9a-118">**ICallStackCallback**</span></span>](/windows/desktop/direct3dtools/icallstackcallback)

 

 

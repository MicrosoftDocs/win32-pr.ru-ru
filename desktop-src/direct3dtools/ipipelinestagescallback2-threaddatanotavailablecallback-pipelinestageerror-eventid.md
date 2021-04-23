---
description: Обратный вызов, уведомляющий узел о том, что Среаддата недоступен для определенного этапа и события конвейера.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataNotAvailableCallback\_PipeLineStageError\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPipeLineStagesCallback2:: Среаддатанотаваилаблекаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 231DC830-5F1A-4DDA-B5D0-C7FBCEDCB2A0
api_name:
- IPipeLineStagesCallback2.ThreadDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a0c9cc0bc32b6d01394be1403e961d7ae37a1d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673094"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventidspanipipelinestagescallback2threaddatanotavailablecallback-method"></a><span data-ttu-id="ee7b9-103"><span id="vspixengine.ipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventid"></span>Метод IPipeLineStagesCallback2:: Среаддатанотаваилаблекаллбакк</span><span class="sxs-lookup"><span data-stu-id="ee7b9-103"><span id="vspixengine.ipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventid"></span>IPipeLineStagesCallback2::ThreadDataNotAvailableCallback method</span></span>

<span data-ttu-id="ee7b9-104">Обратный вызов, уведомляющий узел о том, что Среаддата недоступен для определенного этапа и события конвейера.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-104">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee7b9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee7b9-105">Syntax</span></span>


```C++
HRESULT ThreadDataNotAvailableCallback(
   PipeLineStageError error,
   EventID            eid
);
```

## <a name="parameters"></a><span data-ttu-id="ee7b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee7b9-106">Parameters</span></span>

<span data-ttu-id="ee7b9-107">*план* </span><span class="sxs-lookup"><span data-stu-id="ee7b9-107">*error* </span></span>  
<span data-ttu-id="ee7b9-108">Ошибка этапа конвейера.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-108">The pipeline stage error.</span></span>

<span data-ttu-id="ee7b9-109">*Аль* </span><span class="sxs-lookup"><span data-stu-id="ee7b9-109">*eid* </span></span>  
<span data-ttu-id="ee7b9-110">Событие, представленное в результатах.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-110">The event represented in the results.</span></span>

## <a name="return-value"></a><span data-ttu-id="ee7b9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee7b9-111">Return value</span></span>

<span data-ttu-id="ee7b9-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ee7b9-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ee7b9-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee7b9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ee7b9-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ee7b9-115">Header</span><span class="sxs-lookup"><span data-stu-id="ee7b9-115">Header</span></span></p></td><td><span data-ttu-id="ee7b9-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="ee7b9-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ee7b9-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="ee7b9-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ee7b9-118">**IPipeLineStagesCallback2**</span><span class="sxs-lookup"><span data-stu-id="ee7b9-118">**IPipeLineStagesCallback2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 

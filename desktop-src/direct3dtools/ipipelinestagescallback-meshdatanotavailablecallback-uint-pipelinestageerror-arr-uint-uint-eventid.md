---
description: Обратный вызов, уведомляющий узел о том, какие этапы конвейера не могут вернуть данные сетки для события, указанного в связанном запросе.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataNotAvailableCallback\_UINT\_PipeLineStageError\_arr\_UINT\_UINT\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипипелинестажескаллбакк:: Мешдатанотаваилаблекаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A51E7C45-C1F0-4576-8638-9C3B185385BA
api_name:
- IPipeLineStagesCallback.MeshDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 42391c342e2f11b39d1535b5286a92e161d0fd9b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495690"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span data-ttu-id="c1679-103"><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>Метод Ипипелинестажескаллбакк:: Мешдатанотаваилаблекаллбакк</span><span class="sxs-lookup"><span data-stu-id="c1679-103"><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>IPipeLineStagesCallback::MeshDataNotAvailableCallback method</span></span>

<span data-ttu-id="c1679-104">Обратный вызов, уведомляющий узел о том, какие этапы конвейера не могут вернуть данные сетки для события, указанного в связанном запросе.</span><span class="sxs-lookup"><span data-stu-id="c1679-104">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1679-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1679-105">Syntax</span></span>


```C++
HRESULT MeshDataNotAvailableCallback(
   UINT                  numberStages,
   PipeLineStageError [] count0_errors,
   UINT                  width,
   UINT                  height,
   EventID               eid
);
```

## <a name="parameters"></a><span data-ttu-id="c1679-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1679-106">Parameters</span></span>

<span data-ttu-id="c1679-107">*нумберстажес* </span><span class="sxs-lookup"><span data-stu-id="c1679-107">*numberStages* </span></span>  
<span data-ttu-id="c1679-108">Число возвращенных ошибок этапа.</span><span class="sxs-lookup"><span data-stu-id="c1679-108">The number of stage errors returned.</span></span>

<span data-ttu-id="c1679-109">*\_ошибки count0* </span><span class="sxs-lookup"><span data-stu-id="c1679-109">*count0\_errors* </span></span>  
<span data-ttu-id="c1679-110">Ошибки этапа конвейера.</span><span class="sxs-lookup"><span data-stu-id="c1679-110">The pipeline stage errors.</span></span>

<span data-ttu-id="c1679-111">*Ширина* </span><span class="sxs-lookup"><span data-stu-id="c1679-111">*width* </span></span>  
<span data-ttu-id="c1679-112">Ширина цепочки подкачки, связана с вызовом Draw.</span><span class="sxs-lookup"><span data-stu-id="c1679-112">The width of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="c1679-113">Используется при запросе изображений предварительного просмотра конвейера.</span><span class="sxs-lookup"><span data-stu-id="c1679-113">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="c1679-114">*равно* </span><span class="sxs-lookup"><span data-stu-id="c1679-114">*height* </span></span>  
<span data-ttu-id="c1679-115">Высота цепочки подкачки, связана с вызовом Draw.</span><span class="sxs-lookup"><span data-stu-id="c1679-115">The height of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="c1679-116">Используется при запросе изображений предварительного просмотра конвейера.</span><span class="sxs-lookup"><span data-stu-id="c1679-116">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="c1679-117">*Аль* </span><span class="sxs-lookup"><span data-stu-id="c1679-117">*eid* </span></span>  
<span data-ttu-id="c1679-118">Событие, представленное в результатах.</span><span class="sxs-lookup"><span data-stu-id="c1679-118">The event represented in the results.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1679-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1679-119">Return value</span></span>

<span data-ttu-id="c1679-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c1679-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c1679-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c1679-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1679-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c1679-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c1679-123">Header</span><span class="sxs-lookup"><span data-stu-id="c1679-123">Header</span></span></p></td><td><span data-ttu-id="c1679-124">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="c1679-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c1679-125"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="c1679-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c1679-126">**ипипелинестажескаллбакк**</span><span class="sxs-lookup"><span data-stu-id="c1679-126">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 

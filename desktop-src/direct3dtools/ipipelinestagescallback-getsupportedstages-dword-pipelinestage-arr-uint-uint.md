---
description: Обратный вызов, уведомляющий узел о том, какие этапы конвейера используются вызовом Draw запроса связана.
MS-HAID: vspixengine.IPipeLineStagesCallback\_GetSupportedStages\_DWORD\_PipeLineStage\_arr\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипипелинестажескаллбакк:: Жетсуппортедстажес'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7046A41-5C9C-42FE-B1E2-879A47CE08E3
api_name:
- IPipeLineStagesCallback.GetSupportedStages
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c55c7f8bfa6b5b69ea2a46dd6023021a6b4ab6c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537004"
---
# <a name="span-idvspixengineipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uintspanipipelinestagescallbackgetsupportedstages-method"></a><span data-ttu-id="18c8b-103"><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>Метод Ипипелинестажескаллбакк:: Жетсуппортедстажес</span><span class="sxs-lookup"><span data-stu-id="18c8b-103"><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>IPipeLineStagesCallback::GetSupportedStages method</span></span>

<span data-ttu-id="18c8b-104">Обратный вызов, уведомляющий узел о том, какие этапы конвейера используются вызовом Draw запроса связана.</span><span class="sxs-lookup"><span data-stu-id="18c8b-104">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="18c8b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18c8b-105">Syntax</span></span>


```C++
HRESULT GetSupportedStages(
   DWORD            numColumns,
   PipeLineStage [] count0_pStages,
   UINT             swapChainWidth,
   UINT             swapChainHeight
);
```

## <a name="parameters"></a><span data-ttu-id="18c8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="18c8b-106">Parameters</span></span>

<span data-ttu-id="18c8b-107">*нумколумнс* </span><span class="sxs-lookup"><span data-stu-id="18c8b-107">*numColumns* </span></span>  
<span data-ttu-id="18c8b-108">Число возвращенных стадий.</span><span class="sxs-lookup"><span data-stu-id="18c8b-108">The number of stages returned.</span></span>

<span data-ttu-id="18c8b-109">*count0 \_ пстажес* </span><span class="sxs-lookup"><span data-stu-id="18c8b-109">*count0\_pStages* </span></span>  
<span data-ttu-id="18c8b-110">Этапы конвейера.</span><span class="sxs-lookup"><span data-stu-id="18c8b-110">The pipeline stages.</span></span>

<span data-ttu-id="18c8b-111">*свапчаинвидс* </span><span class="sxs-lookup"><span data-stu-id="18c8b-111">*swapChainWidth* </span></span>  
<span data-ttu-id="18c8b-112">Ширина цепочки подкачки, связана с вызовом Draw.</span><span class="sxs-lookup"><span data-stu-id="18c8b-112">The width of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="18c8b-113">Используется при запросе изображений предварительного просмотра конвейера.</span><span class="sxs-lookup"><span data-stu-id="18c8b-113">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="18c8b-114">*свапчаинхеигхт* </span><span class="sxs-lookup"><span data-stu-id="18c8b-114">*swapChainHeight* </span></span>  
<span data-ttu-id="18c8b-115">Высота цепочки подкачки, связана с вызовом Draw.</span><span class="sxs-lookup"><span data-stu-id="18c8b-115">The height of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="18c8b-116">Используется при запросе изображений предварительного просмотра конвейера.</span><span class="sxs-lookup"><span data-stu-id="18c8b-116">This is used when requesting pipeline preview images.</span></span>

## <a name="return-value"></a><span data-ttu-id="18c8b-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18c8b-117">Return value</span></span>

<span data-ttu-id="18c8b-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="18c8b-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="18c8b-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18c8b-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="18c8b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="18c8b-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="18c8b-121">Header</span><span class="sxs-lookup"><span data-stu-id="18c8b-121">Header</span></span></p></td><td><span data-ttu-id="18c8b-122">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="18c8b-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="18c8b-123"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="18c8b-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="18c8b-124">**ипипелинестажескаллбакк**</span><span class="sxs-lookup"><span data-stu-id="18c8b-124">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 

---
description: Обратный вызов, уведомляющий узел о результатах запроса журнала пикселей.
MS-HAID: vspixengine.IPixelHistoryCallback\_ResultCallback\_DWORD\_PixelHistoryOperation\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипикселхисторикаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1F7D0EA5-402A-49C4-A83E-91596AE9536B
api_name:
- IPixelHistoryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c43947148e2eb8139f3ad46157f19b1621a6c91e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341975"
---
# <a name="span-idvspixengineipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arrspanipixelhistorycallbackresultcallback-method"></a><span data-ttu-id="042e9-103"><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>Метод Ипикселхисторикаллбакк:: Ресулткаллбакк</span><span class="sxs-lookup"><span data-stu-id="042e9-103"><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback::ResultCallback method</span></span>

<span data-ttu-id="042e9-104">Обратный вызов, уведомляющий узел о результатах запроса журнала пикселей.</span><span class="sxs-lookup"><span data-stu-id="042e9-104">A callback that notifies the host of pixel history request results.</span></span>

## <a name="syntax"></a><span data-ttu-id="042e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="042e9-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD                    count,
   PixelHistoryOperation [] count0_pixelHistoryOperation
);
```

## <a name="parameters"></a><span data-ttu-id="042e9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="042e9-106">Parameters</span></span>

<span data-ttu-id="042e9-107">*расчета* </span><span class="sxs-lookup"><span data-stu-id="042e9-107">*count* </span></span>  
<span data-ttu-id="042e9-108">Число результатов.</span><span class="sxs-lookup"><span data-stu-id="042e9-108">The number of results.</span></span>

<span data-ttu-id="042e9-109">*count0 \_ пикселхисторйоператион* </span><span class="sxs-lookup"><span data-stu-id="042e9-109">*count0\_pixelHistoryOperation* </span></span>  
<span data-ttu-id="042e9-110">Результаты.</span><span class="sxs-lookup"><span data-stu-id="042e9-110">The results.</span></span>

## <a name="return-value"></a><span data-ttu-id="042e9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="042e9-111">Return value</span></span>

<span data-ttu-id="042e9-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="042e9-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="042e9-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="042e9-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="042e9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="042e9-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="042e9-115">Header</span><span class="sxs-lookup"><span data-stu-id="042e9-115">Header</span></span></p></td><td><span data-ttu-id="042e9-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="042e9-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="042e9-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="042e9-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="042e9-118">**ипикселхисторикаллбакк**</span><span class="sxs-lookup"><span data-stu-id="042e9-118">**IPixelHistoryCallback**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback)

 

 

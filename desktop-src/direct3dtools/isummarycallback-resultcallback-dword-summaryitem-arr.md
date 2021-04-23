---
description: Функция обратного вызова, используемая для уведомления узла о сводных данных журнала графики.
MS-HAID: vspixengine.ISummaryCallback\_ResultCallback\_DWORD\_SummaryItem\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Исуммарикаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07569D26-45A6-41A5-868D-8038BAB9079B
api_name:
- ISummaryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c4ea46550628ec9701ab6b0e6bb3af9ab71a2499
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710651"
---
# <a name="span-idvspixengineisummarycallback_resultcallback_dword_summaryitem_arrspanisummarycallbackresultcallback-method"></a><span data-ttu-id="3907f-103"><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>Метод Исуммарикаллбакк:: Ресулткаллбакк</span><span class="sxs-lookup"><span data-stu-id="3907f-103"><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>ISummaryCallback::ResultCallback method</span></span>

<span data-ttu-id="3907f-104">Функция обратного вызова, используемая для уведомления узла о сводных данных журнала графики.</span><span class="sxs-lookup"><span data-stu-id="3907f-104">A callback function used to notify the host of graphics log summary information.</span></span>

## <a name="syntax"></a><span data-ttu-id="3907f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3907f-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD          count,
   SummaryItem [] count0_summaryItem
);
```

## <a name="parameters"></a><span data-ttu-id="3907f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3907f-106">Parameters</span></span>

<span data-ttu-id="3907f-107">*расчета* </span><span class="sxs-lookup"><span data-stu-id="3907f-107">*count* </span></span>  
<span data-ttu-id="3907f-108">Число возвращаемых элементов сводных данных.</span><span class="sxs-lookup"><span data-stu-id="3907f-108">The number of summary information items returned.</span></span>

<span data-ttu-id="3907f-109">*count0 \_ суммаритем* </span><span class="sxs-lookup"><span data-stu-id="3907f-109">*count0\_summaryItem* </span></span>  
<span data-ttu-id="3907f-110">Элементы сводных данных (пары «ключ-значение»).</span><span class="sxs-lookup"><span data-stu-id="3907f-110">The summary information items (key-value pairs).</span></span>

## <a name="return-value"></a><span data-ttu-id="3907f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3907f-111">Return value</span></span>

<span data-ttu-id="3907f-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3907f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3907f-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3907f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3907f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3907f-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3907f-115">Header</span><span class="sxs-lookup"><span data-stu-id="3907f-115">Header</span></span></p></td><td><span data-ttu-id="3907f-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="3907f-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3907f-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="3907f-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3907f-118">**исуммарикаллбакк**</span><span class="sxs-lookup"><span data-stu-id="3907f-118">**ISummaryCallback**</span></span>](/windows/desktop/direct3dtools/isummarycallback)

 

 

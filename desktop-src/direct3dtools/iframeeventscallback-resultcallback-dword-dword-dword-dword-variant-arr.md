---
description: Функция обратного вызова, используемая для уведомления узла о событиях в списке событий.
MS-HAID: vspixengine.IFrameEventsCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ифрамивентскаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5AB67A11-00C1-47AF-8C8C-8B2FDD095BCF
api_name:
- IFrameEventsCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e746c54f2a82adb5042cd479e4ca04299c1b7402
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262398"
---
# <a name="span-idvspixengineiframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arrspaniframeeventscallbackresultcallback-method"></a><span data-ttu-id="c01d4-103"><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>Метод Ифрамивентскаллбакк:: Ресулткаллбакк</span><span class="sxs-lookup"><span data-stu-id="c01d4-103"><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>IFrameEventsCallback::ResultCallback method</span></span>

<span data-ttu-id="c01d4-104">Функция обратного вызова, используемая для уведомления узла о событиях в списке событий.</span><span class="sxs-lookup"><span data-stu-id="c01d4-104">A callback function used to notify the host of information about events in the event list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c01d4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c01d4-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD      frameNumber,
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count1_pRowData
);
```

## <a name="parameters"></a><span data-ttu-id="c01d4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c01d4-106">Parameters</span></span>

<span data-ttu-id="c01d4-107">*фраменумбер* </span><span class="sxs-lookup"><span data-stu-id="c01d4-107">*frameNumber* </span></span>  
<span data-ttu-id="c01d4-108">Номер кадра, связанный с событиями.</span><span class="sxs-lookup"><span data-stu-id="c01d4-108">The frame number associated with the events.</span></span>

<span data-ttu-id="c01d4-109">*нумелементс* </span><span class="sxs-lookup"><span data-stu-id="c01d4-109">*numElements* </span></span>  
<span data-ttu-id="c01d4-110">Общее число полей во всех столбцах всех событий.</span><span class="sxs-lookup"><span data-stu-id="c01d4-110">The total number of fields in all columns of all events.</span></span>

<span data-ttu-id="c01d4-111">*нумровс* </span><span class="sxs-lookup"><span data-stu-id="c01d4-111">*numRows* </span></span>  
<span data-ttu-id="c01d4-112">Число событий в результате.</span><span class="sxs-lookup"><span data-stu-id="c01d4-112">The number of events in the result.</span></span>

<span data-ttu-id="c01d4-113">*нумколумнс* </span><span class="sxs-lookup"><span data-stu-id="c01d4-113">*numColumns* </span></span>  
<span data-ttu-id="c01d4-114">Число столбцов (полей) в каждой строке.</span><span class="sxs-lookup"><span data-stu-id="c01d4-114">The number of columns (fields) in each row.</span></span>

<span data-ttu-id="c01d4-115">*count1 \_ провдата* </span><span class="sxs-lookup"><span data-stu-id="c01d4-115">*count1\_pRowData* </span></span>  
<span data-ttu-id="c01d4-116">Сведения о событиях; один элемент для каждого поля каждого события.</span><span class="sxs-lookup"><span data-stu-id="c01d4-116">Information about the events; one item for each field of each event.</span></span>

## <a name="return-value"></a><span data-ttu-id="c01d4-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c01d4-117">Return value</span></span>

<span data-ttu-id="c01d4-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c01d4-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c01d4-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c01d4-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c01d4-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c01d4-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c01d4-121">Header</span><span class="sxs-lookup"><span data-stu-id="c01d4-121">Header</span></span></p></td><td><span data-ttu-id="c01d4-122">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="c01d4-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c01d4-123"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="c01d4-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c01d4-124">**ифрамивентскаллбакк**</span><span class="sxs-lookup"><span data-stu-id="c01d4-124">**IFrameEventsCallback**</span></span>](/windows/desktop/direct3dtools/iframeeventscallback)

 

 

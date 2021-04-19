---
description: Обратный вызов, уведомляющий узел о том, что сведения о операции примитива журнала пикселей возвращены связанным запросом.
MS-HAID: vspixengine.IPixelHistoryCallback2\_PrimitivesCallback\_DWORD\_PixelHistoryOperation\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryCallback2: метод:P Римитивескаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2A67EC3B-72F2-4347-AD23-961CDE0D456F
api_name:
- IPixelHistoryCallback2.PrimitivesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8512bde1acd96ebbe132eeb91872d04ce043b44f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537922"
---
# <a name="span-idvspixengineipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arrspanipixelhistorycallback2primitivescallback-method"></a><span data-ttu-id="3a7b7-103"><span id="vspixengine.ipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback2: метод:P Римитивескаллбакк</span><span class="sxs-lookup"><span data-stu-id="3a7b7-103"><span id="vspixengine.ipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback2::PrimitivesCallback method</span></span>

<span data-ttu-id="3a7b7-104">Обратный вызов, уведомляющий узел о том, что сведения о операции примитива журнала пикселей возвращены связанным запросом.</span><span class="sxs-lookup"><span data-stu-id="3a7b7-104">A callback that notifies the host of pixel history primitive operation information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a7b7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a7b7-105">Syntax</span></span>


```C++
HRESULT PrimitivesCallback(
   DWORD                    count,
   PixelHistoryOperation [] count0_primitives
);
```

## <a name="parameters"></a><span data-ttu-id="3a7b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a7b7-106">Parameters</span></span>

<span data-ttu-id="3a7b7-107">*расчета* </span><span class="sxs-lookup"><span data-stu-id="3a7b7-107">*count* </span></span>  
<span data-ttu-id="3a7b7-108">Число примитивов.</span><span class="sxs-lookup"><span data-stu-id="3a7b7-108">The number of primitives.</span></span>

<span data-ttu-id="3a7b7-109">*\_примитивы count0* </span><span class="sxs-lookup"><span data-stu-id="3a7b7-109">*count0\_primitives* </span></span>  
<span data-ttu-id="3a7b7-110">Примитивы.</span><span class="sxs-lookup"><span data-stu-id="3a7b7-110">The primitives.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a7b7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a7b7-111">Return value</span></span>

<span data-ttu-id="3a7b7-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3a7b7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3a7b7-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3a7b7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a7b7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3a7b7-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3a7b7-115">Header</span><span class="sxs-lookup"><span data-stu-id="3a7b7-115">Header</span></span></p></td><td><span data-ttu-id="3a7b7-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="3a7b7-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3a7b7-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="3a7b7-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3a7b7-118">**IPixelHistoryCallback2**</span><span class="sxs-lookup"><span data-stu-id="3a7b7-118">**IPixelHistoryCallback2**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback2)

 

 

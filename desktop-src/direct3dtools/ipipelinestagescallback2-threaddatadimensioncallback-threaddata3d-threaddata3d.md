---
description: Обратный вызов, уведомляющий узел о количестве потоков и групп шейдера вычислений в связанном запросе.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataDimensionCallback\_ThreadData3D\_ThreadData3D
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPipeLineStagesCallback2:: Среаддатадименсионкаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E8765C14-0A55-468D-BCA8-3E28E5476DFB
api_name:
- IPipeLineStagesCallback2.ThreadDataDimensionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93a8ee64c863128513563f3ce50dd2bfcdd77714
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423089"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3dspanipipelinestagescallback2threaddatadimensioncallback-method"></a><span data-ttu-id="76f6d-103"><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>Метод IPipeLineStagesCallback2:: Среаддатадименсионкаллбакк</span><span class="sxs-lookup"><span data-stu-id="76f6d-103"><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>IPipeLineStagesCallback2::ThreadDataDimensionCallback method</span></span>

<span data-ttu-id="76f6d-104">Обратный вызов, уведомляющий узел о количестве потоков и групп шейдера вычислений в связанном запросе.</span><span class="sxs-lookup"><span data-stu-id="76f6d-104">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="76f6d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76f6d-105">Syntax</span></span>


```C++
HRESULT ThreadDataDimensionCallback(
   ThreadData3D threadGroupCount,
   ThreadData3D threadGroupSize
);
```

## <a name="parameters"></a><span data-ttu-id="76f6d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="76f6d-106">Parameters</span></span>

<span data-ttu-id="76f6d-107">*среадграупкаунт* </span><span class="sxs-lookup"><span data-stu-id="76f6d-107">*threadGroupCount* </span></span>  
<span data-ttu-id="76f6d-108">Многомерное число групп потоков.</span><span class="sxs-lookup"><span data-stu-id="76f6d-108">The multi-dimensional count of thread groups.</span></span>

<span data-ttu-id="76f6d-109">*среадграупсизе* </span><span class="sxs-lookup"><span data-stu-id="76f6d-109">*threadGroupSize* </span></span>  
<span data-ttu-id="76f6d-110">Многомерный размер каждой группы потоков.</span><span class="sxs-lookup"><span data-stu-id="76f6d-110">The multi-dimensional size of each thread group.</span></span>

## <a name="return-value"></a><span data-ttu-id="76f6d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76f6d-111">Return value</span></span>

<span data-ttu-id="76f6d-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="76f6d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="76f6d-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="76f6d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="76f6d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="76f6d-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="76f6d-115">Header</span><span class="sxs-lookup"><span data-stu-id="76f6d-115">Header</span></span></p></td><td><span data-ttu-id="76f6d-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="76f6d-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="76f6d-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="76f6d-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="76f6d-118">**IPipeLineStagesCallback2**</span><span class="sxs-lookup"><span data-stu-id="76f6d-118">**IPipeLineStagesCallback2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 

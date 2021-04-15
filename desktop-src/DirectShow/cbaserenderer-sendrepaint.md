---
description: Метод Сендрепаинт отправляет событие перерисовки в Диспетчер графа фильтров.
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: Кбасерендерер. Сендрепаинт, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendRepaint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3a88f0c1dae54cb5d9be1e4e9ad3e9677bdd958
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668770"
---
# <a name="cbaserenderersendrepaint-method"></a><span data-ttu-id="1b7ff-103">Кбасерендерер. Сендрепаинт, метод</span><span class="sxs-lookup"><span data-stu-id="1b7ff-103">CBaseRenderer.SendRepaint method</span></span>

<span data-ttu-id="1b7ff-104">`SendRepaint`Метод отправляет событие перерисовки в Диспетчер графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="1b7ff-104">The `SendRepaint` method sends a repaint event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b7ff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b7ff-105">Syntax</span></span>


```C++
void SendRepaint();
```



## <a name="parameters"></a><span data-ttu-id="1b7ff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b7ff-106">Parameters</span></span>

<span data-ttu-id="1b7ff-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1b7ff-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1b7ff-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b7ff-108">Return value</span></span>

<span data-ttu-id="1b7ff-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1b7ff-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b7ff-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b7ff-110">Remarks</span></span>

<span data-ttu-id="1b7ff-111">Этот метод отправляет событие [**\_ перерисовки EC**](ec-repaint.md) в Диспетчер графа фильтров, если выполняются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="1b7ff-111">This method sends an [**EC\_REPAINT**](ec-repaint.md) event to the filter graph manager if the following conditions are true:</span></span>

-   <span data-ttu-id="1b7ff-112">Входной ПИН-код подключен.</span><span class="sxs-lookup"><span data-stu-id="1b7ff-112">The input pin is connected.</span></span>
-   <span data-ttu-id="1b7ff-113">Фильтр не очищает данные.</span><span class="sxs-lookup"><span data-stu-id="1b7ff-113">The filter is not flushing data.</span></span>
-   <span data-ttu-id="1b7ff-114">Конец потока не достигнут.</span><span class="sxs-lookup"><span data-stu-id="1b7ff-114">The end-of-stream was not reached.</span></span>
-   <span data-ttu-id="1b7ff-115">Флаг [**\_ баборт кбасерендерер:: m**](cbaserenderer-m-babort.md) имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1b7ff-115">The [**CBaseRenderer::m\_bAbort**](cbaserenderer-m-babort.md) flag is **FALSE**.</span></span>
-   <span data-ttu-id="1b7ff-116">Флаг [**\_ брепаинтстатус кбасерендерер:: m**](cbaserenderer-m-brepaintstatus.md) имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1b7ff-116">The [**CBaseRenderer::m\_bRepaintStatus**](cbaserenderer-m-brepaintstatus.md) flag is **TRUE**.</span></span>

<span data-ttu-id="1b7ff-117">В зависимости от состояния графа \_ событие ПЕРЕрисовки EC может вызвать повторную отправку примера в вышестоящем фильтре; граф фильтра для поиска в текущем расположении или диспетчер графа фильтров для приостановки на мгновение.</span><span class="sxs-lookup"><span data-stu-id="1b7ff-117">Depending on the state of the graph, the EC\_REPAINT event can cause the upstream filter to re-send a sample; the filter graph to seek to its current location; or the filter graph manager to pause momentarily.</span></span> <span data-ttu-id="1b7ff-118">(См. раздел [**\_ перерисовка EC**](ec-repaint.md).) Это событие потенциально неэффективно, поэтому его следует использовать с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="1b7ff-118">(See [**EC\_REPAINT**](ec-repaint.md).) This event is potentially inefficient, so it should be used sparingly.</span></span> <span data-ttu-id="1b7ff-119">Однако модули подготовки отчетов иногда нуждаются в обновлении экрана.</span><span class="sxs-lookup"><span data-stu-id="1b7ff-119">However, video renderers sometimes need to refresh the display.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b7ff-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1b7ff-120">Requirements</span></span>



| <span data-ttu-id="1b7ff-121">Требование</span><span class="sxs-lookup"><span data-stu-id="1b7ff-121">Requirement</span></span> | <span data-ttu-id="1b7ff-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1b7ff-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b7ff-123">Header</span><span class="sxs-lookup"><span data-stu-id="1b7ff-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1b7ff-124"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b7ff-124"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1b7ff-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1b7ff-125">Library</span></span><br/> | <dl> <span data-ttu-id="1b7ff-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1b7ff-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b7ff-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b7ff-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b7ff-128">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="1b7ff-128">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





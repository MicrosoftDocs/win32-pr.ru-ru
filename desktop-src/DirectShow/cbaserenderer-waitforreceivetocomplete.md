---
description: 'Метод Ваитфоррецеиветокомплете ожидает завершения метода Кбасерендерер:: Receive.'
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: Кбасерендерер. Ваитфоррецеиветокомплете, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForReceiveToComplete
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9033474c71d23fed106205839071bad200df6a23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665083"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a><span data-ttu-id="224b5-103">Кбасерендерер. Ваитфоррецеиветокомплете, метод</span><span class="sxs-lookup"><span data-stu-id="224b5-103">CBaseRenderer.WaitForReceiveToComplete method</span></span>

<span data-ttu-id="224b5-104">`WaitForReceiveToComplete`Метод ожидает завершения метода [**кбасерендерер:: Receive**](cbaserenderer-receive.md) .</span><span class="sxs-lookup"><span data-stu-id="224b5-104">The `WaitForReceiveToComplete` method waits for the [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method to complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="224b5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="224b5-105">Syntax</span></span>


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a><span data-ttu-id="224b5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="224b5-106">Parameters</span></span>

<span data-ttu-id="224b5-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="224b5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="224b5-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="224b5-108">Return value</span></span>

<span data-ttu-id="224b5-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="224b5-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="224b5-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="224b5-110">Remarks</span></span>

<span data-ttu-id="224b5-111">Методы [**кбасерендерер:: останавливают**](cbaserenderer-stop.md) и [**Кбасерендерер:: бегинфлуш**](cbaserenderer-beginflush.md) вызывают этот метод, чтобы синхронизировать изменение состояния с методом **Receive** .</span><span class="sxs-lookup"><span data-stu-id="224b5-111">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call this method to synchronize the state change with the **Receive** method.</span></span>

<span data-ttu-id="224b5-112">В частности, этот метод отправляет сообщения, пока он ожидает, пока флаг [**кбасерендерер:: m \_ бинрецеиве**](cbaserenderer-m-binreceive.md) не станет равным **false**.</span><span class="sxs-lookup"><span data-stu-id="224b5-112">Specifically, this method dispatches messages while it waits for the [**CBaseRenderer::m\_bInReceive**](cbaserenderer-m-binreceive.md) flag to become **FALSE**.</span></span> <span data-ttu-id="224b5-113">Флаг принимает **значение true** в методе [**Кбасерендерер::P репаререцеиве**](cbaserenderer-preparereceive.md) и возвращается в **значение false** после того, как метод **Receive** вызовет метод [**кбасерендерер::P репаререндер**](cbaserenderer-preparerender.md) .</span><span class="sxs-lookup"><span data-stu-id="224b5-113">The flag becomes **TRUE** in the [**CBaseRenderer::PrepareReceive**](cbaserenderer-preparereceive.md) method and switches back to **FALSE** after the **Receive** method calls the [**CBaseRenderer::PrepareRender**](cbaserenderer-preparerender.md) method.</span></span> <span data-ttu-id="224b5-114">Производный класс может использовать **препаререндер** для установки палитры.</span><span class="sxs-lookup"><span data-stu-id="224b5-114">The derived class can use **PrepareRender** to set the palette.</span></span> <span data-ttu-id="224b5-115">Ожидание завершения **препаререндер** гарантирует, что сообщения о смене палитры будут отправлены, прежде чем произойдет изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="224b5-115">Waiting for **PrepareRender** to complete ensures that palette-change messages are dispatched before the state change occurs.</span></span> <span data-ttu-id="224b5-116">Это позволяет избежать возможной взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="224b5-116">This avoids a potential deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="224b5-117">Требования</span><span class="sxs-lookup"><span data-stu-id="224b5-117">Requirements</span></span>



| <span data-ttu-id="224b5-118">Требование</span><span class="sxs-lookup"><span data-stu-id="224b5-118">Requirement</span></span> | <span data-ttu-id="224b5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="224b5-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="224b5-120">Header</span><span class="sxs-lookup"><span data-stu-id="224b5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="224b5-121"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="224b5-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="224b5-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="224b5-122">Library</span></span><br/> | <dl> <span data-ttu-id="224b5-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="224b5-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="224b5-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="224b5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="224b5-125">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="224b5-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





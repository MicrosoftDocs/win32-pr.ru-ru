---
description: Метод Саурцесреадканваит удерживает или освобождает поток потоковой передачи.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: Кбасерендерер. Саурцесреадканваит, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SourceThreadCanWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f01be304ec2b5f845ea61c9609808c6e2f39fca9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657991"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a><span data-ttu-id="e68c9-103">Кбасерендерер. Саурцесреадканваит, метод</span><span class="sxs-lookup"><span data-stu-id="e68c9-103">CBaseRenderer.SourceThreadCanWait method</span></span>

<span data-ttu-id="e68c9-104">`SourceThreadCanWait`Метод удерживает или освобождает поток потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="e68c9-104">The `SourceThreadCanWait` method holds or releases the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="e68c9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e68c9-105">Syntax</span></span>


```C++
virtual HRESULT SourceThreadCanWait(
   BOOL bCanWait
);
```



## <a name="parameters"></a><span data-ttu-id="e68c9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e68c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e68c9-107">*бканваит*</span><span class="sxs-lookup"><span data-stu-id="e68c9-107">*bCanWait*</span></span> 
</dt> <dd>

<span data-ttu-id="e68c9-108">Логическое значение, указывающее, следует ли хранить поток потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="e68c9-108">Boolean value indicating whether to hold the streaming thread.</span></span> <span data-ttu-id="e68c9-109">Если **значение равно true**, поток потоковой передачи блокируется, пока фильтр ожидает отображения следующих выборок.</span><span class="sxs-lookup"><span data-stu-id="e68c9-109">If **TRUE**, the streaming thread is blocked while the filter waits to render the next samples.</span></span> <span data-ttu-id="e68c9-110">Если **значение равно false**, поток потоковой передачи освобождается.</span><span class="sxs-lookup"><span data-stu-id="e68c9-110">If **FALSE**, the streaming thread is released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e68c9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e68c9-111">Return value</span></span>

<span data-ttu-id="e68c9-112">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e68c9-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e68c9-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e68c9-113">Remarks</span></span>

<span data-ttu-id="e68c9-114">Вызов `SourceThreadCanWait` метода со значением **false** приводит к тому, что фильтр возвращается из заблокированного вызова [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="e68c9-114">Calling the `SourceThreadCanWait` method with the value **FALSE** forces the filter to return from a blocked [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) call.</span></span> <span data-ttu-id="e68c9-115">Когда фильтр работает, он блокирует **Получение** вызовов до времени презентации в текущем примере.</span><span class="sxs-lookup"><span data-stu-id="e68c9-115">When the filter is running, it blocks **Receive** calls until the current sample's presentation time.</span></span> <span data-ttu-id="e68c9-116">Если фильтр приостановлен, он блокирует **Получение** вызовов на неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="e68c9-116">When the filter is paused, it blocks **Receive** calls indefinitely.</span></span> <span data-ttu-id="e68c9-117">Это поведение регулирует поток данных в потоке.</span><span class="sxs-lookup"><span data-stu-id="e68c9-117">This behavior regulates the flow of data in the stream.</span></span> <span data-ttu-id="e68c9-118">Однако если фильтр остановлен или сброшен, он не должен блокироваться.</span><span class="sxs-lookup"><span data-stu-id="e68c9-118">When the filter is stopped or flushing, however, it should not block.</span></span>

<span data-ttu-id="e68c9-119">Блокировка управляется методом [**кбасерендерер:: ваитфоррендертиме**](cbaserenderer-waitforrendertime.md) , который ожидает два события: [**кбасерендерер:: m \_ рендеревент**](cbaserenderer-m-renderevent.md) и [**кбасерендерер:: m \_ среадсигнал**](cbaserenderer-m-threadsignal.md).</span><span class="sxs-lookup"><span data-stu-id="e68c9-119">The blocking is controlled by the [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method, which waits on two events: [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) and [**CBaseRenderer::m\_ThreadSignal**](cbaserenderer-m-threadsignal.md).</span></span> <span data-ttu-id="e68c9-120">Событие **m \_ рендеревент** сигнализирует о получении времени презентации.</span><span class="sxs-lookup"><span data-stu-id="e68c9-120">The **m\_RenderEvent** event is signaled when the presentation time arrives.</span></span> <span data-ttu-id="e68c9-121">Событие **m \_ среадсигнал** сигнализирует, когда `SourceThreadCanWait` вызывается со значением **false**.</span><span class="sxs-lookup"><span data-stu-id="e68c9-121">The **m\_ThreadSignal** event is signaled when `SourceThreadCanWait` is called with the value **FALSE**.</span></span> <span data-ttu-id="e68c9-122">Вызов `SourceThreadCanWait` со значением **true** сбрасывает событие.</span><span class="sxs-lookup"><span data-stu-id="e68c9-122">Calling `SourceThreadCanWait` with the value **TRUE** resets the event.</span></span>

<span data-ttu-id="e68c9-123">Методы [**кбасерендерер:: останавливают**](cbaserenderer-stop.md) и [**Кбасерендерер:: бегинфлуш**](cbaserenderer-beginflush.md) вызывают `SourceThreadCanWait` со значением **false** (освобождая поток потоковой передачи).</span><span class="sxs-lookup"><span data-stu-id="e68c9-123">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call `SourceThreadCanWait` with the value **FALSE** (releasing the streaming thread).</span></span> <span data-ttu-id="e68c9-124">Методы [**кбасерендерер::P Аусе**](cbaserenderer-pause.md), [**Кбасерендерер:: Run**](cbaserenderer-run.md)и [**кбасерендерер:: ендфлуш**](cbaserenderer-endflush.md) вызывают `SourceThreadCanWait` значение **true**.</span><span class="sxs-lookup"><span data-stu-id="e68c9-124">The [**CBaseRenderer::Pause**](cbaserenderer-pause.md), [**CBaseRenderer::Run**](cbaserenderer-run.md), and [**CBaseRenderer::EndFlush**](cbaserenderer-endflush.md) methods call `SourceThreadCanWait` with the value **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e68c9-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e68c9-125">Requirements</span></span>



| <span data-ttu-id="e68c9-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e68c9-126">Requirement</span></span> | <span data-ttu-id="e68c9-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e68c9-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e68c9-128">Header</span><span class="sxs-lookup"><span data-stu-id="e68c9-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e68c9-129"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e68c9-129"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e68c9-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e68c9-130">Library</span></span><br/> | <dl> <span data-ttu-id="e68c9-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e68c9-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e68c9-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e68c9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e68c9-133">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="e68c9-133">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





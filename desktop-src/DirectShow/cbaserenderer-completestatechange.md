---
description: Метод Комплетестатечанже определяет, завершен ли переход в приостановленное состояние.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: Кбасерендерер. Комплетестатечанже, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteStateChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2465aeed3347f6ebc592dbe01bc3580a30983e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668743"
---
# <a name="cbaserenderercompletestatechange-method"></a><span data-ttu-id="44518-103">Кбасерендерер. Комплетестатечанже, метод</span><span class="sxs-lookup"><span data-stu-id="44518-103">CBaseRenderer.CompleteStateChange method</span></span>

<span data-ttu-id="44518-104">`CompleteStateChange`Метод определяет, завершен ли переход в приостановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="44518-104">The `CompleteStateChange` method determines whether a transition to the paused state is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="44518-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44518-105">Syntax</span></span>


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a><span data-ttu-id="44518-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="44518-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44518-107">*олдстате*</span><span class="sxs-lookup"><span data-stu-id="44518-107">*OldState*</span></span> 
</dt> <dd>

<span data-ttu-id="44518-108">Состояние до перехода.</span><span class="sxs-lookup"><span data-stu-id="44518-108">State prior to the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44518-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44518-109">Return value</span></span>

<span data-ttu-id="44518-110">Возвращает значение \_ ОК, если переход завершен.</span><span class="sxs-lookup"><span data-stu-id="44518-110">Returns S\_OK if the transition is complete.</span></span> <span data-ttu-id="44518-111">В противном случае возвращает \_ значение S false.</span><span class="sxs-lookup"><span data-stu-id="44518-111">Otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="44518-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44518-112">Remarks</span></span>

<span data-ttu-id="44518-113">Метод [**кбасерендерер::P Аусе**](cbaserenderer-pause.md) вызывает этот метод для обновления состояния перехода состояния.</span><span class="sxs-lookup"><span data-stu-id="44518-113">The [**CBaseRenderer::Pause**](cbaserenderer-pause.md) method calls this method to update the state-transition status.</span></span> <span data-ttu-id="44518-114">Как правило, переход на приостановку не завершается до тех пор, пока фильтр не получит пример.</span><span class="sxs-lookup"><span data-stu-id="44518-114">In general, the transition to paused does not finish until the filter receives a sample.</span></span> <span data-ttu-id="44518-115">Однако в некоторых ситуациях переход завершается немедленно: например, если фильтр не подключен или достигнут конец потока.</span><span class="sxs-lookup"><span data-stu-id="44518-115">However, in some situations the transition completes immediately: for example, if the filter is unconnected, or if the end of the stream was reached.</span></span> <span data-ttu-id="44518-116">Этот метод проверяет различные критерии, а затем вызывает метод [**кбасерендерер:: Ready**](cbaserenderer-ready.md) или метод [**Кбасерендерер:: NotReady**](cbaserenderer-notready.md) для обновления состояния перехода.</span><span class="sxs-lookup"><span data-stu-id="44518-116">This method checks the various criteria and then calls the [**CBaseRenderer::Ready**](cbaserenderer-ready.md) method or the [**CBaseRenderer::NotReady**](cbaserenderer-notready.md) method to update the transition status.</span></span>

## <a name="requirements"></a><span data-ttu-id="44518-117">Требования</span><span class="sxs-lookup"><span data-stu-id="44518-117">Requirements</span></span>



| <span data-ttu-id="44518-118">Требование</span><span class="sxs-lookup"><span data-stu-id="44518-118">Requirement</span></span> | <span data-ttu-id="44518-119">Значение</span><span class="sxs-lookup"><span data-stu-id="44518-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44518-120">Header</span><span class="sxs-lookup"><span data-stu-id="44518-120">Header</span></span><br/>  | <dl> <span data-ttu-id="44518-121"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44518-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="44518-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="44518-122">Library</span></span><br/> | <dl> <span data-ttu-id="44518-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="44518-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44518-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44518-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44518-125">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="44518-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





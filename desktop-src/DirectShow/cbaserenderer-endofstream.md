---
description: Метод EndOfStream уведомляет фильтр о том, что входной ПИН-код получил уведомление о завершении потока.
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: Кбасерендерер. EndOfStream, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e12da02ffbce99b29d324c1166b3d4cdf2265c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657476"
---
# <a name="cbaserendererendofstream-method"></a><span data-ttu-id="0bb64-103">Кбасерендерер. EndOfStream, метод</span><span class="sxs-lookup"><span data-stu-id="0bb64-103">CBaseRenderer.EndOfStream method</span></span>

<span data-ttu-id="0bb64-104">`EndOfStream`Метод уведомляет фильтр о том, что входной ПИН-код получил уведомление об окончании потока.</span><span class="sxs-lookup"><span data-stu-id="0bb64-104">The `EndOfStream` method notifies the filter that the input pin received an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb64-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bb64-105">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="0bb64-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bb64-106">Parameters</span></span>

<span data-ttu-id="0bb64-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0bb64-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0bb64-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0bb64-108">Return value</span></span>

<span data-ttu-id="0bb64-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0bb64-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bb64-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0bb64-110">Remarks</span></span>

<span data-ttu-id="0bb64-111">Входной ПИН-код фильтра вызывает этот метод при получении уведомления о завершении потока.</span><span class="sxs-lookup"><span data-stu-id="0bb64-111">The filter's input pin calls this method when it receives an end-of-stream notification.</span></span>

<span data-ttu-id="0bb64-112">Этот метод задает для флага [**кбасерендерер:: m \_ Беос**](cbaserenderer-m-beos.md) **значение true** и вызывает метод [**кбасерендерер:: сендендофстреам**](cbaserenderer-sendendofstream.md) , чтобы запланировать событие [**\_ завершения EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="0bb64-112">This method sets the [**CBaseRenderer::m\_bEOS**](cbaserenderer-m-beos.md) flag to **TRUE** and calls the [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) method to schedule an [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="0bb64-113">Если фильтр приостановлен и ожидает выборка, этот метод завершает переход состояния.</span><span class="sxs-lookup"><span data-stu-id="0bb64-113">If the filter is paused and waiting for a sample, this method completes the state transition.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb64-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0bb64-114">Requirements</span></span>



| <span data-ttu-id="0bb64-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0bb64-115">Requirement</span></span> | <span data-ttu-id="0bb64-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0bb64-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb64-117">Header</span><span class="sxs-lookup"><span data-stu-id="0bb64-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0bb64-118"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0bb64-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0bb64-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0bb64-119">Library</span></span><br/> | <dl> <span data-ttu-id="0bb64-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0bb64-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bb64-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0bb64-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bb64-122">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="0bb64-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





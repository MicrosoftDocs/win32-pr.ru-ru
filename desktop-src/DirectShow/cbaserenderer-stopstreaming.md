---
description: Метод Стопстреаминг останавливает потоковую передачу, когда фильтр переходит из состояния выполнения.
ms.assetid: 465dde15-adec-46da-b8c8-56743e0cbd29
title: Кбасерендерер. Стопстреаминг, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfd943de6a53383d7505fa9e884dcc152da6e5f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669339"
---
# <a name="cbaserendererstopstreaming-method"></a><span data-ttu-id="49524-103">Кбасерендерер. Стопстреаминг, метод</span><span class="sxs-lookup"><span data-stu-id="49524-103">CBaseRenderer.StopStreaming method</span></span>

<span data-ttu-id="49524-104">`StopStreaming`Метод останавливает потоковую передачу, когда фильтр переходит из состояния выполнения.</span><span class="sxs-lookup"><span data-stu-id="49524-104">The `StopStreaming` method halts streaming when the filter switches out of the running state.</span></span>

## <a name="syntax"></a><span data-ttu-id="49524-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49524-105">Syntax</span></span>


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="49524-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="49524-106">Parameters</span></span>

<span data-ttu-id="49524-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="49524-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="49524-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49524-108">Return value</span></span>

<span data-ttu-id="49524-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="49524-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="49524-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49524-110">Remarks</span></span>

<span data-ttu-id="49524-111">Этот метод вызывает метод [**кбасерендерер:: онстопстреаминг**](cbaserenderer-onstopstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="49524-111">This method calls the [**CBaseRenderer::OnStopStreaming**](cbaserenderer-onstopstreaming.md) method.</span></span> <span data-ttu-id="49524-112">Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.</span><span class="sxs-lookup"><span data-stu-id="49524-112">That method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="49524-113">Требования</span><span class="sxs-lookup"><span data-stu-id="49524-113">Requirements</span></span>



| <span data-ttu-id="49524-114">Требование</span><span class="sxs-lookup"><span data-stu-id="49524-114">Requirement</span></span> | <span data-ttu-id="49524-115">Значение</span><span class="sxs-lookup"><span data-stu-id="49524-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49524-116">Header</span><span class="sxs-lookup"><span data-stu-id="49524-116">Header</span></span><br/>  | <dl> <span data-ttu-id="49524-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49524-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="49524-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="49524-118">Library</span></span><br/> | <dl> <span data-ttu-id="49524-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="49524-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49524-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49524-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49524-121">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="49524-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





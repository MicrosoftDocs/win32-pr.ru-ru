---
description: Метод Stop останавливает фильтр.
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: Метод Кбасерендерер. останавливаться (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddd8194bbf76c4a4311aa90335f94d1e7548a356
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657990"
---
# <a name="cbaserendererstop-method"></a><span data-ttu-id="a796a-103">Кбасерендерер. останавливаться, метод</span><span class="sxs-lookup"><span data-stu-id="a796a-103">CBaseRenderer.Stop method</span></span>

<span data-ttu-id="a796a-104">`Stop`Метод останавливает фильтр.</span><span class="sxs-lookup"><span data-stu-id="a796a-104">The `Stop` method stops the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a796a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a796a-105">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="a796a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a796a-106">Parameters</span></span>

<span data-ttu-id="a796a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a796a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a796a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a796a-108">Return value</span></span>

<span data-ttu-id="a796a-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a796a-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a796a-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a796a-110">Remarks</span></span>

<span data-ttu-id="a796a-111">Этот метод переопределяет метод [**кбасефилтер:: останавливаться**](cbasefilter-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="a796a-111">This method overrides the [**CBaseFilter::Stop**](cbasefilter-stop.md) method.</span></span> <span data-ttu-id="a796a-112">Он выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a796a-112">It performs the following actions:</span></span>

-   <span data-ttu-id="a796a-113">Вызывает [**кбасефилтер:: останавливаться**](cbasefilter-stop.md).</span><span class="sxs-lookup"><span data-stu-id="a796a-113">Calls [**CBaseFilter::Stop**](cbasefilter-stop.md).</span></span>
-   <span data-ttu-id="a796a-114">Отменяет выделение распределителя.</span><span class="sxs-lookup"><span data-stu-id="a796a-114">Decommits the allocator.</span></span> <span data-ttu-id="a796a-115">(См. раздел [**имемаллокатор::D екоммит**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)</span><span class="sxs-lookup"><span data-stu-id="a796a-115">(See [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)</span></span>
-   <span data-ttu-id="a796a-116">Отменяет любую запланированную отрисовку и освобождает поток потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="a796a-116">Cancels any scheduled rendering and releases the streaming thread.</span></span>
-   <span data-ttu-id="a796a-117">Ожидает завершения любого ожидающего вызова **Receive** .</span><span class="sxs-lookup"><span data-stu-id="a796a-117">Waits for any pending **Receive** call to complete.</span></span>

## <a name="requirements"></a><span data-ttu-id="a796a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a796a-118">Requirements</span></span>



| <span data-ttu-id="a796a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a796a-119">Requirement</span></span> | <span data-ttu-id="a796a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a796a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a796a-121">Header</span><span class="sxs-lookup"><span data-stu-id="a796a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a796a-122"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a796a-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a796a-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a796a-123">Library</span></span><br/> | <dl> <span data-ttu-id="a796a-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a796a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a796a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a796a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a796a-126">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="a796a-126">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





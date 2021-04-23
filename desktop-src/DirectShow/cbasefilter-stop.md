---
description: 'Метод Stop останавливает фильтр. Этот метод реализует метод Имедиафилтер:: останавливаться.'
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: Метод Кбасефилтер. останавливаться (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4c4893edcf02fa18da3dc207a49f87c91b2a9ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657331"
---
# <a name="cbasefilterstop-method"></a><span data-ttu-id="aa0f1-104">Кбасефилтер. останавливаться, метод</span><span class="sxs-lookup"><span data-stu-id="aa0f1-104">CBaseFilter.Stop method</span></span>

<span data-ttu-id="aa0f1-105">`Stop`Метод останавливает фильтр.</span><span class="sxs-lookup"><span data-stu-id="aa0f1-105">The `Stop` method stops the filter.</span></span> <span data-ttu-id="aa0f1-106">Этот метод реализует метод [**имедиафилтер:: останавливаться**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="aa0f1-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa0f1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa0f1-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="aa0f1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa0f1-108">Parameters</span></span>

<span data-ttu-id="aa0f1-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="aa0f1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa0f1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa0f1-110">Return value</span></span>

<span data-ttu-id="aa0f1-111">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="aa0f1-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa0f1-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa0f1-112">Remarks</span></span>

<span data-ttu-id="aa0f1-113">Этот метод вызывает метод [**кбасепин:: Inactive**](cbasepin-inactive.md) для каждого подключенного контакта фильтра.</span><span class="sxs-lookup"><span data-stu-id="aa0f1-113">This method calls the [**CBasePin::Inactive**](cbasepin-inactive.md) method on each of the filter's connected pins.</span></span> <span data-ttu-id="aa0f1-114">Он также устанавливает состояние фильтра в состояние \_ остановлено.</span><span class="sxs-lookup"><span data-stu-id="aa0f1-114">It also sets the filter's state to State\_Stopped.</span></span>

<span data-ttu-id="aa0f1-115">Когда фильтр останавливается, он должен отклонять выборки из вышестоящего, прекращать доставку образцов, завершать рабочие потоки и освобождать все ресурсы, используемые для потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="aa0f1-115">When the filter stops, it should reject samples from upstream, stop delivering samples downstream, shut down worker threads, and free any resources that it used for streaming.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa0f1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="aa0f1-116">Requirements</span></span>



| <span data-ttu-id="aa0f1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="aa0f1-117">Requirement</span></span> | <span data-ttu-id="aa0f1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="aa0f1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0f1-119">Header</span><span class="sxs-lookup"><span data-stu-id="aa0f1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="aa0f1-120"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa0f1-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="aa0f1-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="aa0f1-121">Library</span></span><br/> | <dl> <span data-ttu-id="aa0f1-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="aa0f1-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa0f1-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa0f1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa0f1-124">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="aa0f1-124">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 





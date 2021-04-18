---
description: Метод Сетконфигинфо задает указатель Играфконфиг и событие завершения.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: Кдинамикаутпутпин. Сетконфигинфо, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SetConfigInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0c14342a629a38a878649ac59d8f1f814874f12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657231"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a><span data-ttu-id="1f821-103">Кдинамикаутпутпин. Сетконфигинфо, метод</span><span class="sxs-lookup"><span data-stu-id="1f821-103">CDynamicOutputPin.SetConfigInfo method</span></span>

<span data-ttu-id="1f821-104">`SetConfigInfo`Метод задает указатель [**играфконфиг**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) и событие завершения.</span><span class="sxs-lookup"><span data-stu-id="1f821-104">The `SetConfigInfo` method specifies the [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) pointer and the stop event.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f821-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f821-105">Syntax</span></span>


```C++
void SetConfigInfo(
   IGraphConfig *pGraphConfig,
   HANDLE       hStopEvent
);
```



## <a name="parameters"></a><span data-ttu-id="1f821-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f821-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f821-107">*пграфконфиг*</span><span class="sxs-lookup"><span data-stu-id="1f821-107">*pGraphConfig*</span></span> 
</dt> <dd>

<span data-ttu-id="1f821-108">Указатель на интерфейс [**играфконфиг**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1f821-108">Pointer to the [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) interface, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1f821-109">*хстопевент*</span><span class="sxs-lookup"><span data-stu-id="1f821-109">*hStopEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="1f821-110">Дескриптор события, сигнального при остановке фильтра, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1f821-110">Handle to an event that is signaled when the filter stops, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f821-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f821-111">Return value</span></span>

<span data-ttu-id="1f821-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1f821-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f821-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f821-113">Remarks</span></span>

<span data-ttu-id="1f821-114">Фильтр должен вызвать этот метод при соединении графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="1f821-114">The filter must call this method when it joins the filter graph.</span></span> <span data-ttu-id="1f821-115">Диспетчер графов фильтров поддерживает **играфконфиг**.</span><span class="sxs-lookup"><span data-stu-id="1f821-115">The filter graph manager supports **IGraphConfig**.</span></span> <span data-ttu-id="1f821-116">Для параметра *хстопевент* Создайте событие ручного сброса.</span><span class="sxs-lookup"><span data-stu-id="1f821-116">For the *hStopEvent* parameter, create a manual-reset event.</span></span> <span data-ttu-id="1f821-117">Когда фильтр покидает граф фильтра, вызовите этот метод еще раз с **нулевым значением** для обоих параметров.</span><span class="sxs-lookup"><span data-stu-id="1f821-117">When the filter leaves the filter graph, call this method again with **NULL** for both parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f821-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1f821-118">Requirements</span></span>



| <span data-ttu-id="1f821-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1f821-119">Requirement</span></span> | <span data-ttu-id="1f821-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1f821-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f821-121">Header</span><span class="sxs-lookup"><span data-stu-id="1f821-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1f821-122"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f821-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1f821-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1f821-123">Library</span></span><br/> | <dl> <span data-ttu-id="1f821-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1f821-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f821-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f821-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f821-126">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="1f821-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 





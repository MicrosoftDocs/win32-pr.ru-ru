---
description: Метод Жоинфилтерграф отправляет \_ \_ уведомление о событии, уничтоженное ОКНОм EC, при удалении фильтра из графа фильтра.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: Кбасевидеорендерер. Жоинфилтерграф, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acabb6deeb6577fa04479fc4014e210d4a5654d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675902"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a><span data-ttu-id="089e2-103">Кбасевидеорендерер. Жоинфилтерграф, метод</span><span class="sxs-lookup"><span data-stu-id="089e2-103">CBaseVideoRenderer.JoinFilterGraph method</span></span>

<span data-ttu-id="089e2-104">`JoinFilterGraph`Метод отправляет уведомление о событии, [**\_ \_ уничтоженное окном EC**](ec-window-destroyed.md) , при удалении фильтра из графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="089e2-104">The `JoinFilterGraph` method sends [**EC\_WINDOW\_DESTROYED**](ec-window-destroyed.md) event notification when a filter is removed from the filter graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="089e2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="089e2-105">Syntax</span></span>


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="089e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="089e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="089e2-107">*пграф*</span><span class="sxs-lookup"><span data-stu-id="089e2-107">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="089e2-108">Указатель на граф фильтра для объединения.</span><span class="sxs-lookup"><span data-stu-id="089e2-108">Pointer to the filter graph to join.</span></span>

</dd> <dt>

<span data-ttu-id="089e2-109">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="089e2-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="089e2-110">Указатель на имя добавляемого фильтра.</span><span class="sxs-lookup"><span data-stu-id="089e2-110">Pointer to the name of the filter being added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="089e2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="089e2-111">Return value</span></span>

<span data-ttu-id="089e2-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="089e2-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="089e2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="089e2-113">Remarks</span></span>

<span data-ttu-id="089e2-114">Эта функция члена переопределяет функцию члена [**кбасефилтер:: жоинфилтерграф**](cbasefilter-joinfiltergraph.md) .</span><span class="sxs-lookup"><span data-stu-id="089e2-114">This member function overrides the [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) member function.</span></span> <span data-ttu-id="089e2-115">Если фильтр выходит за пределы графа фильтра (*пграф* имеет **значение NULL**), он отправляет уведомление о событии в [**окне EC, \_ \_**](ec-window-destroyed.md) чтобы диспетчер ресурсов не удерживал обработчик в качестве объекта фокуса.</span><span class="sxs-lookup"><span data-stu-id="089e2-115">If the filter is leaving the filter graph (*pGraph* is **NULL**), it sends an [**EC\_WINDOW\_DESTROYED**](ec-window-destroyed.md) event notification so that the resource manager does not hold on to the renderer as a focus object.</span></span>

## <a name="requirements"></a><span data-ttu-id="089e2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="089e2-116">Requirements</span></span>



| <span data-ttu-id="089e2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="089e2-117">Requirement</span></span> | <span data-ttu-id="089e2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="089e2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="089e2-119">Header</span><span class="sxs-lookup"><span data-stu-id="089e2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="089e2-120"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="089e2-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="089e2-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="089e2-121">Library</span></span><br/> | <dl> <span data-ttu-id="089e2-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="089e2-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="089e2-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="089e2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="089e2-124">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="089e2-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 





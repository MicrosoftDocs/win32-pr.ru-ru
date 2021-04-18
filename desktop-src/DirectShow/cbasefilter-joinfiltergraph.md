---
description: 'Метод Жоинфилтерграф уведомляет фильтр о соединении или на графе фильтра. Этот метод реализует метод Ибасефилтер:: Жоинфилтерграф.'
ms.assetid: ee02650c-aaf0-4a0e-914f-180230010709
title: Кбасефилтер. Жоинфилтерграф, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45453c6423b8fa9f68e5d8dff86d13b130d65f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657798"
---
# <a name="cbasefilterjoinfiltergraph-method"></a><span data-ttu-id="f09c9-104">Кбасефилтер. Жоинфилтерграф, метод</span><span class="sxs-lookup"><span data-stu-id="f09c9-104">CBaseFilter.JoinFilterGraph method</span></span>

<span data-ttu-id="f09c9-105">`JoinFilterGraph`Метод уведомляет фильтр о соединении или влево граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="f09c9-105">The `JoinFilterGraph` method notifies the filter that it has joined or left a filter graph.</span></span> <span data-ttu-id="f09c9-106">Этот метод реализует метод [**ибасефилтер:: жоинфилтерграф**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) .</span><span class="sxs-lookup"><span data-stu-id="f09c9-106">This method implements the [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f09c9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f09c9-107">Syntax</span></span>


```C++
HRESULT JoinFilterGraph(
       IFilterGraph *pGraph,
  [in] LPCWSTR      pName
);
```



## <a name="parameters"></a><span data-ttu-id="f09c9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f09c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f09c9-109">*пграф*</span><span class="sxs-lookup"><span data-stu-id="f09c9-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="f09c9-110">Указатель на интерфейс [**ифилтерграф**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) диспетчера графа фильтров или **значение NULL** , если фильтр выходит из графа.</span><span class="sxs-lookup"><span data-stu-id="f09c9-110">Pointer to the filter graph manager's [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) interface, or **NULL** if the filter is leaving the graph.</span></span>

</dd> <dt>

<span data-ttu-id="f09c9-111">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f09c9-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f09c9-112">Указатель на строку в Юникоде, содержащую имя фильтра.</span><span class="sxs-lookup"><span data-stu-id="f09c9-112">Pointer to a Unicode string containing a name for the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f09c9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f09c9-113">Return value</span></span>

<span data-ttu-id="f09c9-114">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f09c9-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f09c9-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f09c9-115">Remarks</span></span>

<span data-ttu-id="f09c9-116">Этот метод задает переменную члена [**кбасефилтер:: m \_ пграф**](cbasefilter-m-pgraph.md) , равную параметру *пграф* .</span><span class="sxs-lookup"><span data-stu-id="f09c9-116">This method sets the [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md) member variable equal to the *pGraph* parameter.</span></span> <span data-ttu-id="f09c9-117">Он также запрашивает указатель интерфейса [**имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) и сохраняет его в переменной члена [**кбасефилтер:: m \_ псинк**](cbasefilter-m-psink.md) .</span><span class="sxs-lookup"><span data-stu-id="f09c9-117">It also queries for an [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface pointer and stores it in the [**CBaseFilter::m\_pSink**](cbasefilter-m-psink.md) member variable.</span></span> <span data-ttu-id="f09c9-118">Однако фильтр не сохраняет счетчик ссылок ни для одного из этих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="f09c9-118">However, the filter does not keep a reference count on either of these interfaces.</span></span> <span data-ttu-id="f09c9-119">Это приведет к созданию циклического счетчика ссылок, так как диспетчер графа фильтров сохранит счетчик ссылок на фильтре.</span><span class="sxs-lookup"><span data-stu-id="f09c9-119">Doing so would create a circular reference count, because the filter graph manager keeps a reference count on the filter.</span></span>

<span data-ttu-id="f09c9-120">Метод копирует строку, указанную параметром *pName* , в переменную члена [**кбасефилтер:: m \_ pName**](cbasefilter-m-pname.md) .</span><span class="sxs-lookup"><span data-stu-id="f09c9-120">The method copies the string specified by *pName* into the [**CBaseFilter::m\_pName**](cbasefilter-m-pname.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="f09c9-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f09c9-121">Requirements</span></span>



| <span data-ttu-id="f09c9-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f09c9-122">Requirement</span></span> | <span data-ttu-id="f09c9-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f09c9-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f09c9-124">Header</span><span class="sxs-lookup"><span data-stu-id="f09c9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f09c9-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f09c9-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f09c9-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f09c9-126">Library</span></span><br/> | <dl> <span data-ttu-id="f09c9-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f09c9-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f09c9-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f09c9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f09c9-129">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="f09c9-129">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 





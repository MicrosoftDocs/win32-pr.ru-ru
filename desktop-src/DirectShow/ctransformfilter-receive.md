---
description: Метод Receive получает пример носителя, обрабатывает его и доставляет образец вывода в нисходящий фильтр.
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: Метод Ктрансформфилтер. Receive (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67924bffc4d4d80b998e686d80d0e50afcd040ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657746"
---
# <a name="ctransformfilterreceive-method"></a><span data-ttu-id="80895-103">Ктрансформфилтер. Receive, метод</span><span class="sxs-lookup"><span data-stu-id="80895-103">CTransformFilter.Receive method</span></span>

<span data-ttu-id="80895-104">`Receive`Метод получает пример носителя, обрабатывает его и доставляет образец вывода в нисходящий фильтр.</span><span class="sxs-lookup"><span data-stu-id="80895-104">The `Receive` method receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="80895-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80895-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="80895-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80895-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80895-107">*псампле*</span><span class="sxs-lookup"><span data-stu-id="80895-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="80895-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) в образце входных данных.</span><span class="sxs-lookup"><span data-stu-id="80895-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the input sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80895-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80895-109">Return value</span></span>

<span data-ttu-id="80895-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80895-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="80895-111">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="80895-111">Possible values include the following:</span></span>



| <span data-ttu-id="80895-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="80895-112">Return code</span></span>                                                                             | <span data-ttu-id="80895-113">Описание</span><span class="sxs-lookup"><span data-stu-id="80895-113">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="80895-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="80895-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="80895-115">Вышестоящий фильтр должен закончить отправку образцов.</span><span class="sxs-lookup"><span data-stu-id="80895-115">The upstream filter should stop sending samples.</span></span><br/> |
| <dl> <span data-ttu-id="80895-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="80895-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="80895-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="80895-117">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="80895-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80895-118">Remarks</span></span>

<span data-ttu-id="80895-119">Входной ПИН-код фильтра вызывает этот метод при получении примера.</span><span class="sxs-lookup"><span data-stu-id="80895-119">The filter's input pin calls this method when it receives a sample.</span></span> <span data-ttu-id="80895-120">Этот метод вызывает метод [**ктрансформфилтер:: инитиализеаутпутсампле**](ctransformfilter-initializeoutputsample.md) , подготавливающий новый образец выходных данных.</span><span class="sxs-lookup"><span data-stu-id="80895-120">This method calls the [**CTransformFilter::InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) method, which prepares a new output sample.</span></span> <span data-ttu-id="80895-121">Затем вызывается метод [**ктрансформфилтер:: Transform**](ctransformfilter-transform.md) , который должен реализовываться производным классом.</span><span class="sxs-lookup"><span data-stu-id="80895-121">Then it calls the [**CTransformFilter::Transform**](ctransformfilter-transform.md) method, which the derived class must implement.</span></span> <span data-ttu-id="80895-122">Метод **Transform** обрабатывает входные данные и создает выходные данные.</span><span class="sxs-lookup"><span data-stu-id="80895-122">The **Transform** method processes the input data and produces output data.</span></span>

<span data-ttu-id="80895-123">Если метод **Transform** возвращает \_ значение false, `Receive` метод удаляет этот образец.</span><span class="sxs-lookup"><span data-stu-id="80895-123">If the **Transform** method returns S\_FALSE, the `Receive` method drops this sample.</span></span> <span data-ttu-id="80895-124">В первом удаленном примере фильтр отправляет событие EC об [**\_ \_ изменении качества**](ec-quality-change.md) в Диспетчер графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="80895-124">On the first dropped sample, the filter sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager.</span></span> <span data-ttu-id="80895-125">В противном случае, если метод **Transform** возвращает значение S \_ , фильтр доставляет образец Output.</span><span class="sxs-lookup"><span data-stu-id="80895-125">Otherwise, if the **Transform** method returns S\_OK, the filter delivers the output sample.</span></span> <span data-ttu-id="80895-126">Для этого он вызывает метод [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) для входного контакта нисходящего входа.</span><span class="sxs-lookup"><span data-stu-id="80895-126">To do so, it calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="80895-127">Требования</span><span class="sxs-lookup"><span data-stu-id="80895-127">Requirements</span></span>



| <span data-ttu-id="80895-128">Требование</span><span class="sxs-lookup"><span data-stu-id="80895-128">Requirement</span></span> | <span data-ttu-id="80895-129">Значение</span><span class="sxs-lookup"><span data-stu-id="80895-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80895-130">Header</span><span class="sxs-lookup"><span data-stu-id="80895-130">Header</span></span><br/>  | <dl> <span data-ttu-id="80895-131"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80895-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="80895-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80895-132">Library</span></span><br/> | <dl> <span data-ttu-id="80895-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="80895-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80895-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80895-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80895-135">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="80895-135">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





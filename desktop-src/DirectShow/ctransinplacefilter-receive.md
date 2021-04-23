---
description: Метод Receive получает пример носителя, обрабатывает его и доставляет в подчиненный фильтр.
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: Метод Ктрансинплацефилтер. Receive (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e7a1f87617b59c31139cb3d857c83d4470fd709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657743"
---
# <a name="ctransinplacefilterreceive-method"></a><span data-ttu-id="7ca56-103">Ктрансинплацефилтер. Receive, метод</span><span class="sxs-lookup"><span data-stu-id="7ca56-103">CTransInPlaceFilter.Receive method</span></span>

<span data-ttu-id="7ca56-104">`Receive`Метод получает пример носителя, обрабатывает его и доставляет его в нисходящий фильтр.</span><span class="sxs-lookup"><span data-stu-id="7ca56-104">The `Receive` method receives a media sample, processes it, and delivers it to the downstream filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ca56-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ca56-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="7ca56-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ca56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ca56-107">*псампле*</span><span class="sxs-lookup"><span data-stu-id="7ca56-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="7ca56-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) в образце.</span><span class="sxs-lookup"><span data-stu-id="7ca56-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ca56-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ca56-109">Return value</span></span>

<span data-ttu-id="7ca56-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7ca56-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7ca56-111">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7ca56-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="7ca56-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7ca56-112">Return code</span></span>                                                                                  | <span data-ttu-id="7ca56-113">Описание</span><span class="sxs-lookup"><span data-stu-id="7ca56-113">Description</span></span>                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="7ca56-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca56-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="7ca56-115">Успешно</span><span class="sxs-lookup"><span data-stu-id="7ca56-115">Success</span></span><br/>          |
| <dl> <span data-ttu-id="7ca56-116"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="7ca56-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="7ca56-117">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="7ca56-117">Unexpected error</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ca56-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ca56-118">Remarks</span></span>

<span data-ttu-id="7ca56-119">Входной ПИН-код фильтра вызывает этот метод при получении примера.</span><span class="sxs-lookup"><span data-stu-id="7ca56-119">The filter's input pin calls this method when it receives a sample.</span></span> <span data-ttu-id="7ca56-120">Фильтр вызывает метод [**Transform**](ctransinplacefilter-transform.md) , который должен реализовываться производным классом.</span><span class="sxs-lookup"><span data-stu-id="7ca56-120">The filter calls the [**Transform**](ctransinplacefilter-transform.md) method, which the derived class must implement.</span></span> <span data-ttu-id="7ca56-121">Метод **Transform** обрабатывает данные.</span><span class="sxs-lookup"><span data-stu-id="7ca56-121">The **Transform** method processes the data.</span></span> <span data-ttu-id="7ca56-122">Если фильтр использует только один распределитель, он передает *псампле* непосредственно методу **Transform** .</span><span class="sxs-lookup"><span data-stu-id="7ca56-122">If the filter is using only one allocator, it passes *pSample* directly to the **Transform** method.</span></span> <span data-ttu-id="7ca56-123">В противном случае он копирует *псампле* и передает копию.</span><span class="sxs-lookup"><span data-stu-id="7ca56-123">Otherwise, it copies *pSample* and passes the copy.</span></span>

<span data-ttu-id="7ca56-124">Если метод **Transform** возвращает \_ значение false, `Receive` метод удаляет пример.</span><span class="sxs-lookup"><span data-stu-id="7ca56-124">If the **Transform** method returns S\_FALSE, the `Receive` method drops the sample.</span></span> <span data-ttu-id="7ca56-125">В первом удаленном примере фильтр отправляет событие EC об [**\_ \_ изменении качества**](ec-quality-change.md) в Диспетчер графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="7ca56-125">On the first dropped sample, the filter sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager.</span></span> <span data-ttu-id="7ca56-126">В противном случае, если метод **Transform** возвращает значение S \_ , фильтр доставляет образец Output.</span><span class="sxs-lookup"><span data-stu-id="7ca56-126">Otherwise, if the **Transform** method returns S\_OK, the filter delivers the output sample.</span></span> <span data-ttu-id="7ca56-127">Для этого он вызывает метод [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) для входного контакта нисходящего входа.</span><span class="sxs-lookup"><span data-stu-id="7ca56-127">To do so, it calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ca56-128">Требования</span><span class="sxs-lookup"><span data-stu-id="7ca56-128">Requirements</span></span>



| <span data-ttu-id="7ca56-129">Требование</span><span class="sxs-lookup"><span data-stu-id="7ca56-129">Requirement</span></span> | <span data-ttu-id="7ca56-130">Значение</span><span class="sxs-lookup"><span data-stu-id="7ca56-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca56-131">Header</span><span class="sxs-lookup"><span data-stu-id="7ca56-131">Header</span></span><br/>  | <dl> <span data-ttu-id="7ca56-132"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ca56-132"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7ca56-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7ca56-133">Library</span></span><br/> | <dl> <span data-ttu-id="7ca56-134"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7ca56-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ca56-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ca56-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca56-136">**Класс Ктрансинплацефилтер**</span><span class="sxs-lookup"><span data-stu-id="7ca56-136">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 





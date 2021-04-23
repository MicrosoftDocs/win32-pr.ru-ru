---
description: 'Метод Run уведомляет ПИН-код о том, что фильтр выполняется. Этот метод переопределяет метод Кбасепин:: Run.'
ms.assetid: ee0285aa-9afd-464a-b8b4-d8b7faa49dbd
title: Метод Крендерединпутпин. Run (Амекстра. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef3de4d5ab9a06766ccce171c9d417639ce66a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657418"
---
# <a name="crenderedinputpinrun-method"></a><span data-ttu-id="02d56-104">Крендерединпутпин. Run, метод</span><span class="sxs-lookup"><span data-stu-id="02d56-104">CRenderedInputPin.Run method</span></span>

<span data-ttu-id="02d56-105">`Run`Метод уведомляет ПИН-код о том, что теперь фильтр работает.</span><span class="sxs-lookup"><span data-stu-id="02d56-105">The `Run` method notifies the pin that the filter is now running.</span></span> <span data-ttu-id="02d56-106">Этот метод переопределяет метод [**кбасепин:: Run**](cbasepin-run.md) .</span><span class="sxs-lookup"><span data-stu-id="02d56-106">This method overrides the [**CBasePin::Run**](cbasepin-run.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="02d56-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02d56-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="02d56-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="02d56-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02d56-109">*тстарт*</span><span class="sxs-lookup"><span data-stu-id="02d56-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="02d56-110">Время начала, которое было передано в метод [**имедиафилтер:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) фильтра.</span><span class="sxs-lookup"><span data-stu-id="02d56-110">The start time that was passed to the filter's [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02d56-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02d56-111">Return value</span></span>

<span data-ttu-id="02d56-112">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="02d56-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="02d56-113">Требования</span><span class="sxs-lookup"><span data-stu-id="02d56-113">Requirements</span></span>



| <span data-ttu-id="02d56-114">Требование</span><span class="sxs-lookup"><span data-stu-id="02d56-114">Requirement</span></span> | <span data-ttu-id="02d56-115">Значение</span><span class="sxs-lookup"><span data-stu-id="02d56-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02d56-116">Header</span><span class="sxs-lookup"><span data-stu-id="02d56-116">Header</span></span><br/>  | <dl> <span data-ttu-id="02d56-117"><dt>Амекстра. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02d56-117"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="02d56-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="02d56-118">Library</span></span><br/> | <dl> <span data-ttu-id="02d56-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="02d56-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02d56-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02d56-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02d56-121">**Класс Крендерединпутпин**</span><span class="sxs-lookup"><span data-stu-id="02d56-121">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 





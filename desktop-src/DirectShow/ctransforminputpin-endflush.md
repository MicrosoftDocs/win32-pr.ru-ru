---
description: 'Ктрансформинпутпин. Ендфлуш, метод Ендфлуш завершает операцию очистки. Этот метод реализует метод Ипин:: Ендфлуш.'
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: Ктрансформинпутпин. Ендфлуш, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5e080b4531d05160bebd42a68145842c4783bea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095062"
---
# <a name="ctransforminputpinendflush-method"></a><span data-ttu-id="55949-104">Ктрансформинпутпин. Ендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="55949-104">CTransformInputPin.EndFlush method</span></span>

<span data-ttu-id="55949-105">`EndFlush`Метод завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="55949-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="55949-106">Этот метод реализует метод [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="55949-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="55949-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55949-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="55949-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="55949-108">Parameters</span></span>

<span data-ttu-id="55949-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="55949-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="55949-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55949-110">Return value</span></span>

<span data-ttu-id="55949-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="55949-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="55949-112">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="55949-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="55949-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="55949-113">Return code</span></span>                                                                                           | <span data-ttu-id="55949-114">Описание</span><span class="sxs-lookup"><span data-stu-id="55949-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="55949-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="55949-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="55949-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="55949-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="55949-117"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="55949-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="55949-118">Выходной ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="55949-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="55949-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="55949-119">Remarks</span></span>

<span data-ttu-id="55949-120">Этот метод вызывает метод [**ктрансформфилтер:: ендфлуш**](ctransformfilter-endflush.md) фильтра для доставки вызова в нисходящем направлении.</span><span class="sxs-lookup"><span data-stu-id="55949-120">This method calls the filter's [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method to deliver the call downstream.</span></span> <span data-ttu-id="55949-121">Затем вызывается метод [**кбасеинпутпин:: ендфлуш**](cbaseinputpin-endflush.md) ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="55949-121">Then it calls the pin's [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="55949-122">Требования</span><span class="sxs-lookup"><span data-stu-id="55949-122">Requirements</span></span>



| <span data-ttu-id="55949-123">Требование</span><span class="sxs-lookup"><span data-stu-id="55949-123">Requirement</span></span> | <span data-ttu-id="55949-124">Значение</span><span class="sxs-lookup"><span data-stu-id="55949-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55949-125">Header</span><span class="sxs-lookup"><span data-stu-id="55949-125">Header</span></span><br/>  | <dl> <span data-ttu-id="55949-126"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55949-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="55949-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="55949-127">Library</span></span><br/> | <dl> <span data-ttu-id="55949-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="55949-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





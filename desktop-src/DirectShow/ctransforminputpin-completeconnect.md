---
description: Метод Комплетеконнект завершает подключение к другому ПИН-коду.
ms.assetid: 568cee55-b9ea-4fc2-ac9d-0080b7de9790
title: Ктрансформинпутпин. Комплетеконнект, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 455517968481b9333fbeba590aca644b34b2f5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675654"
---
# <a name="ctransforminputpincompleteconnect-method"></a><span data-ttu-id="42d70-103">Ктрансформинпутпин. Комплетеконнект, метод</span><span class="sxs-lookup"><span data-stu-id="42d70-103">CTransformInputPin.CompleteConnect method</span></span>

<span data-ttu-id="42d70-104">`CompleteConnect`Метод завершает подключение к другому ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="42d70-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="42d70-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42d70-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="42d70-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42d70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42d70-107">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="42d70-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="42d70-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="42d70-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42d70-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42d70-109">Return value</span></span>

<span data-ttu-id="42d70-110">Возвращает \_ значение, равное ОК или другому значению **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="42d70-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42d70-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42d70-111">Remarks</span></span>

<span data-ttu-id="42d70-112">Этот метод переопределяет метод [**кбасепин:: комплетеконнект**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="42d70-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="42d70-113">Он вызывает метод [**ктрансформфилтер:: комплетеконнект**](ctransformfilter-completeconnect.md) фильтра, который возвращает \_ значение s ОК в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="42d70-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="42d70-114">Производный класс может переопределить метод **ктрансформфилтер:: комплетеконнект** для выполнения дополнительных проверок.</span><span class="sxs-lookup"><span data-stu-id="42d70-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d70-115">Требования</span><span class="sxs-lookup"><span data-stu-id="42d70-115">Requirements</span></span>



| <span data-ttu-id="42d70-116">Требование</span><span class="sxs-lookup"><span data-stu-id="42d70-116">Requirement</span></span> | <span data-ttu-id="42d70-117">Значение</span><span class="sxs-lookup"><span data-stu-id="42d70-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42d70-118">Header</span><span class="sxs-lookup"><span data-stu-id="42d70-118">Header</span></span><br/>  | <dl> <span data-ttu-id="42d70-119"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42d70-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="42d70-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="42d70-120">Library</span></span><br/> | <dl> <span data-ttu-id="42d70-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="42d70-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





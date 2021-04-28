---
description: Ктрансформаутпутпин. Комплетеконнект, метод Комплетеконнект завершает подключение к другому ПИН-коду.
ms.assetid: 14bc48bc-ddfb-4491-8d5b-9e5ac601ba04
title: Ктрансформаутпутпин. Комплетеконнект, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ab3d7e56473094b31c0d97d0e15c083ff61a21d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094922"
---
# <a name="ctransformoutputpincompleteconnect-method"></a><span data-ttu-id="b4ea8-103">Ктрансформаутпутпин. Комплетеконнект, метод</span><span class="sxs-lookup"><span data-stu-id="b4ea8-103">CTransformOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="b4ea8-104">`CompleteConnect`Метод завершает подключение к другому ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="b4ea8-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4ea8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4ea8-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="b4ea8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4ea8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4ea8-107">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="b4ea8-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="b4ea8-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="b4ea8-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4ea8-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4ea8-109">Return value</span></span>

<span data-ttu-id="b4ea8-110">Возвращает \_ значение, равное ОК или другому значению **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b4ea8-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4ea8-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="b4ea8-111">Remarks</span></span>

<span data-ttu-id="b4ea8-112">Этот метод переопределяет метод [**кбасеаутпутпин:: комплетеконнект**](cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="b4ea8-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="b4ea8-113">Он вызывает метод [**ктрансформфилтер:: комплетеконнект**](ctransformfilter-completeconnect.md) фильтра, который возвращает \_ значение s ОК в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="b4ea8-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="b4ea8-114">Производный класс может переопределить метод **ктрансформфилтер:: комплетеконнект** для выполнения дополнительных проверок.</span><span class="sxs-lookup"><span data-stu-id="b4ea8-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4ea8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b4ea8-115">Requirements</span></span>



| <span data-ttu-id="b4ea8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b4ea8-116">Requirement</span></span> | <span data-ttu-id="b4ea8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b4ea8-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ea8-118">Header</span><span class="sxs-lookup"><span data-stu-id="b4ea8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b4ea8-119"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4ea8-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b4ea8-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b4ea8-120">Library</span></span><br/> | <dl> <span data-ttu-id="b4ea8-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b4ea8-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





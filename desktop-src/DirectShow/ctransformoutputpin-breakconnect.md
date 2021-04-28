---
description: Ктрансформаутпутпин. Бреакконнект, метод Бреакконнект освобождает ПИН-код из соединения.
ms.assetid: bf68aca3-93e5-4f9d-9980-1a5eed1513f5
title: Ктрансформаутпутпин. Бреакконнект, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92854041e1d553945d0a1ab1755ef3557bd4a8b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084962"
---
# <a name="ctransformoutputpinbreakconnect-method"></a><span data-ttu-id="98f81-103">Ктрансформаутпутпин. Бреакконнект, метод</span><span class="sxs-lookup"><span data-stu-id="98f81-103">CTransformOutputPin.BreakConnect method</span></span>

<span data-ttu-id="98f81-104">`BreakConnect`Метод освобождает ПИН-код из соединения.</span><span class="sxs-lookup"><span data-stu-id="98f81-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="98f81-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98f81-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="98f81-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="98f81-106">Parameters</span></span>

<span data-ttu-id="98f81-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="98f81-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98f81-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98f81-108">Return value</span></span>

<span data-ttu-id="98f81-109">Возвращает \_ значение, равное ОК или другому значению **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="98f81-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98f81-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="98f81-110">Remarks</span></span>

<span data-ttu-id="98f81-111">Этот метод переопределяет метод [**кбасеаутпутпин:: бреакконнект**](cbaseoutputpin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="98f81-111">This method overrides the [**CBaseOutputPin::BreakConnect**](cbaseoutputpin-breakconnect.md) method.</span></span> <span data-ttu-id="98f81-112">Он вызывает метод [**ктрансформфилтер:: бреакконнект**](ctransformfilter-breakconnect.md) фильтра, который возвращает \_ значение s ОК в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="98f81-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="98f81-113">Производный класс может переопределить метод **ктрансформфилтер:: бреакконнект** .</span><span class="sxs-lookup"><span data-stu-id="98f81-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="98f81-114">Требования</span><span class="sxs-lookup"><span data-stu-id="98f81-114">Requirements</span></span>



| <span data-ttu-id="98f81-115">Требование</span><span class="sxs-lookup"><span data-stu-id="98f81-115">Requirement</span></span> | <span data-ttu-id="98f81-116">Значение</span><span class="sxs-lookup"><span data-stu-id="98f81-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98f81-117">Header</span><span class="sxs-lookup"><span data-stu-id="98f81-117">Header</span></span><br/>  | <dl> <span data-ttu-id="98f81-118"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98f81-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="98f81-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="98f81-119">Library</span></span><br/> | <dl> <span data-ttu-id="98f81-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="98f81-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





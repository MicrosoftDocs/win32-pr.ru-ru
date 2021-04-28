---
description: Ктрансформинпутпин. Чеккмедиатипе, метод Чеккмедиатипе определяет, принимает ли ПИН-код конкретный тип носителя.
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: Ктрансформинпутпин. Чеккмедиатипе, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c775618c9fe30de6171919d5b8bc8a80ea81d3a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085002"
---
# <a name="ctransforminputpincheckmediatype-method"></a><span data-ttu-id="9e5b1-103">Ктрансформинпутпин. Чеккмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="9e5b1-103">CTransformInputPin.CheckMediaType method</span></span>

<span data-ttu-id="9e5b1-104">`CheckMediaType`Метод определяет, принимает ли ПИН-код конкретный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e5b1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e5b1-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="9e5b1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e5b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e5b1-107">*мтин*</span><span class="sxs-lookup"><span data-stu-id="9e5b1-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="9e5b1-108">Указатель на объект [**кмедиатипе**](cmediatype.md) , который содержит предложенный тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e5b1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e5b1-109">Return value</span></span>

<span data-ttu-id="9e5b1-110">Возвращает \_ значение, равное ОК или другому значению **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9e5b1-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e5b1-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="9e5b1-111">Remarks</span></span>

<span data-ttu-id="9e5b1-112">Этот метод реализует чистый виртуальный метод [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="9e5b1-112">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="9e5b1-113">Он вызывает метод [**ктрансформфилтер:: чеккинпуттипе**](ctransformfilter-checkinputtype.md) фильтра, который также является чистым виртуальным.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-113">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method, which is also pure virtual.</span></span> <span data-ttu-id="9e5b1-114">Производный класс фильтра должен реализовать **чеккинпуттипе** , чтобы определить, допустим ли данный входной тип.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-114">The filter's derived class must implement **CheckInputType** to determine whether a given input type is acceptable.</span></span>

<span data-ttu-id="9e5b1-115">Если закрепление вывода фильтра подключено, этот метод также вызывает метод [**ктрансформфилтер:: чекктрансформ**](ctransformfilter-checktransform.md) фильтра, чтобы определить, совместим ли входной тип с выходным типом.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-115">If the filter's output pin is connected, this method also calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method to determine whether the input type is compatible with the output type.</span></span> <span data-ttu-id="9e5b1-116">Метод **чекктрансформ** также является чистым виртуальным.</span><span class="sxs-lookup"><span data-stu-id="9e5b1-116">The **CheckTransform** method is pure virtual as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e5b1-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9e5b1-117">Requirements</span></span>



| <span data-ttu-id="9e5b1-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9e5b1-118">Requirement</span></span> | <span data-ttu-id="9e5b1-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9e5b1-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e5b1-120">Header</span><span class="sxs-lookup"><span data-stu-id="9e5b1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9e5b1-121"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e5b1-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9e5b1-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9e5b1-122">Library</span></span><br/> | <dl> <span data-ttu-id="9e5b1-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9e5b1-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





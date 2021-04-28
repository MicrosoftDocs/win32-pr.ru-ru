---
description: Ктрансформаутпутпин. Чеккконнект, метод Чеккконнект определяет, подходит ли подключение по ПИН-коду.
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: Ктрансформаутпутпин. Чеккконнект, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 190acd2fbab5206b114b57719d350e3ad5eac0c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094952"
---
# <a name="ctransformoutputpincheckconnect-method"></a><span data-ttu-id="d5bb2-103">Ктрансформаутпутпин. Чеккконнект, метод</span><span class="sxs-lookup"><span data-stu-id="d5bb2-103">CTransformOutputPin.CheckConnect method</span></span>

<span data-ttu-id="d5bb2-104">`CheckConnect`Метод определяет, подходит ли подключение по ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="d5bb2-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5bb2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5bb2-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="d5bb2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5bb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5bb2-107">*ппин*</span><span class="sxs-lookup"><span data-stu-id="d5bb2-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d5bb2-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="d5bb2-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5bb2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5bb2-109">Return value</span></span>

<span data-ttu-id="d5bb2-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d5bb2-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d5bb2-111">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="d5bb2-111">Possible values include the following.</span></span>



| <span data-ttu-id="d5bb2-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d5bb2-112">Return code</span></span>                                                                                  | <span data-ttu-id="d5bb2-113">Описание</span><span class="sxs-lookup"><span data-stu-id="d5bb2-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="d5bb2-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d5bb2-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d5bb2-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="d5bb2-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d5bb2-116"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="d5bb2-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="d5bb2-117">Входной ПИН-код фильтра не подключен.</span><span class="sxs-lookup"><span data-stu-id="d5bb2-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d5bb2-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="d5bb2-118">Remarks</span></span>

<span data-ttu-id="d5bb2-119">Этот метод переопределяет метод [**кбасеаутпутпин:: чеккконнект**](cbaseoutputpin-checkconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="d5bb2-119">This method overrides the [**CBaseOutputPin::CheckConnect**](cbaseoutputpin-checkconnect.md) method.</span></span> <span data-ttu-id="d5bb2-120">Он вызывает метод [**ктрансформфилтер:: чеккконнект**](ctransformfilter-checkconnect.md) фильтра, который возвращает \_ значение s ОК в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="d5bb2-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="d5bb2-121">Производный класс может переопределить метод **ктрансформфилтер:: чеккконнект** для выполнения дополнительных проверок.</span><span class="sxs-lookup"><span data-stu-id="d5bb2-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5bb2-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d5bb2-122">Requirements</span></span>



| <span data-ttu-id="d5bb2-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d5bb2-123">Requirement</span></span> | <span data-ttu-id="d5bb2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d5bb2-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5bb2-125">Header</span><span class="sxs-lookup"><span data-stu-id="d5bb2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d5bb2-126"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5bb2-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d5bb2-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d5bb2-127">Library</span></span><br/> | <dl> <span data-ttu-id="d5bb2-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d5bb2-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





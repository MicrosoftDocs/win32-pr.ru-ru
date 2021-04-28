---
description: Ктрансформинпутпин. Чеккконнект, метод Чеккконнект определяет, подходит ли подключение по ПИН-коду.
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: Ктрансформинпутпин. Чеккконнект, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e981254677c2e0a361a0a21f125f734ff1403db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095092"
---
# <a name="ctransforminputpincheckconnect-method"></a><span data-ttu-id="305b7-103">Ктрансформинпутпин. Чеккконнект, метод</span><span class="sxs-lookup"><span data-stu-id="305b7-103">CTransformInputPin.CheckConnect method</span></span>

<span data-ttu-id="305b7-104">`CheckConnect`Метод определяет, подходит ли подключение по ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="305b7-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="305b7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="305b7-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="305b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="305b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="305b7-107">*ппин*</span><span class="sxs-lookup"><span data-stu-id="305b7-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="305b7-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="305b7-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="305b7-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="305b7-109">Return value</span></span>

<span data-ttu-id="305b7-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="305b7-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="305b7-111">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="305b7-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="305b7-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="305b7-112">Return code</span></span>                                                                                               | <span data-ttu-id="305b7-113">Описание</span><span class="sxs-lookup"><span data-stu-id="305b7-113">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="305b7-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="305b7-114"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="305b7-115">Успешное завершение</span><span class="sxs-lookup"><span data-stu-id="305b7-115">Success</span></span><br/>             |
| <dl> <span data-ttu-id="305b7-116"><dt>**VFW \_ E \_ недопустимое \_ направление**</dt></span><span class="sxs-lookup"><span data-stu-id="305b7-116"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="305b7-117">Неправильное направление ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="305b7-117">Wrong pin direction</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="305b7-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="305b7-118">Remarks</span></span>

<span data-ttu-id="305b7-119">Этот метод переопределяет метод [**кбасепин:: чеккконнект**](cbasepin-checkconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="305b7-119">This method overrides the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method.</span></span> <span data-ttu-id="305b7-120">Он вызывает метод [**ктрансформфилтер:: чеккконнект**](ctransformfilter-checkconnect.md) фильтра, который возвращает \_ значение s ОК в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="305b7-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="305b7-121">Производный класс может переопределить метод **ктрансформфилтер:: чеккконнект** для выполнения дополнительных проверок.</span><span class="sxs-lookup"><span data-stu-id="305b7-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="305b7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="305b7-122">Requirements</span></span>



| <span data-ttu-id="305b7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="305b7-123">Requirement</span></span> | <span data-ttu-id="305b7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="305b7-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="305b7-125">Header</span><span class="sxs-lookup"><span data-stu-id="305b7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="305b7-126"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="305b7-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="305b7-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="305b7-127">Library</span></span><br/> | <dl> <span data-ttu-id="305b7-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="305b7-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





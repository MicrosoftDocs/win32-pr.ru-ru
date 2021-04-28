---
description: Кбасеаутпутпин. Чеккконнект, метод Чеккконнект определяет, подходит ли подключение по ПИН-коду.
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Кбасеаутпутпин. Чеккконнект, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ea5ad32de18046f3d23145d82e971391c3e304c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096192"
---
# <a name="cbaseoutputpincheckconnect-method"></a><span data-ttu-id="f8832-103">Кбасеаутпутпин. Чеккконнект, метод</span><span class="sxs-lookup"><span data-stu-id="f8832-103">CBaseOutputPin.CheckConnect method</span></span>

<span data-ttu-id="f8832-104">`CheckConnect`Метод определяет, подходит ли подключение по ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="f8832-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8832-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8832-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="f8832-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8832-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8832-107">*ппин*</span><span class="sxs-lookup"><span data-stu-id="f8832-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="f8832-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) входного контакта.</span><span class="sxs-lookup"><span data-stu-id="f8832-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8832-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8832-109">Return value</span></span>

<span data-ttu-id="f8832-110">Возвращает одно из следующих значений **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8832-110">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="f8832-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f8832-111">Return code</span></span>                                                                                               | <span data-ttu-id="f8832-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f8832-112">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8832-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f8832-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="f8832-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="f8832-114">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="f8832-115"><dt>**\_интерфейс E**</dt></span><span class="sxs-lookup"><span data-stu-id="f8832-115"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="f8832-116">ПИН-код ввода не поддерживает [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span><span class="sxs-lookup"><span data-stu-id="f8832-116">Input pin does not support [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span></span><br/> |
| <dl> <span data-ttu-id="f8832-117"><dt>**VFW \_ E \_ недопустимое \_ направление**</dt></span><span class="sxs-lookup"><span data-stu-id="f8832-117"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="f8832-118">Направления ПИН-кода несовместимы.</span><span class="sxs-lookup"><span data-stu-id="f8832-118">Pin directions are not compatible.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="f8832-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="f8832-119">Remarks</span></span>

<span data-ttu-id="f8832-120">Этот метод вызывает метод [**кбасепин:: чеккконнект**](cbasepin-checkconnect.md) базового класса, а затем запрашивает входной ПИН-код для своего интерфейса [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="f8832-120">This method calls the base-class [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method, and then queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8832-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f8832-121">Requirements</span></span>



| <span data-ttu-id="f8832-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f8832-122">Requirement</span></span> | <span data-ttu-id="f8832-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f8832-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8832-124">Header</span><span class="sxs-lookup"><span data-stu-id="f8832-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f8832-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8832-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f8832-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f8832-126">Library</span></span><br/> | <dl> <span data-ttu-id="f8832-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f8832-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8832-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f8832-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8832-129">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="f8832-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





---
description: Метод Чеккконнект определяет, подходит ли подключение по ПИН-коду.
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
ms.openlocfilehash: f3274e47e9a77d86f350c17aaca04ec0cdb95ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657520"
---
# <a name="cbaseoutputpincheckconnect-method"></a><span data-ttu-id="06850-103">Кбасеаутпутпин. Чеккконнект, метод</span><span class="sxs-lookup"><span data-stu-id="06850-103">CBaseOutputPin.CheckConnect method</span></span>

<span data-ttu-id="06850-104">`CheckConnect`Метод определяет, подходит ли подключение по ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="06850-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="06850-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06850-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="06850-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="06850-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06850-107">*ппин*</span><span class="sxs-lookup"><span data-stu-id="06850-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="06850-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) входного контакта.</span><span class="sxs-lookup"><span data-stu-id="06850-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06850-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06850-109">Return value</span></span>

<span data-ttu-id="06850-110">Возвращает одно из следующих значений **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06850-110">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="06850-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="06850-111">Return code</span></span>                                                                                               | <span data-ttu-id="06850-112">Описание</span><span class="sxs-lookup"><span data-stu-id="06850-112">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06850-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="06850-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="06850-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="06850-114">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="06850-115"><dt>**\_интерфейс E**</dt></span><span class="sxs-lookup"><span data-stu-id="06850-115"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="06850-116">ПИН-код ввода не поддерживает [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span><span class="sxs-lookup"><span data-stu-id="06850-116">Input pin does not support [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span></span><br/> |
| <dl> <span data-ttu-id="06850-117"><dt>**VFW \_ E \_ недопустимое \_ направление**</dt></span><span class="sxs-lookup"><span data-stu-id="06850-117"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="06850-118">Направления ПИН-кода несовместимы.</span><span class="sxs-lookup"><span data-stu-id="06850-118">Pin directions are not compatible.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="06850-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06850-119">Remarks</span></span>

<span data-ttu-id="06850-120">Этот метод вызывает метод [**кбасепин:: чеккконнект**](cbasepin-checkconnect.md) базового класса, а затем запрашивает входной ПИН-код для своего интерфейса [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="06850-120">This method calls the base-class [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method, and then queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="06850-121">Требования</span><span class="sxs-lookup"><span data-stu-id="06850-121">Requirements</span></span>



| <span data-ttu-id="06850-122">Требование</span><span class="sxs-lookup"><span data-stu-id="06850-122">Requirement</span></span> | <span data-ttu-id="06850-123">Значение</span><span class="sxs-lookup"><span data-stu-id="06850-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06850-124">Header</span><span class="sxs-lookup"><span data-stu-id="06850-124">Header</span></span><br/>  | <dl> <span data-ttu-id="06850-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06850-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="06850-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="06850-126">Library</span></span><br/> | <dl> <span data-ttu-id="06850-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="06850-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06850-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06850-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06850-129">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="06850-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





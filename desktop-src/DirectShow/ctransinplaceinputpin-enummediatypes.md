---
description: 'Ктрансинплацеинпутпин. Енуммедиатипес, метод Енуммедиатипес перечисляет предпочтительные типы мультимедиа для ПИН-кода. Этот метод реализует метод Ипин:: Енуммедиатипес.'
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: Ктрансинплацеинпутпин. Енуммедиатипес, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f9e05d0e9db50cabc700da7b3803c1606efab78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094762"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a><span data-ttu-id="c48fa-104">Ктрансинплацеинпутпин. Енуммедиатипес, метод</span><span class="sxs-lookup"><span data-stu-id="c48fa-104">CTransInPlaceInputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="c48fa-105">`EnumMediaTypes`Метод перечисляет предпочтительные типы мультимедиа для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="c48fa-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="c48fa-106">Этот метод реализует метод [**Ипин:: енуммедиатипес**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="c48fa-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c48fa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c48fa-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="c48fa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c48fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c48fa-109">*ппенум*</span><span class="sxs-lookup"><span data-stu-id="c48fa-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="c48fa-110">Получает указатель на интерфейс [**иенуммедиатипес**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="c48fa-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c48fa-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c48fa-111">Return value</span></span>

<span data-ttu-id="c48fa-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c48fa-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c48fa-113">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c48fa-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c48fa-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c48fa-114">Return code</span></span>                                                                                           | <span data-ttu-id="c48fa-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c48fa-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="c48fa-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c48fa-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="c48fa-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c48fa-117">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="c48fa-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c48fa-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="c48fa-119">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="c48fa-119">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="c48fa-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="c48fa-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="c48fa-121">**Пустой** указатель.</span><span class="sxs-lookup"><span data-stu-id="c48fa-121">**NULL** pointer.</span></span><br/>                |
| <dl> <span data-ttu-id="c48fa-122"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="c48fa-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c48fa-123">Выходной ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="c48fa-123">The output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c48fa-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="c48fa-124">Remarks</span></span>

<span data-ttu-id="c48fa-125">Этот метод возвращает интерфейс **иенуммедиатипес** из нисходящего входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="c48fa-125">This method returns the **IEnumMediaTypes** interface from downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="c48fa-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c48fa-126">Requirements</span></span>



| <span data-ttu-id="c48fa-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c48fa-127">Requirement</span></span> | <span data-ttu-id="c48fa-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c48fa-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c48fa-129">Header</span><span class="sxs-lookup"><span data-stu-id="c48fa-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c48fa-130"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c48fa-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c48fa-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c48fa-131">Library</span></span><br/> | <dl> <span data-ttu-id="c48fa-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c48fa-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c48fa-133">См. также</span><span class="sxs-lookup"><span data-stu-id="c48fa-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c48fa-134">**Класс Ктрансинплацеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="c48fa-134">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 





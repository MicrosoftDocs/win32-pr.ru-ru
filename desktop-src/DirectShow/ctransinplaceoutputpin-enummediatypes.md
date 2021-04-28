---
description: 'Ктрансинплацеаутпутпин. Енуммедиатипес, метод Енуммедиатипес перечисляет предпочтительные типы мультимедиа для ПИН-кода. Этот метод реализует метод Ипин:: Енуммедиатипес.'
ms.assetid: 942c6594-3053-484a-a0f7-286dcd3f7550
title: Ктрансинплацеаутпутпин. Енуммедиатипес, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26dd58f23dc18a086c6c59f6f8a6a098e3449fea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084638"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a><span data-ttu-id="c8ea5-104">Ктрансинплацеаутпутпин. Енуммедиатипес, метод</span><span class="sxs-lookup"><span data-stu-id="c8ea5-104">CTransInPlaceOutputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="c8ea5-105">`EnumMediaTypes`Метод перечисляет предпочтительные типы мультимедиа для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="c8ea5-106">Этот метод реализует метод [**Ипин:: енуммедиатипес**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="c8ea5-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8ea5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8ea5-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="c8ea5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8ea5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8ea5-109">*ппенум*</span><span class="sxs-lookup"><span data-stu-id="c8ea5-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="c8ea5-110">Получает указатель на интерфейс [**иенуммедиатипес**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="c8ea5-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8ea5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8ea5-111">Return value</span></span>

<span data-ttu-id="c8ea5-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c8ea5-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c8ea5-113">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c8ea5-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c8ea5-114">Return code</span></span>                                                                                           | <span data-ttu-id="c8ea5-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c8ea5-115">Description</span></span>                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="c8ea5-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea5-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="c8ea5-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-117">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="c8ea5-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea5-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="c8ea5-119">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-119">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="c8ea5-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea5-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="c8ea5-121">**Пустой** указатель.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-121">**NULL** pointer.</span></span><br/>                        |
| <dl> <span data-ttu-id="c8ea5-122"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea5-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c8ea5-123">Входной ПИН-код фильтра не подключен.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-123">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c8ea5-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="c8ea5-124">Remarks</span></span>

<span data-ttu-id="c8ea5-125">Этот метод возвращает интерфейс **иенуммедиатипес** из вышестоящего выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="c8ea5-125">This method returns the **IEnumMediaTypes** interface from the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8ea5-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c8ea5-126">Requirements</span></span>



| <span data-ttu-id="c8ea5-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c8ea5-127">Requirement</span></span> | <span data-ttu-id="c8ea5-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c8ea5-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ea5-129">Header</span><span class="sxs-lookup"><span data-stu-id="c8ea5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c8ea5-130"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea5-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c8ea5-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c8ea5-131">Library</span></span><br/> | <dl> <span data-ttu-id="c8ea5-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea5-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8ea5-133">См. также</span><span class="sxs-lookup"><span data-stu-id="c8ea5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8ea5-134">**Класс Ктрансинплацеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="c8ea5-134">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 





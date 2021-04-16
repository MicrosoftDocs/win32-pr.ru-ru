---
description: 'Метод Енуммедиатипес перечисляет предпочтительные типы мультимедиа для ПИН-кода. Этот метод реализует метод Ипин:: Енуммедиатипес.'
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
ms.openlocfilehash: ffa634fa695eb0007b49fc1c36c730c7fbde361b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657086"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a><span data-ttu-id="a2696-104">Ктрансинплацеинпутпин. Енуммедиатипес, метод</span><span class="sxs-lookup"><span data-stu-id="a2696-104">CTransInPlaceInputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="a2696-105">`EnumMediaTypes`Метод перечисляет предпочтительные типы мультимедиа для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="a2696-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="a2696-106">Этот метод реализует метод [**Ипин:: енуммедиатипес**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="a2696-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2696-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2696-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="a2696-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2696-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2696-109">*ппенум*</span><span class="sxs-lookup"><span data-stu-id="a2696-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="a2696-110">Получает указатель на интерфейс [**иенуммедиатипес**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="a2696-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2696-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2696-111">Return value</span></span>

<span data-ttu-id="a2696-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a2696-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a2696-113">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a2696-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="a2696-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a2696-114">Return code</span></span>                                                                                           | <span data-ttu-id="a2696-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a2696-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="a2696-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a2696-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="a2696-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="a2696-117">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="a2696-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a2696-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="a2696-119">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="a2696-119">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="a2696-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="a2696-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="a2696-121">**Пустой** указатель.</span><span class="sxs-lookup"><span data-stu-id="a2696-121">**NULL** pointer.</span></span><br/>                |
| <dl> <span data-ttu-id="a2696-122"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="a2696-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="a2696-123">Выходной ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="a2696-123">The output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a2696-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2696-124">Remarks</span></span>

<span data-ttu-id="a2696-125">Этот метод возвращает интерфейс **иенуммедиатипес** из нисходящего входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="a2696-125">This method returns the **IEnumMediaTypes** interface from downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2696-126">Требования</span><span class="sxs-lookup"><span data-stu-id="a2696-126">Requirements</span></span>



| <span data-ttu-id="a2696-127">Требование</span><span class="sxs-lookup"><span data-stu-id="a2696-127">Requirement</span></span> | <span data-ttu-id="a2696-128">Значение</span><span class="sxs-lookup"><span data-stu-id="a2696-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2696-129">Header</span><span class="sxs-lookup"><span data-stu-id="a2696-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a2696-130"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2696-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a2696-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a2696-131">Library</span></span><br/> | <dl> <span data-ttu-id="a2696-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a2696-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2696-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2696-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2696-134">**Класс Ктрансинплацеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="a2696-134">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 





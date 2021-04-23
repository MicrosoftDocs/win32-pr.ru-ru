---
description: Метод Комплетеконнект завершает соединение с входным закреплением.
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: Кбасеаутпутпин. Комплетеконнект, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4614e8531a21d88a1c2f4cfd75fcbe05a9210f13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668778"
---
# <a name="cbaseoutputpincompleteconnect-method"></a><span data-ttu-id="06359-103">Кбасеаутпутпин. Комплетеконнект, метод</span><span class="sxs-lookup"><span data-stu-id="06359-103">CBaseOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="06359-104">`CompleteConnect`Метод завершает соединение с входным закреплением.</span><span class="sxs-lookup"><span data-stu-id="06359-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="06359-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06359-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="06359-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="06359-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06359-107">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="06359-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="06359-108">Указатель на входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="06359-108">Pointer to the input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06359-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06359-109">Return value</span></span>

<span data-ttu-id="06359-110">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="06359-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="06359-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06359-111">Remarks</span></span>

<span data-ttu-id="06359-112">Этот метод переопределяет метод [**кбасепин:: комплетеконнект**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="06359-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="06359-113">Он вызывает метод [**деЦидеаллокатор**](cbaseoutputpin-decideallocator.md) , который выбирает механизм выделения памяти, используемый для этого соединения.</span><span class="sxs-lookup"><span data-stu-id="06359-113">It calls the [**DecideAllocator**](cbaseoutputpin-decideallocator.md) method, which selects the memory allocator to use for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="06359-114">Требования</span><span class="sxs-lookup"><span data-stu-id="06359-114">Requirements</span></span>



| <span data-ttu-id="06359-115">Требование</span><span class="sxs-lookup"><span data-stu-id="06359-115">Requirement</span></span> | <span data-ttu-id="06359-116">Значение</span><span class="sxs-lookup"><span data-stu-id="06359-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06359-117">Header</span><span class="sxs-lookup"><span data-stu-id="06359-117">Header</span></span><br/>  | <dl> <span data-ttu-id="06359-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06359-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="06359-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="06359-119">Library</span></span><br/> | <dl> <span data-ttu-id="06359-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="06359-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06359-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06359-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06359-122">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="06359-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





---
description: Кбасеаутпутпин. Комплетеконнект, метод Комплетеконнект завершает соединение с входным закреплением.
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
ms.openlocfilehash: cd4bc52db99b88c4d6f16c549fbb558bb6423730
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099542"
---
# <a name="cbaseoutputpincompleteconnect-method"></a><span data-ttu-id="cdc8d-103">Кбасеаутпутпин. Комплетеконнект, метод</span><span class="sxs-lookup"><span data-stu-id="cdc8d-103">CBaseOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="cdc8d-104">`CompleteConnect`Метод завершает соединение с входным закреплением.</span><span class="sxs-lookup"><span data-stu-id="cdc8d-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc8d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdc8d-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="cdc8d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cdc8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdc8d-107">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="cdc8d-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="cdc8d-108">Указатель на входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="cdc8d-108">Pointer to the input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdc8d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cdc8d-109">Return value</span></span>

<span data-ttu-id="cdc8d-110">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="cdc8d-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdc8d-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="cdc8d-111">Remarks</span></span>

<span data-ttu-id="cdc8d-112">Этот метод переопределяет метод [**кбасепин:: комплетеконнект**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="cdc8d-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="cdc8d-113">Он вызывает метод [**деЦидеаллокатор**](cbaseoutputpin-decideallocator.md) , который выбирает механизм выделения памяти, используемый для этого соединения.</span><span class="sxs-lookup"><span data-stu-id="cdc8d-113">It calls the [**DecideAllocator**](cbaseoutputpin-decideallocator.md) method, which selects the memory allocator to use for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc8d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cdc8d-114">Requirements</span></span>



| <span data-ttu-id="cdc8d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cdc8d-115">Requirement</span></span> | <span data-ttu-id="cdc8d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cdc8d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc8d-117">Header</span><span class="sxs-lookup"><span data-stu-id="cdc8d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="cdc8d-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdc8d-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cdc8d-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cdc8d-119">Library</span></span><br/> | <dl> <span data-ttu-id="cdc8d-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cdc8d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdc8d-121">См. также</span><span class="sxs-lookup"><span data-stu-id="cdc8d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdc8d-122">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="cdc8d-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





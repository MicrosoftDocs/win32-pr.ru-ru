---
description: Метод Синчронаусблоккаутпутпин блокирует ПИН-код; не возвращает значение, пока ПИН-код не будет заблокирован.
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: Кдинамикаутпутпин. Синчронаусблоккаутпутпин, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fff1a0a1f093b97d07c74d7916ef2a7511d0e16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669358"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a><span data-ttu-id="fbb32-103">Кдинамикаутпутпин. Синчронаусблоккаутпутпин, метод</span><span class="sxs-lookup"><span data-stu-id="fbb32-103">CDynamicOutputPin.SynchronousBlockOutputPin method</span></span>

<span data-ttu-id="fbb32-104">`SynchronousBlockOutputPin`Метод блокирует ПИН-код; не возвращает, пока ПИН-код не будет заблокирован.</span><span class="sxs-lookup"><span data-stu-id="fbb32-104">The `SynchronousBlockOutputPin` method blocks the pin; does not return until the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbb32-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbb32-105">Syntax</span></span>


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="fbb32-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbb32-106">Parameters</span></span>

<span data-ttu-id="fbb32-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fbb32-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fbb32-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fbb32-108">Return value</span></span>

<span data-ttu-id="fbb32-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fbb32-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fbb32-110">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fbb32-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="fbb32-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fbb32-111">Return code</span></span>                                                                                                                    | <span data-ttu-id="fbb32-112">Описание</span><span class="sxs-lookup"><span data-stu-id="fbb32-112">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="fbb32-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fbb32-113"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="fbb32-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="fbb32-114">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="fbb32-115"><dt>**\_ \_ ПИН-код VFW E \_ уже \_ заблокирован**</dt></span><span class="sxs-lookup"><span data-stu-id="fbb32-115"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="fbb32-116">ПИН-код уже заблокирован в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="fbb32-116">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="fbb32-117"><dt>**\_ \_ ПИН-код VFW E \_ уже \_ заблокирован \_ в \_ этом \_ потоке**</dt></span><span class="sxs-lookup"><span data-stu-id="fbb32-117"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="fbb32-118">ПИН-код уже заблокирован в вызывающем потоке.</span><span class="sxs-lookup"><span data-stu-id="fbb32-118">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fbb32-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fbb32-119">Remarks</span></span>

<span data-ttu-id="fbb32-120">Не вызывайте этот метод из потока потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="fbb32-120">Do not call this method from the streaming thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbb32-121">Требования</span><span class="sxs-lookup"><span data-stu-id="fbb32-121">Requirements</span></span>



| <span data-ttu-id="fbb32-122">Требование</span><span class="sxs-lookup"><span data-stu-id="fbb32-122">Requirement</span></span> | <span data-ttu-id="fbb32-123">Значение</span><span class="sxs-lookup"><span data-stu-id="fbb32-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbb32-124">Header</span><span class="sxs-lookup"><span data-stu-id="fbb32-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fbb32-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fbb32-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fbb32-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fbb32-126">Library</span></span><br/> | <dl> <span data-ttu-id="fbb32-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fbb32-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbb32-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbb32-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbb32-129">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="fbb32-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 





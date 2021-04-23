---
description: 'Метод Комплетеконнект завершает соединение с выходным закреплением. Этот метод переопределяет метод Кбасепин:: Комплетеконнект.'
ms.assetid: 32d95815-e018-4724-8cf3-8cd093ede517
title: Крендереринпутпин. Комплетеконнект, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e868693308d40fb786f201a9d7f056dd88326ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658012"
---
# <a name="crendererinputpincompleteconnect-method"></a><span data-ttu-id="6ff7a-104">Крендереринпутпин. Комплетеконнект, метод</span><span class="sxs-lookup"><span data-stu-id="6ff7a-104">CRendererInputPin.CompleteConnect method</span></span>

<span data-ttu-id="6ff7a-105">`CompleteConnect`Метод завершает соединение с выходным закреплением.</span><span class="sxs-lookup"><span data-stu-id="6ff7a-105">The `CompleteConnect` method completes a connection to an output pin.</span></span> <span data-ttu-id="6ff7a-106">Этот метод переопределяет метод [**кбасепин:: комплетеконнект**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="6ff7a-106">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ff7a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ff7a-107">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="6ff7a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ff7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ff7a-109">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="6ff7a-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="6ff7a-110">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) выходного контакта</span><span class="sxs-lookup"><span data-stu-id="6ff7a-110">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ff7a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ff7a-111">Return value</span></span>

<span data-ttu-id="6ff7a-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6ff7a-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ff7a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6ff7a-113">Requirements</span></span>



| <span data-ttu-id="6ff7a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6ff7a-114">Requirement</span></span> | <span data-ttu-id="6ff7a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6ff7a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff7a-116">Header</span><span class="sxs-lookup"><span data-stu-id="6ff7a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6ff7a-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ff7a-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6ff7a-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6ff7a-118">Library</span></span><br/> | <dl> <span data-ttu-id="6ff7a-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6ff7a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ff7a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ff7a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff7a-121">**Класс Крендереринпутпин**</span><span class="sxs-lookup"><span data-stu-id="6ff7a-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 





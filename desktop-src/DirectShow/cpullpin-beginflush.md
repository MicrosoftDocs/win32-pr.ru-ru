---
description: Метод Бегинфлуш информирует фильтр-владелец о необходимости сброса нисходящих фильтров. Производный класс должен реализовывать этот метод.
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: Кпуллпин. Бегинфлуш, метод (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2e4c26b99c78794449077e73040d98b5481fb91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675589"
---
# <a name="cpullpinbeginflush-method"></a><span data-ttu-id="e0d63-104">Кпуллпин. Бегинфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="e0d63-104">CPullPin.BeginFlush method</span></span>

<span data-ttu-id="e0d63-105">`BeginFlush`Метод информирует фильтр-владелец о необходимости сброса нисходящих фильтров.</span><span class="sxs-lookup"><span data-stu-id="e0d63-105">The `BeginFlush` method informs the owning filter to flush the downstream filters.</span></span> <span data-ttu-id="e0d63-106">Производный класс должен реализовывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="e0d63-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0d63-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0d63-107">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="e0d63-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0d63-108">Parameters</span></span>

<span data-ttu-id="e0d63-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e0d63-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0d63-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0d63-110">Return value</span></span>

<span data-ttu-id="e0d63-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e0d63-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0d63-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0d63-112">Remarks</span></span>

<span data-ttu-id="e0d63-113">Метод [**кпуллпин:: Seek**](cpullpin-seek.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="e0d63-113">The [**CPullPin::Seek**](cpullpin-seek.md) method calls this method.</span></span> <span data-ttu-id="e0d63-114">Реализуйте этот метод, чтобы вызвать метод [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) для каждого нисходящиго входного ПИН-кода, получающего данные от этого объекта.</span><span class="sxs-lookup"><span data-stu-id="e0d63-114">Implement this method to call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="e0d63-115">Если закрепление вывода фильтра является производным от [**кбасеаутпутпин**](cbaseoutputpin.md), вызовите метод [**Кбасеаутпутпин::D еливербегинфлуш**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="e0d63-115">If your filter's output pin(s) derive from [**CBaseOutputPin**](cbaseoutputpin.md), call the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span>

<span data-ttu-id="e0d63-116">Такая схема позволяет фильтровать поиск в потоке, просто вызывая метод **Seek** для объекта **кпуллпин** .</span><span class="sxs-lookup"><span data-stu-id="e0d63-116">This design enables the filter to seek the stream simply by calling **Seek** on the **CPullPin** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0d63-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e0d63-117">Requirements</span></span>



| <span data-ttu-id="e0d63-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e0d63-118">Requirement</span></span> | <span data-ttu-id="e0d63-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e0d63-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d63-120">Header</span><span class="sxs-lookup"><span data-stu-id="e0d63-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e0d63-121"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0d63-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="e0d63-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e0d63-122">Library</span></span><br/> | <dl> <span data-ttu-id="e0d63-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e0d63-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0d63-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0d63-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0d63-125">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="e0d63-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 





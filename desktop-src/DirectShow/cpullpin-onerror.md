---
description: Метод OnError вызывается при возникновении ошибки во время потоковой передачи. Производный класс должен реализовывать этот метод.
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: Метод Кпуллпин. OnError (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dc8bf7f307ab56609b5f90f6955a1f666854270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669052"
---
# <a name="cpullpinonerror-method"></a><span data-ttu-id="eedec-104">Кпуллпин. OnError, метод</span><span class="sxs-lookup"><span data-stu-id="eedec-104">CPullPin.OnError method</span></span>

<span data-ttu-id="eedec-105">`OnError`Метод вызывается при возникновении ошибки во время потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="eedec-105">The `OnError` method is called if an error occurs during streaming.</span></span> <span data-ttu-id="eedec-106">Производный класс должен реализовывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="eedec-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eedec-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eedec-107">Syntax</span></span>


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="eedec-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="eedec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eedec-109">*ч*</span><span class="sxs-lookup"><span data-stu-id="eedec-109">*hr*</span></span> 
</dt> <dd>

<span data-ttu-id="eedec-110">Указывает значение **HRESULT** , возвращаемое методом, который завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="eedec-110">Specifies the **HRESULT** value returned by the method that failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eedec-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eedec-111">Return value</span></span>

<span data-ttu-id="eedec-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="eedec-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eedec-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eedec-113">Remarks</span></span>

<span data-ttu-id="eedec-114">Объект вызывает этот метод каждый раз, когда возникает ошибка, которая останавливает поток извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="eedec-114">The object calls this method whenever an error occurs that halts the data-pulling thread.</span></span> <span data-ttu-id="eedec-115">Фильтр может использовать этот метод для корректного устранения ошибок потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="eedec-115">The filter can use this method to recover from streaming errors gracefully.</span></span> <span data-ttu-id="eedec-116">В большинстве случаев ошибка возвращается из вышестоящего фильтра, поэтому вышестоящий фильтр отвечает за передачу отчета диспетчеру графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="eedec-116">In most cases, the error is returned from the upstream filter, so the upstream filter is responsible for reporting it to the Filter Graph Manager.</span></span> <span data-ttu-id="eedec-117">Если ошибка возникает в методе [**кпуллпин:: Receive**](cpullpin-receive.md) , то фильтр должен отправить событие [**EC \_ еррораборт**](ec-errorabort.md) .</span><span class="sxs-lookup"><span data-stu-id="eedec-117">If the error occurs inside the [**CPullPin::Receive**](cpullpin-receive.md) method, your filter should send an [**EC\_ERRORABORT**](ec-errorabort.md) event.</span></span> <span data-ttu-id="eedec-118">(См. [**имедиаевентсинк:: notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)</span><span class="sxs-lookup"><span data-stu-id="eedec-118">(See [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)</span></span>

## <a name="requirements"></a><span data-ttu-id="eedec-119">Требования</span><span class="sxs-lookup"><span data-stu-id="eedec-119">Requirements</span></span>



| <span data-ttu-id="eedec-120">Требование</span><span class="sxs-lookup"><span data-stu-id="eedec-120">Requirement</span></span> | <span data-ttu-id="eedec-121">Значение</span><span class="sxs-lookup"><span data-stu-id="eedec-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eedec-122">Header</span><span class="sxs-lookup"><span data-stu-id="eedec-122">Header</span></span><br/>  | <dl> <span data-ttu-id="eedec-123"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="eedec-123"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="eedec-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eedec-124">Library</span></span><br/> | <dl> <span data-ttu-id="eedec-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="eedec-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eedec-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eedec-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eedec-127">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="eedec-127">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 





---
description: Метод EOS доставляет вызов конца потока входного ПИН-кода.
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: Каутпуткуеуе. EOS, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab05d4ab3f2620c11bd62d566be851e16b28cecd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675895"
---
# <a name="coutputqueueeos-method"></a><span data-ttu-id="546eb-103">Каутпуткуеуе. EOS, метод</span><span class="sxs-lookup"><span data-stu-id="546eb-103">COutputQueue.EOS method</span></span>

<span data-ttu-id="546eb-104">`EOS`Метод доставляет вызов конца потока входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="546eb-104">The `EOS` method delivers an end-of-stream call to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="546eb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="546eb-105">Syntax</span></span>


```C++
void EOS();
```



## <a name="parameters"></a><span data-ttu-id="546eb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="546eb-106">Parameters</span></span>

<span data-ttu-id="546eb-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="546eb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="546eb-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="546eb-108">Return value</span></span>

<span data-ttu-id="546eb-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="546eb-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="546eb-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="546eb-110">Remarks</span></span>

<span data-ttu-id="546eb-111">Если объект использует поток, он помещает в очередь \_ сообщение управления пакетами EOS.</span><span class="sxs-lookup"><span data-stu-id="546eb-111">If the object is using a thread, it queues an EOS\_PACKET control message.</span></span> <span data-ttu-id="546eb-112">Поток доставляет все ожидающие выборки и вызывает метод [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="546eb-112">The thread delivers any pending samples and calls the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method on the input pin.</span></span>

<span data-ttu-id="546eb-113">Если объект не использует поток, он вызывает метод [**каутпуткуеуе:: сенданивай**](coutputqueue-sendanyway.md) для доставки всех ожидающих выборок.</span><span class="sxs-lookup"><span data-stu-id="546eb-113">If the object is not using a thread, it calls the [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) method to deliver any pending samples.</span></span> <span data-ttu-id="546eb-114">Затем он вызывает **Ипин:: EndOfStream** для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="546eb-114">Then it calls **IPin::EndOfStream** on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="546eb-115">Требования</span><span class="sxs-lookup"><span data-stu-id="546eb-115">Requirements</span></span>



| <span data-ttu-id="546eb-116">Требование</span><span class="sxs-lookup"><span data-stu-id="546eb-116">Requirement</span></span> | <span data-ttu-id="546eb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="546eb-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="546eb-118">Header</span><span class="sxs-lookup"><span data-stu-id="546eb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="546eb-119"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="546eb-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="546eb-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="546eb-120">Library</span></span><br/> | <dl> <span data-ttu-id="546eb-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="546eb-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="546eb-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="546eb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="546eb-123">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="546eb-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 





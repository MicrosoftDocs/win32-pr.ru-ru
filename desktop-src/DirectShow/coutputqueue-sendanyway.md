---
description: Метод Сенданивай доставляет все ожидающие выборки.
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: Каутпуткуеуе. Сенданивай, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SendAnyway
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6fa5495371e020310e2367aea7e7bed9ef113f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674878"
---
# <a name="coutputqueuesendanyway-method"></a><span data-ttu-id="32955-103">Каутпуткуеуе. Сенданивай, метод</span><span class="sxs-lookup"><span data-stu-id="32955-103">COutputQueue.SendAnyway method</span></span>

<span data-ttu-id="32955-104">`SendAnyway`Метод доставляет все ожидающие выборки.</span><span class="sxs-lookup"><span data-stu-id="32955-104">The `SendAnyway` method delivers any pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="32955-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32955-105">Syntax</span></span>


```C++
void SendAnyway();
```



## <a name="parameters"></a><span data-ttu-id="32955-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="32955-106">Parameters</span></span>

<span data-ttu-id="32955-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="32955-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32955-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32955-108">Return value</span></span>

<span data-ttu-id="32955-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="32955-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32955-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32955-110">Remarks</span></span>

<span data-ttu-id="32955-111">Если переменная-член [**каутпуткуеуе:: m \_ Ббатчексакт**](coutputqueue-m-bbatchexact.md) имеет **значение true**, объект заполняет массив [**каутпуткуеуе:: m \_ ппсамплес**](coutputqueue-m-ppsamples.md) до того, как он доставляет пакет примеров.</span><span class="sxs-lookup"><span data-stu-id="32955-111">If the [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) member variable is **TRUE**, the object fills the [**COutputQueue::m\_ppSamples**](coutputqueue-m-ppsamples.md) array before it delivers a batch of samples.</span></span> <span data-ttu-id="32955-112">Вызовите этот метод для доставки частичного пакета.</span><span class="sxs-lookup"><span data-stu-id="32955-112">Call this method to deliver a partial batch.</span></span> <span data-ttu-id="32955-113">Например, метод [**каутпуткуеуе:: EOS**](coutputqueue-eos.md) вызывает `SendAnyway` сериализацию сообщений конца потока.</span><span class="sxs-lookup"><span data-stu-id="32955-113">For example, the [**COutputQueue::EOS**](coutputqueue-eos.md) method calls `SendAnyway` to serialize end-of-stream messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="32955-114">Требования</span><span class="sxs-lookup"><span data-stu-id="32955-114">Requirements</span></span>



| <span data-ttu-id="32955-115">Требование</span><span class="sxs-lookup"><span data-stu-id="32955-115">Requirement</span></span> | <span data-ttu-id="32955-116">Значение</span><span class="sxs-lookup"><span data-stu-id="32955-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32955-117">Header</span><span class="sxs-lookup"><span data-stu-id="32955-117">Header</span></span><br/>  | <dl> <span data-ttu-id="32955-118"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32955-118"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="32955-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="32955-119">Library</span></span><br/> | <dl> <span data-ttu-id="32955-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="32955-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32955-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32955-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32955-122">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="32955-122">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 





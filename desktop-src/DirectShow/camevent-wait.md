---
description: Метод Wait блокируется до получения сигнала о событии или до истечения времени ожидания.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: Метод Камевент. Wait (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ab5bc2aabf77fb73739528e99cda7961ae87e9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657775"
---
# <a name="cameventwait-method"></a><span data-ttu-id="fffeb-103">Камевент. Wait, метод</span><span class="sxs-lookup"><span data-stu-id="fffeb-103">CAMEvent.Wait method</span></span>

<span data-ttu-id="fffeb-104">`Wait`Метод блокируется до получения сигнала о событии или до истечения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="fffeb-104">The `Wait` method blocks until the event is signaled, or until a time-out occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="fffeb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fffeb-105">Syntax</span></span>


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a><span data-ttu-id="fffeb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fffeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fffeb-107">*двтимеаут*</span><span class="sxs-lookup"><span data-stu-id="fffeb-107">*dwTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="fffeb-108">Необязательное значение времени ожидания, представленное в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="fffeb-108">Optional time-out value, represented in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fffeb-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fffeb-109">Return value</span></span>

<span data-ttu-id="fffeb-110">Возвращает **значение true** , если событие имеет сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="fffeb-110">Returns **TRUE** if the event is signaled.</span></span> <span data-ttu-id="fffeb-111">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="fffeb-111">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fffeb-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fffeb-112">Remarks</span></span>

<span data-ttu-id="fffeb-113">Для событий автоматического сброса событие сбрасывается в несигнальное состояние, когда этот метод возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fffeb-113">For auto-reset events, the event is reset to a nonsignaled state when this method returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="fffeb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fffeb-114">Requirements</span></span>



| <span data-ttu-id="fffeb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="fffeb-115">Requirement</span></span> | <span data-ttu-id="fffeb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fffeb-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fffeb-117">Header</span><span class="sxs-lookup"><span data-stu-id="fffeb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fffeb-118"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fffeb-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="fffeb-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fffeb-119">Library</span></span><br/> | <dl> <span data-ttu-id="fffeb-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fffeb-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fffeb-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fffeb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fffeb-122">**Класс Камевент**</span><span class="sxs-lookup"><span data-stu-id="fffeb-122">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 





---
description: Метод Стреамингсреадусингаутпутпин определяет, выполняет ли поток потоковую операцию с закреплением.
ms.assetid: b6432a11-4e8b-4eb4-ad8e-aaff9398641b
title: Кдинамикаутпутпин. Стреамингсреадусингаутпутпин, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StreamingThreadUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 797dcb94e227861642de2a05e6edf24f675bb4e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669130"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a><span data-ttu-id="f5aa6-103">Кдинамикаутпутпин. Стреамингсреадусингаутпутпин, метод</span><span class="sxs-lookup"><span data-stu-id="f5aa6-103">CDynamicOutputPin.StreamingThreadUsingOutputPin method</span></span>

<span data-ttu-id="f5aa6-104">Метод Стреамингсреадусингаутпутпин определяет, выполняет ли поток потоковую операцию с закреплением.</span><span class="sxs-lookup"><span data-stu-id="f5aa6-104">The StreamingThreadUsingOutputPin method determines whether any thread is performing a streaming operation on the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5aa6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5aa6-105">Syntax</span></span>


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="f5aa6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5aa6-106">Parameters</span></span>

<span data-ttu-id="f5aa6-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f5aa6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5aa6-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5aa6-108">Return value</span></span>

<span data-ttu-id="f5aa6-109">Возвращает **значение true** , если поток выполняет потоковую операцию над закреплением.</span><span class="sxs-lookup"><span data-stu-id="f5aa6-109">Returns **TRUE** if a thread is performing a streaming operation on the pin.</span></span> <span data-ttu-id="f5aa6-110">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f5aa6-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5aa6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5aa6-111">Remarks</span></span>

<span data-ttu-id="f5aa6-112">Если какие-либо потоки успешно возвращали метод [**кдинамикаутпутпин:: стартусингаутпутпин**](cdynamicoutputpin-startusingoutputpin.md) и не выполнили соответствующий вызов метода [**Кдинамикаутпутпин:: стопусингаутпутпин**](cdynamicoutputpin-stopusingoutputpin.md) , этот метод возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="f5aa6-112">If any threads have successfully returned from the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method and have not made a corresponding call to the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method, this method returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5aa6-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f5aa6-113">Requirements</span></span>



| <span data-ttu-id="f5aa6-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f5aa6-114">Requirement</span></span> | <span data-ttu-id="f5aa6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f5aa6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5aa6-116">Header</span><span class="sxs-lookup"><span data-stu-id="f5aa6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f5aa6-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5aa6-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f5aa6-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f5aa6-118">Library</span></span><br/> | <dl> <span data-ttu-id="f5aa6-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f5aa6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5aa6-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5aa6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5aa6-121">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="f5aa6-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 





---
description: Метод Pause сигнализирует потоку потоковой передачи на активное выполнение.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: Метод Ксаурцестреам. Pause (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6f7cd3b38144edebd98ca655b32bf6092f44269
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676003"
---
# <a name="csourcestreampause-method"></a><span data-ttu-id="b968a-103">Ксаурцестреам. Pause, метод</span><span class="sxs-lookup"><span data-stu-id="b968a-103">CSourceStream.Pause method</span></span>

<span data-ttu-id="b968a-104">`Pause`Метод сигнализирует потоку потоковой передачи на активность.</span><span class="sxs-lookup"><span data-stu-id="b968a-104">The `Pause` method signals the streaming thread to become active.</span></span>

## <a name="syntax"></a><span data-ttu-id="b968a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b968a-105">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="b968a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b968a-106">Parameters</span></span>

<span data-ttu-id="b968a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b968a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b968a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b968a-108">Return value</span></span>

<span data-ttu-id="b968a-109">Непредвиденное значение: S \_ (ОК или E) \_ .</span><span class="sxs-lookup"><span data-stu-id="b968a-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="b968a-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b968a-110">Remarks</span></span>

<span data-ttu-id="b968a-111">Метод [**ксаурцестреам:: Active**](csourcestream-active.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="b968a-111">The [**CSourceStream::Active**](csourcestream-active.md) method calls this method.</span></span> <span data-ttu-id="b968a-112">Когда метод [**ксаурцестреам:: среадпрок**](csourcestream-threadproc.md) получает этот запрос, он вызывает метод [**Ксаурцестреам::D обуфферпроцессинглуп**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="b968a-112">When the [**CSourceStream::ThreadProc**](csourcestream-threadproc.md) method receives this request, it calls the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b968a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b968a-113">Requirements</span></span>



| <span data-ttu-id="b968a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b968a-114">Requirement</span></span> | <span data-ttu-id="b968a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b968a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b968a-116">Header</span><span class="sxs-lookup"><span data-stu-id="b968a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b968a-117"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b968a-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b968a-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b968a-118">Library</span></span><br/> | <dl> <span data-ttu-id="b968a-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b968a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b968a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b968a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b968a-121">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="b968a-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 





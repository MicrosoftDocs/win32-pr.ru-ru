---
description: Метод GetNext ожидает следующий запрос потока.
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: Метод Ксаурцестреам. WebRequest (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f45e6f6cf269f7aca6741d8e1c150c7054b07f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657627"
---
# <a name="csourcestreamgetrequest-method"></a><span data-ttu-id="5e307-103">Ксаурцестреам. метод запроса</span><span class="sxs-lookup"><span data-stu-id="5e307-103">CSourceStream.GetRequest method</span></span>

<span data-ttu-id="5e307-104">`GetRequest`Метод ожидает следующего запроса потока.</span><span class="sxs-lookup"><span data-stu-id="5e307-104">The `GetRequest` method waits for the next thread request.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e307-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e307-105">Syntax</span></span>


```C++
Command GetRequest();
```



## <a name="parameters"></a><span data-ttu-id="5e307-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e307-106">Parameters</span></span>

<span data-ttu-id="5e307-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5e307-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e307-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e307-108">Return value</span></span>

<span data-ttu-id="5e307-109">Возвращает следующий запрос потока.</span><span class="sxs-lookup"><span data-stu-id="5e307-109">Returns the next thread request.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e307-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e307-110">Remarks</span></span>

<span data-ttu-id="5e307-111">Этот метод переопределяет метод [**камсреад:: WebRequest**](camthread-getrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="5e307-111">This method overrides the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span> <span data-ttu-id="5e307-112">Возвращаемое значение приводится к следующему перечислимому типу:</span><span class="sxs-lookup"><span data-stu-id="5e307-112">The return value is cast to the following enumerated type:</span></span>


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a><span data-ttu-id="5e307-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5e307-113">Requirements</span></span>



| <span data-ttu-id="5e307-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5e307-114">Requirement</span></span> | <span data-ttu-id="5e307-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5e307-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e307-116">Header</span><span class="sxs-lookup"><span data-stu-id="5e307-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5e307-117"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e307-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5e307-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5e307-118">Library</span></span><br/> | <dl> <span data-ttu-id="5e307-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5e307-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e307-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e307-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e307-121">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="5e307-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 





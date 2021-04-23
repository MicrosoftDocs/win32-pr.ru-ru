---
description: Метод Жетрекуестпарам извлекает последний запрос.
ms.assetid: f5bf4935-29ea-45b9-a57e-9fdcd9cde20a
title: Камсреад. Жетрекуестпарам, метод (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestParam
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dd6584123663bb36f1db4771fb3f86d7ac4f5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689105"
---
# <a name="camthreadgetrequestparam-method"></a><span data-ttu-id="4c709-103">Камсреад. Жетрекуестпарам, метод</span><span class="sxs-lookup"><span data-stu-id="4c709-103">CAMThread.GetRequestParam method</span></span>

<span data-ttu-id="4c709-104">`GetRequestParam`Метод получает последний запрос.</span><span class="sxs-lookup"><span data-stu-id="4c709-104">The `GetRequestParam` method retrieves the latest request.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c709-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c709-105">Syntax</span></span>


```C++
DWORD GetRequestParam() const;
```



## <a name="parameters"></a><span data-ttu-id="4c709-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c709-106">Parameters</span></span>

<span data-ttu-id="4c709-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4c709-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c709-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c709-108">Return value</span></span>

<span data-ttu-id="4c709-109">Возвращает значение параметра, которое было передано в последнее время в метод [**камсреад:: каллворкер**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="4c709-109">Returns the value of the parameter that was passed most recently to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c709-110">Требования</span><span class="sxs-lookup"><span data-stu-id="4c709-110">Requirements</span></span>



| <span data-ttu-id="4c709-111">Требование</span><span class="sxs-lookup"><span data-stu-id="4c709-111">Requirement</span></span> | <span data-ttu-id="4c709-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4c709-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c709-113">Header</span><span class="sxs-lookup"><span data-stu-id="4c709-113">Header</span></span><br/>  | <dl> <span data-ttu-id="4c709-114"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c709-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4c709-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4c709-115">Library</span></span><br/> | <dl> <span data-ttu-id="4c709-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4c709-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c709-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c709-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c709-118">**Класс Камсреад**</span><span class="sxs-lookup"><span data-stu-id="4c709-118">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 





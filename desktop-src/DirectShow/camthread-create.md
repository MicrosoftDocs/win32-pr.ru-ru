---
description: Метод Create создает поток.
ms.assetid: 453972eb-7cf6-43c6-820e-c1992675260e
title: Метод Камсреад. Create (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Create
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0316cf053326d23d45c0d82f3c410d68d68a92dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689098"
---
# <a name="camthreadcreate-method"></a><span data-ttu-id="54e11-103">Камсреад. Create, метод</span><span class="sxs-lookup"><span data-stu-id="54e11-103">CAMThread.Create method</span></span>

<span data-ttu-id="54e11-104">`Create`Метод создает поток.</span><span class="sxs-lookup"><span data-stu-id="54e11-104">The `Create` method creates the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="54e11-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54e11-105">Syntax</span></span>


```C++
BOOL Create();
```



## <a name="parameters"></a><span data-ttu-id="54e11-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="54e11-106">Parameters</span></span>

<span data-ttu-id="54e11-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="54e11-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="54e11-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54e11-108">Return value</span></span>

<span data-ttu-id="54e11-109">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="54e11-109">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="54e11-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54e11-110">Remarks</span></span>

<span data-ttu-id="54e11-111">Этот метод создает поток, используя метод [**камсреад:: инитиалсреадпрок**](camthread-initialthreadproc.md) для процедуры потока и `this` для аргумента потока.</span><span class="sxs-lookup"><span data-stu-id="54e11-111">This method creates the thread, using the [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method for the thread procedure and `this` for the thread argument.</span></span>

<span data-ttu-id="54e11-112">Метод завершается ошибкой, если поток уже существует.</span><span class="sxs-lookup"><span data-stu-id="54e11-112">The method fails if the thread already exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="54e11-113">Требования</span><span class="sxs-lookup"><span data-stu-id="54e11-113">Requirements</span></span>



| <span data-ttu-id="54e11-114">Требование</span><span class="sxs-lookup"><span data-stu-id="54e11-114">Requirement</span></span> | <span data-ttu-id="54e11-115">Значение</span><span class="sxs-lookup"><span data-stu-id="54e11-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54e11-116">Header</span><span class="sxs-lookup"><span data-stu-id="54e11-116">Header</span></span><br/>  | <dl> <span data-ttu-id="54e11-117"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54e11-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="54e11-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="54e11-118">Library</span></span><br/> | <dl> <span data-ttu-id="54e11-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="54e11-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54e11-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54e11-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54e11-121">**Класс Камсреад**</span><span class="sxs-lookup"><span data-stu-id="54e11-121">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 





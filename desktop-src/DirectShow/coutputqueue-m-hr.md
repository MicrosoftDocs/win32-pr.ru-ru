---
description: Значение HRESULT, указывающее, будет ли объект принимать выборки. Если значение равно S \_ , объект будет принимать выборки. В противном случае он отклоняет выборки.
ms.assetid: e05d4d2e-cc3e-4b83-8531-bc4bd6d665ac
title: 'Элемент Каутпуткуеуе:: m_hr (Аутпутк. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hr
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b786afa24f974d5eab7e13062105f26386da1c30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665489"
---
# <a name="coutputqueuem_hr-member"></a><span data-ttu-id="258a5-105">Каутпуткуеуе:: m \_ HR, элемент</span><span class="sxs-lookup"><span data-stu-id="258a5-105">COutputQueue::m\_hr member</span></span>

<span data-ttu-id="258a5-106">Значение **HRESULT** , указывающее, будет ли объект принимать выборки.</span><span class="sxs-lookup"><span data-stu-id="258a5-106">**HRESULT** value that indicates whether the object will accept samples.</span></span> <span data-ttu-id="258a5-107">Если значение равно S \_ , объект будет принимать выборки.</span><span class="sxs-lookup"><span data-stu-id="258a5-107">If the value is S\_OK, the object will accept samples.</span></span> <span data-ttu-id="258a5-108">В противном случае он отклоняет выборки.</span><span class="sxs-lookup"><span data-stu-id="258a5-108">Otherwise, it rejects samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="258a5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="258a5-109">Syntax</span></span>


```C++
HRESULT m_hr;
```



## <a name="remarks"></a><span data-ttu-id="258a5-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="258a5-110">Remarks</span></span>

<span data-ttu-id="258a5-111">Эта переменная-член используется для координации действий между потоками.</span><span class="sxs-lookup"><span data-stu-id="258a5-111">This member variable is used to coordinate activities across threads.</span></span> <span data-ttu-id="258a5-112">Если перечислитель входных данных отклоняет выборку или если объект начинает запись на диск, то для него устанавливается значение S \_ false или код ошибки.</span><span class="sxs-lookup"><span data-stu-id="258a5-112">If the downstream input pin rejects a sample, or if the object begins flushing, the value is set to S\_FALSE or an error code.</span></span> <span data-ttu-id="258a5-113">Объект не будет доставлять выборки до завершения очистки или до вызова метода [**каутпуткуеуе:: Reset**](coutputqueue-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="258a5-113">The object will not deliver any more samples until flushing is complete, or until the [**COutputQueue::Reset**](coutputqueue-reset.md) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="258a5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="258a5-114">Requirements</span></span>



| <span data-ttu-id="258a5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="258a5-115">Requirement</span></span> | <span data-ttu-id="258a5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="258a5-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="258a5-117">Header</span><span class="sxs-lookup"><span data-stu-id="258a5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="258a5-118"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="258a5-118"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="258a5-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="258a5-119">Library</span></span><br/> | <dl> <span data-ttu-id="258a5-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="258a5-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="258a5-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="258a5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="258a5-122">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="258a5-122">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 





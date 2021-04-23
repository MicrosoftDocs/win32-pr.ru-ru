---
description: Метод деструктора.
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: Деструктор Камсреад. ~ Камсреад (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.~CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0b0a4dde858811a75347105b9fccd2f499c4faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657457"
---
# <a name="camthreadcamthread-destructor"></a><span data-ttu-id="c75ec-103">Деструктор Камсреад. ~ Камсреад</span><span class="sxs-lookup"><span data-stu-id="c75ec-103">CAMThread.~CAMThread destructor</span></span>

<span data-ttu-id="c75ec-104">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="c75ec-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c75ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c75ec-105">Syntax</span></span>


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a><span data-ttu-id="c75ec-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="c75ec-106">Remarks</span></span>

<span data-ttu-id="c75ec-107">Деструктор вызывает метод [**камсреад:: Close**](camthread-close.md) , который ожидает выхода из потока.</span><span class="sxs-lookup"><span data-stu-id="c75ec-107">The destructor calls the [**CAMThread::Close**](camthread-close.md) method, which waits for the thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="c75ec-108">Требования</span><span class="sxs-lookup"><span data-stu-id="c75ec-108">Requirements</span></span>



| <span data-ttu-id="c75ec-109">Требование</span><span class="sxs-lookup"><span data-stu-id="c75ec-109">Requirement</span></span> | <span data-ttu-id="c75ec-110">Значение</span><span class="sxs-lookup"><span data-stu-id="c75ec-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c75ec-111">Header</span><span class="sxs-lookup"><span data-stu-id="c75ec-111">Header</span></span><br/>  | <dl> <span data-ttu-id="c75ec-112"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c75ec-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c75ec-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c75ec-113">Library</span></span><br/> | <dl> <span data-ttu-id="c75ec-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c75ec-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c75ec-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c75ec-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c75ec-116">**Класс Камсреад**</span><span class="sxs-lookup"><span data-stu-id="c75ec-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 





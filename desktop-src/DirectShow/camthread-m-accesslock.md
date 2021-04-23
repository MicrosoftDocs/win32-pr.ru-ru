---
description: Критическая секция, которая блокирует доступ к потоку из других потоков.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: 'Элемент Камсреад:: m_AccessLock (Вксутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_AccessLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6edb4b58b630cfdcfd6eefc43b908cf6aeb0f084
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689104"
---
# <a name="camthreadm_accesslock-member"></a><span data-ttu-id="ee46d-103">Элемент Камсреад:: m \_ акцесслокк</span><span class="sxs-lookup"><span data-stu-id="ee46d-103">CAMThread::m\_AccessLock member</span></span>

<span data-ttu-id="ee46d-104">Критическая секция, которая блокирует доступ к потоку из других потоков.</span><span class="sxs-lookup"><span data-stu-id="ee46d-104">Critical section that locks the thread from being accessed by other threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee46d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee46d-105">Syntax</span></span>


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a><span data-ttu-id="ee46d-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="ee46d-106">Remarks</span></span>

<span data-ttu-id="ee46d-107">Методы [**камсреад:: Create**](camthread-create.md) и [**Камсреад:: каллворкер**](camthread-callworker.md) содержат эту блокировку для сериализации операций в потоке.</span><span class="sxs-lookup"><span data-stu-id="ee46d-107">The [**CAMThread::Create**](camthread-create.md) and [**CAMThread::CallWorker**](camthread-callworker.md) methods hold this lock, to serialize operations on the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee46d-108">Требования</span><span class="sxs-lookup"><span data-stu-id="ee46d-108">Requirements</span></span>



| <span data-ttu-id="ee46d-109">Требование</span><span class="sxs-lookup"><span data-stu-id="ee46d-109">Requirement</span></span> | <span data-ttu-id="ee46d-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ee46d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee46d-111">Header</span><span class="sxs-lookup"><span data-stu-id="ee46d-111">Header</span></span><br/>  | <dl> <span data-ttu-id="ee46d-112"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee46d-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ee46d-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ee46d-113">Library</span></span><br/> | <dl> <span data-ttu-id="ee46d-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ee46d-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee46d-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee46d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee46d-116">**Класс Камсреад**</span><span class="sxs-lookup"><span data-stu-id="ee46d-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 





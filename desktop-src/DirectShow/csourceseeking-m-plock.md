---
description: Указатель на объект критической секции.
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: 'Элемент Ксаурцесикинг:: m_pLock (Ктлутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f8de9159e917d24701635a428e0f5e6a1b9cb55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688971"
---
# <a name="csourceseekingm_plock-member"></a><span data-ttu-id="90259-103">Элемент Ксаурцесикинг:: m \_ плокк</span><span class="sxs-lookup"><span data-stu-id="90259-103">CSourceSeeking::m\_pLock member</span></span>

<span data-ttu-id="90259-104">Указатель на объект критической секции.</span><span class="sxs-lookup"><span data-stu-id="90259-104">Pointer to a critical section object.</span></span> <span data-ttu-id="90259-105">`CSourceSeeking`Класс использует эту критическую секцию для синхронизации доступа к переменным времени начала и окончания, длительности и скорости.</span><span class="sxs-lookup"><span data-stu-id="90259-105">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and rate variables.</span></span> <span data-ttu-id="90259-106">Эта переменная инициализируется в методе-конструкторе. см. раздел [**ксаурцесикинг:: ксаурцесикинг**](csourceseeking-csourceseeking.md).</span><span class="sxs-lookup"><span data-stu-id="90259-106">This variable is initialized in the constructor method; see [**CSourceSeeking::CSourceSeeking**](csourceseeking-csourceseeking.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="90259-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90259-107">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a><span data-ttu-id="90259-108">Требования</span><span class="sxs-lookup"><span data-stu-id="90259-108">Requirements</span></span>



| <span data-ttu-id="90259-109">Требование</span><span class="sxs-lookup"><span data-stu-id="90259-109">Requirement</span></span> | <span data-ttu-id="90259-110">Значение</span><span class="sxs-lookup"><span data-stu-id="90259-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90259-111">Header</span><span class="sxs-lookup"><span data-stu-id="90259-111">Header</span></span><br/>  | <dl> <span data-ttu-id="90259-112"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90259-112"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="90259-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="90259-113">Library</span></span><br/> | <dl> <span data-ttu-id="90259-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="90259-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90259-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90259-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90259-116">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="90259-116">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





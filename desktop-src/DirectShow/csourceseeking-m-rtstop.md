---
description: Время окончания. По умолчанию для этого параметра задано очень большое число. Производный класс может сбрасывать значение в его конструкторе или при инициализации фильтра.
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: 'Элемент Ксаурцесикинг:: m_rtStop (Ктлутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28031f245ef877eca38129df2a86210f90093db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657653"
---
# <a name="csourceseekingm_rtstop-member"></a><span data-ttu-id="4f28a-105">Элемент Ксаурцесикинг:: m \_ ртстоп</span><span class="sxs-lookup"><span data-stu-id="4f28a-105">CSourceSeeking::m\_rtStop member</span></span>

<span data-ttu-id="4f28a-106">Время окончания.</span><span class="sxs-lookup"><span data-stu-id="4f28a-106">Stop time.</span></span> <span data-ttu-id="4f28a-107">По умолчанию для этого параметра задано очень большое число.</span><span class="sxs-lookup"><span data-stu-id="4f28a-107">By default, the value is set to a very large number.</span></span> <span data-ttu-id="4f28a-108">Производный класс может сбрасывать значение в его конструкторе или при инициализации фильтра.</span><span class="sxs-lookup"><span data-stu-id="4f28a-108">The derived class can reset the value in its constructor, or when the filter is initialized.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f28a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f28a-109">Syntax</span></span>


```C++
CRefTime m_rtStop;
```



## <a name="remarks"></a><span data-ttu-id="4f28a-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="4f28a-110">Remarks</span></span>

<span data-ttu-id="4f28a-111">Чтобы получить доступ к этой переменной, удерживайте критический раздел **m \_ плокк** .</span><span class="sxs-lookup"><span data-stu-id="4f28a-111">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f28a-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4f28a-112">Requirements</span></span>



| <span data-ttu-id="4f28a-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4f28a-113">Requirement</span></span> | <span data-ttu-id="4f28a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4f28a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f28a-115">Header</span><span class="sxs-lookup"><span data-stu-id="4f28a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="4f28a-116"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f28a-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4f28a-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4f28a-117">Library</span></span><br/> | <dl> <span data-ttu-id="4f28a-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4f28a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f28a-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f28a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f28a-120">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="4f28a-120">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





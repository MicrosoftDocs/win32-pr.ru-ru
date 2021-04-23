---
description: Количество невыполненных блокировок для этого объекта.
ms.assetid: 27506c1d-6a9a-4410-80fb-6d4f2fd2f824
title: 'Элемент Ккритсек:: m_lockCount (Вксутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lockCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88098a8ded025a899e2092a96308bd6c54750758
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668835"
---
# <a name="ccritsecm_lockcount-member"></a><span data-ttu-id="ad75a-103">Элемент Ккритсек:: m \_ локккаунт</span><span class="sxs-lookup"><span data-stu-id="ad75a-103">CCritSec::m\_lockCount member</span></span>

<span data-ttu-id="ad75a-104">Количество невыполненных блокировок для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="ad75a-104">Number of outstanding locks on this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad75a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad75a-105">Syntax</span></span>


```C++
DWORD m_lockCount;
```



## <a name="remarks"></a><span data-ttu-id="ad75a-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="ad75a-106">Remarks</span></span>

<span data-ttu-id="ad75a-107">Эта переменная-член определена только в отладочной версии базового класса.</span><span class="sxs-lookup"><span data-stu-id="ad75a-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="ad75a-108">Функции [отладки критического раздела](critical-section-debugging-functions.md) используют этот элемент.</span><span class="sxs-lookup"><span data-stu-id="ad75a-108">The [Critical Section Debugging Functions](critical-section-debugging-functions.md) functions use this member.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad75a-109">Требования</span><span class="sxs-lookup"><span data-stu-id="ad75a-109">Requirements</span></span>



| <span data-ttu-id="ad75a-110">Требование</span><span class="sxs-lookup"><span data-stu-id="ad75a-110">Requirement</span></span> | <span data-ttu-id="ad75a-111">Значение</span><span class="sxs-lookup"><span data-stu-id="ad75a-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad75a-112">Header</span><span class="sxs-lookup"><span data-stu-id="ad75a-112">Header</span></span><br/>  | <dl> <span data-ttu-id="ad75a-113"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad75a-113"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ad75a-114">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ad75a-114">Library</span></span><br/> | <dl> <span data-ttu-id="ad75a-115"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ad75a-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad75a-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad75a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad75a-117">**Класс Ккритсек**</span><span class="sxs-lookup"><span data-stu-id="ad75a-117">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 





---
description: Идентификатор потока владеющего потока.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: 'Элемент Ккритсек:: m_currentOwner (Вксутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6dcb8d968f1f437087a94c5b08db12d31952d92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657953"
---
# <a name="ccritsecm_currentowner-member"></a><span data-ttu-id="c3d1d-103">Элемент Ккритсек:: m \_ куррентовнер</span><span class="sxs-lookup"><span data-stu-id="c3d1d-103">CCritSec::m\_currentOwner member</span></span>

<span data-ttu-id="c3d1d-104">Идентификатор потока владеющего потока.</span><span class="sxs-lookup"><span data-stu-id="c3d1d-104">Thread identifier of the owning thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d1d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3d1d-105">Syntax</span></span>


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a><span data-ttu-id="c3d1d-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="c3d1d-106">Remarks</span></span>

<span data-ttu-id="c3d1d-107">Эта переменная-член определена только в отладочной версии базового класса.</span><span class="sxs-lookup"><span data-stu-id="c3d1d-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="c3d1d-108">[Функции отладки критического раздела](critical-section-debugging-functions.md) используют этот элемент.</span><span class="sxs-lookup"><span data-stu-id="c3d1d-108">The [Critical Section Debugging Functions](critical-section-debugging-functions.md) use this member.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3d1d-109">Требования</span><span class="sxs-lookup"><span data-stu-id="c3d1d-109">Requirements</span></span>



| <span data-ttu-id="c3d1d-110">Требование</span><span class="sxs-lookup"><span data-stu-id="c3d1d-110">Requirement</span></span> | <span data-ttu-id="c3d1d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="c3d1d-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d1d-112">Header</span><span class="sxs-lookup"><span data-stu-id="c3d1d-112">Header</span></span><br/>  | <dl> <span data-ttu-id="c3d1d-113"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3d1d-113"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c3d1d-114">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c3d1d-114">Library</span></span><br/> | <dl> <span data-ttu-id="c3d1d-115"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c3d1d-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3d1d-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3d1d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d1d-117">**Класс Ккритсек**</span><span class="sxs-lookup"><span data-stu-id="c3d1d-117">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 





---
description: Указатель на критическую секцию.
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: 'Элемент Кбасемедиафилтер:: m_pLock (Амфилтер. h)'
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
ms.openlocfilehash: 126aa213004dd032eea43b28198b6f8b49fe7f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657659"
---
# <a name="cbasemediafilterm_plock-member"></a><span data-ttu-id="ba5b4-103">Элемент Кбасемедиафилтер:: m \_ плокк</span><span class="sxs-lookup"><span data-stu-id="ba5b4-103">CBaseMediaFilter::m\_pLock member</span></span>

<span data-ttu-id="ba5b4-104">Указатель на критическую секцию.</span><span class="sxs-lookup"><span data-stu-id="ba5b4-104">Pointer to a critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba5b4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba5b4-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a><span data-ttu-id="ba5b4-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="ba5b4-106">Remarks</span></span>

<span data-ttu-id="ba5b4-107">Критическая секция удерживается во время переходов между состояниями ([**кбасемедиафилтер:: Run**](cbasemediafilter-run.md), [**кбасемедиафилтер::P Аусе**](cbasemediafilter-pause.md), [**кбасемедиафилтер:: останавливаются**](cbasemediafilter-stop.md)) при доступе к эталонному времени ([**кбасемедиафилтер:: сетсинксаурце**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter:: GetSyncSource**](cbasemediafilter-getsyncsource.md)) и в методе [**CBaseMediaFilter::**](cbasemediafilter-isactive.md) IsReference.</span><span class="sxs-lookup"><span data-stu-id="ba5b4-107">The critical section is held during state transitions ([**CBaseMediaFilter::Run**](cbasemediafilter-run.md), [**CBaseMediaFilter::Pause**](cbasemediafilter-pause.md), [**CBaseMediaFilter::Stop**](cbasemediafilter-stop.md)), when accessing the reference clock ([**CBaseMediaFilter::SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter::GetSyncSource**](cbasemediafilter-getsyncsource.md)), and in the [**CBaseMediaFilter::IsActive**](cbasemediafilter-isactive.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba5b4-108">Требования</span><span class="sxs-lookup"><span data-stu-id="ba5b4-108">Requirements</span></span>



| <span data-ttu-id="ba5b4-109">Требование</span><span class="sxs-lookup"><span data-stu-id="ba5b4-109">Requirement</span></span> | <span data-ttu-id="ba5b4-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ba5b4-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba5b4-111">Header</span><span class="sxs-lookup"><span data-stu-id="ba5b4-111">Header</span></span><br/>  | <dl> <span data-ttu-id="ba5b4-112"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba5b4-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ba5b4-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ba5b4-113">Library</span></span><br/> | <dl> <span data-ttu-id="ba5b4-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ba5b4-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba5b4-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba5b4-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba5b4-116">**Класс Кбасемедиафилтер**</span><span class="sxs-lookup"><span data-stu-id="ba5b4-116">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 





---
description: Метод Сетсинксаурце задает часы, используемые для времени.
ms.assetid: 646d4d24-f9b7-438a-b842-58e90eb6a945
title: Ккмдкуеуе. Сетсинксаурце, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 995df3afa5185d8f50278899ac6a5d67dc6d230e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656850"
---
# <a name="ccmdqueuesetsyncsource-method"></a><span data-ttu-id="f6e31-103">Ккмдкуеуе. Сетсинксаурце, метод</span><span class="sxs-lookup"><span data-stu-id="f6e31-103">CCmdQueue.SetSyncSource method</span></span>

<span data-ttu-id="f6e31-104">`SetSyncSource`Метод задает часы, используемые для времени.</span><span class="sxs-lookup"><span data-stu-id="f6e31-104">The `SetSyncSource` method sets the clock used for timing.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6e31-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6e31-105">Syntax</span></span>


```C++
virtual HRESULT SetSyncSource(
   IReferenceClock *pIrc
);
```



## <a name="parameters"></a><span data-ttu-id="f6e31-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6e31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6e31-107">*пирк*</span><span class="sxs-lookup"><span data-stu-id="f6e31-107">*pIrc*</span></span> 
</dt> <dd>

<span data-ttu-id="f6e31-108">Указатель на интерфейс [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) .</span><span class="sxs-lookup"><span data-stu-id="f6e31-108">Pointer to the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6e31-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6e31-109">Return value</span></span>

<span data-ttu-id="f6e31-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f6e31-110">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6e31-111">Требования</span><span class="sxs-lookup"><span data-stu-id="f6e31-111">Requirements</span></span>



| <span data-ttu-id="f6e31-112">Требование</span><span class="sxs-lookup"><span data-stu-id="f6e31-112">Requirement</span></span> | <span data-ttu-id="f6e31-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f6e31-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6e31-114">Header</span><span class="sxs-lookup"><span data-stu-id="f6e31-114">Header</span></span><br/>  | <dl> <span data-ttu-id="f6e31-115"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6e31-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f6e31-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f6e31-116">Library</span></span><br/> | <dl> <span data-ttu-id="f6e31-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f6e31-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6e31-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6e31-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6e31-119">**Класс Ккмдкуеуе**</span><span class="sxs-lookup"><span data-stu-id="f6e31-119">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 





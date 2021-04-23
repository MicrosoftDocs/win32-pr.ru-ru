---
description: Метод Run переключается в режим выполнения, чтобы можно было выполнить команды, отложенные в потокового времени.
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: Метод Ккмдкуеуе. Run (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 424914e53a12ff0f43e8b7e2a3345c28d84437d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674863"
---
# <a name="ccmdqueuerun-method"></a><span data-ttu-id="d89ba-103">Ккмдкуеуе. Run, метод</span><span class="sxs-lookup"><span data-stu-id="d89ba-103">CCmdQueue.Run method</span></span>

<span data-ttu-id="d89ba-104">`Run`Метод переключается в режим выполнения, чтобы можно было выполнить команды, отложенные потоком времени.</span><span class="sxs-lookup"><span data-stu-id="d89ba-104">The `Run` method switches to running mode so that commands that are deferred by the stream time can be run.</span></span>

## <a name="syntax"></a><span data-ttu-id="d89ba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d89ba-105">Syntax</span></span>


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a><span data-ttu-id="d89ba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d89ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d89ba-107">*тстреамтимеоффсет*</span><span class="sxs-lookup"><span data-stu-id="d89ba-107">*tStreamTimeOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="d89ba-108">Время смещения.</span><span class="sxs-lookup"><span data-stu-id="d89ba-108">Offset time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d89ba-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d89ba-109">Return value</span></span>

<span data-ttu-id="d89ba-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d89ba-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d89ba-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d89ba-111">Remarks</span></span>

<span data-ttu-id="d89ba-112">Во время выполнения поддерживается сопоставление потоков во время презентации.</span><span class="sxs-lookup"><span data-stu-id="d89ba-112">During running mode, stream-time-to-presentation-time mapping is known.</span></span>

## <a name="requirements"></a><span data-ttu-id="d89ba-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d89ba-113">Requirements</span></span>



| <span data-ttu-id="d89ba-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d89ba-114">Requirement</span></span> | <span data-ttu-id="d89ba-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d89ba-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d89ba-116">Header</span><span class="sxs-lookup"><span data-stu-id="d89ba-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d89ba-117"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d89ba-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d89ba-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d89ba-118">Library</span></span><br/> | <dl> <span data-ttu-id="d89ba-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d89ba-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d89ba-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d89ba-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d89ba-121">**Класс Ккмдкуеуе**</span><span class="sxs-lookup"><span data-stu-id="d89ba-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 





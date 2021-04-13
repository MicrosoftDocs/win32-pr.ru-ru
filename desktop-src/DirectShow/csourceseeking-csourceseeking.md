---
description: Метод конструктора.
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: Конструктор Ксаурцесикинг. Ксаурцесикинг (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 309e926ddf001cf9933b19334992f5210fc7f17b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657760"
---
# <a name="csourceseekingcsourceseeking-constructor"></a><span data-ttu-id="1020d-103">Ксаурцесикинг. Ксаурцесикинг, конструктор</span><span class="sxs-lookup"><span data-stu-id="1020d-103">CSourceSeeking.CSourceSeeking constructor</span></span>

<span data-ttu-id="1020d-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="1020d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1020d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1020d-105">Syntax</span></span>


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a><span data-ttu-id="1020d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1020d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1020d-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="1020d-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1020d-108">Указатель на строку, содержащую имя объекта.</span><span class="sxs-lookup"><span data-stu-id="1020d-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="1020d-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="1020d-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="1020d-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="1020d-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="1020d-111">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="1020d-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="1020d-112">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="1020d-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="1020d-113">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1020d-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1020d-114">*фр*</span><span class="sxs-lookup"><span data-stu-id="1020d-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="1020d-115">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1020d-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="1020d-116">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="1020d-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="1020d-117">*плокк*</span><span class="sxs-lookup"><span data-stu-id="1020d-117">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="1020d-118">Указатель на объект [**ккритсек**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="1020d-118">Pointer to a [**CCritSec**](ccritsec.md) object.</span></span> <span data-ttu-id="1020d-119">В производном классе объявите переменную-член **ккритсек** и используйте ее адрес для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="1020d-119">In your derived class, declare a **CCritSec** member variable and use the address of it for this parameter.</span></span> <span data-ttu-id="1020d-120">`CSourceSeeking`Класс использует эту критическую секцию для синхронизации доступа к времени начала и окончания, длительности и скорости воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1020d-120">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and playback rate.</span></span> <span data-ttu-id="1020d-121">При каждом обращении к этим переменным в производном классе удерживайте эту блокировку.</span><span class="sxs-lookup"><span data-stu-id="1020d-121">Whenever you access those variables in your derived class, hold this lock.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1020d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1020d-122">Requirements</span></span>



| <span data-ttu-id="1020d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1020d-123">Requirement</span></span> | <span data-ttu-id="1020d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1020d-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1020d-125">Header</span><span class="sxs-lookup"><span data-stu-id="1020d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1020d-126"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1020d-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1020d-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1020d-127">Library</span></span><br/> | <dl> <span data-ttu-id="1020d-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1020d-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1020d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1020d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1020d-130">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="1020d-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





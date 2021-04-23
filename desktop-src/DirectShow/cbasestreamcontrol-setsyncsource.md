---
description: Метод Сетсинксаурце уведомляет базовый класс о текущем ссылочном времени.
ms.assetid: 056385ac-682c-456e-9a5f-86490bd6e05f
title: Кбасестреамконтрол. Сетсинксаурце, метод (Стрмктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60832d1bf7ceca59089875f10579d52cf2cfec4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674798"
---
# <a name="cbasestreamcontrolsetsyncsource-method"></a><span data-ttu-id="2afd2-103">Кбасестреамконтрол. Сетсинксаурце, метод</span><span class="sxs-lookup"><span data-stu-id="2afd2-103">CBaseStreamControl.SetSyncSource method</span></span>

<span data-ttu-id="2afd2-104">`SetSyncSource`Метод уведомляет базовый класс о текущем ссылочном времени.</span><span class="sxs-lookup"><span data-stu-id="2afd2-104">The `SetSyncSource` method notifies the base class of the current reference clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="2afd2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2afd2-105">Syntax</span></span>


```C++
void SetSyncSource(
   IReferenceClock *pRefClock
);
```



## <a name="parameters"></a><span data-ttu-id="2afd2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2afd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2afd2-107">*префклокк*</span><span class="sxs-lookup"><span data-stu-id="2afd2-107">*pRefClock*</span></span> 
</dt> <dd>

<span data-ttu-id="2afd2-108">Указатель на интерфейс [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) ссылочного времени.</span><span class="sxs-lookup"><span data-stu-id="2afd2-108">Pointer to the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface of the reference clock.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2afd2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2afd2-109">Return value</span></span>

<span data-ttu-id="2afd2-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2afd2-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2afd2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2afd2-111">Remarks</span></span>

<span data-ttu-id="2afd2-112">Вызовите этот метод из метода [**имедиафилтер:: сетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) фильтра.</span><span class="sxs-lookup"><span data-stu-id="2afd2-112">Call this method from inside the filter's [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span> <span data-ttu-id="2afd2-113">Класс **кбасестреамконтрол** использует интерфейс **иреференцеклокк** , чтобы предотвратить слишком быстрое удаление примеров.</span><span class="sxs-lookup"><span data-stu-id="2afd2-113">The **CBaseStreamControl** class uses the **IReferenceClock** interface to ensure that it does not discard samples too quickly.</span></span>

## <a name="examples"></a><span data-ttu-id="2afd2-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="2afd2-114">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::SetSyncSource(IReferenceClock *pClock)
{
    // Note: It's OK if pClock is NULL.

    m_pMyPin->SetSyncSource(pClock);
    return CBaseFilter::SetSyncSource(pClock);
}
```



## <a name="requirements"></a><span data-ttu-id="2afd2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2afd2-115">Requirements</span></span>



| <span data-ttu-id="2afd2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2afd2-116">Requirement</span></span> | <span data-ttu-id="2afd2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2afd2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2afd2-118">Header</span><span class="sxs-lookup"><span data-stu-id="2afd2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2afd2-119"><dt>Стрмктл. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2afd2-119"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2afd2-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2afd2-120">Library</span></span><br/> | <dl> <span data-ttu-id="2afd2-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2afd2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2afd2-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2afd2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2afd2-123">**Класс Кбасестреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="2afd2-123">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 





---
description: Метод Нотифифилтерстате уведомляет ПИН-код при изменении состояния фильтра.
ms.assetid: 0eb3b0e5-9c44-464e-b4ca-bcded731e813
title: Кбасестреамконтрол. Нотифифилтерстате, метод (Стрмктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.NotifyFilterState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ccb96361c8f4938bd95ffdc29229a035a239cc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657818"
---
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a><span data-ttu-id="1500a-103">Кбасестреамконтрол. Нотифифилтерстате, метод</span><span class="sxs-lookup"><span data-stu-id="1500a-103">CBaseStreamControl.NotifyFilterState method</span></span>

<span data-ttu-id="1500a-104">`NotifyFilterState`Метод уведомляет ПИН-код при изменении состояния фильтра.</span><span class="sxs-lookup"><span data-stu-id="1500a-104">The `NotifyFilterState` method notifies the pin when the filter's state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1500a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1500a-105">Syntax</span></span>


```C++
void NotifyFilterState(
   FILTER_STATE   new_state,
   REFERENCE_TIME tStart = 0
);
```



## <a name="parameters"></a><span data-ttu-id="1500a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1500a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1500a-107">*новое \_ состояние*</span><span class="sxs-lookup"><span data-stu-id="1500a-107">*new\_state*</span></span> 
</dt> <dd>

<span data-ttu-id="1500a-108">Задает новое состояние в качестве члена перечисления [**\_ состояния фильтра**](/windows/win32/api/strmif/ne-strmif-filter_state) .</span><span class="sxs-lookup"><span data-stu-id="1500a-108">Specifies the new state, as a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="1500a-109">*тстарт*</span><span class="sxs-lookup"><span data-stu-id="1500a-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="1500a-110">Указывает время начала.</span><span class="sxs-lookup"><span data-stu-id="1500a-110">Specifies the start time.</span></span> <span data-ttu-id="1500a-111">Если новое состояние фильтра находится в состоянии \_ выполняется, передайте значение из метода [**имедиафилтер:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="1500a-111">If the new filter state is State\_Running, pass in the value from the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span> <span data-ttu-id="1500a-112">В противном случае используйте значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1500a-112">Otherwise, use the default value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1500a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1500a-113">Return value</span></span>

<span data-ttu-id="1500a-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1500a-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1500a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1500a-115">Remarks</span></span>

<span data-ttu-id="1500a-116">Этот метод заставляет метод [**кбасестреамконтрол:: чеккстреамстате**](cbasestreamcontrol-checkstreamstate.md) прерывать ожидание.</span><span class="sxs-lookup"><span data-stu-id="1500a-116">This method causes the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method to stop waiting.</span></span> <span data-ttu-id="1500a-117">Этот метод следует вызывать каждый раз при изменении состояния фильтра-владельца.</span><span class="sxs-lookup"><span data-stu-id="1500a-117">Call this method whenever the owning filter changes state.</span></span>

## <a name="examples"></a><span data-ttu-id="1500a-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="1500a-118">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::Run(REFERENCE_TIME tStart)
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Running, tStart);
   return CBaseFilter::Run(tStart); // Call the filter base class.
}

STDMETHODIMP CMyFilter::Pause()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Paused);
   return CBaseFilter::Pause();
}

STDMETHODIMP CMyFilter::Stop()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Stopped);
   return CBaseFilter::Stop();
}
```



## <a name="requirements"></a><span data-ttu-id="1500a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1500a-119">Requirements</span></span>



| <span data-ttu-id="1500a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1500a-120">Requirement</span></span> | <span data-ttu-id="1500a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1500a-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1500a-122">Header</span><span class="sxs-lookup"><span data-stu-id="1500a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1500a-123"><dt>Стрмктл. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1500a-123"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1500a-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1500a-124">Library</span></span><br/> | <dl> <span data-ttu-id="1500a-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1500a-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1500a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1500a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1500a-127">**Класс Кбасестреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="1500a-127">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 





---
description: Метод WebMethod получает состояние фильтров (запущено, остановлено или приостановлено).
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: Метод Кбасерендерер. WebMethod (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 451078a6167ff7ca89ad4153c416826af8ac6d05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665348"
---
# <a name="cbaserenderergetstate-method"></a><span data-ttu-id="fc3bb-103">Кбасерендерер. метод State</span><span class="sxs-lookup"><span data-stu-id="fc3bb-103">CBaseRenderer.GetState method</span></span>

<span data-ttu-id="fc3bb-104">`GetState`Метод получает состояние фильтров (запущено, остановлено или приостановлено).</span><span class="sxs-lookup"><span data-stu-id="fc3bb-104">The `GetState` method retrieves the filters's state (running, stopped, or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="fc3bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc3bb-105">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="fc3bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc3bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc3bb-107">*двмиллисекстимеаут*</span><span class="sxs-lookup"><span data-stu-id="fc3bb-107">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="fc3bb-108">Интервал времени ожидания (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="fc3bb-108">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="fc3bb-109">*Состояние*</span><span class="sxs-lookup"><span data-stu-id="fc3bb-109">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="fc3bb-110">Указатель на переменную, которая получает Член перечисляемого [**типа \_ состояния фильтра**](/windows/win32/api/strmif/ne-strmif-filter_state) , указывающий состояние фильтра.</span><span class="sxs-lookup"><span data-stu-id="fc3bb-110">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the filter's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc3bb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc3bb-111">Return value</span></span>

<span data-ttu-id="fc3bb-112">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fc3bb-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="fc3bb-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fc3bb-113">Return code</span></span>                                                                                                | <span data-ttu-id="fc3bb-114">Описание</span><span class="sxs-lookup"><span data-stu-id="fc3bb-114">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="fc3bb-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fc3bb-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="fc3bb-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="fc3bb-116">Success.</span></span><br/>                                            |
| <dl> <span data-ttu-id="fc3bb-117"><dt>**\_ \_ промежуточное состояние VFW S \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc3bb-117"><dt>**VFW\_S\_STATE\_INTERMEDIATE**</dt></span></span> </dl> | <span data-ttu-id="fc3bb-118">Фильтр переходит в указанное состояние.</span><span class="sxs-lookup"><span data-stu-id="fc3bb-118">The filter is transitioning to the indicated state.</span></span><br/> |
| <dl> <span data-ttu-id="fc3bb-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="fc3bb-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="fc3bb-120">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="fc3bb-120">**NULL** pointer argument.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="fc3bb-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc3bb-121">Remarks</span></span>

<span data-ttu-id="fc3bb-122">Этот метод переопределяет метод [**кбасефилтер::**](cbasefilter-getstate.md) WebMethod.</span><span class="sxs-lookup"><span data-stu-id="fc3bb-122">This method overrides the [**CBaseFilter::GetState**](cbasefilter-getstate.md) method.</span></span> <span data-ttu-id="fc3bb-123">Когда модуль подготовки отчетов приостанавливается, он не завершает переход состояния до тех пор, пока не будет получен пример для отображения.</span><span class="sxs-lookup"><span data-stu-id="fc3bb-123">When the renderer is paused, it does not complete the state transition until it receives a sample to render.</span></span> <span data-ttu-id="fc3bb-124">Если время ожидания истекает до завершения перехода состояния, метод возвращает в качестве \_ \_ промежуточного состояния VFW S \_ .</span><span class="sxs-lookup"><span data-stu-id="fc3bb-124">If the time-out expires before the state transition is complete, the method returns VFW\_S\_STATE\_INTERMEDIATE.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc3bb-125">Требования</span><span class="sxs-lookup"><span data-stu-id="fc3bb-125">Requirements</span></span>



| <span data-ttu-id="fc3bb-126">Требование</span><span class="sxs-lookup"><span data-stu-id="fc3bb-126">Requirement</span></span> | <span data-ttu-id="fc3bb-127">Значение</span><span class="sxs-lookup"><span data-stu-id="fc3bb-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc3bb-128">Header</span><span class="sxs-lookup"><span data-stu-id="fc3bb-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fc3bb-129"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc3bb-129"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fc3bb-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fc3bb-130">Library</span></span><br/> | <dl> <span data-ttu-id="fc3bb-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fc3bb-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc3bb-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc3bb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc3bb-133">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="fc3bb-133">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





---
description: 'Метод WebMethod получает состояние фильтров (запущено, остановлено или приостановлено). Этот метод реализует метод Имедиафилтер:: WebMethod.'
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: Метод Кбасефилтер. WebMethod (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c9470e5d71bf71f4e37e6eef84015becdf05f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657804"
---
# <a name="cbasefiltergetstate-method"></a><span data-ttu-id="3fb2e-104">Кбасефилтер. метод State</span><span class="sxs-lookup"><span data-stu-id="3fb2e-104">CBaseFilter.GetState method</span></span>

<span data-ttu-id="3fb2e-105">`GetState`Метод получает состояние фильтров (запущено, остановлено или приостановлено).</span><span class="sxs-lookup"><span data-stu-id="3fb2e-105">The `GetState` method retrieves the filters's state (running, stopped, or paused).</span></span> <span data-ttu-id="3fb2e-106">Этот метод реализует метод [**имедиафилтер::**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) WebMethod.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-106">This method implements the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb2e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3fb2e-107">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="3fb2e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3fb2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fb2e-109">*двмиллисекстимеаут*</span><span class="sxs-lookup"><span data-stu-id="3fb2e-109">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="3fb2e-110">Интервал времени ожидания (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="3fb2e-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="3fb2e-111">*Состояние*</span><span class="sxs-lookup"><span data-stu-id="3fb2e-111">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="3fb2e-112">Указатель на переменную, которая получает Член перечисляемого [**типа \_ состояния фильтра**](/windows/win32/api/strmif/ne-strmif-filter_state) , указывающий состояние фильтра.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-112">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the filter's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fb2e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3fb2e-113">Return value</span></span>

<span data-ttu-id="3fb2e-114">Возвращает значение S \_ (ОК) или \_ указатель E.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-114">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fb2e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3fb2e-115">Remarks</span></span>

<span data-ttu-id="3fb2e-116">В базовом классе все переходы состояния являются синхронными, а параметр *двмиллисекстимеаут* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-116">In the base class, all state transitions are synchronous and the *dwMilliSecsTimeout* parameter is ignored.</span></span> <span data-ttu-id="3fb2e-117">Если производный класс выполняет асинхронные переходы состояний, он должен переопределять этот метод для ожидания во время переходов состояния с истечением времени ожидания *двмиллисекстимеаут* миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="3fb2e-117">If a derived class performs asynchronous state transitions, it should override this method to wait during state transitions, with a time-out of *dwMilliSecsTimeout* milliseconds.</span></span>

<span data-ttu-id="3fb2e-118">Если фильтр не доставляет данные при приостановке, переопределите `GetState` метод, чтобы он возвращал значение VFW S не может быть \_ \_ \_ подсказкой, если фильтр приостановлен (см. раздел [Доставка образцов](delivering-samples.md)).</span><span class="sxs-lookup"><span data-stu-id="3fb2e-118">If your filter does not deliver data while paused, override the `GetState` method to return the value VFW\_S\_CANT\_CUE when the filter is paused (see [Delivering Samples](delivering-samples.md)).</span></span> <span data-ttu-id="3fb2e-119">Пример:</span><span class="sxs-lookup"><span data-stu-id="3fb2e-119">For example:</span></span>


```C++
CMyFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
        return VFW_S_CANT_CUE;
    else
        return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="3fb2e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="3fb2e-120">Requirements</span></span>



| <span data-ttu-id="3fb2e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="3fb2e-121">Requirement</span></span> | <span data-ttu-id="3fb2e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="3fb2e-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb2e-123">Header</span><span class="sxs-lookup"><span data-stu-id="3fb2e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3fb2e-124"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3fb2e-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3fb2e-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3fb2e-125">Library</span></span><br/> | <dl> <span data-ttu-id="3fb2e-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3fb2e-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fb2e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fb2e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb2e-128">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="3fb2e-128">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 





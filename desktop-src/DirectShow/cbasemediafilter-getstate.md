---
description: 'Метод GetObject получает состояние объекта (запущен, остановлен или приостановлен). Этот метод реализует метод Имедиафилтер:: WebMethod.'
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: Метод Кбасемедиафилтер. WebMethod (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eeda91433e0e1474e936902da115e15c37e32e09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665279"
---
# <a name="cbasemediafiltergetstate-method"></a><span data-ttu-id="fe217-104">Кбасемедиафилтер. метод State</span><span class="sxs-lookup"><span data-stu-id="fe217-104">CBaseMediaFilter.GetState method</span></span>

<span data-ttu-id="fe217-105">`GetState`Метод получает состояние объекта (запущен, остановлен или приостановлен).</span><span class="sxs-lookup"><span data-stu-id="fe217-105">The `GetState` method retrieves the object's state (running, stopped, or paused).</span></span> <span data-ttu-id="fe217-106">Этот метод реализует метод [**имедиафилтер::**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) WebMethod.</span><span class="sxs-lookup"><span data-stu-id="fe217-106">This method implements the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe217-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe217-107">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="fe217-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe217-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe217-109">*двмиллисекстимеаут*</span><span class="sxs-lookup"><span data-stu-id="fe217-109">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="fe217-110">Интервал времени ожидания (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="fe217-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="fe217-111">*Состояние*</span><span class="sxs-lookup"><span data-stu-id="fe217-111">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="fe217-112">Указатель на переменную, которая получает член перечислимого [**типа \_ состояния фильтра**](/windows/win32/api/strmif/ne-strmif-filter_state) , указывая состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="fe217-112">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the object's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe217-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe217-113">Return value</span></span>

<span data-ttu-id="fe217-114">Возвращает значение S \_ (ОК) или \_ указатель E.</span><span class="sxs-lookup"><span data-stu-id="fe217-114">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe217-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe217-115">Remarks</span></span>

<span data-ttu-id="fe217-116">В базовом классе все переходы состояния являются синхронными, а параметр *двмиллисекстимеаут* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="fe217-116">In the base class, all state transitions are synchronous and the *dwMilliSecsTimeout* parameter is ignored.</span></span> <span data-ttu-id="fe217-117">Если производный класс выполняет асинхронные переходы состояний, он должен переопределять этот метод для ожидания во время переходов состояния с истечением времени ожидания *двмиллисекстимеаут* миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="fe217-117">If a derived class performs asynchronous state transitions, it should override this method to wait during state transitions, with a time-out of *dwMilliSecsTimeout* milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe217-118">Требования</span><span class="sxs-lookup"><span data-stu-id="fe217-118">Requirements</span></span>



| <span data-ttu-id="fe217-119">Требование</span><span class="sxs-lookup"><span data-stu-id="fe217-119">Requirement</span></span> | <span data-ttu-id="fe217-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fe217-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe217-121">Header</span><span class="sxs-lookup"><span data-stu-id="fe217-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fe217-122"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe217-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fe217-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fe217-123">Library</span></span><br/> | <dl> <span data-ttu-id="fe217-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fe217-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe217-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe217-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe217-126">**Класс Кбасемедиафилтер**</span><span class="sxs-lookup"><span data-stu-id="fe217-126">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 





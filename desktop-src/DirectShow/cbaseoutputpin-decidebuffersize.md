---
description: Кбасеаутпутпин. ДеЦидебуфферсизе, метод ДеЦидебуфферсизе задает требования к буферу.
ms.assetid: 1f7a3424-18ba-4a10-b09f-947ee8585ffa
title: Кбасеаутпутпин. ДеЦидебуфферсизе, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7a76f058e2f9c07a344453db87046704e26280a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099532"
---
# <a name="cbaseoutputpindecidebuffersize-method"></a><span data-ttu-id="a3818-103">Кбасеаутпутпин. ДеЦидебуфферсизе, метод</span><span class="sxs-lookup"><span data-stu-id="a3818-103">CBaseOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="a3818-104">`DecideBufferSize`Метод задает требования к буферу.</span><span class="sxs-lookup"><span data-stu-id="a3818-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3818-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3818-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="a3818-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3818-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3818-107">*паллок*</span><span class="sxs-lookup"><span data-stu-id="a3818-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="a3818-108">Указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя.</span><span class="sxs-lookup"><span data-stu-id="a3818-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a3818-109">*ппропинпутрекуест*</span><span class="sxs-lookup"><span data-stu-id="a3818-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="a3818-110">Указатель на структуру [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая содержит требования к буферу входного контакта.</span><span class="sxs-lookup"><span data-stu-id="a3818-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span> <span data-ttu-id="a3818-111">Если у входного контакта нет каких-либо требований, вызывающий объект должен обнулить члены этой структуры перед вызовом метода.</span><span class="sxs-lookup"><span data-stu-id="a3818-111">If the input pin does not have any requirements, the caller should zero out the members of this structure before calling the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3818-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3818-112">Return value</span></span>

<span data-ttu-id="a3818-113">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="a3818-113">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3818-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="a3818-114">Remarks</span></span>

<span data-ttu-id="a3818-115">Переопределите этот метод в производном классе.</span><span class="sxs-lookup"><span data-stu-id="a3818-115">Override this method in your derived class.</span></span> <span data-ttu-id="a3818-116">Вызовите метод [**имемаллокатор:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) , чтобы указать требования к буферу.</span><span class="sxs-lookup"><span data-stu-id="a3818-116">Call the [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) method to specify your buffer requirements.</span></span> <span data-ttu-id="a3818-117">Как правило, производный класс будет учитывать требования к буферу входного контакта, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="a3818-117">Typically, the derived class will honor the input pin's buffer requirements, but it is not required to.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3818-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a3818-118">Requirements</span></span>



| <span data-ttu-id="a3818-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a3818-119">Requirement</span></span> | <span data-ttu-id="a3818-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a3818-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3818-121">Header</span><span class="sxs-lookup"><span data-stu-id="a3818-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a3818-122"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3818-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a3818-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a3818-123">Library</span></span><br/> | <dl> <span data-ttu-id="a3818-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a3818-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3818-125">См. также</span><span class="sxs-lookup"><span data-stu-id="a3818-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3818-126">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="a3818-126">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 





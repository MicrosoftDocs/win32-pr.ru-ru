---
description: 'Метод SetProperties задает количество выделяемых буферов и размер каждого буфера. Этот метод реализует метод Имемаллокатор:: SetProperties.'
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: Кбасеаллокатор. SetProperties, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 000da3ee359ad727e3af972fc4aa6d0dbbb9133e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689232"
---
# <a name="cbaseallocatorsetproperties-method"></a><span data-ttu-id="6257d-104">Кбасеаллокатор. SetProperties, метод</span><span class="sxs-lookup"><span data-stu-id="6257d-104">CBaseAllocator.SetProperties method</span></span>

<span data-ttu-id="6257d-105">`SetProperties`Метод задает количество выделяемых буферов и размер каждого буфера.</span><span class="sxs-lookup"><span data-stu-id="6257d-105">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span> <span data-ttu-id="6257d-106">Этот метод реализует метод [**имемаллокатор:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) .</span><span class="sxs-lookup"><span data-stu-id="6257d-106">This method implements the [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6257d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6257d-107">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="6257d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6257d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6257d-109">*предпоручение*</span><span class="sxs-lookup"><span data-stu-id="6257d-109">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="6257d-110">Указатель на структуру [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая содержит требования к буферу.</span><span class="sxs-lookup"><span data-stu-id="6257d-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="6257d-111">*пактуал*</span><span class="sxs-lookup"><span data-stu-id="6257d-111">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="6257d-112">Указатель на структуру **\_ свойств распределителя** , которая получает фактические свойства буфера.</span><span class="sxs-lookup"><span data-stu-id="6257d-112">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6257d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6257d-113">Return value</span></span>

<span data-ttu-id="6257d-114">Возвращает одно из следующих значений **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6257d-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="6257d-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6257d-115">Return code</span></span>                                                                                                 | <span data-ttu-id="6257d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6257d-116">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="6257d-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6257d-117"><dt>**S\_OK**</dt></span></span> </dl>                        | <span data-ttu-id="6257d-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="6257d-118">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="6257d-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="6257d-119"><dt>**E\_POINTER**</dt></span></span> </dl>                   | <span data-ttu-id="6257d-120">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="6257d-120">**NULL** pointer argument.</span></span><br/>                                 |
| <dl> <span data-ttu-id="6257d-121"><dt>**VFW \_ E \_ уже \_ зафиксирован**</dt></span><span class="sxs-lookup"><span data-stu-id="6257d-121"><dt>**VFW\_E\_ALREADY\_COMMITTED**</dt></span></span> </dl>   | <span data-ttu-id="6257d-122">Невозможно изменить выделенную память, пока фильтр активен.</span><span class="sxs-lookup"><span data-stu-id="6257d-122">Cannot change allocated memory while the filter is active.</span></span><br/> |
| <dl> <span data-ttu-id="6257d-123"><dt>**VFW \_ E \_ бадалигн**</dt></span><span class="sxs-lookup"><span data-stu-id="6257d-123"><dt>**VFW\_E\_BADALIGN**</dt></span></span> </dl>             | <span data-ttu-id="6257d-124">Указано недопустимое выравнивание.</span><span class="sxs-lookup"><span data-stu-id="6257d-124">An invalid alignment was specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="6257d-125"><dt>**\_ \_ необработанных буферов VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6257d-125"><dt>**VFW\_E\_BUFFERS\_OUTSTANDING**</dt></span></span> </dl> | <span data-ttu-id="6257d-126">Один или несколько буферов все еще активны.</span><span class="sxs-lookup"><span data-stu-id="6257d-126">One or more buffers are still active.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="6257d-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6257d-127">Remarks</span></span>

<span data-ttu-id="6257d-128">Этот метод задает требования к буферу, но не выделяет буферы.</span><span class="sxs-lookup"><span data-stu-id="6257d-128">This method specifies the buffer requirements, but does not allocate any buffers.</span></span> <span data-ttu-id="6257d-129">Вызовите метод [**кбасеаллокатор:: Commit**](cbaseallocator-commit.md) для выделения буферов.</span><span class="sxs-lookup"><span data-stu-id="6257d-129">Call the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method to allocate buffers.</span></span>

<span data-ttu-id="6257d-130">Вызывающий объект выделяет две \_ структуры свойств распределителя.</span><span class="sxs-lookup"><span data-stu-id="6257d-130">The caller allocates two ALLOCATOR\_PROPERTIES structures.</span></span> <span data-ttu-id="6257d-131">Параметр  предусловия содержит требования к буферу вызывающего объекта, включая количество буферов и размер каждого буфера.</span><span class="sxs-lookup"><span data-stu-id="6257d-131">The *pRequest* parameter contains the caller's buffer requirements, including the number of buffers and the size of each buffer.</span></span> <span data-ttu-id="6257d-132">Когда метод возвращает значение, параметр *пактуал* содержит фактические свойства буфера, заданные распределителем.</span><span class="sxs-lookup"><span data-stu-id="6257d-132">When the method returns, the *pActual* parameter contains the actual buffer properties, as set by the allocator.</span></span> <span data-ttu-id="6257d-133">В базовом классе, предполагая, что метод выполняется правильно, фактические свойства всегда соответствуют запрошенным свойствам.</span><span class="sxs-lookup"><span data-stu-id="6257d-133">In the base class, assuming that the method succeeds, the actual properties always match the requested properties.</span></span> <span data-ttu-id="6257d-134">Производные классы могут переопределить это поведение.</span><span class="sxs-lookup"><span data-stu-id="6257d-134">Derived classes might override this behavior.</span></span>

<span data-ttu-id="6257d-135">Распределитель не должен зафиксирован и не должен иметь необработанные буферы.</span><span class="sxs-lookup"><span data-stu-id="6257d-135">The allocator must not be committed, and must not have outstanding buffers.</span></span> <span data-ttu-id="6257d-136">В базовом классе выравнивание должно равняться 1.</span><span class="sxs-lookup"><span data-stu-id="6257d-136">In the base class, the alignment must equal 1.</span></span> <span data-ttu-id="6257d-137">Класс [**кмемаллокатор**](cmemallocator.md) переопределяет это требование.</span><span class="sxs-lookup"><span data-stu-id="6257d-137">The [**CMemAllocator**](cmemallocator.md) class overrides this requirement.</span></span>

## <a name="requirements"></a><span data-ttu-id="6257d-138">Требования</span><span class="sxs-lookup"><span data-stu-id="6257d-138">Requirements</span></span>



| <span data-ttu-id="6257d-139">Требование</span><span class="sxs-lookup"><span data-stu-id="6257d-139">Requirement</span></span> | <span data-ttu-id="6257d-140">Значение</span><span class="sxs-lookup"><span data-stu-id="6257d-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6257d-141">Header</span><span class="sxs-lookup"><span data-stu-id="6257d-141">Header</span></span><br/>  | <dl> <span data-ttu-id="6257d-142"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6257d-142"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6257d-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6257d-143">Library</span></span><br/> | <dl> <span data-ttu-id="6257d-144"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6257d-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6257d-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6257d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6257d-146">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="6257d-146">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 





---
description: Метод SetProperties задает количество выделяемых буферов и размер каждого буфера.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: Кмемаллокатор. SetProperties, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8505916245cca81fdd84132e4523fe9dd03b971b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675666"
---
# <a name="cmemallocatorsetproperties-method"></a><span data-ttu-id="8f8b1-103">Кмемаллокатор. SetProperties, метод</span><span class="sxs-lookup"><span data-stu-id="8f8b1-103">CMemAllocator.SetProperties method</span></span>

<span data-ttu-id="8f8b1-104">`SetProperties`Метод задает количество выделяемых буферов и размер каждого буфера.</span><span class="sxs-lookup"><span data-stu-id="8f8b1-104">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f8b1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f8b1-105">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="8f8b1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f8b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f8b1-107">*предпоручение*</span><span class="sxs-lookup"><span data-stu-id="8f8b1-107">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="8f8b1-108">Указатель на структуру [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая содержит требования к буферу.</span><span class="sxs-lookup"><span data-stu-id="8f8b1-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="8f8b1-109">*пактуал*</span><span class="sxs-lookup"><span data-stu-id="8f8b1-109">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="8f8b1-110">Указатель на структуру **\_ свойств распределителя** , которая получает фактические свойства буфера.</span><span class="sxs-lookup"><span data-stu-id="8f8b1-110">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f8b1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f8b1-111">Return value</span></span>

<span data-ttu-id="8f8b1-112">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8f8b1-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="8f8b1-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8f8b1-113">Return code</span></span>                                                                                                 | <span data-ttu-id="8f8b1-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8f8b1-114">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f8b1-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8f8b1-115"><dt>**S\_OK**</dt></span></span> </dl>                        | <span data-ttu-id="8f8b1-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="8f8b1-116">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="8f8b1-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="8f8b1-117"><dt>**E\_POINTER**</dt></span></span> </dl>                   | <span data-ttu-id="8f8b1-118">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="8f8b1-118">**NULL** pointer argument.</span></span><br/>                                 |
| <dl> <span data-ttu-id="8f8b1-119"><dt>**VFW \_ E \_ уже \_ зафиксирован**</dt></span><span class="sxs-lookup"><span data-stu-id="8f8b1-119"><dt>**VFW\_E\_ALREADY\_COMMITTED**</dt></span></span> </dl>   | <span data-ttu-id="8f8b1-120">Невозможно изменить выделенную память, пока фильтр активен.</span><span class="sxs-lookup"><span data-stu-id="8f8b1-120">Cannot change allocated memory while the filter is active.</span></span><br/> |
| <dl> <span data-ttu-id="8f8b1-121"><dt>**VFW \_ E \_ бадалигн**</dt></span><span class="sxs-lookup"><span data-stu-id="8f8b1-121"><dt>**VFW\_E\_BADALIGN**</dt></span></span> </dl>             | <span data-ttu-id="8f8b1-122">Указано недопустимое выравнивание.</span><span class="sxs-lookup"><span data-stu-id="8f8b1-122">An invalid alignment was specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="8f8b1-123"><dt>**\_ \_ необработанных буферов VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8f8b1-123"><dt>**VFW\_E\_BUFFERS\_OUTSTANDING**</dt></span></span> </dl> | <span data-ttu-id="8f8b1-124">Один или несколько буферов все еще активны.</span><span class="sxs-lookup"><span data-stu-id="8f8b1-124">One or more buffers are still active.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="8f8b1-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f8b1-125">Remarks</span></span>

<span data-ttu-id="8f8b1-126">Этот метод переопределяет метод [**кбасеаллокатор:: SetProperties**](cbaseallocator-setproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="8f8b1-126">This method overrides the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method.</span></span>

<span data-ttu-id="8f8b1-127">Выравнивание буфера, заданное элементом **кбалигн** структуры **\_ свойств распределителя** , должно быть четной степенью двух.</span><span class="sxs-lookup"><span data-stu-id="8f8b1-127">The buffer alignment, specified by the **cbAlign** member of the **ALLOCATOR\_PROPERTIES** structure, must be an even power of two.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f8b1-128">Требования</span><span class="sxs-lookup"><span data-stu-id="8f8b1-128">Requirements</span></span>



| <span data-ttu-id="8f8b1-129">Требование</span><span class="sxs-lookup"><span data-stu-id="8f8b1-129">Requirement</span></span> | <span data-ttu-id="8f8b1-130">Значение</span><span class="sxs-lookup"><span data-stu-id="8f8b1-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f8b1-131">Header</span><span class="sxs-lookup"><span data-stu-id="8f8b1-131">Header</span></span><br/>  | <dl> <span data-ttu-id="8f8b1-132"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f8b1-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8f8b1-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8f8b1-133">Library</span></span><br/> | <dl> <span data-ttu-id="8f8b1-134"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8f8b1-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f8b1-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f8b1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f8b1-136">**Класс Кмемаллокатор**</span><span class="sxs-lookup"><span data-stu-id="8f8b1-136">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 





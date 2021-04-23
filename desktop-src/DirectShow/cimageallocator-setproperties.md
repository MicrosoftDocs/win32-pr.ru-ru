---
description: 'Метод SetProperties задает количество выделяемых буферов и размер каждого буфера. Этот метод переопределяет метод Кбасеаллокатор:: SetProperties.'
ms.assetid: 8d419432-a9a7-44fb-b916-8dacd08eb6ec
title: Цимажеаллокатор. SetProperties, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c04501fe3511d9cdd45f3513c68082d2ffece0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657845"
---
# <a name="cimageallocatorsetproperties-method"></a><span data-ttu-id="2e4c7-104">Цимажеаллокатор. SetProperties, метод</span><span class="sxs-lookup"><span data-stu-id="2e4c7-104">CImageAllocator.SetProperties method</span></span>

<span data-ttu-id="2e4c7-105">`SetProperties`Метод задает количество выделяемых буферов и размер каждого буфера.</span><span class="sxs-lookup"><span data-stu-id="2e4c7-105">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span> <span data-ttu-id="2e4c7-106">Этот метод переопределяет метод [**кбасеаллокатор:: SetProperties**](cbaseallocator-setproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="2e4c7-106">This method overrides the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e4c7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e4c7-107">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="2e4c7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e4c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e4c7-109">*предпоручение*</span><span class="sxs-lookup"><span data-stu-id="2e4c7-109">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="2e4c7-110">Указатель на структуру [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая содержит требования к буферу.</span><span class="sxs-lookup"><span data-stu-id="2e4c7-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="2e4c7-111">*пактуал*</span><span class="sxs-lookup"><span data-stu-id="2e4c7-111">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="2e4c7-112">Указатель на структуру **\_ свойств распределителя** , которая получает фактические свойства буфера.</span><span class="sxs-lookup"><span data-stu-id="2e4c7-112">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e4c7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e4c7-113">Return value</span></span>

<span data-ttu-id="2e4c7-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e4c7-114">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e4c7-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e4c7-115">Remarks</span></span>

<span data-ttu-id="2e4c7-116">Этот метод вызывает [**Цимажеаллокатор:: чекксизес**](cimageallocator-checksizes.md) для проверки запрошенного размера буфера.</span><span class="sxs-lookup"><span data-stu-id="2e4c7-116">This method calls [**CImageAllocator::CheckSizes**](cimageallocator-checksizes.md) to validate the requested buffer size.</span></span> <span data-ttu-id="2e4c7-117">Он также вызывает версию базового класса `SetProperties` .</span><span class="sxs-lookup"><span data-stu-id="2e4c7-117">It also calls the base-class version of `SetProperties`.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e4c7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2e4c7-118">Requirements</span></span>



| <span data-ttu-id="2e4c7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2e4c7-119">Requirement</span></span> | <span data-ttu-id="2e4c7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2e4c7-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e4c7-121">Header</span><span class="sxs-lookup"><span data-stu-id="2e4c7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2e4c7-122"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e4c7-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2e4c7-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2e4c7-123">Library</span></span><br/> | <dl> <span data-ttu-id="2e4c7-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2e4c7-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e4c7-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e4c7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e4c7-126">**Класс Цимажеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="2e4c7-126">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




